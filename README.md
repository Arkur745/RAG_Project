# 🤖 RAG PDF Chatbot with Chat History

A conversational AI app that lets you **chat with your PDFs**!  
Upload any PDF, ask questions about its content, and enjoy a contextual conversation powered by Retrieval-Augmented Generation (RAG), LangChain, Streamlit, and Groq.

---

## 🚀 Features

- **PDF Upload:** Instantly chat with any PDF (research papers, manuals, reports, etc.)
- **Conversational Memory:** Maintains chat history for context-aware Q&A
- **RAG Pipeline:** Uses LangChain’s RAG for accurate, document-grounded answers
- **LLM-Powered:** Utilizes Groq LLM and HuggingFace Embeddings
- **Interactive UI:** Built with Streamlit for a seamless web experience

---

## 🛠️ Tech Stack

- Python
- [Streamlit](https://streamlit.io/)
- [LangChain](https://www.langchain.com/)
- [Groq LLM](https://groq.com/)
- [HuggingFace Embeddings](https://huggingface.co/)
- [ChromaDB](https://www.trychroma.com/)
- [dotenv](https://pypi.org/project/python-dotenv/)

---

## 📦 Installation

1. **Clone the repo:**
    ```bash
    git clone https://github.com/yourusername/rag-pdf-chatbot.git
    cd rag-pdf-chatbot
    ```

2. **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

3. **Set up environment variables:**
    - Create a `.env` file in the root directory (do **not** commit this file!):
      ```
      GROQ_API_KEY=your_groq_api_key
      HF_TOKEN=your_huggingface_token
      ```
    - (Optional) Copy `.env.example` to `.env` and fill in your keys.

---

## ▶️ Usage

1. **Run the app:**
    ```bash
    streamlit run app.py
    ```

2. **Open your browser** to the Streamlit URL (usually [http://localhost:8501](http://localhost:8501)).

3. **Upload a PDF** and start chatting!

---

## 💡 How It Works

- **Upload:** The PDF is loaded and split into chunks.
- **Embed:** Chunks are embedded using HuggingFace models and stored in ChromaDB.
- **Ask:** Your question (and chat history) is used to reformulate ambiguous queries.
- **Retrieve:** The most relevant chunks are retrieved from the vector store.
- **Answer:** The LLM answers your question, grounded in the document content.

---


## ⚠️ Security

**Never commit your `.env` file or any file containing API keys.**  
Add `.env` to your `.gitignore` and share a `.env.example` with placeholder values.

---

