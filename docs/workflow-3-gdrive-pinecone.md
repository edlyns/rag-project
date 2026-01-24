# Workflow 3: Google Drive → Embedding → Pinecone

## Deskripsi
Workflow RAG untuk membuat vector database dari dokumen di Google Drive.

## Komponen
1. Google Drive Trigger
2. Download file
3. Extract from File
4. Code in JavaScript (chunking)
5. Pinecone Vector Store (Google Gemini embeddings)

## Results
- Successfully processed documents
- 1,900+ vectors stored in Pinecone
- Index: rag-documents (768 dimensions)

## Tech Stack
- Google Drive API
- Google Gemini (text-embedding-004)
- Pinecone Vector Database
- n8n workflow orchestration
