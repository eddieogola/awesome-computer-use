<div align="center">

# Awesome Computer Use

[![Awesome](https://awesome.re/badge-flat2.svg)](https://awesome.re)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![License: CC0-1.0](https://img.shields.io/badge/License-CC0_1.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

**A curated collection of resources for building and deploying Computer Use Agents (CUA)**

*Vision-language models that see screens and take actions like humans do*

[Models](#open-source-models) · [Tools](#developer-tools) · [Papers](#papers) · [Benchmarks](#benchmarks) · [Contributing](#contributing)

</div>

---

## Contents

- [Open Source Models](#open-source-models)
- [Developer Tools](#developer-tools)
  - [SDKs & APIs](#sdks--apis)
  - [Agent Frameworks](#agent-frameworks)
  - [Sandboxing & Execution](#sandboxing--execution)
- [Papers](#papers)
  - [Technical Deep Dives](#technical-deep-dives)
  - [Survey](#survey)
  - [Modeling & Architecture](#modeling--architecture)
  - [GUI Grounding](#gui-grounding)
  - [Agent Data & Trajectory Synthesis](#agent-data--trajectory-synthesis)
  - [Benchmarks & Evaluation](#benchmarks--evaluation)
  - [Safety & Security](#safety--security)
- [Commercial Platforms](#commercial-platforms)
- [Videos & Talks](#videos--talks)
- [Blogs & Articles](#blogs--articles)
- [Community](#community)
- [Contributing](#contributing)

---

## Open Source Models

Production-ready open source models for GUI automation.

| Model | Params | Highlights | Links |
|-------|--------|------------|-------|
| **[Northstar CUA Fast](https://huggingface.co/Tzafon/Northstar-CUA-Fast)** | 4B | RL-trained with GRPO on synthetic environments. Excels at error recovery and multi-turn interactions. 55% on OSWorld Chrome. | [HuggingFace](https://huggingface.co/Tzafon/Northstar-CUA-Fast) · [API](https://docs.lightcone.ai) |
| [UI-TARS](https://github.com/bytedance/UI-TARS) | 7B/72B | Native GUI agent with System-2 reasoning. 24.6 on OSWorld. | [Paper](https://arxiv.org/abs/2501.12326) · [GitHub](https://github.com/bytedance/UI-TARS) |
| [Aguvis](https://github.com/xlang-ai/aguvis) | 7B/72B | Unified pure vision GUI agent across platforms. | [Paper](https://arxiv.org/abs/2412.04454) · [GitHub](https://github.com/xlang-ai/aguvis) |
| [CogAgent](https://github.com/THUDM/CogVLM2) | 18B | High-resolution cross-module attention for GUI understanding. | [Paper](https://arxiv.org/abs/2312.08914) · [GitHub](https://github.com/THUDM/CogVLM2) |
| [SeeClick](https://github.com/njucckevin/SeeClick) | 7B | Visual GUI agent with element grounding capabilities. | [Paper](https://arxiv.org/abs/2401.10935) · [GitHub](https://github.com/njucckevin/SeeClick) |
| [ShowUI](https://github.com/showui/showui) | 2B | Lightweight vision-language-action model for UI grounding. | [GitHub](https://github.com/showui/showui) |
| [Ferret-UI](https://github.com/apple/ml-ferret/tree/main/ferretui) | - | Apple's grounded mobile UI understanding with multimodal LLMs. | [Paper](https://arxiv.org/abs/2404.05719) · [GitHub](https://github.com/apple/ml-ferret) |
| [OmniParser](https://microsoft.github.io/OmniParser/) | - | Microsoft's vision-based GUI agent parser. | [Website](https://microsoft.github.io/OmniParser/) · [GitHub](https://github.com/microsoft/OmniParser) |

---

## Developer Tools

### SDKs & APIs

- **[Lightcone SDK](https://docs.lightcone.ai)** - The API and runtime for Northstar CUA. Supports task-based automation, custom agent loops, and OpenAI-compatible endpoints. Available for Python (`pip install tzafon`) and Node.js (`npm install @tzafon/lightcone`). *Tzafon AI*

- [Claude Computer Use API](https://docs.anthropic.com/en/docs/build-with-claude/computer-use) - Anthropic's official computer use documentation and API reference.

- [Browser Use](https://github.com/browser-use/browser-use) - High-level framework for building browser automation agents with LLMs.

### Agent Frameworks

- [Computer Use OOTB](https://github.com/showlab/computer_use_ootb) - Out-of-the-box computer use implementation.

- [Self-Operating Computer](https://github.com/OthersideAI/self-operating-computer) - Framework for multimodal AI computer control.

- [OpenInterpreter](https://github.com/OpenInterpreter/open-interpreter) - Natural language interface for computer control.

- [Grunty](https://github.com/suitedaces/computer-agent) - Lightweight computer use agent.

- [Agent-E](https://arxiv.org/abs/2407.13032) - Foundational design principles in agentic systems. [Paper](https://arxiv.org/abs/2407.13032)

- [OS-Copilot](https://arxiv.org/abs/2402.07456) - Generalist computer agents with self-improvement. [Paper](https://arxiv.org/abs/2402.07456)

- [Cradle](https://arxiv.org/abs/2403.03186) - Empowering foundation agents towards general computer control. [Paper](https://arxiv.org/abs/2403.03186) · [GitHub](https://github.com/BAAI-Agents/Cradle)

- **[Lightcone Agent Harness](https://github.com/tzafon/lightcone)** - Full desktop automation loop with sandbox execution (Apache 2.0). *Tzafon AI*

### Sandboxing & Execution

- [E2B Desktop Sandbox](https://github.com/e2b-dev/desktop) - Secure cloud sandboxes for running GUI agents.

- [OSWorld Docker](https://github.com/xlang-ai/OSWorld#docker-setup) - Containerized environments for agent evaluation.

- [AgentStudio](https://arxiv.org/abs/2403.17918) - Toolkit for building general virtual agents.

### Platform-Specific

- [Claude Computer Use for macOS](https://github.com/deedy/mac_computer_use) - Anthropic computer use adapted for Mac.

- [Fazm](https://github.com/m13v/fazm) - MIT-licensed voice-controlled AI agent for macOS using accessibility APIs.

- [AppAgent](https://appagent-official.github.io/) - Multimodal agents as smartphone users. [Paper](https://arxiv.org/abs/2312.16427) · [GitHub](https://github.com/mnotgod96/AppAgent)

### Other Projects

- [OpenAdapt](https://github.com/OpenAdaptAI/OpenAdapt) - Open source process automation.
- [Open-Interface](https://github.com/AmberSahdev/Open-Interface/) - Natural language computer interface.
- [Bytebot](https://github.com/bytebot-ai/bytebot) - AI-powered automation bot.
- [WebMarker](https://github.com/reidbarber/webmarker) - Visual element marking for web agents.
- [Cua](https://github.com/trycua/cua) - Computer use agent framework.
- [UI-Act](https://github.com/TobiasNorlund/UI-Act) - UI interaction agent.

---

## Papers

### Technical Deep Dives

- **[Training VLM for CUA](https://www.tzafon.ai/blog/training-vlm-for-cua)** - Deep dive into why SFT saturates, how positional encoding affects click accuracy (40% → 80% improvement), and why multi-turn RL enables robust error recovery. *Tzafon AI*

### Survey

- [AI Agents for Computer Use: A Review of Instruction-based Computer Control, GUI Automation, and Operator Assistants](https://arxiv.org/abs/2501.16150) - Comprehensive survey of the field. *2025*

- [OS Agents: A Survey on MLLM-based Agents for General Computing Devices Use](https://openreview.net/pdf/ed2f5ee6b84c3b118cb953b6e750486dbd700419.pdf) - Survey on multimodal agents for computing devices.

### Modeling & Architecture

- **[EvoCUA: Evolving Computer Use Agents via Learning from Scalable Synthetic Experience](https://arxiv.org/abs/2601.15876)** - Self-improving CUA through synthetic data generation and iterative RL. 56.7% on OSWorld. *Fudan et al., 2025*

- **[UI-TARS: Pioneering Automated GUI Interaction with Native Agents](https://arxiv.org/abs/2501.12326)** - Native GUI agent with System-2 reasoning. State-of-the-art on 10+ benchmarks. *Alibaba, 2025*

- [Learn-by-interact: A Data-Centric Framework for Self-Adaptive Agents](https://arxiv.org/abs/2501.10893) - Self-adaptive agents in realistic environments. *2025*

- [PC Agent: While You Sleep, AI Works](https://arxiv.org/abs/2412.17589) - Cognitive journey into digital world. *2024*

- [Aguvis: Unified Pure Vision Agents for Autonomous GUI Interaction](https://arxiv.org/abs/2412.04454) - Pure vision approach without HTML parsing. *2024*

- [Agent S: An Open Agentic Framework that Uses Computers Like a Human](https://arxiv.org/abs/2410.08164) - Experience-augmented hierarchical planning. *2024*

- [Agent Q: Advanced Reasoning and Learning for Autonomous AI Agents](https://arxiv.org/abs/2408.07199) - Advanced reasoning capabilities. *2024*

- [OSCAR: Operating System Control via State-Aware Reasoning](https://arxiv.org/abs/2410.18963) - State-aware reasoning and re-planning. *2024*

- [AgentStore: Scalable Integration of Heterogeneous Agents](https://arxiv.org/abs/2410.18603) - Specialized generalist computer assistant. *2024*

- [Agent Workflow Memory](https://arxiv.org/abs/2409.07429) - Memory systems for agent workflows. *2024*

- [Web Agents with World Models](https://arxiv.org/abs/2410.13232) - Learning environment dynamics for web navigation. *2024*

- [AgentOccam: A Simple Yet Strong Baseline for LLM-Based Web Agents](https://arxiv.org/abs/2410.13825) - Simple but effective baseline. *2024*

- [Tree Search for Language Model Agents](https://arxiv.org/abs/2407.01476) - Tree search methods for LLM agents. *2024*

- [WebRL: Training LLM Web Agents via Self-Evolving Online Curriculum RL](https://arxiv.org/html/2411.02337v1) - Self-evolving curriculum reinforcement learning. *Tsinghua, 2024*

- [ECLAIR: Enterprise sCaLe AI for woRkflows](https://hazyresearch.stanford.edu/blog/2024-05-18-eclair) - Enterprise-scale AI workflows. *Stanford, 2024* · [GitHub](https://github.com/HazyResearch/eclair-agents)

- [SeeAct: GPT-4V(ision) is a Generalist Web Agent, if Grounded](https://osu-nlp-group.github.io/SeeAct/) - Visual grounding for generalist web agents. *OSU, 2024* · [GitHub](https://github.com/OSU-NLP-Group/SeeAct)

- [WebVoyager: Building an End-to-End Web Agent with Large Multimodal Models](https://arxiv.org/abs/2401.13919) - LMM-powered web navigation. *2024*

- [ICAL: Continual Learning of Multimodal Agents by Transforming Trajectories](https://arxiv.org/abs/2406.14596) - Actionable insights from trajectories. *NeurIPS 2024*

- [CogAgent: A Visual Language Model for GUI Agents](https://arxiv.org/abs/2312.08914) - High-resolution cross-module attention. *Tsinghua, 2023*

### GUI Grounding

- [GUI-Actor: Coordinate-Free Visual Grounding for GUI Agents](https://arxiv.org/abs/2506.03143) - Coordinate-free visual grounding approach. *2025*

- [Attention-driven GUI Grounding](https://arxiv.org/abs/2412.10840) - Leveraging pretrained MLLMs without fine-tuning. *AAAI 2025*

- [Navigating the Digital World as Humans Do](https://arxiv.org/abs/2410.05243) - Universal visual grounding for GUI agents. *2024*

- [OS-ATLAS: Foundation Action Model for Generalist GUI Agents](https://arxiv.org/abs/2410.23218) - Foundation model for GUI grounding. *ICLR 2025*

- [OmniParser for Pure Vision Based GUI Agent](https://arxiv.org/abs/2408.00203) - Vision-based GUI parsing. *Microsoft, 2024*

- [Ferret-UI 2: Universal User Interface Understanding Across Platforms](https://arxiv.org/abs/2410.18967) - Cross-platform UI understanding. *Apple, 2024*

- [SeeClick: Harnessing GUI Grounding for Advanced Visual GUI Agents](https://arxiv.org/abs/2401.10935) - GUI grounding pre-training. *ACL 2024*

- [Set-of-Mark (SoM) Prompting](https://som-gpt4v.github.io/) - Unleashing visual grounding in GPT-4V. *Microsoft, 2023* · [GitHub](https://github.com/microsoft/SoM)

### Agent Data & Trajectory Synthesis

- [Explorer: Robust Collection of Interactable GUI Elements](https://arxiv.org/abs/2504.09352) - GUI element collection. *2025*

- [Explorer: Scaling Exploration-driven Web Trajectory Synthesis](https://arxiv.org/pdf/2502.11357) - Multimodal web agents data. *2025*

- [OS-Genesis: Automating GUI Agent Trajectory Construction](https://arxiv.org/abs/2412.19723) - Reverse task synthesis. *ACL 2025*

- [AgentTrek: Agent Trajectory Synthesis via Guiding Replay](https://arxiv.org/abs/2412.09605) - Web tutorials for trajectory synthesis. *ICLR 2025*

- [AndroidLab: Training and Benchmarking Android Autonomous Agents](https://arxiv.org/abs/2410.24024) - Android agent training data. *2024*

- [GUI-World: A GUI-oriented Dataset for Multimodal LLM-based Agents](https://arxiv.org/abs/2406.10819) - Comprehensive GUI dataset. *2024*

- [Synatra: Turning Indirect Knowledge into Direct Demonstrations](https://arxiv.org/abs/2409.15637) - Digital agents at scale. *NeurIPS 2024*

### Benchmarks & Evaluation

- **[OSWorld: Benchmarking Multimodal Agents for Open-Ended Tasks](https://arxiv.org/abs/2404.07972)** - The definitive benchmark. 369 tasks across Ubuntu, Windows, macOS. Best AI: 12.24% vs 72% human. *NeurIPS 2024* · [Website](https://os-world.github.io/) · [GitHub](https://github.com/xlang-ai/OSWorld)

- [AndroidWorld: A Dynamic Benchmarking Environment](https://arxiv.org/abs/2405.14573) - Dynamic Android environment benchmark. *2024* · [GitHub](https://github.com/google-research/android_world)

- [Windows Agent Arena: Evaluating Multi-Modal OS Agents at Scale](https://arxiv.org/abs/2409.08264) - Windows-specific benchmark. *2024*

- [WebArena](https://webarena.dev) - Realistic web environment with functional evaluation.

- [VisualWebArena](https://jykoh.com/vwa) - Multimodal web agent benchmark.

- [Mind2Web](https://osu-nlp-group.github.io/Mind2Web/) - Large-scale web agent dataset.

- [ScreenSpot](https://github.com/njucckevin/SeeClick#screenspot) - GUI grounding benchmark across platforms. · [Pro Version](https://github.com/likaixin2000/ScreenSpot-Pro-GUI-Grounding)

- [CRAB: Cross-environment Agent Benchmark](https://arxiv.org/abs/2407.01511) - Multimodal language model agents. *2024*

- [MobileAgentBench](https://arxiv.org/abs/2406.08184) - Efficient benchmark for mobile LLM agents. *2024*

- [Spider2-V: Automating Data Science Workflows](https://arxiv.org/abs/2407.10956) - Data science automation benchmark. *NeurIPS 2024*

- [ScienceBoard: Scientific Workflows Evaluation](https://arxiv.org/abs/2505.19897) - Multimodal agents in realistic scientific workflows. *2025*

### Safety & Security

- [Attacking Vision-Language Computer Agents via Pop-ups](https://arxiv.org/abs/2411.02391) - Adversarial attacks through pop-up injection. *2024*

- [MobileSafetyBench: Evaluating Safety of Autonomous Agents](https://arxiv.org/abs/2410.17520) - Mobile device control safety. *2024*

- [GuardAgent: Safeguard LLM Agent via Knowledge-Enabled Reasoning](https://arxiv.org/abs/2406.09187) - Guard agent architecture. *2024*

- [EIA: Environmental Injection Attack for Privacy Leakage](https://arxiv.org/abs/2409.11295) - Privacy attacks on web agents. *2024*

- [Adversarial Attacks on Multimodal Agents](https://arxiv.org/abs/2406.12814) - Comprehensive attack analysis. *2024*

---

## Commercial Platforms

- [Claude Computer Use](https://www.anthropic.com/news/3-5-models-and-computer-use) - Anthropic's computer use via Claude API. [Model Card](https://assets.anthropic.com/m/1cd9d098ac3e6467/original/Claude-3-Model-Card-October-Addendum.pdf) · [Docs](https://docs.anthropic.com/en/docs/build-with-claude/computer-use) · [Blog](https://www.anthropic.com/news/developing-computer-use)

- [OpenAI Operator](https://openai.com/operator) - Browser automation agent from OpenAI.

- [Google Mariner](https://deepmind.google/technologies/project-mariner/) - DeepMind's multimodal web agent.

---

## Videos & Talks

- [Claude | Computer use for coding](https://www.youtube.com/watch?v=vH2f7cjXjKI) - Official Anthropic tutorial
- [Claude | Computer use for automating operations](https://www.youtube.com/watch?v=ODaHJzOyVCQ) - Operations automation demo
- [Claude | Computer use for orchestrating tasks](https://www.youtube.com/watch?v=jqx18KgIzAE) - Task orchestration walkthrough
- [LLMs as Computer Users: An Overview](https://www.figma.com/deck/rsWK4sRl0dOahG59bfMhql) - Comprehensive slide deck

---

## Blogs & Articles

### Industry Perspectives

- [Bill Gates | AI is about to completely change how you use computers](https://www.gatesnotes.com/AI-agents) - Gates on AI agents
- [Ethan Mollick | When you give a Claude a mouse](https://www.oneusefulthing.org/p/when-you-give-a-claude-a-mouse) - Analysis of computer use implications
- [Nathan Lambert | Claude's agentic future](https://www.interconnects.ai/p/claudes-agency) - Frontier models and agency

### Technical Analysis

- **[Training VLM for CUA](https://www.tzafon.ai/blog/training-vlm-for-cua)** - Deep technical analysis of VLM training for computer use. *Tzafon AI*
- [Simon Willison | Initial explorations of Computer Use](https://simonwillison.net/2024/Oct/22/computer-use/) - Technical exploration
- [Notes on Anthropic's Computer Use Ability](https://composio.dev/blog/claude-computer-use/) - Implementation notes

### Tutorials & Guides

- [Computer Use by Anthropic: 5-Minute Setup Guide](https://glama.ai/blog/2024-10-22-automate-computer-using-claude) - Quick start guide
- [Automating macOS using Claude Computer Use](https://glama.ai/blog/2024-10-23-automating-macos-using-claude) - macOS-specific tutorial
- [Anthropic Computer Use: Automate Your Desktop With Claude 3.5](https://www.datacamp.com/blog/what-is-anthropic-computer-use) - DataCamp tutorial
- [Instant Claude Computer Use Demo](https://labex.io/tutorials/docker-instant-claude-computer-use-demo-414899) - Docker-based demo

---

## Community

- [r/ClaudeAI](https://reddit.com/r/ClaudeAI) - Claude discussions including computer use
- [r/LocalLLaMA](https://reddit.com/r/LocalLLaMA) - Local model discussions
- [LangChain Discord](https://discord.gg/langchain) - LangChain community

---

## Contributing

Contributions are welcome! Please read our [Contributing Guidelines](CONTRIBUTING.md) first.

### Quick Guide

1. **Fork** the repository
2. **Add** your resource to the appropriate section
3. **Follow** the formatting conventions
4. **Submit** a pull request

### Formatting

**Papers:** `- [Title](url) - Brief description. *Institution, Year*`

**Tools:** `- [Name](url) - Description of features.`

**Models:** Add to the table with params, highlights, and links.

See [CONTRIBUTING.md](CONTRIBUTING.md) for detailed guidelines.

---

<div align="center">

**[Back to Top](#awesome-computer-use)**

*Maintained by the community. Star this repo to show support!*

</div>
