# Latest in AI

Discover the innovations and developments shaping the future of AI — thoughtfully explored and carefully curated.

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
