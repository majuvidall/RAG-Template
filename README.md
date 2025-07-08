# Retrieval-Augmented Generation (RAG) Template with LangChain

This repository contains a practical, customizable **RAG (Retrieval-Augmented Generation)** pipeline template using **LangChain**, featuring PDF document loading, **chunking**, **embeddings** generation, and integration with LLMs (such as **OpenAI**).

In this template, we use a base document (a scientific article on RAG) located in the `meus_arquivos` folder. All parameters and prompts are configured for that document—you should replace it with your own document and adapt the parameters and prompts as shown in each step.

---

## Introduction

**RAG (Retrieval-Augmented Generation)** is an approach that combines:
- Information retrieval from external sources (like PDF files)  
- Text generation with language models  

This template lets you build a complete pipeline that:
- Loads one or more PDF documents  
- Splits the texts into smaller pieces (chunks)  
- Generates embeddings for semantic search  
- Uses an LLM to answer questions based on the loaded documents  

---

## Environment Setup

Before starting, it’s recommended to use a virtual environment to avoid library conflicts and keep the project organized.

### Create a virtual environment and install dependencies

#### macOS / Linux / WSL
```
python3 -m venv rag-env
source rag-env/bin/activate
pip install -r requirements.txt

```
#### Windows PowerShell
```
python3 -m venv rag-env
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope Process
.\rag-env\Scripts\Activate
pip install -r requirements.txt

```

### Install required libraries

The libraries used in this project are listed in `requirements.txt`. Running:

```
pip install -r requirements.txt
```
This will install all listed packages. You only need to do this once.


## Project Structure

```
├── meus_arquivos       # Folder containing PDF files to process  
├── main_rag.ipynb      # Main notebook with the RAG pipeline  
├── requirements.txt    # Required libraries  
├── .env                # Stores your OpenAI API key  
└── README.md           # This file  
```

- The my_files folder contains the base document (a scientific article on RAGs). Replace it with the files you want to load into the RAG.

- .env is not included in the repo—you must create this file and add your OpenAI API key (https://openai.com/api/).


## OpenAI API Key Configuration

Create a `.env` file in the project root with your API key:

OPENAI_API_KEY=sk-xxxxxxxxxxxxxxxxxxxxxxxx

The notebook will use load_dotenv() to read this key automatically.


## Running the Pipeline

1. Activate your virtual environment and install dependencies  
2. Create the `.env` file and obtain your OpenAI API key  
3. Run the `main_rag.ipynb` notebook  
4. Follow these steps in order:  
   - Imports  
   - Document loading  
   - Chunking  
   - Embeddings creation and storage  
   - Retriever setup  
   - Prompt generation  
   - RAG Chain execution  













