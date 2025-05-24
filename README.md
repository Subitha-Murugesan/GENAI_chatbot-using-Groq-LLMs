# GENAI_chatbot-using-Groq-LLMs

This is a simple Streamlit application that uses **LangChain**, **Groq LLMs**, **FAISS**, and **Web Document Retrieval** to answer user questions based on web documentation.

## Features

* Loads documentation from a URL using `WebBaseLoader`
* Splits and embeds documents with `OllamaEmbeddings` and `FAISS`
* Uses `Groq` LLM (`gemma2-9b-it`) to generate answers
* Retrieval-augmented generation using LangChain's `retrieval_chain`
* Interactive UI with Streamlit
* Shows document chunks used to generate the answer

## Requirements

Install dependencies with:

```bash
pip install -r requirements.txt
```

Example `requirements.txt`:

```
streamlit
langchain
langchain-community
langchain-core
langchain-groq
faiss-cpu
python-dotenv
```

## Environment Variables

Create a `.env` file with your Groq API key:

```
GROQ_API_KEY=your_groq_api_key_here
```

## 🏁 How to Run

```bash
streamlit run app.py
```

## How It Works

1. **Load**: Web documentation is loaded from LangChain's docs.
2. **Split**: Text is chunked using `RecursiveCharacterTextSplitter`.
3. **Embed**: Embeddings are generated with `OllamaEmbeddings`.
4. **Store**: Documents are stored in a FAISS vector store.
5. **Retrieve & Generate**: Given a prompt, relevant docs are retrieved and fed into Groq's LLM to answer.

## Screenshot
![image](https://github.com/user-attachments/assets/bd0956c3-0ef4-47de-be38-637e7de9d8b9)


