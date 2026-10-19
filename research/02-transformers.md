# Stage 2: The Transformer & GPT

The architecture that replaced RNNs, and the first generative pretrained Transformers.

## The architecture

- [ ] ⭐ **[Attention Is All You Need](https://arxiv.org/abs/1706.03762)** (Vaswani et al., Google, 2017)
  The Transformer: self-attention + MLP blocks with residuals and layer norm, no recurrence. Every model in this library builds on it.
  Read alongside [The Annotated Transformer](https://nlp.seas.harvard.edu/annotated-transformer/).
- [ ] **[On Layer Normalization in the Transformer Architecture](https://arxiv.org/abs/2002.04745)** (Xiong et al., 2020)
  Explains why **pre-LN** (norm before attention/MLP) trains more stably. GPT-2 and later use it.
- [ ] **[Root Mean Square Layer Normalization](https://arxiv.org/abs/1910.07467)** (Zhang & Sennrich, 2019)
  RMSNorm, the cheaper LayerNorm used in Llama, Mistral and DeepSeek.
- [ ] **[GLU Variants Improve Transformer](https://arxiv.org/abs/2002.05202)** (Shazeer, Google, 2020)
  SwiGLU MLPs, standard in modern open models.
- [ ] ⭐ **[RoFormer: Enhanced Transformer with Rotary Position Embedding](https://arxiv.org/abs/2104.09864)** (Su et al., 2021)
  RoPE, the position encoding used by nearly all modern LLMs.
- [ ] **[SentencePiece](https://arxiv.org/abs/1808.06226)** (Kudo & Richardson, Google, 2018)
  Language-independent subword tokenization.

## The first GPTs (OpenAI)

- [ ] ⭐ **[Improving Language Understanding by Generative Pre-Training](https://cdn.openai.com/research-covers/language-unsupervised/language_understanding_paper.pdf)** (Radford et al., OpenAI, 2018). GPT-1.
  Pretrain a decoder-only Transformer on unlabeled text, then fine-tune. This set the template for later LLMs.
- [ ] ⭐ **[Language Models are Unsupervised Multitask Learners](https://cdn.openai.com/better-language-models/language_models_are_unsupervised_multitask_learners.pdf)** (Radford et al., OpenAI, 2019). GPT-2.
  At 1.5B parameters, the model does tasks zero-shot from the prompt alone. Also introduces byte-level BPE.

## The encoder & encoder-decoder branch (Google)

- [ ] ⭐ **[BERT: Pre-training of Deep Bidirectional Transformers](https://arxiv.org/abs/1810.04805)** (Devlin et al., Google, 2018)
  Masked-language-model pretraining. It dominated NLP benchmarks until generative models took over.
- [ ] **[Exploring the Limits of Transfer Learning with a Unified Text-to-Text Transformer](https://arxiv.org/abs/1910.10683)** (Raffel et al., Google, 2019). T5.
  Frames every task as text-to-text. A careful study of what matters in pretraining.

## Build it

- Implement a GPT in [train.py](../train.py): token + position embeddings → N × (attention + MLP) → LM head.
  Train it on Tiny Shakespeare ([notebooks/01_data.ipynb](../notebooks/01_data.ipynb)).
- Then swap in RoPE, RMSNorm and SwiGLU, and compare loss curves.
