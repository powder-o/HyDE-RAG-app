# Retrieval-Augmented Generation (RAG) with HyDE Implementation

This project is a Python implementation of a **Retrieval-Augmented Generation (RAG)** system enhanced with **Hypothetical Document Embeddings (HyDE)**. The system takes user questions, retrieves relevant context using a hypothetical document generation step, and then uses a language model to generate an informed response. This approach is particularly useful for generating more accurate answers for complex or vague queries.

## Features
- **Retrieval-Augmented Generation (RAG)**: Uses document retrieval to provide relevant context for the language model.
- **HyDE (Hypothetical Document Embeddings)**: Generates hypothetical responses to guide document retrieval and enhance context relevance.
- **Vector Store**: Uses **Chroma** to store and retrieve document embeddings.
- **HuggingFace Embeddings**: Embeddings are generated using HuggingFace models.
- **Groq LLM API**: Uses **Llama3** through the Groq API for generating both hypothetical documents and final responses.

## Installation
1. Clone the repository:
   ```sh
   git clone https://github.com/your-username/rag-hyde-implementation.gi
   ```

2. Install the required dependencies:
   ```sh
   pip install -r requirements.txt
   ```

3. Create a `.env` file in the project root to provide your Groq API key:
   ```
   GROQ_API_TOKEN=your_groq_api_key_here
   ```


## How It Works
1. **Document Storage**: Initializes a vector store using Chroma to store document embeddings. Sample documents are added to the vector store.
2. **Hypothetical Document Generation**: The user query is first used to generate a hypothetical response using the LLM.
3. **Document Retrieval**: The generated hypothetical document is embedded and used to retrieve similar documents from the vector store.
4. **Final Response Generation**: The retrieved documents, combined with the original query, are used to generate a comprehensive response via the language model.

## File Structure
- `rag_hyde_pipeline.py`: Main script for running the RAG pipeline with HyDE.
- `.env`: Environment file containing API keys.


## Requirements
- Python 3.8+
- **Chroma**: Vector store for document embedding storage.
- **HuggingFace**: For embedding functions.
- **Langchain**: Provides LLM and RAG chain support.
- **Groq API**: For interacting with the Llama3 model.
- **dotenv**: For environment variable management.

## Notes
- The vector store is persisted locally. You can modify the `persist_directory` path as needed.
- The API key must be provided in the `.env` file to access the Groq LLM service.

## Contributing
Feel free to open issues or submit pull requests if you'd like to contribute to the project.


