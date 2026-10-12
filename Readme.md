# LangGraph Persistence and Checkpointing

## Overview

This project demonstrates persistence and checkpointing in LangGraph using `InMemorySaver`. It builds a simple joke generation workflow with two sequential nodes: generating a joke and explaining it.

## Concepts Covered

* **Persistence:** Saving graph state through checkpoints.
* **InMemorySaver:** Storing checkpoints in memory.
* **Thread ID:** Identifying a workflow thread.
* **get_state():** Retrieving the latest state snapshot.
* **get_state_history():** Accessing checkpoint history.

## Workflow

1. Accept a topic as input.
2. Generate a joke using an LLM.
3. Generate an explanation of the joke.
4. Save checkpoints during execution.
5. Inspect the latest state and checkpoint history.

## Technologies Used

* Python
* LangGraph
* LangChain
* Groq LLM
* TypedDict

## Installation

```bash
pip install langgraph langchain-groq python-dotenv
```

## Usage

Configure your Groq API key in a `.env` file, execute the notebook or Python script, and inspect the saved states using `get_state()` and `get_state_history()`.

## Note

`InMemorySaver` stores checkpoints in memory, so they are generally lost when the Python process ends. For persistent storage across restarts, use a database-backed checkpointer.

## Learning Goal

Understand how LangGraph saves workflow states, organizes checkpoints by thread ID, and retrieves execution history.
