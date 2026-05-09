# 🤖 Building ReAct Agents with LangGraph & Groq

Welcome to this hands-on exploration of Agentic AI! This repository contains a Jupyter Notebook (`AiAgents.ipynb`) that demonstrates how to evolve a standard Large Language Model into a capable, tool-using autonomous agent. 

By leveraging the lightning-fast inference of Groq and the orchestration power of LangGraph, this project walks through the foundational steps of giving an LLM the ability to do math and search the real-time web.

## 🛠️ Tech Stack

* **Frameworks:** [LangChain](https://python.langchain.com/) & [LangGraph](https://langchain-ai.github.io/langgraph/)
* **LLM Provider:** [Groq](https://groq.com/) (Using `llama-3.3-70b-versatile`)
* **Tools:** Custom Python Functions (`@tool`), DuckDuckGo Web Search

## 🚀 What's Inside

This notebook is structured as a step-by-step learning progression:

1.  **The Baseline:** Initializing the LLaMA 3.3 70B model via Groq and testing its base generation capabilities with a short data analysis essay.
2.  **The Limitation:** Asking the raw model a complex math question (`952124 * 123991`) to demonstrate where pure LLMs struggle.
3.  **Equipping Tools:** Creating custom Python functions for multiplication and division using LangChain's `@tool` decorator.
4.  **Building the ReAct Agent:** Using LangGraph's `create_react_agent` to bind our custom math tools to the LLM, allowing it to successfully calculate and divide large numbers autonomously.
5.  **Breaking the Knowledge Cutoff:** The model naturally fails to know who the US President is in 2026. We solve this by integrating the `DuckDuckGoSearchRun` tool, giving the agent real-time access to the internet to find the correct answer.

## 💻 Getting Started

To run this notebook locally or in Google Colab:

1. Clone this repository.
2. Ensure you have your Groq API key ready. (In Colab, add it to your secrets as `groq_api`).
3. Install the required dependencies:
   ```bash
   pip install langchain langchain-groq langgraph duckduckgo-search
