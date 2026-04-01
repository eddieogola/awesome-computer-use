<div align="center">

# Awesome Computer Use

[![Awesome](https://awesome.re/badge-flat2.svg)](https://awesome.re)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![License: CC0-1.0](https://img.shields.io/badge/License-CC0_1.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

**A curated collection of resources for building and deploying Computer Use Agents (CUA)**

*Vision-language models that see screens and take actions like humans do*

[Open Source Models](#open-source-computer-use) · [Developer Tools](#developer-tools) · [Research](#research) · [Benchmarks](#benchmarks) · [Contributing](#contributing)

</div>

---

## Contents

- [Open Source Computer Use](#open-source-computer-use)
- [Developer Tools](#developer-tools)
- [Research](#research)
  - [Technical Deep Dives](#technical-deep-dives)
  - [Foundational Papers](#foundational-papers)
  - [Agent Architectures](#agent-architectures)
  - [Benchmarks & Evaluation](#benchmarks--evaluation)
  - [Safety & Security](#safety--security)
- [Commercial Platforms](#commercial-platforms)
- [Demos & Tutorials](#demos--tutorials)
- [Community](#community)
- [Contributing](#contributing)

---

## Open Source Computer Use

Production-ready open source models for GUI automation.

| Model | Parameters | Highlights | Links |
|-------|------------|------------|-------|
| **[Northstar CUA Fast](https://huggingface.co/Tzafon/Northstar-CUA-Fast)** | 4B | RL-trained with GRPO on synthetic environments. Excels at error recovery and multi-turn interactions. 55% on OSWorld Chrome. | [HuggingFace](https://huggingface.co/Tzafon/Northstar-CUA-Fast) · [API](https://docs.lightcone.ai) |
| [UI-TARS](https://github.com/AliYun/UI-TARS) | 7B/72B | Native GUI agent with System-2 reasoning. 24.6 on OSWorld. | [Paper](https://arxiv.org/abs/2501.12326) · [Code](https://github.com/AliYun/UI-TARS) |
| [ShowUI](https://github.com/showui/showui) | 2B | Lightweight vision-language-action model for UI grounding. | [GitHub](https://github.com/showui/showui) |
| [SeeClick](https://github.com/njucckevin/SeeClick) | 7B | Visual GUI agent with element grounding capabilities. | [Paper](https://arxiv.org/abs/2401.10935) · [Code](https://github.com/njucckevin/SeeClick) |
| [CogAgent](https://github.com/THUDM/CogAgent) | 18B | GUI agent with high-resolution cross-module attention. | [Paper](https://arxiv.org/abs/2312.08914) · [Code](https://github.com/THUDM/CogAgent) |
| [Aguvis](https://github.com/AguVis/AguVis) | 7B/72B | Unified pure vision GUI agent across platforms. | [Paper](https://arxiv.org/abs/2412.04454) · [Code](https://github.com/AguVis/AguVis) |

---

## Developer Tools

SDKs, frameworks, and infrastructure for building computer use applications.

### SDKs & APIs

- **[Lightcone SDK](https://docs.lightcone.ai)** - The API and runtime for Northstar CUA. Supports task-based automation, custom agent loops, and OpenAI-compatible endpoints. Available for Python (`pip install tzafon`) and Node.js (`npm install @tzafon/lightcone`).

- [Browser Use](https://github.com/browser-use/browser-use) - High-level framework for building browser automation agents with LLMs.

- [Computer Use OOTB](https://github.com/anthropics/anthropic-quickstarts/tree/main/computer-use-demo) - Anthropic's reference implementation for Claude computer use.

### Agent Frameworks

- [Playwright MCP](https://github.com/anthropics/mcp-server-playwright) - Model Context Protocol server for browser automation.

- [LangChain Computer Use](https://python.langchain.com/docs/integrations/tools/computer_use) - LangChain integration for computer use agents.

- [Lightcone Agent Harness](https://github.com/tzafon/lightcone) - Full desktop automation loop with sandbox execution (Apache 2.0).

### Sandboxing & Execution

- [E2B Desktop](https://e2b.dev/docs/desktop) - Secure cloud sandboxes for running GUI agents.

- [OSWorld Docker](https://github.com/xlang-ai/OSWorld#docker-setup) - Containerized environments for agent evaluation.

---

## Research

### Technical Deep Dives

- **[Training VLM for CUA](https://www.tzafon.ai/blog/training-vlm-for-cua)** - Deep dive into why SFT saturates, how positional encoding affects click accuracy (40% → 80% improvement), and why multi-turn RL enables robust error recovery. *Tzafon AI*

### Foundational Papers

- **[EvoCUA: Evolving Computer Use Agents via Learning from Scalable Synthetic Experience](https://arxiv.org/abs/2601.15876)** - Self-improving CUA through synthetic data generation and iterative RL. Achieves 56.7% on OSWorld, outperforming 72B models. *Fudan et al., 2025*

- **[OSWorld: Benchmarking Multimodal Agents for Open-Ended Tasks in Real Computer Environments](https://arxiv.org/abs/2404.07972)** - The definitive benchmark for computer use agents. 369 tasks across Ubuntu, Windows, and macOS. Best AI achieves 12.24% vs 72% human performance. *Salesforce et al., 2024* · [Code](https://github.com/xlang-ai/OSWorld)

- **[UI-TARS: Pioneering Automated GUI Interaction with Native Agents](https://arxiv.org/abs/2501.12326)** - Native GUI agent with enhanced perception, unified action modeling, and System-2 reasoning. State-of-the-art on 10+ benchmarks. *Alibaba et al., 2025*

### Agent Architectures

- [SeeClick: Harnessing GUI Grounding for Advanced Visual GUI Agents](https://arxiv.org/abs/2401.10935) - GUI grounding pre-training for improved element localization. *HKUST, 2024*

- [CogAgent: A Visual Language Model for GUI Agents](https://arxiv.org/abs/2312.08914) - High-resolution cross-module attention for GUI understanding. *Tsinghua, 2023*

- [Aguvis: Unified Pure Vision Agents for Autonomous GUI Interaction](https://arxiv.org/abs/2412.04454) - Pure vision approach without HTML/accessibility tree parsing. *2024*

- [WebVoyager: Building an End-to-End Web Agent with Large Multimodal Models](https://arxiv.org/abs/2401.13919) - LMM-powered agent for real-world web navigation. *2024*

- [Agent S: An Open Agentic Framework that Uses Computers Like a Human](https://arxiv.org/abs/2410.08164) - Experience-augmented hierarchical planning for complex tasks. *2024*

### Benchmarks & Evaluation

- [OSWorld](https://github.com/xlang-ai/OSWorld) - Real computer environments benchmark (Ubuntu/Windows/macOS)
- [WebArena](https://webarena.dev) - Realistic web environment benchmark with functional evaluation
- [AndroidWorld](https://github.com/google-deepmind/android_world) - Dynamic Android environment benchmark
- [VisualWebArena](https://jykoh.com/vwa) - Multimodal web agent benchmark
- [Mind2Web](https://osu-nlp-group.github.io/Mind2Web/) - Large-scale web agent dataset with real websites
- [ScreenSpot](https://github.com/njucckevin/ScreenSpot) - GUI grounding benchmark across mobile/desktop/web

### Safety & Security

- [Attacking Vision-Language Computer Agents via Pop-ups](https://arxiv.org/abs/2411.02391) - Adversarial attacks on GUI agents through pop-up injection. *2024*

- [Computer Use in the Real World](https://arxiv.org/abs/2412.10574) - Safety analysis and failure modes of deployed computer agents. *2024*

---

## Commercial Platforms

- [Claude Computer Use](https://www.anthropic.com/news/computer-use) - Anthropic's computer use capabilities via the Claude API.
- [OpenAI Operator](https://openai.com/operator) - Browser automation agent from OpenAI.
- [Google Mariner](https://deepmind.google/technologies/mariner/) - DeepMind's multimodal web agent.

---

## Demos & Tutorials

### Videos

- [Anthropic: Introducing Computer Use](https://www.youtube.com/watch?v=vH2f7cjXjKI) - Official introduction to Claude computer use
- [Building with Computer Use](https://www.youtube.com/watch?v=e9Q7DePPPcE) - Step-by-step implementation tutorial

### Interactive Demos

- [OSWorld Demo](https://os-world.github.io/) - Try the OSWorld benchmark interface
- [Lightcone Playground](https://lightcone.ai/dashboard) - Interactive Northstar CUA testing

---

## Community

- [Computer Use Discord](https://discord.gg/computer-use) - Community discussions
- [LangChain Discord #computer-use](https://discord.gg/langchain) - LangChain community channel
- [r/LocalLLaMA](https://reddit.com/r/LocalLLaMA) - Local model discussions including CUA

---

## Contributing

Contributions are welcome! This list aims to be a comprehensive resource for the computer use community.

### How to Contribute

1. **Fork** the repository
2. **Add** your resource in the appropriate section
3. **Follow** the formatting guidelines below
4. **Submit** a pull request

### Formatting Guidelines

**For papers:**
```markdown
- [Paper Title](https://arxiv.org/abs/XXXX.XXXXX) - Brief description. *Institution, Year* · [Code](url)
```

**For tools/projects:**
```markdown
- [Project Name](url) - Description of what it does and key features.
```

**For models:**
Add to the table with parameters, highlights, and relevant links.

### Quality Standards

- Resources must be **directly related** to computer use / GUI automation
- Papers should be from **peer-reviewed venues** or reputable preprint servers
- Projects should be **actively maintained** or historically significant
- Commercial tools should have **public documentation**

### What We're Looking For

- Open source models and weights
- Novel architectures and training approaches
- Benchmark results and evaluations
- Developer tools and frameworks
- Tutorials and educational content
- Safety and security research

---

<div align="center">

**[Back to Top](#awesome-computer-use)**

*Maintained by the community. Star this repo to show support!*

</div>
