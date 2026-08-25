Somnath Chatterjee

Principal iOS Engineer · Local AI · Developer Intelligence

Exploring how Swift, MLX, local LLMs, and code intelligence can shape the next generation of developer tools.

I come from production iOS engineering and I’m increasingly interested in what happens when mobile engineering, Apple silicon, and local AI converge.

<p>
  <img src="https://img.shields.io/badge/Swift-FA7343?style=flat-square&logo=swift&logoColor=white" />
  <img src="https://img.shields.io/badge/UIKit-2396F3?style=flat-square&logo=apple&logoColor=white" />
  <img src="https://img.shields.io/badge/SwiftUI-0D96F6?style=flat-square&logo=swift&logoColor=white" />
  <img src="https://img.shields.io/badge/MLX-Apple_Silicon-222222?style=flat-square&logo=apple&logoColor=white" />
  <img src="https://img.shields.io/badge/Local_LLMs-On_Device-6C5CE7?style=flat-square" />
  <img src="https://img.shields.io/badge/Code_Intelligence-AST-00A67E?style=flat-square" />
  <img src="https://img.shields.io/badge/Agentic_AI-Developer_Tooling-8E44AD?style=flat-square" />
</p>

⸻

👋 About me

I’m a Principal iOS Engineer focused on building production mobile systems with Swift, UIKit, and SwiftUI.

Alongside mobile engineering, I’m exploring local AI and developer intelligence — particularly how smaller models running on Apple silicon can become more capable when they’re supported by better context, tools, and codebase understanding.

The part that interests me isn’t simply connecting an application to an LLM.

It’s the engineering around the model.

             Developer
                 │
                 ▼
        Developer Intelligence
                 │
      ┌──────────┼──────────┐
      ▼          ▼          ▼
   Context      Tools    Reasoning
      │          │          │
      └──────────┼──────────┘
                 ▼
             Local LLM
                 │
                 ▼
                MLX
                 │
                 ▼
          Apple Silicon

⸻

🍎 Exploring MLX

I’m experimenting with MLX as a native foundation for local AI on Apple silicon.

Running a model locally is only the starting point.

I’m interested in understanding how the layers below an AI application influence the experience above it:

             Apple Silicon
                   │
                   ▼
                  MLX
                   │
         ┌─────────┼─────────┐
         ▼         ▼         ▼
      Models     Memory   Inference
         │         │         │
         └─────────┼─────────┘
                   ▼
               Local LLM
                   │
                   ▼
            Developer Tools

Areas I’m exploring

* ⚡ Time to first token
* 🚀 Token generation throughput
* 🧠 Unified memory behavior
* 📦 Model loading and lifecycle
* 🗜️ Quantization trade-offs
* 🌊 Streaming generation
* 🔤 Tokenization
* 🧩 Swift integration
* 📊 Memory vs latency trade-offs
* 💻 Running capable models on consumer Apple silicon

The question isn’t only:

Can this model run locally?

It’s also:

How do we engineer the system around a local model so the model doesn’t need to solve everything itself?

⸻

🧠 Context engineering

One area I’m particularly interested in is codebase understanding.

Traditional LLM workflows often treat a repository primarily as text:

Large Repository
       │
       ▼
     Search
       │
       ▼
   Read Files
       │
       ▼
 Search Again
       │
       ▼
  More Files
       │
       ▼
 Bigger Context
       │
       ▼
      LLM

That works — but I’m interested in what happens if we understand the structure of the project first.

Source Code
     │
     ▼
    AST
     │
     ▼
Structured Knowledge
     │
     ▼
Relevant Context
     │
     ▼
    LLM

Instead of continuously increasing the amount of context, retrieve the part of the codebase that actually matters.

Don’t give the model more context. Give it better context.

This becomes particularly interesting with local models, where context size, memory usage, and inference latency directly affect the developer experience.

⸻

🕸️ Code intelligence

Source code contains much more information than its raw text.

There are:

Types
  │
  ├── Methods
  │
  ├── Properties
  │
  └── Protocols
Modules
  │
  └── Dependencies
Symbols
  │
  └── References
Components
  │
  └── Relationships

I’m exploring how compiler and source-code information can become part of an AI developer system.

Areas of interest

ASTs · Symbols · Types · Dependencies
Code Graphs · Project Knowledge · Semantic Retrieval

The interesting transition is:

Source Code
     ↓
Syntax
     ↓
Structure
     ↓
Relationships
     ↓
Project Knowledge
     ↓
AI Context

The goal is developer tooling that understands how a project is connected, rather than treating the repository as an unrelated collection of files.

⸻

🎯 Context over context windows

More context isn’t always better context.

I’m interested in systems where:

Repository
    │
    ▼
Project Intelligence
    │
    ▼
Relevant Knowledge
    │
    ▼
Focused Context
    │
    ▼
Local Model

instead of:

Repository
    │
    ▼
