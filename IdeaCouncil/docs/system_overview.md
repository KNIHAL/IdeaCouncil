# 🧠 System Overview: IdeaCouncil AI

**IdeaCouncil AI** is a hierarchical multi-agent system designed to evaluate startup ideas across four critical domains — Tech, Business, Finance, and Legal — under the coordination of a central Chief Critique Agent.

## 🚀 Objective

To simulate a real-world startup advisory board by assigning specialized AI agents to dissect and critique a given idea from multiple expert lenses.

## 🧩 System Architecture

- **ChiefCritiqueAgent** receives the idea, breaks it down, and delegates it to:
  - **TechManager** → ArchitectureExpert, InfraExpert, AIExpert
  - **BusinessManager** → GTMExpert, MarketExpert
  - **FinanceManager** → PricingExpert, CostExpert
  - **LegalManager** → [Regulatory & Risk Experts]

Each manager synthesizes their sub-agent feedback and reports back to the Chief.

## 🔁 Execution Flow

1. User submits startup idea
2. Chief agent structures the idea
3. Domain managers assign tasks to experts
4. Experts return evaluations → manager consolidates
5. Chief generates final verdict (Pursue, Refine, Reject)

## ✅ Why This Is Impressive

- True **CrewAI Flows + hierarchical logic**
- Modular agent delegation
- Mimics boardroom-like expert decision-making
