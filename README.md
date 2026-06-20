# 🔗 Smart URL Answer Bot

A Retrieval-Augmented Generation (RAG) application that allows users to provide website URLs, automatically extract and index their content, and then ask questions based on that content using an LLM.

Built with Streamlit, LangChain, ChromaDB, Hugging Face Embeddings, and Groq Llama 3.3.

---

## 🚀 Features

- Process up to 3 URLs simultaneously
- Extract content directly from web pages
- Automatically split content into chunks
- Generate vector embeddings using Hugging Face models
- Store embeddings in Chroma Vector Database
- Ask natural language questions about the processed content
- Retrieve source references along with answers
- Interactive Streamlit UI

---

## 🏗️ Architecture

```text
User URLs
    │
    ▼
UnstructuredURLLoader
    │
    ▼
Text Splitter
    │
    ▼
Hugging Face Embeddings
    │
    ▼
Chroma Vector Store
    │
    ▼
Retriever
    │
    ▼
Groq Llama 3.3
    │
    ▼
Answer + Sources
```

---

## 🛠️ Tech Stack

### Frontend
- Streamlit

### LLM
- Groq
- Llama 3.3 70B Versatile

### Embeddings
- Alibaba-NLP/gte-base-en-v1.5

### Vector Database
- ChromaDB

### Frameworks
- LangChain

### Data Loading
- UnstructuredURLLoader

---

## 📂 Project Structure

```text
RAG_app/
│
├── main.py
├── rag.py
├── requirements.txt
│
├── resources/
│   └── vector_store/
│
└── .env
```

---

## ⚙️ Installation

### 1. Clone Repository

```bash
git clone https://github.com/pranavmulaye08/News_Rag_App.git
cd News_Rag_App
```

### 2. Create Virtual Environment

Windows:

```bash
python -m venv venv
venv\Scripts\activate
```

Linux/Mac:

```bash
python -m venv venv
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 🔑 Environment Variables

Create a `.env` file in the project root.

```env
GROQ_API_KEY=your_groq_api_key
HUGGINGFACEHUB_API_TOKEN=your_huggingface_token
```

### Get API Keys

#### Groq

https://console.groq.com

#### Hugging Face

https://huggingface.co/settings/tokens

---

## ▶️ Run Application

```bash
streamlit run main.py
```

Application will launch at:

```text
http://localhost:8501
```

---

## 📖 How to Use

### Step 1

Enter one or more URLs in the sidebar.

Example:

```text
https://example.com/article1
https://example.com/article2
```

### Step 2

Click:

```text
🚀 Process URLs
```

The application will:

- Load webpage content
- Split content into chunks
- Generate embeddings
- Store vectors in ChromaDB

### Step 3

Ask questions in the chat box.

Example:

```text
What is the main topic discussed?
```

```text
Summarize the article in 5 points.
```

```text
What are the key findings?
```

---

## 🔍 Example Workflow

### URLs

```text
https://en.wikipedia.org/wiki/Artificial_intelligence
```

### Question

```text
What is Artificial Intelligence?
```

### Output

```text
Artificial Intelligence (AI) is a field of computer science focused on creating systems capable of performing tasks that typically require human intelligence.
```

---

## 🧠 Model Details

| Component | Model |
|------------|---------|
| LLM | Llama 3.3 70B Versatile |
| Provider | Groq |
| Embedding Model | Alibaba-NLP/gte-base-en-v1.5 |
| Vector DB | ChromaDB |

---

## 📸 Application Screenshot

Add your screenshot here:

```text
docs/app_screenshot.png
```

---

## 🚧 Future Enhancements

- Upload PDF support
- Upload DOCX support
- Multi-document chat
- Conversation memory
- Streaming responses
- Citation highlighting
- Deploy on Streamlit Cloud
- Docker support

---

## 👨‍💻 Author

**Pranav Mulaye**

Data Analyst | AI/ML Enthusiast | Generative AI Developer

GitHub:
https://github.com/pranavmulaye08

---

## 📄 License

This project is licensed under the MIT License.
