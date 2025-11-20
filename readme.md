
# Drafter ✍️ — AI-Powered Document Editing Assistant

[![Python](https://img.shields.io/badge/Python-3.9%2B-blue?logo=python)](https://python.org)
[![OpenAI GPT-4o](https://img.shields.io/badge/OpenAI-GPT--4o-000000?logo=openai)](https://openai.com)
[![LangChain](https://img.shields.io/badge/LangChain-v0.1%2B-brightgreen)](https://python.langchain.com)
[![LangGraph](https://img.shields.io/badge/LangGraph-Stateful_Agents-ff69b4)](https://langchain-ai.github.io/langgraph/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

**Drafter** is a conversational, stateful document editing assistant built entirely with **LangGraph** and **OpenAI GPT-4o**.  
You interact naturally in the terminal — instruct it to write, rewrite, expand, summarize, or finalize — and Drafter maintains full document state across turns using a proper graph-based state machine.

Perfect showcase of modern agent design: tool calling, persistent memory, conditional routing, and clean separation of concerns.

## ✨ Features

- Fully natural language document creation & editing
- Persistent document state using global + LangGraph memory
- Smart tool usage: `update` (replace entire content) · `save` (write to `.txt` and end)
- Real-time feedback after every change
- Proper conditional graph termination when document is saved
- Minimal, readable, production-grade LangGraph architecture

## 🚀 Quick Start (Run in < 60 seconds)

```bash
# 1. Clone the repo
git clone https://github.com/darshan3131/Drafter-AI.git
cd Drafter-AI

# 2. Install dependencies
pip install langchain langchain-openai langgraph python-dotenv

# 3. Set your OpenAI key
export OPENAI_API_KEY="sk-..."    # Linux/Mac
# set OPENAI_API_KEY=sk-...       # Windows

# 4. Run Drafter
python drafter.py
```

→ Just type what you want ("Write a cover letter for a Python developer role", "Make it more concise", "Add a strong closing paragraph", "Save as cover_letter.txt") and watch the magic.

## 🛠️ How It Works (Core Logic)

```python
Tools:
├─ update(content: str) → Replaces entire document with new content
└─ save(filename: str) → Writes document to .txt and triggers graceful exit

Graph Flow:
entry → agent → tools → (continue → agent) OR (saved → END)
```

- The agent always sees the **current full document** via dynamic system prompt
- Every update is atomic (full content replacement) — ensures consistency
- Termination only after successful `save` tool invocation

## 📂 Project Structure

```
Drafter-AI/
├── drafter.py              # Complete runnable script (single file)
├── .env.example            # Template for environment variables
├── requirements.txt
├── README.md
└── output/                 # Saved documents appear here
```

## 💡 Example Session

```
 ===== DRAFTER =====
 AI: I'm ready to help you update a document. What would you like to create?

What would you like to do with the document? Write a professional summary for a Python developer with 3 years of experience

 AI: Document has been updated successfully! The current content is:
 Experienced Python developer with over 3 years...

What would you like to do with the document? Make it shorter and add focus on AI agents

 TOOL RESULT: Document has been updated successfully...

What would you like to do with the document? Save as python_dev_summary.txt

 TOOL RESULT: Document has been saved successfully to 'python_dev_summary.txt'

 ===== DRAFTER FINISHED =====
```

## 🤝 Contributing

Issues, feature ideas (GUI, Markdown support, multi-file projects, memory persistence, etc.), and pull requests are very welcome!

## 👨‍💻 Author

**K C Darshan**  
Exploring the frontiers of stateful AI agents and human-AI collaboration.  
GitHub: [@darshan3131](https://github.com/darshan3131)

## 📄 License

MIT License – feel free to use, modify, and build upon this project.

---

⭐ If this minimal yet powerful agent pattern helped you understand LangGraph better, please consider giving it a star — it truly motivates further open-source work!

Made with passion for clean, intelligent systems.
```

### Additional Files to Add (Optional but Recommended)

**requirements.txt**
```txt
langchain>=0.1.0
langchain-openai
langgraph
python-dotenv
```

**.env.example**
```env
OPENAI_API_KEY=your_key_here
```

