# Stage 5: Interpretability

Reverse-engineering what happens inside neural networks. Anthropic's
[Transformer Circuits Thread](https://transformer-circuits.pub/) is the main body of work here. Most of it
is published as long interactive web articles rather than arXiv papers.

## Circuits & the Transformer as a mechanism

- [ ] ⭐ **[Zoom In: An Introduction to Circuits](https://distill.pub/2020/circuits/zoom-in/)** (Olah et al., OpenAI, 2020)
  The claim that networks contain understandable features connected into circuits. The starting point for this field.
- [ ] ⭐ **[A Mathematical Framework for Transformer Circuits](https://transformer-circuits.pub/2021/framework/index.html)** (Elhage et al., Anthropic, 2021)
  The residual stream as a communication channel. Attention heads decompose into QK and OV circuits.
- [ ] ⭐ **[In-context Learning and Induction Heads](https://arxiv.org/abs/2209.11895)** (Olsson et al., Anthropic, 2022)
  A specific two-head circuit that copies patterns. Evidence suggests it drives much of in-context learning.
- [ ] **[Interpretability in the Wild: Indirect Object Identification in GPT-2 small](https://arxiv.org/abs/2211.00593)** (Wang et al., 2022)
  A complete circuit for a real behaviour in a real model.
- [ ] **[Locating and Editing Factual Associations in GPT](https://arxiv.org/abs/2202.05262)** (Meng et al., 2022). ROME.
  Facts are stored in mid-layer MLPs and can be edited directly.

## Superposition & sparse features

- [ ] ⭐ **[Toy Models of Superposition](https://arxiv.org/abs/2209.10652)** (Elhage et al., Anthropic, 2022)
  Networks represent more features than they have neurons, which is why individual neurons are polysemantic.
- [ ] ⭐ **[Towards Monosemanticity: Decomposing Language Models With Dictionary Learning](https://transformer-circuits.pub/2023/monosemantic-features/index.html)** (Bricken et al., Anthropic, 2023)
  Sparse autoencoders (SAEs) pull interpretable features out of a small Transformer.
- [ ] ⭐ **[Scaling Monosemanticity: Extracting Interpretable Features from Claude 3 Sonnet](https://transformer-circuits.pub/2024/scaling-monosemanticity/index.html)** (Templeton et al., Anthropic, 2024)
  Millions of features in a production model, including the "Golden Gate Bridge" feature, and steering the model by clamping them.
- [ ] **[Scaling and Evaluating Sparse Autoencoders](https://arxiv.org/abs/2406.04093)** (Gao et al., OpenAI, 2024)
- [ ] **[Language Models Can Explain Neurons in Language Models](https://openaipublic.blob.core.windows.net/neuron-explainer/paper/index.html)** (Bills et al., OpenAI, 2023)
  Uses GPT-4 to automatically label neurons in GPT-2.

## Attribution graphs & model biology

- [ ] ⭐ **[Circuit Tracing: Revealing Computational Graphs in Language Models](https://transformer-circuits.pub/2025/attribution-graphs/methods.html)** (Ameisen et al., Anthropic, 2025)
- [ ] ⭐ **[On the Biology of a Large Language Model](https://transformer-circuits.pub/2025/attribution-graphs/biology.html)** (Lindsey et al., Anthropic, 2025)
  Traces how Claude 3.5 Haiku plans rhymes ahead, does multi-step reasoning and handles multiple languages.

## Other angles

- [ ] **[Grokking: Generalization Beyond Overfitting on Small Algorithmic Datasets](https://arxiv.org/abs/2201.02177)** (Power et al., OpenAI, 2022)
- [ ] **[Progress Measures for Grokking via Mechanistic Interpretability](https://arxiv.org/abs/2301.05217)** (Nanda et al., 2023)
  Fully reverse-engineers the algorithm a network learns for modular addition (Fourier features).
- [ ] **[Representation Engineering: A Top-Down Approach to AI Transparency](https://arxiv.org/abs/2310.01405)** (Zou et al., 2023)
  Find and steer concept directions (e.g. honesty) in activations.

## Build it

- Train your GPT on a toy task, then use [TransformerLens](https://github.com/TransformerLensOrg/TransformerLens)
  to find an induction head in GPT-2 small.
