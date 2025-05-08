# ITC-finance-app
# 📊 ITC Reports Analyzer – Offline HuggingFace-Powered Q&A App

This intelligent Q&A app enables **offline, privacy-focused** analysis of ITC Ltd.’s financial and sustainability reports using **local Hugging Face models**. Ask questions about revenue, ESG efforts, or annual KPIs – the app retrieves accurate answers with **local inference and vector search**.

---

## 🌟 Key Capabilities

- 🤖 **Offline HuggingFace LLMs**: Uses models like `flan-t5-base` for fully local question answering – no cloud required.
- 🧬 **Local Embeddings**: Powered by `sentence-transformers` and stored in a Chroma vector DB for fast, relevant document retrieval.
- 🗂️ **Persistent ChromaDB**: Easily zip, reuse, or update the vector store without recomputing embeddings.
- 🧑‍💻 **Custom Streamlit UI**: Styled with distinct color schemes and layouts for better UX.

---

## 📚 ITC PDF Extractor (Preprocessing Module)

Use any pre-extraction tool (e.g., `tavily`, `PyMuPDF`, or `pdfplumber`) to convert ITC Annual Reports (2023–2024) into plain text and metadata-rich LangChain Documents.

### 🧪 Sample Preprocessing Pipeline

- ✅ Chunk using `RecursiveCharacterTextSplitter`
- ✅ Embed with `sentence-transformers/all-mpnet-base-v2`
- ✅ Persist to local vector store using ChromaDB

bash
pip install langchain chromadb sentence-transformers
## 🧠 Local Question Answering Engine

This module powers the Q&A logic using an **offline pipeline**:

- 🔍 **Semantic search using MMR** (Maximal Marginal Relevance)
- 💬 **Answer generation** with Hugging Face models (`flan-t5-small`, `base`, or `large`)
- 🧾 **Answers include contextual source snippets** for full transparency
## 💬 Streamlit Chat UI

The frontend provides a chat-style interface where users can:

- ❓ Ask questions like “What were the sustainability efforts in 2023?”
- 📄 View exact answers and see which report content was used
- 🎨 Enjoy a modern design with custom input boxes and background styling
## ⚙️ Getting Started

1. **Clone the repository**

bash
git clone https://github.com/yourusername/itc-offline-analyzer.git
cd itc-offline-analyzer
Place your preprocessed Chroma DB folder (e.g., `chroma_db_new`) in the root directory.

Run the Streamlit app:

bash
streamlit run app.py




# check out the link: https://huggingface.co/spaces/AbhiReddy1/itc_revenue

