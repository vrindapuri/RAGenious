# 📚 PDF Document Assistant

An intelligent document exploration tool powered by React + FastAPI. Upload your PDFs, ask natural language questions, and get instant answers — all from your local machine.

---

## 🌟 Project Highlights

- 🔍 Ask questions across uploaded PDF documents
- 📄 Drag and drop multi-PDF upload support
- 🧠 RAG-powered backend using local vector DB (Chroma)
- ⚛️ Frontend built with React and Axios
- ⚡ Real-time query response via FastAPI endpoints

---

## 🧠 Why This Project?

Reading long PDF documents and manually searching for information is tedious. This assistant turns **static documents into interactive knowledge bases**, allowing you to **query documents conversationally**.

---

## 🛠️ Tech Stack

| Layer      | Tech                              |
|------------|-----------------------------------|
| Frontend   | React, JavaScript, Axios          |
| Backend    | FastAPI, Python                   |
| Embedding  | LangChain + Sentence Transformers |
| Vector DB  | Chroma                            |

---

## 🚀 How to Run Locally

### ⚙️ Backend Setup (FastAPI)

```bash
cd backend
python -m venv venv
venv\Scripts\activate       # Windows
# or
source venv/bin/activate   # Mac/Linux

pip install -r requirements.txt
uvicorn main:app --reload