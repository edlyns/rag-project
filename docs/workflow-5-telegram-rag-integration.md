# Workflow 5: Telegram RAG Bot Integration

## Deskripsi
Bot Telegram yang dapat menjawab pertanyaan berdasarkan dokumen yang tersimpan di Pinecone vector database.

## Cara Kerja
1. User kirim pertanyaan via Telegram
2. AI Agent pakai Pinecone tool untuk search dokumen relevan
3. AI generate jawaban berdasarkan context dari Pinecone
4. Bot reply ke user

## Komponen
- Telegram Trigger (receive messages)
- AI Agent dengan Pinecone Vector Store tool
- Send Message (reply to user)

## Tech Stack
- Telegram Bot API
- Google Gemini (AI Agent)
- Pinecone Vector Store (knowledge base)
- n8n orchestration

## Test Results
✅ Bot successfully answers questions from knowledge base
✅ Correctly retrieves context from Pinecone
✅ Responds "I cannot answer" when info not in knowledge base
