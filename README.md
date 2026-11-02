# 🤖 AI Agent Development — From Zero to AI Agents

**A day-by-day practical journey to learn AI, LLMs, and AI Agent Development using Python.**

Building AI applications step by step — from basic AI assistants to conversation memory, configurable personalities, Python tool integration, document-based question answering, RAG, and LLM-based planning.

---

## 🎯 Project Goal

Learn AI Agent Development through hands-on coding, understand each concept, identify limitations, and progressively build more capable AI applications using Python.

## 📚 Daily Learning Roadmap

| Day | Topic | What I Learned | Status |
|---|---|---|---|
| Day 1 | Basic AI Assistant | API integration, user input, AI responses | ✅ Completed |
| Day 2 | AI Assistant with Memory | Lists, dictionaries, conversation history | ✅ Completed |
| Day 3 | System Prompts & AI Personalities | Custom instructions and configurable behaviour | ✅ Completed |
| Day 4 | AI Assistant with Tools | Python tools, tool manager, refactoring, SRP | ✅ Completed |
| Day 5 | File Reading & Document Q&A | Read text files, summarize, explain, answer questions | ✅ Completed |
| Day 6 | RAG Workflow — Embeddings & Semantic Search | Knowledge base, nomic-embed-text, embeddings, cosine similarity | ✅ Completed |
| Day 7 | AI Planner & Tool Execution | LLM-based planning, intelligent tool selection, Python execution | ✅ Completed |
| Day 8 | Coming Next | To be updated | ⏳ Upcoming |

---

## 🧠 Learning Progress

### Day 1 — Basic AI Assistant

- Connected Python to an OpenAI-compatible API.
- Loaded credentials using `.env` and `python-dotenv`.
- Built a basic and interactive AI assistant.
- Learned how to send user messages and display AI responses.

**Limitation:** Previous conversation history was not sent to the AI.

[📂 Explore Day 1 →](./Day-1/README.md)

### Day 2 — AI Assistant with Memory

- Stored conversation messages in a Python list.
- Used dictionaries to identify `role` and `content`.
- Saved user messages and AI replies using `append()`.
- Sent conversation history to the AI for contextual responses.
- Displayed stored messages in a readable chat format.

**Limitation:** Session memory is lost when the program stops.

[📂 Explore Day 2 →](./Day-2/README.md)

### Day 3 — System Prompts & AI Personalities

- Created five selectable AI personalities using a dictionary.
- Used `roles.get()` to retrieve personality instructions.
- Added system instructions using `"role": "system"`.
- Configured the AI's role, tone, and response behaviour.
- Combined system instructions with conversation history.

**Limitation:** Only one personality is selected at a time, and settings are not permanently saved.

[📂 Explore Day 3 →](./Day-3/README.md)

### Day 4 — AI Assistant with Tools

- Created reusable Python tools for date/time, dice rolling, and password generation.
- Built `tool_manager.py` to identify matching requests and execute tools.
- Integrated tool execution into the AI assistant.
- Tested utility functions and tool routing using separate test files.
- Refactored code into modules with separate responsibilities.
- Learned **Refactoring** and the **Single Responsibility Principle (SRP)**.

**Limitation:** Tool selection uses keyword matching rather than AI-driven tool calling. Tool results are not saved in conversation history, and memory remains session-based.

[📂 Explore Day 4 →](./Day-4/README.md)

### Day 5 — File Reading & Document Q&A

- Created `read_text_file()` to read local text files.
- Added commands to summarize and explain document content.
- Implemented document-based questions using the `ask` command.
- Combined document content, instructions, and questions into a single prompt.
- Sent the prompt to the AI model and displayed the response.
- Added basic handling for missing files.

**Limitation:** The current implementation reads text files only. PDF/DOCX parsing, persistent document memory, and advanced handling of large documents are not implemented.

[📂 Explore Day 5 →](./Day-5/README.md)

### Day 6 — RAG Workflow: Embeddings & Semantic Search

- Created a local knowledge base using `.txt` documents.
- Loaded documents from the `knowledge/` folder using `pathlib`.
- Used the **`nomic-embed-text`** embedding model to convert documents into numerical vectors.
- Generated embeddings for user questions.
- Learned how embeddings represent semantic meaning in numerical form.
- Implemented cosine similarity using NumPy to compare question and document vectors.
- Retrieved the document with the highest similarity score.
- Combined retrieved document content and user question into a prompt.
- Sent the context-based prompt to the LLM to generate an answer.

**Limitation:** Documents are embedded as complete files without chunking. Embeddings are stored in memory rather than a vector database. Only the highest-scoring document is selected, and no minimum similarity threshold is implemented.

[📂 Explore Day 6 →](./Day-6/README.md)

### Day 7 — AI Planner & Tool Execution

- Created `planner.py` to make tool-selection decisions using an LLM.
- Used an AI planner to understand user requests and select appropriate tools.
- Created `test_planner.py` to test different user requests.
- Connected the planner with the main AI assistant.
- Integrated Python tool execution based on planner decisions.
- Executed tools for current time, dice rolling, and password generation.
- Passed tool results back to the LLM through prompt construction.
- Generated natural-language responses using tool outputs.
- Learned the difference between keyword-based routing and LLM-based planning.

**Limitation:** Planner decisions use plain-text tool names rather than native function calling. Voice/audio output and persistent conversation memory are not implemented.

[📂 Explore Day 7 →](./Day-7/README.md)

---

## 🚀 Project Evolution — Interactive Roadmap

**From basic AI responses to intelligent, document-aware and tool-enabled AI assistants.**

