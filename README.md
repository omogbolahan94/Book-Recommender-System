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
* Install other dependencies:
```{bash}
uv pip install numpy pandas matplotlib seaborn
uv pip install langchain langchain_community
uv pip install langchain_openai
uv pip install langchain_chroma
```
