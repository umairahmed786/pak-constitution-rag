# ConstitutionRAG 🇵🇰
**Retrieval-Augmented Generation (RAG) on the Constitution of Pakistan**

This project is an AI-powered **legal assistant** that allows users to **chat with the Constitution of Pakistan**.  
It uses **LangChain**, **ChromaDB**, and **OpenAI GPT models** to provide accurate, context-aware answers directly from the text of the Constitution.  

---

## 🚀 Features
- 📄 Load and process the **Constitution of Pakistan (PDF)**  
- ✂️ Split documents into semantic **chunks** for efficient retrieval  
- 🧠 Store embeddings in a **ChromaDB vector store**  
- 📊 **2D & 3D visualization** of embeddings using **t-SNE + Plotly**  
- 🔎 RAG pipeline with **LangChain’s ConversationalRetrievalChain**  
- 💬 Interactive **Gradio chat interface** for user queries  

---

## ⚙️ Tech Stack
- [LangChain](https://www.langchain.com/) – RAG pipeline  
- [ChromaDB](https://www.trychroma.com/) – Vector database  
- [OpenAI GPT](https://platform.openai.com/) – LLM (gpt-4o-mini)  
- [PyPDFLoader](https://api.python.langchain.com/en/latest/loaders/langchain.document_loaders.pdf.PyPDFLoader.html) – PDF document loader  
- [t-SNE](https://scikit-learn.org/stable/modules/generated/sklearn.manifold.TSNE.html) + [Plotly](https://plotly.com/python/) – Embedding visualization  
- [Gradio](https://www.gradio.app/) – Web-based chat interface  

---

## 📂 Workflow
1. Upload **Constitution.pdf** into Colab  
2. Load and split into chunks (1000 tokens, 200 overlap)  
3. Generate embeddings with **OpenAIEmbeddings**  
4. Store in **ChromaDB**  
5. Visualize embeddings in **2D/3D**  
6. Query via **ConversationalRetrievalChain**  
7. Chat interactively with the Constitution using **Gradio**  

---

## ▶️ Run in Google Colab
1. Upload `Constitution.pdf` to `/content/`  
2. Set your **OpenAI API Key** in Colab:
   ```python
   from google.colab import userdata
   openapikey = userdata.get('OPENAI_API_KEY') ```
3. Run the notebook cells step by step
4. Launch Gradio interface and start chatting 🎉


## 📌 Future Improvements
- Add support for multiple legal documents (e.g., PPC, PECA)
- Enable multilingual queries (Urdu + English)
- Improve retrieval with hybrid search (BM25 + embeddings)
