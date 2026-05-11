ScholarBot: Research Paper Q&A Assistant

A Retrieval-Augmented Generation (RAG) based Research Paper Question Answering system developed using Open-LLaMA 3B, FAISS, LangChain, and Gradio.

The application enables users to upload research paper PDFs and ask natural language questions related to the document. The system retrieves relevant contextual information from the uploaded paper and generates answers using a Large Language Model (LLM).

---

Features:

- Upload and process research paper PDFs
- Natural language question answering
- Retrieval-Augmented Generation (RAG) pipeline
- Semantic search using FAISS vector database
- Open-LLaMA 3B integration
- HuggingFace embeddings support
- Interactive Gradio web interface
- Dynamic PDF-based knowledge base
- GPU acceleration support in Google Colab

---

Technologies Used:

- Python
- Transformers
- LangChain
- FAISS
- Sentence Transformers
- Open-LLaMA 3B
- Gradio
- PyPDF2
- pdfplumber
- Google Colab

---

Project Structure:

```bash
research-paper-qa-assistant/
│── notebook.ipynb
│── README.md
│── requirements.txt
│── .gitignore

```
Model Loading

The project supports two methods for loading the language model.

1. Loading the Model from Google Drive

The Open-LLaMA 3B model is stored in Google Drive and loaded directly into Google Colab during runtime.

Example:

model_path = "/content/drive/MyDrive/OpenLLaMA_Models/openllama3b_model"

2. Loading the Model from HuggingFace

The model can also be downloaded directly from HuggingFace.

Example:

llama_model_name = "openlm-research/open_llama_3b"

How to Run
Step 1: Open the Notebook in Google Colab

Upload or open notebook.ipynb in Google Colab.

Step 2: Install Dependencies

Run all notebook cells to install the required packages.

Step 3: Load the Model

Choose either:

Google Drive model loading
HuggingFace model loading
Step 4: Launch the Application

Run the Gradio interface cell:

demo.launch(share=True, debug=True, show_error=True)
PDF Processing Workflow
Upload a research paper PDF
Extract text using PyPDF2 or pdfplumber
Split text into chunks
Generate embeddings
Store embeddings in the FAISS vector database
Retrieve relevant context for user queries
Generate answers using Open-LLaMA 3B

Notes
Best performance is achieved using GPU-enabled Google Colab runtime.
Text-based PDFs work better than scanned PDFs.
Large model files are not uploaded to GitHub due to storage limitations.

Author
Abhinav Upadhyay
