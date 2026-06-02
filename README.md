# Nth AI - Autonomous Research Desk (Challenge 1)

An end-to-end, autonomous multi-agent system that executes deep research, synthesizes findings, and self-corrects without human intervention. Built for Nth AI's engineering challenge.

## 🧠 Architecture: The Agentic Org Chart
This system is orchestrated using **LangGraph** and deployed as a **FastAPI** service. It utilizes a 100% local, open-source stack (`llama3` via Ollama and DuckDuckGo for search) to demonstrate architectural agnosticism and cost-efficiency.

The "Organization" consists of four distinct agents:
1. **The Planner:** Parses the initial user prompt and breaks it into 3 highly specific search queries.
2. **The Researcher:** Executes web searches and compiles the raw data context.
3. **The Synthesizer:** Drafts a markdown report strictly grounded in the retrieved context.
4. **The Critic (The QA Loop):** Evaluates the draft against the original prompt. If the draft is shallow or missing information, it generates specific feedback and routes the workflow *back* to the Researcher to find missing data.

## 🚀 Quick Start (Local Setup)

### Prerequisites
You will need Python 3.10+ and [Ollama](https://ollama.com/) installed on your machine.

