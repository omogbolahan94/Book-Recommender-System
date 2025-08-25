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
    * Leverages the fine-tuned open-source model j-hartmann/emotion-english-distilroberta-base from Hugging Face.
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

* Install Huggingface dependencies for zero-shot classifier pre-trained model:
```{bash}
uv pip install transformers, torch
pip install hf_xet
```

* Install gradio module for application interface:
```{bash}
uv pip install --upgrade gradio
```
