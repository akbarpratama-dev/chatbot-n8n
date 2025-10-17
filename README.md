# Gemini Chatbot dengan n8n

Chatbot menggunakan Google Gemini AI dan n8n workflow automation.

## 🚀 Quick Start

1. Clone repository:
   ```bash
   git clone <your-repo-url>
   cd chatbot-n8n
   ```

2. Setup environment variables:
   ```bash
   cp .env.example .env
   # Edit .env dan tambahkan Gemini API key Anda
   ```

3. Jalankan dengan Docker:
   ```bash
   docker-compose up -d
   ```

4. Akses aplikasi:
   - **n8n Editor**: http://localhost:5678
   - **Web Interface**: http://localhost:8080

5. Import workflow:
   - Di n8n, import file `workflow-gemini.json`
   - Edit node "Prepare Data" dan ganti API key dengan API key Anda
   - Aktifkan workflow

## 📋 Struktur Project

```
chatbot-n8n/
├── docker-compose.yml      # Konfigurasi Docker
├── workflow-gemini.json    # n8n workflow
├── web/                    # Frontend web
│   └── index.html
├── .env.example           # Template environment variables
├── .gitignore             # Git ignore rules
└── README.md              # Dokumentasi
```

## 🔑 Mendapatkan API Key

1. Kunjungi [Google AI Studio](https://aistudio.google.com/app/apikey)
2. Login dengan akun Google
3. Klik "Create API Key"
4. Copy API key dan simpan di tempat aman

## 📝 Cara Menggunakan

1. Import `workflow-gemini.json` ke n8n
2. Edit node "Prepare Data" dan ganti `GANTI_DENGAN_API_KEY_GEMINI_ANDA` dengan API key Anda
3. Aktifkan workflow
4. Buka web interface di http://localhost:8080
5. Mulai chat dengan AI

## 🛠️ Tech Stack

- **n8n** - Workflow automation
- **Google Gemini AI** - Large Language Model (gemini-2.0-flash-exp)
- **Docker & Docker Compose** - Containerization
- **Nginx** - Web server

## ⚠️ Catatan Keamanan

- **JANGAN** commit file `.env` ke repository
- **JANGAN** hardcode API key di workflow untuk production
- Data n8n disimpan di Docker volume `n8n-data`

## 📄 License

MIT