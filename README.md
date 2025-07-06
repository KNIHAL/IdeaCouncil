
# 🧠 IdeaCouncil AI – Docs

**Multi-agent startup critique system built with CrewAI.**  
IdeaCouncil simulates a panel of domain experts who collaboratively evaluate a startup idea — like having a team of seasoned consultants in your terminal.

---

## 📌 Table of Contents
- [Overview](#overview)
- [Why This Project Matters](#why-this-project-matters)
- [Agent Architecture](#agent-architecture)
- [Prompt Design Strategy](#prompt-design-strategy)
- [Domains & Expert Roles](#domains--expert-roles)
- [How It Works (Flow Logic)](#how-it-works-flow-logic)
- [Tech Stack](#tech-stack)
- [Limitations](#limitations)
- [License](#license)

---

## 🧩 Overview

**IdeaCouncil** is a multi-agent system designed to mimic how real-world experts across Tech, Business, Finance, and Legal domains assess startup ideas.  
This repository contains **blueprints only** — including:
- Agent roles
- Prompting strategies
- Architecture diagrams
- Flow logic
- Design reasoning

🚫 This repo does **not** contain the core source code. It serves as a professional *blueprint* to demonstrate agent architecture design and delegation logic.

---

## 💡 Why This Project Matters

Most early-stage founders struggle to access objective, critical feedback on startup ideas. IdeaCouncil solves this problem by:

- Acting like an **AI-powered advisory board**
- Delivering feedback from multiple expert personas
- Guiding founders toward clarity and better decision-making

### 🔧 Use Cases
- Solo founders validating startup ideas
- Hackathon teams analyzing product-market fit
- Startup studios running idea pipelines
- AI-powered pitch deck critique tools

---

## 🧠 Agent Architecture

📌 See: [`docs/system_overview.md`](docs/system_overview.md)

IdeaCouncil follows a **hierarchical, domain-based delegation model**:

User Input

↓

ChiefCritiqueAgent

↓

Domain Experts [Tech, Business, Finance, Legal Leaders]

↓

sub-agent

---

**Each domain has:**
- A domain **manager agent** who assigns tasks
- **Sub-experts** who perform analysis
- Final results get routed back to the **Chief**, who writes the final report

🖼️ *Architecture diagram:* [`architecture.png`](architecture.png)

---

## 🪄 Prompt Design Strategy

📌 See: [`docs/prompts/`](docs/prompts/)

Prompts are crafted using **CrewAI's structured agent format**, including:
- `role` (who the agent is)
- `goal` (what they want to achieve)
- `backstory` (personality and behavior modeling)
- `task.description` (precise instruction)
- `expected_output` (format of response)

This ensures:
- Role clarity
- High-quality task output
- Minimal hallucination

---

## 🧭 Domains & Expert Roles

📌 See: [`docs/agent_roles.md`](docs/agent_roles.md)

Each domain operates as an internal team. Breakdown:

### 🧑‍💻 Tech Domain
- **TechManager** → Leads domain
- **AIExpert**
- **ArchitectureExpert**
- **InfraExpert**

### 💼 Business Domain
- **BusinessManager** → Leads domain
- **MarketExpert**
- **GTMExpert**

### 💰 Finance Domain
- **FinanceManager** → Leads domain
- **PricingExpert**
- **CostExpert**

### ⚖️ Legal Domain *(planned)*
- **LegalManager**
- **IPExpert**
- **ComplianceExpert**

---

## ⚙️ How It Works (Flow Logic)

📌 See: [`src/crew/flow_design.md`](src/crew/flow_design.md)

The flow is orchestrated using `CrewAI Flow`:

1. ChiefCritiqueAgent receives user idea
2. Breaks it down and delegates to domain managers
3. Domain managers assign to their sub-agents
4. Sub-agents analyze and return their verdicts
5. Managers summarize domain-level insights
6. ChiefAgent consolidates all domain verdicts into a final critique

✅ *All flows follow `Process.hierarchical` logic*

---

## 🧰 Tech Stack

| Tool/Library     | Purpose                                  |
|------------------|------------------------------------------|
| `CrewAI`         | Multi-agent orchestration                |
| `LangChain`      | Tool integrations (for tools layer)      |
| `Python`         | Agent classes and logic scripting        |
| `Pydantic`       | Managing flow state                      |
| `Markdown`       | Blueprint formatting and documentation   |

---

## ⚠️ Limitations

- This is a **blueprint repo only** — core execution code is private
- Does not include API, CLI, or frontend layers
- Assumes basic understanding of CrewAI

---
## 📬 Collaborate

🚀 *Looking to collaborate on intelligent agent systems or AI startup tooling? Connect with me on [email](nihalpandey1205@gmail.com) or [LinkedIn](https://www.linkedin.com/in/kumar-nihal-260b7a351).*

----

## 📝 Note

This repository is intended for **educational and architectural demonstration** purposes only.  
It shares design patterns, agent logic, and prompt strategies—but **does not** include execution code.  
Feel free to reference or adapt the blueprint for your own experiments or frameworks.

🚫 Not licensed for commercial use or deployment.



---





