# Stage 3: Scaling & Pretraining

The discovery that bigger models, more data and more compute improve performance predictably,
and the models that put that discovery to use.

## Scaling laws

- [ ] ⭐ **[Scaling Laws for Neural Language Models](https://arxiv.org/abs/2001.08361)** (Kaplan et al., OpenAI, 2020)
  Loss falls as a power law in parameters, data and compute. This justified the bet on GPT-3. Several authors later co-founded Anthropic.
- [ ] **[Scaling Laws for Autoregressive Generative Modeling](https://arxiv.org/abs/2010.14701)** (Henighan et al., OpenAI, 2020)
  The same power laws hold for images, video and math.
- [ ] ⭐ **[Training Compute-Optimal Large Language Models](https://arxiv.org/abs/2203.15556)** (Hoffmann et al., DeepMind, 2022). Chinchilla.
  Shows earlier models were undertrained. The rule of thumb: ~20 tokens per parameter for compute-optimal training.
- [ ] **[Tensor Programs V: Tuning Large Neural Networks via Zero-Shot Hyperparameter Transfer](https://arxiv.org/abs/2203.03466)** (Yang et al., Microsoft/OpenAI, 2022). µP.
  Tune hyperparameters on a small model and transfer them to a large one.
- [ ] **[Emergent Abilities of Large Language Models](https://arxiv.org/abs/2206.07682)** (Wei et al., Google, 2022)
  …and the counterpoint: **[Are Emergent Abilities of LLMs a Mirage?](https://arxiv.org/abs/2304.15004)** (Schaeffer et al., 2023).

## Frontier pretrained models

- [ ] ⭐ **[Language Models are Few-Shot Learners](https://arxiv.org/abs/2005.14165)** (Brown et al., OpenAI, 2020). GPT-3.
  175B parameters. Introduces in-context learning: the model picks up a task from examples in the prompt.
- [ ] **[Evaluating Large Language Models Trained on Code](https://arxiv.org/abs/2107.03374)** (Chen et al., OpenAI, 2021). Codex.
  GPT fine-tuned on code. Introduced HumanEval and led to GitHub Copilot.
- [ ] **[Scaling Language Models: Methods, Analysis & Insights from Training Gopher](https://arxiv.org/abs/2112.11446)** (Rae et al., DeepMind, 2021)
- [ ] **[PaLM: Scaling Language Modeling with Pathways](https://arxiv.org/abs/2204.02311)** (Chowdhery et al., Google, 2022)
- [ ] ⭐ **[GPT-4 Technical Report](https://arxiv.org/abs/2303.08774)** (OpenAI, 2023)
  Multimodal and much stronger. Notable for predicting final loss from small runs, and for disclosing few details.
- [ ] **[Gemini: A Family of Highly Capable Multimodal Models](https://arxiv.org/abs/2312.11805)** (Google DeepMind, 2023)

## Open models

- [ ] ⭐ **[LLaMA: Open and Efficient Foundation Language Models](https://arxiv.org/abs/2302.13971)** (Touvron et al., Meta, 2023)
  Chinchilla-style training released openly. It started the open-weights ecosystem.
- [ ] **[Llama 2: Open Foundation and Fine-Tuned Chat Models](https://arxiv.org/abs/2307.09288)** (Meta, 2023)
  A detailed public account of RLHF for a chat model.
- [ ] ⭐ **[The Llama 3 Herd of Models](https://arxiv.org/abs/2407.21783)** (Meta, 2024)
  Probably the most complete public description of a frontier-scale training pipeline (data, infra, post-training).
- [ ] **[Mistral 7B](https://arxiv.org/abs/2310.06825)** (Mistral AI, 2023)
- [ ] ⭐ **[DeepSeek-V3 Technical Report](https://arxiv.org/abs/2412.19437)** (DeepSeek, 2024)
  Frontier-level quality at low training cost using MoE, multi-head latent attention, FP8 training and multi-token prediction.

## Data

- [ ] **[The Pile: An 800GB Dataset of Diverse Text](https://arxiv.org/abs/2101.00027)** (Gao et al., EleutherAI, 2020)
- [ ] ⭐ **[The FineWeb Datasets](https://arxiv.org/abs/2406.17557)** (Penedo et al., Hugging Face, 2024)
  A public, well-documented account of filtering web data for LLM pretraining.

## Build it

- Train your GPT at 3–4 sizes, plot final loss against parameters on a log-log scale, and check for a power law.
