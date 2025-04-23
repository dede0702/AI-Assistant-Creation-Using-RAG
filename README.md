# 🤖 Assistente Virtual de IA com Arquitetura RAG

André Rovai Jr RM555848

Este projeto tem como objetivo criar um **assistente virtual inteligente** para responder dúvidas sobre os **avanços mais recentes em Inteligência Artificial**, utilizando a arquitetura **RAG (Retrieval-Augmented Generation)**. A aplicação é alimentada por conteúdos extraídos de **PDFs e links web especializados**, oferecendo respostas contextualizadas e atualizadas.

---

## 📚 Objetivo do Exercício

Desenvolver um assistente virtual com as seguintes características:

- Utiliza **RAG (Retrieval-Augmented Generation)** como base.
- Integra um modelo LLM da OpenAI (`gpt-4o-mini`) para geração de respostas.
- Alimentado com **PDFs** e **links da web** sobre IA contemporânea.
- Utiliza **FAISS** para indexação local e busca semântica.
- Exclui vídeos do YouTube (nesta versão).

---

## 🔧 Tecnologias Utilizadas

- **LangChain** – Framework para criação de aplicações LLM.
- **OpenAI GPT-4o-mini** – Modelo de linguagem usado para respostas.
- **FAISS** – Vetorização e indexação eficiente de documentos.
- **LangChain Text Splitters** – Para dividir os documentos em pedaços manejáveis.
- **PDFLoader & UnstructuredURLLoader** – Para carregar fontes em PDF e URLs.
- **Google Colab** – Ambiente de desenvolvimento (pode ser adaptado para ambiente local).
- **Python 3.10+**

---

## 🚀 Como Executar

1. **Clone o repositório** e abra o notebook:
    ```bash
    git clone https://github.com/seu-usuario/assistente-ia-rag.git
    cd assistente-ia-rag
    ```

2. **Instale as dependências**:
    - No Google Colab, elas já estão no notebook.
    - Para rodar localmente:
      ```bash
      pip install -r requirements.txt
      ```

3. **Insira sua chave da OpenAI**:
    - No Colab, use `userdata.get()` ou insira manualmente quando solicitado.
    - Localmente, defina como variável de ambiente:
      ```bash
      export OPENAI_API_KEY="sua-chave-aqui"
      ```

4. **Execute o notebook** passo a passo para carregar os dados e inicializar o assistente.

---

## 🧠 Funcionamento

1. O sistema carrega os conteúdos (PDFs e links).
2. Os textos são divididos em fragmentos menores.
3. É feita a vetorização com `text-embedding-ada-002`.
4. Os vetores são armazenados em um índice FAISS.
5. Quando o usuário faz uma pergunta, o sistema:
   - Recupera os trechos mais relevantes.
   - Gera uma resposta com base no contexto usando o LLM.

---

## 📂 Estrutura do Projeto

```
📁 assistente-ia-rag/
├── AI_Assistant_Creation_Using_RAG.ipynb  # Notebook principal
├── requirements.txt                       # Dependências para ambiente local
└── README.md                              # Este arquivo
```

---

## ✅ Requisitos

- Conta na [OpenAI](https://platform.openai.com) com chave da API ativa.
- Google Colab (ou ambiente local com Python 3.10+).
- Conexão com a internet para carregar URLs e baixar PDFs.

---

## 💡 Sugestões Futuras

- Adicionar suporte a vídeos do YouTube com transcrição.
- Criar interface gráfica (web ou chatbot).
- Usar banco de dados em nuvem para persistência.
- Deploy em ambiente de produção com FastAPI.

---

## 👥 Autoria

Desenvolvido como parte do exercício de criação de assistente RAG para a disciplina de **Inteligência Artificial**, com foco em temas atuais e arquitetura moderna de sistemas baseados em LLM.
