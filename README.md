
# 🚀 **FastAPI RAG Server**  
### 🧠 a lightweight FastAPI server designed for a Retrieval Augmented Generation (RAG) system

---

## 📝 **Overview**

This project implements a **lightweight FastAPI server** designed to support a **Retrieval Augmented Generation (RAG)** system. The server processes various document formats, generates embeddings using **Hugging Face's sentence-transformers**, and provides efficient querying via **ChromaDB** for vector-based retrieval.

---

## 🎯 **Key Features**

- **FastAPI Server**: Lightweight and asynchronous for handling **non-blocking operations**.  
- **ChromaDB Integration**: Persistent vector database for storing and querying document embeddings.  
- **Multi-format Support**: Ingestion support for **PDF**, **DOC**, **DOCX**, and **TXT** files.  
- **Embeddings**: Utilizes **sentence-transformers/all-MiniLM-L6-v2** for generating document embeddings.  
- **Concurrency**: Efficient handling of multiple requests using **FastAPI's async capabilities**.  
- **RAG System**: Retrieves relevant document chunks and generates context-aware responses.

---

## ⚙️ **Technologies Used**

- **FastAPI**: For building the server backend.  
- **ChromaDB**: Vector database for storing document embeddings.  
- **Sentence-Transformers**: For embedding generation.  
- **Hugging Face Inference API**: For generating RAG-based responses.  
- **PyPDF2 & python-docx**: For parsing and ingesting PDF and DOCX documents.  
- **Asyncio**: For handling asynchronous operations and tasks.

---

## 🛠️ **Installation & Setup**

1. **Clone the Repository**  
   ```bash
   git clone https://github.com/your-username/fastapi-rag-server.git
   cd fastapi-rag-server
   ```

2. **Create a Virtual Environment**  
   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows: venv\Scripts\activate
   ```

3. **Install Dependencies**  
   ```bash
   pip install -r requirements.txt
   ```

4. **Start the FastAPI Server**  
   ```bash
   uvicorn app:app --reload
   ```

5. **Access the Server**  
   Open your browser and go to `http://127.0.0.1:8000/docs` to see the interactive API documentation.

![image](https://github.com/user-attachments/assets/fdeac90d-39c2-4598-8075-023cb9a69f71)

---

## 📂 **Project Structure**

```
rag_server/
├── app.py              # Main FastAPI application
├── vector_db.py        # ChromaDB integration logic
├── load_data.py        # Document loading and splitting logic
├── prompts.py          # RAG prompt generation
├── utils.py            # Utility functions (e.g., async helpers)
├── ingest.py           # Document ingestion logic
├── COLLECTIONS.txt     # List of document collections
└── data/               # Directory for uploaded documents
```

---

## 🚀 **Endpoints**

### 1️⃣ **Upload Documents**  
**POST /upload**  
Upload documents (PDF, DOC, DOCX, or TXT) to the server for ingestion.
![image](https://github.com/user-attachments/assets/9f4f8aa1-ca09-4305-95be-6e6ff086256a)


### 2️⃣ **Query Documents**  
**POST /query**  
Submit a query to retrieve relevant document chunks using the embeddings generated by sentence-transformers.

![image](https://github.com/user-attachments/assets/99644ca1-bdc7-4c23-810f-0878d1c31cca)


### 3️⃣ **List Collections**  
**GET /collections**  
View all document collections stored in the database.

![image](https://github.com/user-attachments/assets/ec004007-00d7-4a3c-90ab-c7e9fe946b0b)

---

## 🌟 **Results**

The RAG server is capable of:

- **Uploading** and processing multiple document formats.
- **Efficiently querying** stored document collections using vector-based retrieval.
- Providing **contextual responses** based on the documents ingested.
- **Scalable** to handle various document types and collections with ease.

---

## 👨‍💻 **Contributing**

Contributions are welcome! To contribute:

1. Fork the repository.  
2. Create a new branch: `git checkout -b feature-branch-name`.  
3. Make your changes and commit them: `git commit -m 'Add some feature'`.  
4. Push to the branch: `git push origin feature-branch-name`.  
5. Submit a pull request!

---

## 📜 **License**

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🎉 **Conclusion**

This project demonstrates the power of modern **Python async programming**, advanced **NLP models**, and vector-based information retrieval with **ChromaDB** to create an efficient and scalable **Retrieval Augmented Generation system**.
