cat > workflow-2-webapp-gemini.md << 'EOF'

# Workflow 2: WebApp to Google Gemini via n8n

## Deskripsi

WebApp sederhana yang mengirim pertanyaan ke n8n melalui webhook, diproses oleh Google Gemini AI, dan mengirim response kembali ke WebApp.

## Komponen

- **Webhook**: Menerima POST request dari WebApp
- **AI Agent (Google Gemini)**: Memproses pertanyaan
- **Edit Fields**: Format response
- **Respond to Webhook**: Mengirim jawaban kembali

## Tech Stack

- Frontend: HTML, CSS, JavaScript
- Backend: n8n workflow
- AI Model: Google Gemini
- Tunnel: ngrok

## Setup

1. Import workflow JSON ke n8n
2. Configure Google Gemini credential
3. Set ngrok URL
4. Activate workflow
5. Update webhook URL di index.html
6. Run local server: `python3 -m http.server 5500`

## Webhook URL

`https://unprefigured-rehabilitative-galilea.ngrok-free.dev/webhook/chat`

## Local WebApp URL

`http://localhost:5500`

## Testing

1. Buka `http://localhost:5500`
2. Ketik pertanyaan
3. AI akan menjawab via Google Gemini
   EOF
