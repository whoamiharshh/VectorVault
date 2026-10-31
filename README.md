# 🚀 VectorVault
### AI-Powered Semantic Search & Question Answering System

VectorVault is a Retrieval-Augmented Generation (RAG) application that allows users to ask questions and receive context-aware answers using semantic search.

It uses **Google Gemini Embeddings** to convert text into vector representations, **MongoDB Atlas Vector Search** to retrieve relevant information, and **LangChain with Gemini** to generate answers based on the retrieved context.

## ✨ Features

- **Semantic Search:** Finds relevant information based on meaning, not just keyword matching.
- **Vector Embeddings:** Converts documents and user queries into numerical vectors using Gemini.
- **MongoDB Atlas Vector Search:** Retrieves the nearest matching document chunks.
- **Context-Based Answers:** Uses retrieved information to generate relevant answers.
- **RAG Architecture:** Combines information retrieval with generative AI.

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| Google Gemini | Embeddings and answer generation |
| MongoDB Atlas | Document and vector storage |
| MongoDB Vector Search | Similarity-based retrieval |
| LangChain | Prompt management and LLM orchestration |
| Jupyter Notebook | Development environment |

## ⚙️ How It Works

1. **Data Ingestion:** Retrieves movie data from MongoDB.
2. **Document Processing:** Converts records into LangChain documents.
3. **Text Chunking:** Splits documents into smaller chunks using `RecursiveCharacterTextSplitter`.
4. **Embedding Generation:** Generates vector embeddings using `gemini-embedding-001`.
5. **Vector Storage:** Stores text chunks and embeddings in MongoDB Atlas.
6. **User Query:** Accepts a question from the user.
7. **Query Embedding:** Converts the question into a vector.
8. **Vector Search:** Finds the most relevant chunks using MongoDB Atlas Vector Search.
9. **Context Refinement:** Selects relevant retrieved information.
10. **Answer Generation:** Sends the context and question to Gemini through LangChain to generate an answer.

## 📦 Installation

Clone the repository:

```bash
git clone <your-repository-url>
cd VectorVault
```

Install dependencies:

```bash
pip install pymongo google-genai python-dotenv langchain-core langchain-text-splitters langchain-google-genai scikit-learn
```

## 🔑 Environment Variables

Create a `.env` file in your project directory:

```env
GEMINI_API_KEY=your_gemini_api_key
MONGODB_URI=your_mongodb_connection_string
```

Never commit your `.env` file or expose your API keys.

Add this to `.gitignore`:

```gitignore
.env
.ipynb_checkpoints/
__pycache__/
```

## 🗄️ MongoDB Vector Search Index

Create a Vector Search index in MongoDB Atlas with the following configuration:

- **Index Name:** `vector_index`
- **Vector Field:** `embedding`
- **Dimensions:** `3072` (for the default Gemini embedding output)
- **Similarity:** `cosine`

## ▶️ Usage

1. Configure your Gemini API key and MongoDB connection string.
2. Run the Jupyter Notebook.
3. Load and process your documents.
4. Generate and store embeddings in MongoDB.
5. Create the MongoDB Vector Search index.
6. Enter a question when prompted.
7. Retrieve relevant chunks and generate an answer.

## 🧠 RAG Architecture

```text
       User Question
             |
             v
      Gemini Embedding
             |
             v
      Query Vector
             |
             v
    MongoDB Vector Search
             |
             v
     Relevant Documents
             |
             v
      Context Refinement
             |
             v
       LangChain Prompt
             |
             v
       Gemini LLM
             |
             v
       Final Answer
```

## 🎯 Project Objective

The objective of VectorVault is to understand and implement the core concepts of Retrieval-Augmented Generation, vector embeddings, semantic search, document chunking, and LLM-based question answering.

## 🔮 Future Improvements

- Add a Streamlit or web-based user interface.
- Implement advanced document reranking.
- Support PDF and multiple document formats.
- Add conversation memory.
- Improve retrieval accuracy and response evaluation.
- Support multiple knowledge bases.

## 👨‍💻 Author

**Your Name**

Built with Python, MongoDB, Gemini, and LangChain.

---

⭐ If you find this project interesting, consider giving it a star!