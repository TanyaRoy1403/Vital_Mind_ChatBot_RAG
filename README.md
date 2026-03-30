<h1 align="center">🧠 VitalMind - AI Powered RAG Chatbot</h1>

An end-to-end **Retrieval-Augmented Generation (RAG)** based chatbot that processes PDF documents, converts them into embeddings, and enables intelligent question answering using LLMs (Mistral AI).

---

## 🚀 Project Overview

VitalMind is a production-ready AI system that:

⚠️ Currently, the system is configured using a medical-domain PDF dataset to demonstrate domain-specific question answering.
* 📄 Ingests PDF documents
* ✂️ Splits text into chunks using LangChain
* 🧠 Converts text into embeddings
* 📦 Stores embeddings in FAISS vector database
* 🔍 Retrieves relevant context using semantic search
* 🤖 Generates answers using Mistral LLM
* 🌐 Serves responses via Flask web application

---

## 🧠 How It Works (RAG Pipeline)

1. PDF is loaded from `data/`
2. Text is split into smaller chunks
3. Each chunk is converted into embeddings
4. Embeddings are stored in FAISS (`vectorstore/`)
5. User query → converted into embedding
6. Similar chunks retrieved using vector search
7. Context + Query → passed to Mistral LLM
8. Final response generated and shown in UI

---

## 🏗️ Project Architecture

### ⚙️ Setup & Configuration

* Virtual environment setup
* Logging system
* Custom exception handling
* Environment variables

### 📂 Data Processing

* PDF loading
* Text chunking (LangChain)
* Embedding generation
* FAISS storage

### 🤖 LLM & Retrieval

* Mistral AI integration
* Retriever pipeline
* Semantic search

### 🌐 Application Layer

* Flask backend
* HTML/CSS frontend

### 🚢 Deployment & DevOps

* Docker containerization
* Jenkins CI/CD pipeline
* Trivy security scan
* AWS ECR + App Runner deployment

---

## 🛠️ Tech Stack

| Category        | Tools                 |
| --------------- | --------------------- |
| Language        | Python                |
| Backend         | Flask                 |
| LLM             | Mistral AI            |
| NLP             | LangChain             |
| Vector DB       | FAISS                 |
| Frontend        | HTML, CSS             |
| DevOps          | Docker, Jenkins       |
| Cloud           | AWS (ECR, App Runner) |
| Version Control | GitHub                |

---

## 📁 Project Structure

```
Vital_Mind_ChatBot_RAG/
│
├── app/
│   ├── __pycache__/
│   ├── common/          # Utilities & shared code
│   ├── components/      # Core pipeline logic (RAG)
│   ├── config/          # Configuration files
│   ├── templates/       # HTML frontend
│   ├── __init__.py
│   └── application.py   # Main Flask app
│
├── custom_jenkins/
│   └── Dockerfile       # CI/CD Docker config
│
├── data/
│   └── *.pdf            # Input documents
│
├── logs/                # Application logs
│
├── vectorstore/
│   └── db_faiss/
│       ├── index.faiss  # Vector index
│       └── index.pkl    # Metadata
│
├── Dockerfile
├── Jenkinsfile
├── requirements.txt
├── setup.py
└── .gitignore
```

---

## ⚡ Setup Instructions

### 1. Clone Repo

```
git clone https://github.com/TanyaRoy1403/Vital_Mind_ChatBot_RAG.git
cd Vital_Mind_ChatBot_RAG
```

### 2. Create Virtual Environment

```
python -m venv venv
venv\Scripts\activate
```

### 3. Install Dependencies

```
pip install -r requirements.txt
```

### 4. Add Environment Variables

Create `.env` file:

```
MISTRAL_API_KEY=your_api_key
```

### 5. Run Application

```
python app/application.py
```

---

## 🐳 Docker Setup

### Build

```
docker build -t vitalmind .
```

### Run

```
docker run -p 5000:5000 vitalmind
```

---

## 🔁 CI/CD Pipeline

1. Code pushed to GitHub
2. Jenkins triggers pipeline
3. Docker image built
4. Security scan using Trivy
5. Image pushed to AWS ECR
6. Deployed via AWS App Runner

---

## 🧪 Example Usage

**Input Query:**

```
What is mental health?
```

**Output:**

```
Mental health refers to a person’s emotional, psychological, and social well-being...
```

---

## ✨ Key Features

* 📄 PDF-based knowledge system
* 🔍 Semantic search (FAISS)
* 🤖 LLM-powered answers
* ⚡ Fast retrieval pipeline
* 🌐 Web interface (Flask)
* 🚀 Production-ready deployment

---

## 🔮 Future Improvements

* Multi-PDF support
* Chat history memory
* Authentication system
* UI improvements
* Multi-LLM support

---

## 👩‍💻 Author

**Tanya Roy**

---

## ⭐ If you like this project

Give it a ⭐ on GitHub and feel free to contribute!

---


