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
