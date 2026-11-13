# RAG Chatbot with n8n, Gemini & Pinecone

An AI chatbot that answers questions based on your own documents, using **Retrieval-Augmented Generation (RAG)**. Documents from Google Drive are split into chunks, embedded with Google Gemini, and stored in a Pinecone vector database. Users can then ask questions through a **Telegram bot** or a **web app**, and the AI answers using only the relevant document context.

Built step by step in January 2026 as six n8n workflows, from a simple chatbot to a full RAG system with public deployment.

## Features

- **Document ingestion pipeline**: Google Drive → text extraction → chunking (JavaScript) → Gemini embeddings → Pinecone (1,900+ vectors, 768 dimensions)
- **Telegram RAG bot**: answers questions from the knowledge base and says it cannot answer when the information is not in the documents
- **Web app chat**: HTML/CSS/JavaScript frontend connected to n8n through a webhook
- **Deployment**: n8n in Docker, exposed with Cloudflare Tunnel; frontend deployed on Vercel / Cloudflare Pages

## Workflows

| # | Workflow | What it does |
|---|----------|--------------|
| 1 | Telegram Bot → OpenAI | Basic Telegram chatbot powered by OpenAI |
| 2 | WebApp → Google Gemini | Web chat that sends questions to Gemini via an n8n webhook |
| 3 | Google Drive → Pinecone | Builds the vector database from documents in Google Drive |
| 5 | Telegram RAG Bot | Telegram bot that retrieves context from Pinecone before answering |
| 6 | WebApp RAG | Web chat with the same RAG capability |

Exported workflow files are in `backend/`, and documentation for each workflow is in `docs/`.

## Tech Stack

- **Orchestration:** n8n
- **AI:** Google Gemini (chat + `text-embedding-004`), OpenAI
- **Vector database:** Pinecone
- **Integrations:** Telegram Bot API, Google Drive API
- **Frontend:** HTML, CSS, JavaScript
- **Infrastructure:** Docker & Docker Compose, Cloudflare Tunnel, Vercel, Cloudflare Pages

## Project Structure

```
rag-project/
├── backend/      # Exported n8n workflows (JSON)
├── frontend/     # Web chat app
├── docker/       # Docker Compose setup for n8n
├── cloudflare/   # Cloudflare Tunnel configuration
└── docs/         # Documentation for each workflow
```

## Running Locally

1. Copy `docker/.env.example` to `docker/.env` and fill in your values.
2. Start n8n: `docker compose -f docker/docker-compose.yml up -d n8n`
3. Open n8n at `http://localhost:5678` and import the workflows from `backend/`.
4. Add your own credentials in n8n (Telegram, Google Gemini, Google Drive, Pinecone).
5. Activate the workflows and update the webhook URL in `frontend/index.html`.
6. To expose n8n publicly, copy `cloudflare/config.example.yaml` to `cloudflare/config.yaml`, fill in your tunnel ID, and run `cloudflared tunnel --config cloudflare/config.yaml run`.

> API keys and tokens are never stored in this repository. Add them through n8n credentials or your local `.env` file.

## Author

Edelyn Ananta · Software Engineering student, UII × Nanjing Xiaozhuang University double degree
