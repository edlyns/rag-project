# RAG Project - Infrastruktur Dasar

## Deskripsi

Setup infrastruktur dasar untuk proyek RAG (Retrieval-Augmented Generation)

## Tools yang Digunakan

- Docker & Docker Compose
- Node.js
- n8n (local)
- VSCode
- Git + GitHub
- Ngrok

## Struktur Folder

```
rag-project/
├── backend/          # Backend services
├── frontend/         # Frontend application
├── docker/           # Docker configurations
├── docs/            # Dokumentasi
├── scripts/         # Utility scripts
└── README.md
```

## Setup

Coming soon...
EOF

# 5. Buat .gitignore

cat > .gitignore << 'EOF'

# Node

node_modules/
npm-debug.log
yarn-error.log
.env
.env.local

# Docker

.docker/

# IDE

.vscode/
.idea/
_.swp
_.swo

# OS

.DS_Store
Thumbs.db

# n8n

.n8n/
EOF

# 6. First commit

git add .
git commit -m "Initial commit: Setup infrastruktur dasar"
Cara 3: Connect Local ke GitHub Repository
Setelah buat repository di GitHub (Cara 1), connect ke local:
bash# Ganti 'username' dan 'nama-repo' dengan milik kamu
git remote add origin https://github.com/username/nama-repo.git

# Push ke GitHub

git branch -M main
git push -u origin main

Kalau Belum Punya Akun GitHub:

Daftar di https://github.com/signup
Verifikasi email
Setup profile

Mana yang mau kamu coba dulu? Atau butuh bantuan untuk step tertentu?excerpt_from_previous_claude_message.txt1 linetxtini ketik dimana?21:04Command itu diketik di Terminal (aplikasi Terminal di Mac kamu).
Langkah-langkahnya:

Buka Terminal:

Tekan ⌘ + Space (Command + Space)
Ketik "Terminal"
Enter

Buat folder proyek dulu:

bash mkdir rag-project
cd rag-project

Baru jalankan command untuk buat README:

bash cat > README.md << 'EOF'

# RAG Project - Infrastruktur Dasar

## Deskripsi

Setup infrastruktur dasar untuk proyek RAG

## Tools yang Digunakan

- Docker & Docker Compose
- Node.js
- n8n
- VSCode
- Git + GitHub
- Ngrok
  EOF
