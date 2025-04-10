# Primeiro 1
mkdir n8n-local
cd n8n-local

# Criar o arquivo
rodar comando: docker compose up -d

# abrir
http://localhost:5678

# testar
curl -X POST "http://localhost:5678/webhook-test/4b9bc3d8-bd57-4b03-8f82-37c34a562b76" ^
  -H "Content-Type: multipart/form-data" ^
  -F "type=text" ^
  -F "text=Quem foi o primeiro presidente do Brasil?"


curl -X POST "http://localhost:5678/webhook-test/4b9bc3d8-bd57-4b03-8f82-37c34a562b76" ^
  -H "Content-Type: multipart/form-data" ^
  -F "file=@audiomp3.mp3;type=audio/mpeg" ^
  -F "type=audio"