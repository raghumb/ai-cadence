# Latest in AI

Discover the innovations and developments shaping the future of AI — thoughtfully explored and carefully curated.

## 20 November 2026
### ✨ Google Agent Substrate — Infrastructure for Running Millions of AI Agents
*![Category](https://img.shields.io/badge/AI_Infrastructure-0D9488)*

Google is taking agent infrastructure a step beyond traditional container orchestration with **Agent Substrate**, an open-source runtime purpose-built for running millions of stateful AI agents securely and efficiently.

Traditional Kubernetes Pods consume resources even when agents are idle, waiting for LLM responses, tool calls, or human intervention. Agent Substrate introduces an actor-based architecture that separates an agent's state from its underlying compute resources. When an agent becomes idle, its memory and filesystem state can be snapshotted, freeing compute resources. When needed again, the agent can resume in under 500 milliseconds.

Built on Kubernetes, it combines reusable worker pools, isolated execution environments, identity-aware gateways, and support for gVisor and microVMs. The project reached version 1.0 and became generally available on GKE in November 2026. Google has also donated Agent Substrate and gVisor to the CNCF Sandbox, encouraging vendor-neutral community development.

**Why it matters:** As enterprises move from individual AI assistants to fleets of autonomous agents, infrastructure must evolve beyond simply hosting containers. Agent Substrate introduces an important architectural building block for secure, stateful, high-density agent execution.

**References:**
- [Google Open Source – Introducing Agent Substrate and CNCF donation](https://opensource.googleblog.com/2026/11/sandboxing-untrusted-ai-agents-at-scale.html)
- [Google Cloud – Open infrastructure for autonomous agents](https://cloud.google.com/blog/products/containers-kubernetes/open-infrastructure-for-autonomous-agents-comes-to-cncf)
- [GitHub – Agent Substrate](https://github.com/agent-substrate/substrate)
- [Documentation](https://ate.dev/)

---

## 19 November 2026
### ✨ Jeveration – Bringing System One Thinking to Image Generation
*![Category](https://img.shields.io/badge/AI_Research-0D9488)*

Researchers from the National University of Singapore introduce Jeveration, an interesting approach that challenges the conventional multi-step image-generation paradigm. It builds on the decision paradigm demonstrated by Jev. Instead of relying on iterative denoising, Jeveration repurposes a frozen vision-language model to generate coherent images in a single forward pass. It coordinates parallel predictions using a shared random state, allowing the model to produce diverse yet globally consistent images. Interestingly, the same architecture supports text-to-image generation, image-to-image transformation and dense prediction. The researchers report generating 512×512 images in just 78 ms, claiming up to 122× faster generation than existing unified models while maintaining competitive image quality. This research points towards a potentially important shift in generative AI: moving from iterative generation towards fast, parallel prediction.

**References:**
- [Hugging Face Papers – Jeveration](https://huggingface.co/papers/2611.24738)
- [Research paper – arXiv](https://arxiv.org/abs/2611.24738)
- [Project page and demos](https://carol-lyh.github.io/Jeveration/)
- [GitHub – Code and model weights](https://github.com/Carol-lyh/Jeveration)

---

## 18 November 2026

### ✨ Harness² – Recursive Agent Harnessing
*![Category](https://img.shields.io/badge/AI_Frameworks_&_Platforms-0D9488)*

Google Research has introduced **Harness²**, an open-source framework that explores how AI agents can improve their own execution harnesses through recursive refinement, without changing or retraining the underlying model. Instead of focusing solely on better models, Harness² focuses on improving the components surrounding an agent – system prompts, guardrails, memory, tools, skills, scripts, subagents and orchestration.

Its approach follows a **Propose–Probe–Compose** cycle: propose modifications to the agent harness, execute the same task using the modified configurations, compare their behaviour against the original execution, and compose the improvements supported by the observed evidence. It introduces two levels of recursion: task-level refinement, which improves the harness for the current task, and harnessing-level refinement, which retains adopted improvements and evidence-backed lessons to guide future tasks.

The project supports both parallel and sequential refinement and can work with OpenCode and Codex executors. Its benchmark results suggest that improving the agent's execution environment can produce meaningful performance gains without changing model weights. An interesting direction for the evolution of self-improving agent systems.

**Explore:**
- [GitHub Repository](https://github.com/google-research/harness2)
- [Research Paper – Harness²: Recursive Agent Harnessing for an Open World](https://arxiv.org/abs/2610.14224)
- [Project Overview](https://harness2.app/)

---

## 17 November 2026

### ✨ PageIndex: Rethinking RAG Without Vector Databases
*![Category](https://img.shields.io/badge/AI_Frameworks_&_Platforms-0D9488)*

What if you could build a RAG system without vector databases, embeddings or traditional document chunking? [PageIndex](https://github.com/VectifyAI/PageIndex) takes a different approach to information retrieval by creating a hierarchical tree index of documents and using LLM reasoning to navigate that structure and identify relevant information. Inspired by how humans navigate lengthy reports by looking at their table of contents and locating relevant sections, PageIndex enables context-aware retrieval with traceable references to the original document. This approach is particularly interesting for complex, lengthy documents such as financial reports, legal filings, regulatory documents and technical manuals, where semantic similarity alone may not be sufficient to identify the right information.

**References:**
- [GitHub – VectifyAI/PageIndex](https://github.com/VectifyAI/PageIndex)
- [PageIndex – Official Website](https://pageindex.ai/)
- [PageIndex – Documentation](https://docs.pageindex.ai/)

---

## 16 November 2026

### ✨ REA — Reverse Engineer Anything

*![Category](https://img.shields.io/badge/AI_Tools-0D9488)*

What if you could ask an AI agent to understand how a feature works inside an application, even when you don't have access to its source code? [REA](https://github.com/morluto/rea) makes this possible by giving agents a set of reverse-engineering capabilities through MCP. It can investigate websites, JavaScript and Electron applications, Android apps, .NET assemblies and native binaries, tracing application behaviour down to code, instructions and runtime evidence. Rather than relying solely on an agent's assumptions, REA provides findings and supporting evidence that the agent can use to explain existing behaviour or help build a similar implementation. An interesting direction for agent-assisted software investigation and reverse engineering.

↗ **References:** [GitHub Repository](https://github.com/morluto/rea) · [Official Website](https://rea.tools)

### ✨ Google Open-Sources the Elephant-Goldfish Model for AI-Assisted Software Development

*![Category](https://img.shields.io/badge/AI_Assisted_Software_Development-0D9488)*

Google has open-sourced its **Elephant-Goldfish Model (EGM)**, a methodology designed to make AI-assisted coding more reliable by separating software design from implementation and introducing independent AI reviews. The approach uses an "Elephant" — a long-running, context-rich AI session where developers discuss requirements, architecture, trade-offs and document implementation plans — and "Goldfish" reviewers, which operate in fresh, stateless contexts to challenge those plans, identify missing requirements, uncover edge cases and verify implementation readiness. The idea is to reduce context bias and catch design flaws before they turn into code. Originally developed for internal use at Google, the open-source plugin is available under the Apache 2.0 license and supports coding environments including Antigravity, Claude Code and Codex.

**References:** 
- [Google Open Source Blog – Introducing the Elephant-Goldfish Model](https://opensource.googleblog.com/2026/10/introducing-elephant-goldfish-model-plugin.html)
- [GitHub – google/elephant-goldfish-model](https://github.com/google/elephant-goldfish-model)
- [Original concept – Elephants, Goldfish and the New Golden Age of Software Engineering](https://research.google/pubs/elephants-goldfish-and-the-new-golden-age-of-software-engineering/)

---

## 15 November 2026

### ✨ Google Gemini 4: A Multi-Model Approach to AI-Assisted Software Development

*![Category](https://img.shields.io/badge/AI_Models-0D9488)*

Google is expanding its Gemini 4 model family with three models targeting different levels of intelligence, speed and efficiency: **Carbon, Argon and Hydrogen**. Rather than relying on a single model for every task, Google is positioning them for complementary roles in agentic workflows. Carbon is designed for complex, long-horizon tasks involving deep reasoning, architectural decisions, multi-step coding and debugging. Argon targets demanding software engineering and knowledge-work tasks, while Hydrogen focuses on fast execution for everyday coding, testing and agentic workflows. 

What's particularly interesting is Google's introduction of **Orchestrator in Antigravity**, which dynamically switches between models within the same session. Carbon can handle complex reasoning and coordination, while Hydrogen can take on implementation and verification tasks. This multi-model approach aims to balance coding quality, execution speed and token costs rather than using the most powerful model for every step.

**References:**
- [Introducing Gemini 4 Hydrogen](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-hydrogen/)
- [Gemini 4 Carbon is now available](https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-4-carbon-now-available/)
- [Google DeepMind – Gemini Models](https://deepmind.google/models/gemini/)

### ✨ Graphify: Turning Codebases into Knowledge Graphs for AI Coding Assistants

*![Category](https://img.shields.io/badge/AI_Assisted_Software_Development-0D9488)*

Ever run into situations where your AI coding agent refers to methods that don't exist, misses important dependencies, or simply doesn't seem to have the right context about your codebase?

Graphify is an open-source tool that transforms an existing codebase into a queryable knowledge graph, helping AI coding assistants understand software structure and relationships beyond what traditional file search can provide. Using Tree-sitter-based AST parsing, it extracts relationships such as function calls, imports, inheritance and dependencies, connecting them into a graph that AI agents can traverse. Developers can invoke it through a `/graphify` skill in coding assistants such as Claude Code, Cursor, Codex and Gemini CLI. The generated graph can be explored visually or queried to understand how components connect, trace dependencies and assess the potential impact of changes. An interesting aspect is that Graphify distinguishes relationships explicitly extracted from source code from those inferred during graph construction, providing greater transparency into the context supplied to AI agents.

**References:**
- [GitHub – Graphify](https://github.com/Graphify-Labs/graphify)
- [Graphify Documentation](https://docs.graphify.com/)

---

## 14 November 2026
### ✨ Microsoft Agent Framework 1.0 – Microsoft's unified platform for building enterprise AI agents
*![Category](https://img.shields.io/badge/AI_Frameworks_&_Platforms-0D9488)*

Microsoft has brought Semantic Kernel and AutoGen together under the Microsoft Agent Framework, reaching GA for Python and .NET on April 3, 2026. The framework combines agent development and multi-agent orchestration with enterprise-oriented capabilities such as middleware, persistent memory, human-in-the-loop approvals and OpenTelemetry-based observability.

An important addition is its graph-based workflow engine, which enables developers to build deterministic agent workflows with branching, parallel execution, checkpointing and recovery. It also introduces declarative YAML configurations for defining agents and workflows, alongside MCP and A2A interoperability. More recent developments extend the framework towards coding-agent orchestration through GitHub Copilot SDK and Claude Code SDK integrations, reusable agent skills and a local debugging experience through DevUI.

This is an important development for teams looking to move beyond experimental multi-agent prototypes towards production-grade, observable and governable agent applications.

**References:**
- [Microsoft Agent Framework 1.0 announcement](https://devblogs.microsoft.com/agent-framework/microsoft-agent-framework-version-1-0/)
- [Official documentation](https://learn.microsoft.com/en-us/agent-framework/overview)
- [Observability and OpenTelemetry](https://learn.microsoft.com/en-us/agent-framework/agents/observability)
- [GitHub repository](https://github.com/microsoft/agent-framework-go)
