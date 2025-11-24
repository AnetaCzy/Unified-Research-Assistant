# Unified Research Assistant

A Python-based AI research assistant that indexes arXiv papers, queries academic content, and provides context-aware answers using an LLM. Built with **LangChain**, **Azure OpenAI**, and **Pinecone**, it intelligently detects user intent, maintains workflow state, and allows seamless research question answering from indexed papers.

---

## Features

### ArXiv Paper Indexing
- Automatically fetch research papers from arXiv based on user-defined topics
- Download PDFs and extract text content
- Split text into manageable chunks
- Store embeddings in Pinecone for semantic search

### Contextual Q&A
- Ask research questions and receive answers using only indexed paper content
- Uses Azure OpenAI LLM for natural language responses
- Provides citations in Markdown format `[Title](URL)`
- Handles multi-paper context seamlessly

### Intelligent Workflow Agent
- Detects user intent (indexing vs querying)
- Maintains the current research topic state
- Caches already indexed topics to avoid duplicate work

### Scalable & Efficient
- Batch upserts to Pinecone for faster indexing
- Splits long documents into manageable chunks
- Supports multiple concurrent topics and queries

---

## Tech Stack
- **Python**
- **LangChain** – AzureChatOpenAI, embeddings, document handling
- **Azure OpenAI** – GPT-4.1, embeddings
- **Pinecone** – vector database for embeddings
- **arXiv API** – research paper retrieval
- **PyPDF2** – PDF text extraction
- **TQDM** – progress tracking

---

## Installation

```bash
git clone https://github.com/AnetaCzy/unified-research-assistant.git
cd unified-research-assistant
pip install -r requirements.txt
