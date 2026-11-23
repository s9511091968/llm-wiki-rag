# Source 02: LangChain Documentation — Text Splitters & Chunking
- **Source**: LangChain Official Conceptual Guide
- **URL**: https://python.langchain.com/docs/concepts/text_splitters/
- **Raw Notes**:
  - Splitting long documents into smaller chunks is essential for fitting text into the model's context window and improving retrieval accuracy.
  - Key parameters:
    1. `chunk_size`: The maximum size of a chunk (measured by characters or tokens).
    2. `chunk_overlap`: The overlap between consecutive chunks to preserve semantic context across boundaries so sentences aren't cut off abruptly.
  - RecursiveCharacterTextSplitter is recommended for generic text as it tries to split on paragraphs, then sentences, then words.