Follow the development journey and select a completed stage to explore its learning notes.

```mermaid
flowchart LR
    START(["🚀 AI Agent<br/>Development"])
    D1["DAY 1<br/>Basic AI Assistant"]
    D2["DAY 2<br/>Session Memory"]
    D3["DAY 3<br/>AI Personalities"]
    D4["DAY 4<br/>Python Tools & SRP"]
    D5["DAY 5<br/>Document Q&A"]
    D6["DAY 6<br/>RAG & Semantic Search"]
    D7["DAY 7<br/>AI Planner & Execution"]
    NEXT["DAY 8<br/>Coming Next"]
    GOAL(["🎯 Advanced<br/>AI Agents"])

    START --> D1 --> D2 --> D3 --> D4 --> D5 --> D6 --> D7 --> NEXT --> GOAL

    click D1 "./Day-1/README.md" "Explore Day 1"
    click D2 "./Day-2/README.md" "Explore Day 2"
    click D3 "./Day-3/README.md" "Explore Day 3"
    click D4 "./Day-4/README.md" "Explore Day 4"
    click D5 "./Day-5/README.md" "Explore Day 5"
    click D6 "./Day-6/README.md" "Explore Day 6"
    click D7 "./Day-7/README.md" "Explore Day 7"

    classDef start fill:#172554,stroke:#60a5fa,color:#ffffff,stroke-width:2px
    classDef completed fill:#dcfce7,stroke:#16a34a,color:#14532d,stroke-width:2px
    classDef upcoming fill:#fef3c7,stroke:#d97706,color:#78350f,stroke-width:2px
    classDef future fill:#dbeafe,stroke:#2563eb,color:#1e3a8a,stroke-width:2px

    class START start
    class D1,D2,D3,D4,D5,D6,D7 completed
    class NEXT upcoming
    class GOAL future
```

### 🔄 How Each Day Improves the Assistant

| Stage | Capability | Improvement |
|---|---|---|
| Day 1 | AI Responses | Connect Python to an AI model |
| Day 2 | Session Memory | Provide previous messages as context |
| Day 3 | Configurable Behaviour | Customize responses using system prompts |
| Day 4 | Python Tool Integration | Execute predefined functions using keyword-based routing |
| Day 5 | Document Q&A | Read text files and answer document-based questions |
| Day 6 | RAG & Semantic Search | Retrieve relevant documents using embeddings and cosine similarity |
| Day 7 | AI Planner & Tool Execution | Use an LLM to select tools and execute Python functions |
| Future | Advanced AI Agents | Progress toward AI-driven tool calling, planning, memory, and task execution |

---

## 🛠️ Tech Stack

- **Language:** Python
- **AI Integration:** OpenAI-compatible API
- **Configuration:** `python-dotenv` and environment variables
- **Embedding Model:** `nomic-embed-text`
- **AI Runtime:** Ollama
- **LLM Model:** Qwen3:1.7b
- **Core Concepts:** Lists, dictionaries, loops, functions, system prompts, conversation history, file handling, embeddings, semantic meaning, cosine similarity, semantic search, AI planning, tool execution
- **Architecture:** Tool management, modular programming, refactoring, Single Responsibility Principle (SRP), basic RAG workflow, LLM-based planning
- **Libraries:** NumPy, pathlib
- **Testing:** Python test scripts for tools, file reading, embeddings, retrieval, and planner decisions
- **Tools:** Visual Studio Code, Git, and GitHub
- **Documentation:** Markdown and Mermaid

## 📁 Repository Structure

```text
AI-AGENT-DEVELOPMENT/
├── Day-1/
│   ├── assistant.py
│   ├── hello_ai.py
│   └── README.md
├── Day-2/
│   ├── assistant.py
│   └── README.md
├── Day-3/
│   ├── assistant.py
│   └── README.md
├── Day-4/
│   ├── assistant.py
│   ├── tools.py
│   ├── tool_manager.py
│   ├── test_tools.py
│   ├── test_tool_manager.py
│   └── README.md
├── Day-5/
│   ├── assistant.py
│   ├── tools.py
│   ├── tool_manager.py
│   ├── test_file_tool.py
│   └── README.md
├── Day-6/
│   ├── knowledge/
│   │   └── *.txt
│   ├── rag.py
│   ├── retriever.py
│   ├── similarity.py
│   ├── test_embedding.py
│   ├── test_retriever.py
│   └── README.md
├── Day-7/
│   ├── assistant.py
│   ├── planner.py
│   ├── test_planner.py
│   ├── tools.py
│   └── README.md
├── .gitignore
└── README.md
```

*Keep this structure aligned with the files actually present in the repository. Do not commit `.env` files.*

---

## 🚀 Learning Approach

1. Understand the concept.
2. Write and run the code.
3. Identify limitations.
4. Improve the implementation.
5. Document each day's learning in its README.
6. Update this Master README and push changes to GitHub.

## 📌 Important Notes

- This repository documents my practical learning journey.
- Each day builds on previously learned concepts.
- Conversation memory currently lasts only for the active session.
- Day 4 tool execution is based on keyword matching.
- Day 5 document processing currently supports local text files only.
- Day 6 uses document embeddings and cosine similarity for basic semantic retrieval.
- Day 6 embeddings are stored in memory; no persistent vector database is integrated.
- Day 7 uses an LLM-based planner that returns tool names for Python execution.
- Day 7 does not yet implement native function calling or actual voice/audio output.
- Never upload `.env` files or API keys to GitHub.

---

**Consistency • Practical Learning • Continuous Improvement** 🚀