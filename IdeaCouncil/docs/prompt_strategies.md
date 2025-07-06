# 🧠 Prompt Strategies for IdeaCouncil AI

## 👥 Role-Goal-Backstory Alignment

Each agent was defined with:
- **Role** → Domain-specific identity
- **Goal** → Clear mission for evaluation
- **Backstory** → Persona context to improve reasoning and consistency

## 🔄 Input Chaining

- The Chief agent first breaks the user idea into structured parts
- That structure is passed as input to all domain managers
- Each domain manager sends the same to their experts

This guarantees **tight focus and no prompt confusion**.

## 🧱 Delegation & Hierarchy

Managers are allowed to delegate, sub-agents are not. This keeps decision-making centralized while allowing distribution of analysis.

## 🧠 Prompting Style

- Always ask for structured output: bullet points, numbered sections
- Use task-specific terms: "Evaluate cost structure", not just "analyze"

## 📌 Example

> "Review the startup's pricing model, revenue logic, and monetization plans."

✅ Clear  
✅ Contextual  
✅ Output-oriented
