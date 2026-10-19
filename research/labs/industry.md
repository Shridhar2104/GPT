# The Rest of the Industry

Major contributions from outside OpenAI and Anthropic. Papers are linked in the stage files. This page
is the map of who did what.

## Google / Google Brain / DeepMind

The Transformer came from Google. Google and DeepMind also produced much of the core architecture and
scaling research.

- 2013 word2vec · 2014 seq2seq · 2017 **Transformer**, sparsely-gated MoE · 2018 **BERT** · 2019 T5, MQA
- 2021 Switch Transformer, Gopher (DeepMind) · 2022 **Chinchilla**, PaLM, **chain-of-thought**, self-consistency, speculative decoding
- 2023 GQA, merger into **Google DeepMind**, **Gemini** · 2024–2025 Gemini 1.5 (long context), Gemini 2.x and Gemma open models
- Research: <https://deepmind.google/research/publications/>

## Meta (FAIR / GenAI)

- 2020 RAG · 2023 **LLaMA**, Llama 2, Toolformer · 2024 **Llama 3** herd paper
- Research: <https://ai.meta.com/research/>

## DeepSeek

Known for publishing detailed technical reports and training frontier-class models at low cost.

- 2024 DeepSeekMoE, DeepSeekMath (**GRPO**), DeepSeek-V2 (**MLA**), **DeepSeek-V3**
- 2025 **DeepSeek-R1**: open o1-style reasoning trained with RL
- GitHub: <https://github.com/deepseek-ai>

## Mistral AI

- 2023 Mistral 7B · 2024 **Mixtral** (open MoE)

## Academia & open source

- **Stanford**: DPO (2023), Alpaca, HELM benchmarks
- **Tri Dao (Princeton / Together AI)**: FlashAttention 1–3 and Mamba (with Albert Gu, CMU)
- **UC Berkeley**: vLLM / PagedAttention
- **University of Washington**: QLoRA, LLM.int8() (Tim Dettmers)
- **EleutherAI**: The Pile, GPT-NeoX, open interpretability tooling
- **Hugging Face**: Transformers library, FineWeb datasets, open-model hub
- **Microsoft**: LoRA, ZeRO/DeepSpeed, µP (with OpenAI)
- **NVIDIA**: Megatron-LM, mixed-precision training

## Generative AI beyond text (for context)

The research path above focuses on LLMs. These were the landmarks in image, audio and video generation:

- [GANs](https://arxiv.org/abs/1406.2661) (2014) · [VAEs](https://arxiv.org/abs/1312.6114) (2013)
- [Denoising Diffusion Probabilistic Models](https://arxiv.org/abs/2006.11239) (2020)
- [CLIP](https://arxiv.org/abs/2103.00020) (OpenAI, 2021)
- [Latent Diffusion / Stable Diffusion](https://arxiv.org/abs/2112.10752) (2021)
- [Whisper](https://arxiv.org/abs/2212.04356) (OpenAI, 2022)
