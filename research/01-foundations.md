# Stage 1: Foundations

Before Transformers: how neural networks learned to model language, and the building blocks
(embeddings, attention, normalisation, optimisers) that LLMs still use today.

## Neural language models & embeddings

- [ ] ⭐ **[A Neural Probabilistic Language Model](https://www.jmlr.org/papers/volume3/bengio03a/bengio03a.pdf)** (Bengio et al., 2003)
  The first neural LM: predict the next word from learned word vectors. GPT works on the same principle, at a much larger scale.
- [ ] ⭐ **[Efficient Estimation of Word Representations in Vector Space](https://arxiv.org/abs/1301.3781)** (Mikolov et al., Google, 2013). Word2vec.
  Shows that cheap training produces embeddings with semantic structure (king − man + woman ≈ queen).
- [ ] **[The Unreasonable Effectiveness of Recurrent Neural Networks](https://karpathy.github.io/2015/05/21/rnn-effectiveness/)** (Karpathy, 2015, blog)
  Character-level RNNs generating Shakespeare. A direct ancestor of this repo's Tiny Shakespeare experiments.
- [ ] **[Neural Machine Translation of Rare Words with Subword Units](https://arxiv.org/abs/1508.07909)** (Sennrich et al., 2015)
  Byte-Pair Encoding (BPE). The tokenizer approach GPT-2 onwards still uses.

## Sequence-to-sequence & attention

- [ ] ⭐ **[Sequence to Sequence Learning with Neural Networks](https://arxiv.org/abs/1409.3215)** (Sutskever, Vinyals, Le, Google, 2014)
  Encoder-decoder LSTMs for translation. Shows that one network can map a sequence to a sequence. Ilya Sutskever later co-founded OpenAI.
- [ ] ⭐ **[Neural Machine Translation by Jointly Learning to Align and Translate](https://arxiv.org/abs/1409.0473)** (Bahdanau, Cho, Bengio, 2014)
  Introduces **attention**: the decoder looks back at all encoder states instead of one fixed vector. The seed of the Transformer.

## Training deep networks

- [ ] ⭐ **[Adam: A Method for Stochastic Optimization](https://arxiv.org/abs/1412.6980)** (Kingma & Ba, 2014)
  The optimiser (as AdamW) used to train essentially every LLM.
- [ ] **[Dropout](https://jmlr.org/papers/v15/srivastava14a.html)** (Srivastava et al., 2014)
  The standard regulariser. Used in early GPTs.
- [ ] ⭐ **[Deep Residual Learning for Image Recognition](https://arxiv.org/abs/1512.03385)** (He et al., Microsoft, 2015)
  Residual connections let very deep networks train. Every Transformer block is built around a residual stream.
- [ ] ⭐ **[Layer Normalization](https://arxiv.org/abs/1607.06450)** (Ba, Kiros, Hinton, 2016)
  Normalisation that works for sequences. Present in every Transformer block.
- [ ] **[Gaussian Error Linear Units (GELUs)](https://arxiv.org/abs/1606.08415)** (Hendrycks & Gimpel, 2016)
  The activation function used in GPT-2/3 and BERT.
- [ ] **[Distilling the Knowledge in a Neural Network](https://arxiv.org/abs/1503.02531)** (Hinton, Vinyals, Dean, 2015)
  Training a small model to mimic a large one. Widely used to make small, fast LLMs.

## Build it

- Bigram model → [notebooks/02_bigram.ipynb](../notebooks/02_bigram.ipynb)
- Next: an MLP language model in the style of Bengio 2003, then add a single attention head.
