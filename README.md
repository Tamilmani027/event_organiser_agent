
# 🎉 Multi-Agent Event Planning & Organising System  
### _Automated Event Planner using Google ADK + Python Multi-Agent Architecture_

---

## 📌 Overview

This project is an **AI-powered multi-agent event planning system** built using the **Google Agent Development Kit (ADK)** and a modular **Planner → Worker → Evaluator** architecture.

It allows users to type natural language prompts like:

> _"Plan a farewell for 80 students under 20,000"_

…and automatically generates a **complete professional event plan**, including:

- Things required  
- Budget breakdown  
- Agenda & time schedule  
- Decor & creative ideas  
- Vendor suggestions  
- Pre-event, event-day, post-event checklists  
- Risks & mitigation strategies  

This project replaces the manual, stressful process of event planning with a fully automated AI concierge.

---

## 🎯 Problem Statement

Event planning involves multiple tasks such as budgeting, logistics, decor design, vendor coordination, scheduling, and risk handling.  
Most organizers—especially students—struggle to organize these components efficiently, leading to:

- overspending  
- missing important tasks  
- poor time management  
- lack of structure  

**This project automates the entire event planning workflow using a multi-agent system**, producing realistic and ready-to-use event plans.

---

## 🤖 Why Multi-Agent Architecture?

Event planning naturally breaks into independent tasks:

- Budgeting  
- Theme ideas  
- Logistics  
- Vendor planning  
- Timeline building  
- Risk management  

Instead of one large model doing everything, we use **specialized worker agents** that collaborate:

- Each agent becomes an expert in one domain.  
- Planner agent assigns tasks.  
- Workers generate specialized outputs.  
- Evaluator ensures the final plan is consistent and complete.

This makes agents **the ideal solution** for complex, multi-step tasks like event planning.

---

## 🧠 What I Created (Architecture)

### **High-Level Flow**
_User prompt → Planner Agent → Worker Agents → Evaluator Agent → Final Plan_

### **Agents Used**
- **Planner Agent** – Extracts budget, event type, headcount, objectives  
- **Theme Worker** – Provides theme, decor, creative ideas  
- **Budget Worker** – Gives detailed budget split  
- **Logistics Worker** – Venue, seating, flow  
- **Vendor Worker** – Vendor categories and suggestions  
- **Timeline Worker** – Pre/Post/Event-day timeline  
- **Risk Worker** – Predicts issues + mitigations  
- **Checklist Worker** – Full actionable checklist  
- **Evaluator Agent** – Validates and merges results into final plan  

---

## 🏗 Architecture Diagram

```

```
                  ┌────────────────┐
                  │   User Input   │
                  └───────┬────────┘
                          │
              ┌───────────▼───────────┐
              │     Planner Agent      │
              └───────┬───────────────┘
                      │ Tasks assigned
    ┌─────────────────┼───────────────────┐
    │                 │                   │
```

┌───────▼─────┐   ┌──────▼──────┐    ┌───────▼──────┐   ...
│ Theme Worker │   │ Budget Worker│    │ Logistics    │
└──────────────┘   └──────────────┘    └──────────────┘
│                 │                   │
└─────────────┬───┴─────┬────────────┘
│         │
┌─────▼─────────▼──────┐
│    Evaluator Agent    │
└─────────┬────────────┘
│
┌─────────▼────────────┐
│    Final Event Plan   │
└───────────────────────┘

```

---

## 📂 Folder Structure

```

event_organiser_agent/
│
├── project/
│   ├── agents/
│   ├── tools/
│   ├── memory/
│   ├── core/
│   ├── main_agent.py
│   ├── app.py
│   ├── run_demo.py
│   └── requirements.txt
│
└── event_organiser_agent.ipynb   ← Full build in Google Colab

```

---

## 🚀 Demo Output (Example)

```

🎉 EVENT PLAN SUMMARY

1️⃣ Event Overview

* Type: college_event
* Headcount: 80
* Budget: 20000

2️⃣ Things Required

* Vendors: caterer, decorator, sound/light
* Decor ideas: stage backdrop, fairy lights
* Important Tasks: venue booking, menu confirmation

3️⃣ Budget Breakdown

* Food: 8000
* Decor: 4000
* Entertainment: 3000
* Misc: 5000

4️⃣ Event Agenda

* Welcome & opening note
* Games & memories session
* Dinner & music
* Group photos

5️⃣ Creative Ideas

* Theme: Campus Fest Vibes
* Memory Wall, neon photo booth

6️⃣ Time Frames

* Planning timeline (T-30 to T-1 day)
* Event-day operations
* Post-event tasks

7️⃣ Risks & Mitigations

* Crowd control: assign volunteers

```

---

## 🛠 Tech Stack Used

### **Core:**
- Python 3  
- Google Agent Development Kit (ADK)
- Jupyter / Google Colab  

### **Architecture:**
- Multi-Agent Planner–Worker–Evaluator system  
- Modular tools for budgeting, decor, risk, timelines  
- A2A (Agent-to-Agent) messaging protocol  
- Session memory + plan memory  

### **Development Tools**
- Git & GitHub  
- Colab notebook automation  
- Modular file writing via `%%writefile`  

---

## 🏛 How I Built It

1. Designed the architecture using Planner/Worker/Evaluator pattern  
2. Created individual agents: Theme, Budget, Logistics, Vendors, etc.  
3. Implemented Python tools (budget calculator, risk analyzer, decor ideas)  
4. Added ADK root agent to integrate LLM reasoning  
5. Developed complete Colab notebook to auto-generate project structure  
6. Tested with multiple event scenarios  
7. Pushed final notebook & code to GitHub  

---

## 🧪 Testing Scenarios

Example test queries:

- “Plan a farewell for 60 students under 20,000.”  
- “Plan a simple birthday for 10 kids under 5,000.”  
- “Plan a 24-hour hackathon for 100 students under 1 lakh.”  
- “Plan a cultural fest for 300 attendees.”  

---

## 🚧 Future Enhancements (If I Had More Time)

- Add **Streamlit/Gradio UI** for user-friendly event planning  
- Export event plan as **PDF**  
- Integrate **real vendor APIs** for search  
- Add **budget optimizer**  
- Support **multi-language output** (Tamil / Hindi / Kannada)  
- Add **voice assistant mode**  
- Convert to a **deployed web service** with a backend + UI  

---

## 📎 GitHub Repository

🔗 **https://github.com/Tamilmani027/event_organiser_agent**

---

## 📜 License
MIT License (or choose your preferred license)

---
