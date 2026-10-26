# 🤖 Day 2 — AI Assistant with Memory

## 🎯 Objective
Build an interactive AI assistant that remembers the conversation during the current session using Python lists and dictionaries.

## 🧠 Key Concepts
- **List (`messages`)** — stores conversation history.
- **Dictionary** — stores each message's `role` and `content`.
- **`append()`** — saves user and AI messages.
- **API Context** — sends conversation history to the AI.
- **`for` loop** — displays readable conversation history.
- **Session Memory** — memory resets when the program stops.

## 🔄 Code Flow

```mermaid
flowchart TD
    A([Start]) --> B[Load Environment Variables]
    B --> C[Create AI Client]
    C --> D[Initialize messages List]
    D --> E[Get User Input]
    E --> F[Save User Message]
    F --> G[Send Conversation History to AI]
    G --> H[Receive AI Reply]
    H --> I[Display AI Reply]
    I --> J[Save AI Reply]
    J --> K{User enters quit?}
    K -- No --> E
    K -- Yes --> L[Display Conversation History]
    L --> M([End])
```

## 💻 Message Structure

```python
messages = [
    {"role": "user", "content": "Hello"},
    {"role": "assistant", "content": "Hi! How can I help?"}
]
```

## 📌 Day 2 Learning
**Day 1:** AI responds to the current input.

**Day 2:** AI receives the stored conversation history for contextual responses.

> Note: This is session-based memory, not permanent memory. The conversation is stored in RAM and is lost when the program ends.

## 🛠️ Technologies
Python • OpenAI-compatible API • python-dotenv • Lists • Dictionaries • Loops
