# Backend CopaBot

## Requisitos
- Python 3.11+
- uv
- Chave da API Groq: https://console.groq.com/keys

## Rodar localmente
1. Copie `.env.example` para `.env` e configure `GROQ_API_KEY`.
2. Instale dependências e gere o lock:
   ```bash
   uv lock
   uv sync
   ```
3. Inicie:
   ```bash
   uv run python app.py
   ```

O serviço fica em `http://127.0.0.1:5000`.

## Render
- Build Command: `uv sync --frozen`
- Start Command: `uv run gunicorn app:app`
- Configure `GROQ_API_KEY` e `FRONTEND_URL` nas Environment Variables.
- `FRONTEND_URL` deve ser a origem do site publicado (sem caminho `/chat`).
- Não publique o arquivo `.env`.
