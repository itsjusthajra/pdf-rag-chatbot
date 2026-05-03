# pdf-rag-chatbot
Chat with any PDF using RAG, powered by Groq (Llama 3.1), LangChain, and FAISS. Deployed on Hugging Face Spaces.

Built this to get hands-on with RAG pipelines and see how well semantic search + LLMs work together on real documents.
 
---
 
## 🔗 Live Demo
 
👉 [Try it on Hugging Face Spaces](https://huggingface.co/spaces/itsjusthajra/ask-my-pdf) 
 
---
 
## How it works
 
1. You upload a PDF
2. The app splits it into chunks and embeds them using `all-MiniLM-L6-v2`
3. Your question is matched against the chunks using FAISS similarity search
4. The top results are passed to Groq's Llama 3.1 to generate a response
   
So the model only answers based on what's actually in your document.

 <img width="703" height="423" alt="image" src="https://github.com/user-attachments/assets/f9ff2097-83f3-4152-b33e-f12b5c78a344" />
 
---
 
## Stack
 
- **LangChain** : document loading, chunking, retrieval pipeline
- **FAISS** : vector similarity search
- **HuggingFace Embeddings** : `all-MiniLM-L6-v2`
- **Groq (Llama 3.1 8B)** : LLM for response generation
- **Gradio** : chat UI
---
 
## Run locally
 
```bash
git clone https://github.com/itsjusthajra/pdf-rag-chatbot
cd pdf-rag-chatbot
pip install -r requirements.txt
```
- Get a free Groq API key at [console.groq.com](https://console.groq.com)
- Enter it in the notebook when prompted
