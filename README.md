# Retrieval-Augmented Generation (RAG) Template with LangChain

Este repositório contém um *template* prático e personalizável para construir uma pipeline de **RAG (Retrieval-Augmented Generation)** utilizando *LangChain*, com carregamento de documentos PDF, *chunking*, geração de *embeddings* e integração com modelos LLM (como *OpenAI*).

Nesse *template*, usaremos um documento base (artigo científico sobre RAG), contido na nossa pasta 'meus_arquivos'. Todos os parâmetros e *prompts* estão configurados para esse documento. Você deve substituí-lo pelo documento que deseja carregar, e adaptar os parâmetros e *prompts*, como veremos em cada etapa. 

---

## Introdução

**RAG (Retrieval-Augmented Generation)** é uma abordagem que combina:
- Recuperação de informação de fontes externas (como arquivos PDF)
- Geração de texto com modelos de linguagem

Este template permite que você construa uma pipeline completa que:
- Carrega um ou mais documentos PDF
- Divide os textos em pedaços menores (chunks)
- Gera embeddings para permitir buscas semânticas
- Utiliza um modelo LLM para responder perguntas com base nos documentos carregados

---

## Setup do Ambiente

Antes de iniciar, é recomendado utilizar um ambiente virtual para evitar conflitos entre bibliotecas e manter o projeto organizado.

### Crie um ambiente virtual e instale as dependências

#### Mac/Linux/WSL

```
$ python3 -m venv rag-env
$ source rag-env/bin/activate
$ pip install -r requirements.txt
```

#### Windows Powershell
```
PS> python3 -m venv rag-env
PS> Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope Process
PS> .\rag-env\Scripts\Activate
PS> pip install -r requirements.txt

```

## Instale as bibliotecas necessárias

As bibliotecas usadas no projeto estão listadas no arquivo requirements.txt. Ao rodar "pip install -r requirements.txt", todas as bibliotecas listadas dentro desse arquivo serão instaladas. Isso só precisa ser feito uma vez. 

## Organização do Projeto


├── meus_arquivos               # Pasta com os arquivos PDF a serem processados
├── main_rag.ipynb              # Notebook principal com o pipeline RAG
├── requirements.txt            # Bibliotecas necessárias
├── .env                        # Armazena sua chave de API da OpenAI
└── README.md                   # Este arquivo


- A pasta 'meus_arquivos' contém um documento base (um artigo ciéntifico sobre RAGs). Você deve substituir com os arquivos que desejar carregar para a RAG. 
- O '.env' não está presente. Portanto, você deve criar esse arquivo, e gerar sua chave de API pelo site da OpenAI (https://openai.com/api/). 

## Configuração da chave da OpenAI 
Crie um arquivo .env na raiz do projeto com sua chave de API:

OPENAI_API_KEY=sk-xxxxxxxxxxxxxxxxxxxxxxxx

O notebook usará load_dotenv() para ler essa chave automaticamente.

##  Execução

1. Ative seu ambiente virtual e instale as bibliotecas

2. Crie o arquivo .env e gere sua chave de API na OpenAI

3. Execute o notebook main_notebook.ipynb

4. Siga as etapas:

    - Importações

    - Carregamento dos documentos

    - Chunking

    - Criação e armazenamento de embeddings

    - Retriever

    - Geração de prompt

    - RAG Chain