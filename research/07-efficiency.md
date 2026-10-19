# Stage 7: Efficiency & Infrastructure

How LLMs are made affordable to train, fine-tune and serve.

## Attention efficiency & long context

- [ ] ⭐ **[FlashAttention: Fast and Memory-Efficient Exact Attention with IO-Awareness](https://arxiv.org/abs/2205.14135)** (Dao et al., 2022)
  Tiles attention to avoid reading and writing the N×N matrix to GPU memory. Exact, and much faster.
  Follow-ups: **[FlashAttention-2](https://arxiv.org/abs/2307.08691)** (2023) · **[FlashAttention-3](https://arxiv.org/abs/2407.08608)** (2024).
- [ ] ⭐ **[Fast Transformer Decoding: One Write-Head is All You Need](https://arxiv.org/abs/1911.02150)** (Shazeer, Google, 2019)
  Multi-query attention (MQA) shrinks the KV cache.
- [ ] ⭐ **[GQA: Training Generalized Multi-Query Transformer Models](https://arxiv.org/abs/2305.13245)** (Ainslie et al., Google, 2023)
  Grouped-query attention, a middle ground between MHA and MQA. Used in Llama 2/3 and Mistral.
- [ ] **[DeepSeek-V2](https://arxiv.org/abs/2405.04434)** (DeepSeek, 2024)
  Multi-head latent attention (MLA) compresses the KV cache into a low-rank latent.
- [ ] **[YaRN: Efficient Context Window Extension of LLMs](https://arxiv.org/abs/2309.00071)** (Peng et al., 2023)
  Extends RoPE models to longer contexts.
- [ ] **[Mamba: Linear-Time Sequence Modeling with Selective State Spaces](https://arxiv.org/abs/2312.00752)** (Gu & Dao, 2023)
  The leading non-attention alternative.

## Mixture of Experts

- [ ] ⭐ **[Outrageously Large Neural Networks: The Sparsely-Gated Mixture-of-Experts Layer](https://arxiv.org/abs/1701.06538)** (Shazeer et al., Google, 2017)
- [ ] ⭐ **[Switch Transformers](https://arxiv.org/abs/2101.03961)** (Fedus, Zoph, Shazeer, Google, 2021)
  Top-1 routing to scale to a trillion parameters.
- [ ] **[Mixtral of Experts](https://arxiv.org/abs/2401.04088)** (Mistral AI, 2024)
- [ ] **[DeepSeekMoE](https://arxiv.org/abs/2401.06066)** (DeepSeek, 2024)
  Fine-grained plus shared experts.

## Distributed training

- [ ] **[Mixed Precision Training](https://arxiv.org/abs/1710.03740)** (Micikevicius et al., NVIDIA/Baidu, 2017)
- [ ] ⭐ **[Megatron-LM: Training Multi-Billion Parameter Language Models Using Model Parallelism](https://arxiv.org/abs/1909.08053)** (Shoeybi et al., NVIDIA, 2019)
  Tensor parallelism.
- [ ] ⭐ **[ZeRO: Memory Optimizations Toward Training Trillion Parameter Models](https://arxiv.org/abs/1910.02054)** (Rajbhandari et al., Microsoft, 2019)
  Shards optimizer state, gradients and parameters. The basis of DeepSpeed and FSDP.

## Fine-tuning efficiently

- [ ] ⭐ **[LoRA: Low-Rank Adaptation of Large Language Models](https://arxiv.org/abs/2106.09685)** (Hu et al., Microsoft, 2021)
  Freeze the model and train small low-rank update matrices.
- [ ] ⭐ **[QLoRA: Efficient Finetuning of Quantized LLMs](https://arxiv.org/abs/2305.14314)** (Dettmers et al., 2023)
  LoRA on a 4-bit base model, which makes it possible to fine-tune 65B models on one GPU.

## Quantization & inference

- [ ] **[LLM.int8(): 8-bit Matrix Multiplication for Transformers at Scale](https://arxiv.org/abs/2208.07339)** (Dettmers et al., 2022)
- [ ] ⭐ **[GPTQ: Accurate Post-Training Quantization for Generative Pre-trained Transformers](https://arxiv.org/abs/2210.17323)** (Frantar et al., 2022)
- [ ] **[AWQ: Activation-aware Weight Quantization](https://arxiv.org/abs/2306.00978)** (Lin et al., MIT, 2023)
- [ ] ⭐ **[Efficient Memory Management for LLM Serving with PagedAttention](https://arxiv.org/abs/2309.06180)** (Kwon et al., Berkeley, 2023). vLLM.
  Manages the KV cache in pages, like virtual memory. Large throughput gains.
- [ ] ⭐ **[Fast Inference from Transformers via Speculative Decoding](https://arxiv.org/abs/2211.17192)** (Leviathan et al., Google, 2022)
  A small draft model proposes tokens and the large model verifies them in parallel. The output distribution is unchanged.
  Independently: **[Accelerating LLM Decoding with Speculative Sampling](https://arxiv.org/abs/2302.01318)** (Chen et al., DeepMind, 2023).

## Build it

- Add a KV cache to your GPT's `generate()` and measure the speedup.
- Fine-tune a small open model with LoRA using [PEFT](https://github.com/huggingface/peft).
