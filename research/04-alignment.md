# Stage 4: Alignment & Safety

How a raw next-token predictor becomes a helpful, honest, harmless assistant, and the research
on keeping increasingly capable models safe. Anthropic has done much of its work here.

## Reinforcement learning from human feedback (RLHF)

- [ ] ⭐ **[Deep Reinforcement Learning from Human Preferences](https://arxiv.org/abs/1706.03741)** (Christiano et al., OpenAI/DeepMind, 2017)
  Learn a reward model from human comparisons, then optimise against it with RL. The origin of RLHF.
- [ ] ⭐ **[Proximal Policy Optimization Algorithms](https://arxiv.org/abs/1707.06347)** (Schulman et al., OpenAI, 2017)
  PPO, the RL algorithm used in classic RLHF.
- [ ] **[Fine-Tuning Language Models from Human Preferences](https://arxiv.org/abs/1909.08593)** (Ziegler et al., OpenAI, 2019)
  The first application of RLHF to language models.
- [ ] ⭐ **[Learning to Summarize from Human Feedback](https://arxiv.org/abs/2009.01325)** (Stiennon et al., OpenAI, 2020)
  RLHF beat supervised learning on summarization. Shows the full SFT → reward model → PPO recipe.
- [ ] ⭐ **[Training Language Models to Follow Instructions with Human Feedback](https://arxiv.org/abs/2203.02155)** (Ouyang et al., OpenAI, 2022). InstructGPT.
  The recipe behind ChatGPT. A 1.3B InstructGPT model was preferred over 175B GPT-3.

## Anthropic's alignment line

- [ ] ⭐ **[A General Language Assistant as a Laboratory for Alignment](https://arxiv.org/abs/2112.00861)** (Askell et al., Anthropic, 2021)
  Anthropic's first major paper. Defines the "helpful, honest, harmless" (HHH) framing.
- [ ] ⭐ **[Training a Helpful and Harmless Assistant with RLHF](https://arxiv.org/abs/2204.05862)** (Bai et al., Anthropic, 2022)
  RLHF at scale with the HH dataset. Studies the tension between helpfulness and harmlessness.
- [ ] **[Red Teaming Language Models to Reduce Harms](https://arxiv.org/abs/2209.07858)** (Ganguli et al., Anthropic, 2022)
- [ ] **[Language Models (Mostly) Know What They Know](https://arxiv.org/abs/2207.05221)** (Kadavath et al., Anthropic, 2022)
  LLMs are fairly well calibrated about their own correctness.
- [ ] ⭐ **[Constitutional AI: Harmlessness from AI Feedback](https://arxiv.org/abs/2212.08073)** (Bai et al., Anthropic, 2022)
  Replaces human harm labels with a written set of principles and AI self-critique (RLAIF). A core part of how Claude is trained.
- [ ] **[Discovering Language Model Behaviors with Model-Written Evaluations](https://arxiv.org/abs/2212.09251)** (Perez et al., Anthropic, 2022)
- [ ] **[Towards Understanding Sycophancy in Language Models](https://arxiv.org/abs/2310.13548)** (Sharma et al., Anthropic, 2023)
- [ ] ⭐ **[Sleeper Agents: Training Deceptive LLMs that Persist Through Safety Training](https://arxiv.org/abs/2401.05566)** (Hubinger et al., Anthropic, 2024)
  Backdoored behaviour can survive standard safety training.
- [ ] **[Many-shot Jailbreaking](https://www.anthropic.com/research/many-shot-jailbreaking)** (Anthropic, 2024)
- [ ] ⭐ **[Alignment Faking in Large Language Models](https://arxiv.org/abs/2412.14093)** (Greenblatt et al., Anthropic & Redwood, 2024)
  A model strategically complied with training it disagreed with in order to preserve its values.
- [ ] **[Constitutional Classifiers](https://arxiv.org/abs/2501.18837)** (Anthropic, 2025)
  Input/output classifiers trained from a constitution to defend against universal jailbreaks.
- [ ] **[Anthropic's Responsible Scaling Policy](https://www.anthropic.com/news/anthropics-responsible-scaling-policy)** (2023, updated since)
  The AI Safety Level (ASL) framework that ties safeguards to model capability.

## Simpler & newer alignment methods

- [ ] ⭐ **[Direct Preference Optimization](https://arxiv.org/abs/2305.18290)** (Rafailov et al., Stanford, 2023)
  Optimises preferences directly, with no reward model or RL loop. Widely used for open models.
- [ ] **[Self-Instruct](https://arxiv.org/abs/2212.10560)** (Wang et al., 2022)
  Bootstrap instruction-tuning data from the model itself.
- [ ] **[Deliberative Alignment](https://arxiv.org/abs/2412.16339)** (OpenAI, 2024)
  Teaches reasoning models to reason explicitly over safety specifications.

## Scalable oversight & big-picture safety

- [ ] ⭐ **[Concrete Problems in AI Safety](https://arxiv.org/abs/1606.06565)** (Amodei et al., 2016)
  A foundational research agenda. Dario Amodei later co-founded Anthropic.
- [ ] **[AI Safety via Debate](https://arxiv.org/abs/1805.00899)** (Irving, Christiano, Amodei, OpenAI, 2018)
- [ ] **[Measuring Progress on Scalable Oversight for LLMs](https://arxiv.org/abs/2211.03540)** (Bowman et al., Anthropic, 2022)
- [ ] **[Weak-to-Strong Generalization](https://arxiv.org/abs/2312.09390)** (Burns et al., OpenAI, 2023)
  Can a weak supervisor elicit the full capability of a stronger model? An analogy for humans supervising superhuman AI.

## Build it

- Fine-tune a small pretrained model on instruction data (SFT), then apply DPO with a public preference dataset
  (e.g. Anthropic's [HH-RLHF](https://github.com/anthropics/hh-rlhf)).
