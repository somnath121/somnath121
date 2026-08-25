Hi, I’m Somnath 👋

Principal iOS Engineer · Local AI · Developer Intelligence

I build production iOS systems and explore how Swift, MLX, local LLMs, and code intelligence can be used to create better developer tools.

Currently interested in the engineering around the model — inference, context, code understanding, tools, and agent orchestration.

<p>
  <img src="https://img.shields.io/badge/Swift-FA7343?style=flat-square&logo=swift&logoColor=white" />
  <img src="https://img.shields.io/badge/UIKit-2396F3?style=flat-square&logo=apple&logoColor=white" />
  <img src="https://img.shields.io/badge/SwiftUI-0D96F6?style=flat-square&logo=swift&logoColor=white" />
  <img src="https://img.shields.io/badge/MLX-Apple_Silicon-222222?style=flat-square&logo=apple&logoColor=white" />
  <img src="https://img.shields.io/badge/Local_LLMs-On_Device-6C5CE7?style=flat-square" />
  <img src="https://img.shields.io/badge/Code_Intelligence-AST-00A67E?style=flat-square" />
</p>

⸻

🍎 Exploring Local AI

I’m experimenting with local AI on Apple silicon, particularly MLX and native Swift integration.

The interesting question for me isn’t only:

Can we run a capable model locally?

It’s:

How do we engineer the system around a local model so it can do more with less?

Some areas I’m exploring:

* MLX and local inference
* Qwen and other local models
* Time to first token (TTFT)
* Token generation performance
* Quantization and memory trade-offs
* Streaming generation
* Tokenization
* Model lifecycle and caching
* Native Swift integration

⸻

🧠 Better Context, Not More Context

Coding agents often spend a significant amount of work discovering a project:

Search → Read → Search → Read → Build Context → Reason

I’m interested in another approach:

Source Code → AST → Structured Knowledge → Relevant Context → Model

The idea is simple:

Don’t give the model more context. Give it better context.

Instead of treating a repository purely as text, source structure can provide useful information about:

* types
* symbols
* dependencies
* references
* protocols
* relationships
* architecture

This becomes especially interesting for smaller local models, where every unnecessary token has a cost.

⸻

🕸️ Code Intelligence

I’m exploring how traditional compiler and static-analysis concepts can contribute to AI developer tooling.

ASTs · Symbols · Types · Dependencies · Code Graphs · Semantic Retrieval

A codebase already contains structure.

The interesting problem is turning that structure into useful project knowledge for an AI system.

Source Code
    ↓
   AST
    ↓
Project Structure
    ↓
Code Intelligence
    ↓
Relevant Context
    ↓
Local Model

⸻

🤖 Agents vs Tools

I’m also interested in where agents actually belong in a developer system.

Not everything needs an LLM.

Deterministic work → Tools

File discovery, parsing, indexing, project structure, filesystem operations.

Reasoning work → Agents

Understanding intent, making decisions, planning changes, coordinating capabilities.

Keeping those responsibilities separate can make local AI systems:

faster · more predictable · easier to control

⸻

🔐 Local-First Developer Tools

Local inference creates an interesting opportunity for developer tooling.

I’m exploring systems where:

* inference stays local
* source code stays local
* filesystem access is explicit
* tools have defined boundaries
* models receive only relevant context
* network access isn’t assumed

Privacy becomes part of the architecture rather than something added afterwards.

⸻

🛠 Engineering Focus

Mobile Engineering

Swift UIKit SwiftUI Architecture Concurrency Performance

Local AI

MLX Local LLMs Inference Quantization Streaming Tokenization

Code Intelligence

AST Code Graphs Project Knowledge Context Retrieval

Agentic Systems

Agents Tools Skills Orchestration RAG

⸻

🔬 Currently Exploring

🍎 MLX on Apple silicon
⚡ Local inference performance and TTFT
🧠 Smaller models + better context
🕸️ AST and graph-based code intelligence
🎯 Context selection instead of context accumulation
🤖 Agent orchestration and tool boundaries
🔧 Native Swift AI tooling
🔐 Privacy-first developer environments

⸻

💡 How I Think About It

The model is only one part of an AI developer system.

Model + Context + Tools + Code Intelligence + Boundaries

The interesting engineering increasingly happens in how those pieces work together.

⸻

🚀 The Direction

I’ve spent years building software for users.

Now I’m exploring software for the systems that build software.

<p align="center">
  <b>Mobile Engineering → Developer Intelligence → Local AI</b>
</p>
<p align="center">
  <i>Building software that understands software.</i>
</p>