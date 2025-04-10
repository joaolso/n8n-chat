# 🧪 Teste Rápido com n8n Local

Este repositório permite subir rapidamente uma instância local do **n8n** via Docker e testar webhooks com texto e áudio.

## 📦 Passo a Passo

### 1. Criar e acessar o diretório
```bash
mkdir n8n-local
cd n8n-local
```

### 2. Subir o container
Certifique-se de que você tenha um `docker-compose.yml` válido no diretório. Então, rode:

```bash
docker compose up -d
```

### 3. Acessar a interface
Abra no navegador:

```
http://localhost:5678
```

---

## 🚀 Testando Webhooks

Você pode testar dois tipos de entrada: **texto** e **áudio**. Use os exemplos abaixo com `curl`.

### 🔤 Enviar texto
```bash
curl -X POST "http://localhost:5678/webhook-test/4b9bc3d8-bd57-4b03-8f82-37c34a562b76" \
  -H "Content-Type: multipart/form-data" \
  -F "type=text" \
  -F "text=Quem foi o primeiro presidente do Brasil?"
```

### 🎧 Enviar áudio
```bash
curl -X POST "http://localhost:5678/webhook-test/4b9bc3d8-bd57-4b03-8f82-37c34a562b76" \
  -H "Content-Type: multipart/form-data" \
  -F "file=@audiomp3.mp3;type=audio/mpeg" \
  -F "type=audio"
```

---

## ✅ Requisitos

- Docker
- Docker Compose
- Navegador ou terminal com `curl`
