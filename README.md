# Book Recommendation & Analysis App

This application provides intelligent book recommendation and analysis features by combining semantic search, classification, and sentiment analysis powered by modern machine learning models.

### 🚀 Features
1. Semantic Search
    * Uses `ChromaDB` as a vector database.
    * Employs `OpenAI Embeddings` to represent book descriptions in vector space.
    * Enables efficient semantic similarity search, so users can find books based on meaning rather than exact keywords.

2. Book Classification (Fiction vs Non-Fiction)
    * Implements `zero-shot` classification using the pre-trained `facebook/bart-large-mnli` model from Hugging Face.
    * Classifies books into Fiction or Non-Fiction categories, even without explicit labels in the dataset.

3. Sentiment & Emotion Analysis
    * Leverages the fine-tuned open-source model `j-hartmann/emotion-english-distilroberta-base` from Hugging Face.
    * Analyzes book descriptions to determine the dominant sentiment/emotion.
    * Supports multiple emotion classes, including joy, sadness, anger, fear, surprise, disgust, and neutral.

### 📌 Use Cases
* 📚 Book Recommendation: Find similar books to what you like.
* 🧠 Reader Insight: Understand the emotions conveyed in books.
* 🎭 Categorization: Automatically sort books into Fiction vs Non-Fiction.

### Dependencies Setup
* Install uv package manager:
```{bash}
pip isntall uv
```
* Create virtual environment with uv:
```{bash}
uv venv .venv
```
* Activate virtual environment:
```{bash}
source .venv/Scripts/activate
```
* Install Langchain dependencies:
```{bash}
uv pip install numpy pandas matplotlib seaborn
uv pip install langchain langchain_community
uv pip install langchain_openai
uv pip install langchain_chroma
```

* Install Huggingface zero-shot classifier pre-trained model:
```{bash}
uv pip install transformers, torch
pip install hf_xet
```

* Install gradio module for application interface:
```{bash}
uv pip install --upgrade gradio
```

### Deployment on Huggingface
* Authenticates your machine to the Hugging Face Hub using an access token:
```{bash}
huggingface-cli login
```
* Create a space on Huggingface
* Clone you huggingface space:
```{bash}
git clone https://huggingface.co/spaces/<username>/<repo name>
```
* Copy all files from gradio_app into the repo above:
```{bash}
cp -r README.md gradio_app/data gradio_app/img gradio_app/app.py gradio_app/helpers.py requirements.txt <repo name>/
```
* CD into the cloned repo:
```{bash}
cd <repo name>
```
* Hugging Face requires binary files like images to be tracked with Git LFS.In our case we have PNG:
```{bash}
git lfs install
git lfs track "*.png"
git add .
git commit -m "<commit message>"
git push origin main
```