More Files
    │
    ▼
More Tokens
    │
    ▼
More Context
    │
    ▼
LLM

Especially for local inference, reducing unnecessary context can potentially mean:

less processing · lower memory pressure · faster responses · better signal

⸻

🤖 Agents, tools, and boundaries

I’m also exploring where agents should — and shouldn’t — be used.

Not every operation needs another LLM call.

                  Request
                     │
                     ▼
                 Reasoning
                     │
          ┌──────────┼──────────┐
          ▼          ▼          ▼
        Tools      Context    Agents
          │          │          │
          └──────────┼──────────┘
                     ▼
                   Result

Some problems need reasoning.

Some need retrieval.

Some need domain knowledge.

And some just need a deterministic tool.

A large part of agent engineering is deciding:

Which layer should own the work?

⸻

🧩 Tools vs agents

I’m particularly interested in separating deterministic capabilities from reasoning capabilities.

                AI System
                    │
         ┌──────────┴──────────┐
         │                     │
         ▼                     ▼
       Tools                 Agents
         │                     │
   Deterministic           Reasoning
   Operations              Decisions
         │                     │
         └──────────┬──────────┘
                    ▼
                  Result

File discovery doesn’t necessarily need an agent.

Parsing source code doesn’t necessarily need an agent.

Building project structure doesn’t necessarily need an agent.

But understanding a developer’s intent often does.

Keeping these boundaries clear can make local AI systems faster, more predictable, and easier to reason about.

⸻

🔐 Local-first AI

Local inference also creates an interesting architectural property:

Privacy can become part of the architecture rather than an additional layer.

I’m interested in systems where:

* inference stays local
* project context stays local
* filesystem access is explicit
* tools operate within defined boundaries
* models receive only the context they need
* network access isn’t assumed

For developer tooling, this becomes particularly interesting when working with private or proprietary codebases.

⸻

⚡ Local AI is a systems problem

The model is important.

But it’s only one layer.

┌─────────────────────────────────────────┐
│          Developer Experience           │
├─────────────────────────────────────────┤
│       Agents · Skills · Reasoning       │
├─────────────────────────────────────────┤
│        Tools · Orchestration            │
├─────────────────────────────────────────┤
│     Retrieval · Code Intelligence       │
├─────────────────────────────────────────┤
│         Context Engineering             │
├─────────────────────────────────────────┤
│          Local Inference · MLX          │
├─────────────────────────────────────────┤
│             Apple Silicon               │
└─────────────────────────────────────────┘

Better models matter.

But so do:

Inference · Retrieval · Tools · Graphs · Context · Orchestration · Security

That’s the part of local AI I’m most interested in exploring.

⸻

🛠 Engineering focus

📱 Mobile Engineering

Swift · UIKit · SwiftUI

Architecture · Concurrency · Performance

🍎 Local AI

MLX · Local LLMs · Inference

Quantization · Streaming · Tokenization

🕸️ Code Intelligence

AST · Code Graphs · Project Knowledge

Context Retrieval · Context Engineering

🤖 Agentic Systems

Agents · Tools · Skills

Orchestration · RAG · Tool Calling

🔐 Local-first Systems

Privacy · Filesystem Boundaries

Controlled Execution · On-device AI

⸻

🔬 Currently exploring

* 🍎 MLX on Apple silicon — local inference beyond simply running a model
* ⚡ Inference performance — TTFT, generation throughput, memory and model lifecycle
* 🧠 Smaller models + better systems — improving capability through architecture
* 🕸️ AST + graph-based intelligence — turning repositories into structured knowledge
* 🎯 Context engineering — selecting relevant context instead of accumulating it
* 🔤 Tokenization — understanding the layer between source text and inference
* 🤖 Agent architecture — reasoning, specialists, skills and deterministic tools
* 🔧 Native Swift AI tooling — building AI infrastructure directly in Swift
* 🔐 Privacy-first AI — local inference with explicit capability boundaries
* 📦 Model experimentation — quantization, memory, latency and capability trade-offs

⸻

💭 A principle I’m exploring

        Better Models
             +
        Better Context
             +
         Better Tools
             +
      Better Boundaries
             ↓
    Better AI Systems

The future of developer tooling probably isn’t just about putting a larger model behind an editor.

It’s also about giving models better representations of the software they’re working with.

⸻

🚀 Where I’m heading

I’ve spent years building software for users.

Now I’m exploring how to build software for the systems that build software.

Mobile Engineering
        │
        ▼
      Swift
        │
        ▼
 Apple Silicon
        │
        ▼
       MLX
        │
        ▼
 Local Inference
        │
        ▼
Code Intelligence
        │
        ▼
Agentic Systems
        │
        ▼
Developer Intelligence
<p align="center">
  <b>Mobile Engineering → Developer Intelligence → Local AI</b>
</p>
<p align="center">
  <i>Building software that understands software.</i>
</p>