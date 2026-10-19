# LLM & Generative AI Research Library

A curated learning path through the research that produced modern LLMs (GPT, Claude,
Gemini, Llama, DeepSeek), from the field's roots to frontier work by OpenAI, Anthropic and the wider
industry.

Every entry links to the original paper or post (arXiv, or the official lab site), with a short
note on **why it matters**. Tick the boxes (`- [x]`) as you read.

## How to use this

1. Go through the stages in order. Each one assumes the stages before it.
2. Read the papers marked ⭐ first. They are the core of each stage. Come back to the others
   once the core makes sense.
3. After each stage, **build something** in this repo (see "Build it" at the end of each stage).
   Reading on its own won't stick. Implementing will.

## The path

| # | Stage | What you'll understand |
|---|-------|------------------------|
| 1 | [Foundations](01-foundations.md) | Neural language models, embeddings, seq2seq, attention, optimisation |
| 2 | [The Transformer & GPT](02-transformers.md) | The architecture behind every modern LLM, GPT-1/2, BERT, T5 |
| 3 | [Scaling & Pretraining](03-scaling.md) | Scaling laws, GPT-3/4, Chinchilla, Llama, DeepSeek, data |
| 4 | [Alignment & Safety](04-alignment.md) | RLHF, InstructGPT, Constitutional AI, DPO, safety research |
| 5 | [Interpretability](05-interpretability.md) | Circuits, superposition, sparse autoencoders, attribution graphs |
| 6 | [Reasoning & Agents](06-reasoning-agents.md) | Chain-of-thought, RL reasoning (o1, R1), tool use, agents |
| 7 | [Efficiency & Infrastructure](07-efficiency.md) | FlashAttention, MoE, LoRA, quantization, inference serving |

## Lab histories

- [Anthropic](labs/anthropic.md): Claude models and research milestones
- [OpenAI](labs/openai.md): GPT models and research milestones
- [The rest of the industry](labs/industry.md): Google/DeepMind, Meta, DeepSeek, Mistral and others

## Companion resources

- [Andrej Karpathy, *Neural Networks: Zero to Hero*](https://karpathy.ai/zero-to-hero.html): build GPT from scratch (this repo follows a similar path)
- [nanoGPT](https://github.com/karpathy/nanoGPT): minimal GPT training code
- [The Annotated Transformer](https://nlp.seas.harvard.edu/annotated-transformer/): the Transformer paper, line by line in PyTorch
- [Anthropic research](https://www.anthropic.com/research) · [Transformer Circuits Thread](https://transformer-circuits.pub/)
- [OpenAI research](https://openai.com/research/)
- [Lilian Weng's blog](https://lilianweng.github.io/): excellent survey posts on most topics here

## How to read a paper

1. **First pass (10 min):** abstract, figures, conclusion. What problem does it solve, and what's the claim?
2. **Second pass (1 hr):** method and experiments. Could you explain the core idea to a friend?
3. **Third pass (optional):** re-derive the math or reimplement the key piece in a notebook.
