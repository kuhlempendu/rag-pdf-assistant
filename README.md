# rag-pdf-assistant
This Python program is a simple Retrieval-Augmented Generation (RAG) pipeline using LangChain and optionally OpenAI or Ollama models.
Main Features:
Environment & Model Setup:

Loads API keys using dotenv.

Dynamically selects between OpenAI's gpt models and llama2 via Ollama based on your chosen MODEL variable.

Model Invocation:

Sends prompts like “Tell me a joke” to the selected language model using LangChain.

PDF Document Processing:

Loads a PDF file (ResearchObjectives.pdf).

Splits it into pages for later retrieval and embedding.

Prompt Engineering:

Creates a prompt template instructing the model to answer based on provided context (or respond with “I don’t know” if unsure).

RAG (Retrieval-Augmented Generation):

Converts PDF content into vector embeddings.

Uses a retriever to find relevant content based on a user's question.

Combines the retrieved context with the prompt to query the model and generate accurate, context-aware answers.

Multi-Question Q&A:

Loops over several research-related questions and prints context-based answers using the document.
