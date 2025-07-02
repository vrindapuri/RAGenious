# RAGenious

RAGenious is a full-stack multi-document search assistant built with Retrieval-Augmented Generation (RAG) techniques. It leverages Generative AI LLMs to provide intelligent answers from user-uploaded PDFs.

Tech stack used:

* 🧠 Langchain + OpenAI (RAG)
* ⚙️ FastAPI + Python backend
* 🧠 ChromaDB (Vector DB)
* ☁️ AWS S3 for file storage
* 🌐 React.js frontend
* 🐳 Docker for containerization
* ☁️ AWS ECR, EC2 for deployment

---

## 🔧 Project Structure

```
RAGenious/
├── backend/            # FastAPI, RAG logic, S3, embedding
├── frontend/           # React UI for PDF upload and chat
├── .env                # Environment variables (not pushed)
├── .gitignore
└── README.md
```

---

## 🚀 Setup & Run Locally

### 1. Clone and Install

```bash
git clone https://github.com/vrindapuri/RAGenious.git
cd RAGenious
```

### 2. Backend Setup

```bash
cd backend
pip install -r requirements.txt
python main.py
```

### 3. Frontend Setup

```bash
cd frontend
npm install
npm start
```

---

## 🌍 Environment Variables (.env)

Make sure you create a `.env` file in the root directory with:

```dotenv
AWS_ACCESS_KEY_ID=your_access_key_here
AWS_SECRET_ACCESS_KEY=your_secret_key_here
AWS_REGION=your_aws_region
AWS_S3_BUCKET_NAME=your_bucket_name
```

> 🔐 **Make sure `.env` is in your `.gitignore`**

---

## 📦 Deployment (Optional)

RAGenious is ready to be deployed using Docker and AWS. Follow these simplified steps:

### 🔨 Docker Build

```bash
# Backend
cd backend
docker build -t rag-backend .

# Frontend
cd ../frontend
docker build -t rag-frontend .
```

### ☁️ AWS ECR Push

* Authenticate to AWS ECR:

```bash
aws ecr get-login-password | docker login --username AWS --password-stdin <your-aws-account>.dkr.ecr.<region>.amazonaws.com
```

* Tag & push:

```bash
docker tag rag-backend:latest <account>.dkr.ecr.<region>.amazonaws.com/rag-backend

docker tag rag-frontend:latest <account>.dkr.ecr.<region>.amazonaws.com/rag-frontend
```

### 🚀 EC2 + NGINX Deployment

Run containers on EC2 and use NGINX to reverse proxy traffic to ports `3000` (frontend) and `8000` (backend).


---

## 📄 License

MIT License 2025 © Vrinda Puri

