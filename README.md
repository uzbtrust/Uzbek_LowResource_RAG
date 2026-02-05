# Hallucination Detector

A lightweight Retrieval-Augmented-Generation (RAG) demo that uses LangChain, Hugging Face models, sentence-transformers embeddings, and FAISS to retrieve context and generate answers constrained to that context. The project is provided as a Jupyter notebook (`main.ipynb`) for experimentation and learning.

**Features**
- Create dense embeddings with `sentence-transformers`.
- Store and query vectors with FAISS.
- Use Hugging Face endpoints and models via LangChain integrations.
- Load API token from environment using `python-dotenv`.

**Prerequisites**
- Python 3.10 or newer
- Recommended: A virtual environment for dependency isolation

**Installation**
1. Create and activate a virtual environment:

```bash
python -m venv .venv
source .venv/bin/activate
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

**Configuration**
1. Create a `.env` file in the project root with your Hugging Face API token:

```
HUGGINGFACEHUB_API_TOKEN=<your_token_here>
```

The notebook calls `load_dotenv()` and reads the token with `os.getenv("HUGGINGFACEHUB_API_TOKEN")` so the token is automatically picked up from `.env`.

**Usage**
1. Start Jupyter Notebook and open `main.ipynb`:

```bash
jupyter notebook main.ipynb
```

2. Run the cells in order. The notebook demonstrates:
- Initializing `HuggingFaceEmbeddings` with `sentence-transformers/paraphrase-multilingual-MiniLM-L12-v2`.
- Building a FAISS vector store from text chunks.
- Loading a Hugging Face model endpoint and constructing a simple RAG pipeline.

**Files**
- [main.ipynb](main.ipynb) — Primary notebook demonstrating the pipeline
- [requirements.txt](requirements.txt) — Pinned Python dependencies
- [.gitignore](.gitignore) — Git ignore rules (includes `.env`)

**Notes & Recommendations**
- If you plan to run large models locally, ensure you have sufficient GPU and memory resources; otherwise use Hugging Face Endpoints or smaller models.
- `faiss-cpu` is specified for CPU-only environments; replace with the GPU variant if available.

Made with :heart by uzbtrust
# Uzbek_LowResource_RAG
