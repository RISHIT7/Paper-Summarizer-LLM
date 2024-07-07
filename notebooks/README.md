# Paper Summarizer Using Llama Notebook
This Jupyter Notebook demonstrates using the Meta-Llama-3-8B-Instruct-GGUF model for summarizing research papers. The notebook leverages HuggingFace's open-source models for natural language processing tasks.

## Usage
The notebook has been conveniently provided as a Kaggle file in the link below, with the used model as a dataset
- [Research Paper Summarizer](https://www.kaggle.com/code/rishitjakharia/research-paper-summarizer)
- [Meta-LlaMA Model Dataset](https://www.kaggle.com/datasets/rishitjakharia/meta-llama)

## Current Architecture (Version 1)
![architecture_0](../images/architecture_0.png)
----
> ### Config
> ---
> - `k = 1`
> - `RecursiveTextSplitter` for Chunking and splitting
> - `Llama-3-8B-Instruct-GGUF.Q5_K_M` as Language Model
> ### Next Version ideas
> ---
> - Currently, we only use abstract for the new summary; next, we will fetch the pdf, store it as embeddings, and use it.
> - Next is to iterate on different embeddings and models and also experiment with parsers to increase accuracy
> - Also, make a GUI and host the application
