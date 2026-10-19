# Stage 6: Reasoning & Agents

From prompting models to "think step by step" to training them with RL to reason, and
connecting them to tools so they can act.

## Prompted reasoning

- [ ] ⭐ **[Chain-of-Thought Prompting Elicits Reasoning in Large Language Models](https://arxiv.org/abs/2201.11903)** (Wei et al., Google, 2022)
  Showing worked examples in the prompt sharply improves math and logic performance.
- [ ] **[Large Language Models are Zero-Shot Reasoners](https://arxiv.org/abs/2205.11916)** (Kojima et al., 2022)
  "Let's think step by step." Chain-of-thought with no examples at all.
- [ ] **[Self-Consistency Improves Chain of Thought Reasoning](https://arxiv.org/abs/2203.11171)** (Wang et al., Google, 2022)
  Sample many reasoning paths and take a majority vote over the answers.
- [ ] **[Tree of Thoughts](https://arxiv.org/abs/2305.10601)** (Yao et al., 2023)

## Training models to reason

- [ ] ⭐ **[Training Verifiers to Solve Math Word Problems](https://arxiv.org/abs/2110.14168)** (Cobbe et al., OpenAI, 2021)
  Introduces GSM8K and the use of verifiers to rank sampled solutions.
- [ ] **[STaR: Bootstrapping Reasoning With Reasoning](https://arxiv.org/abs/2203.14465)** (Zelikman et al., 2022)
  The model trains on its own correct rationales.
- [ ] ⭐ **[Let's Verify Step by Step](https://arxiv.org/abs/2305.20050)** (Lightman et al., OpenAI, 2023)
  Process reward models (rewarding each step) beat outcome rewards on MATH.
- [ ] ⭐ **[Learning to Reason with LLMs](https://openai.com/index/learning-to-reason-with-llms/)** (OpenAI, 2024). o1.
  Large-scale RL on chain-of-thought. Performance scales with **test-time compute** (thinking longer).
- [ ] **[Scaling LLM Test-Time Compute Optimally can be More Effective than Scaling Model Parameters](https://arxiv.org/abs/2408.03314)** (Snell et al., Google DeepMind, 2024)
- [ ] **[DeepSeekMath](https://arxiv.org/abs/2402.03300)** (Shao et al., DeepSeek, 2024)
  Introduces GRPO, a cheaper PPO variant with no value network.
- [ ] ⭐ **[DeepSeek-R1: Incentivizing Reasoning Capability in LLMs via Reinforcement Learning](https://arxiv.org/abs/2501.12948)** (DeepSeek, 2025)
  Open replication of o1-style reasoning. Long chain-of-thought emerges from pure RL with verifiable rewards.
- [ ] **[Reasoning Models Don't Always Say What They Think](https://arxiv.org/abs/2505.05410)** (Chen et al., Anthropic, 2025)
  Chain-of-thought is not always a faithful account of the model's actual reasoning.
- [ ] **[Chain of Thought Monitorability: A New and Fragile Opportunity for AI Safety](https://arxiv.org/abs/2507.11473)** (Korbak et al., multi-lab, 2025)

## Tools, retrieval & agents

- [ ] ⭐ **[Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks](https://arxiv.org/abs/2005.11401)** (Lewis et al., Meta, 2020). RAG.
- [ ] **[WebGPT: Browser-assisted Question-answering with Human Feedback](https://arxiv.org/abs/2112.09332)** (Nakano et al., OpenAI, 2021)
- [ ] ⭐ **[ReAct: Synergizing Reasoning and Acting in Language Models](https://arxiv.org/abs/2210.03629)** (Yao et al., 2022)
  Alternate thought → action → observation. The basic loop most agents still use.
- [ ] **[Toolformer: Language Models Can Teach Themselves to Use Tools](https://arxiv.org/abs/2302.04761)** (Schick et al., Meta, 2023)
- [ ] **[Reflexion: Language Agents with Verbal Reinforcement Learning](https://arxiv.org/abs/2303.11366)** (Shinn et al., 2023)
- [ ] ⭐ **[SWE-bench: Can Language Models Resolve Real-World GitHub Issues?](https://arxiv.org/abs/2310.06770)** (Jimenez et al., Princeton, 2023)
  The benchmark that has tracked coding-agent progress.
- [ ] **[Introducing Computer Use](https://www.anthropic.com/news/3-5-models-and-computer-use)** (Anthropic, 2024)
  Claude operating a desktop through screenshots, mouse and keyboard.
- [ ] ⭐ **[Building Effective Agents](https://www.anthropic.com/engineering/building-effective-agents)** (Anthropic, 2024)
  Practical patterns (workflows vs. agents, orchestrator-workers, evaluator-optimizer). Prefer simple designs.
- [ ] **[Model Context Protocol](https://modelcontextprotocol.io/)** (Anthropic, 2024)
  An open standard for connecting models to tools and data.

## Build it

- Write a ReAct loop by hand: a model, two tools (calculator, file search) and a stop condition. No framework.
