# 🤖 GPT Webhook – n8n Automation Lab

Este flujo usa [n8n](https://n8n.io) para construir una automatización que recibe un mensaje vía Webhook, lo envía a la API de OpenAI (GPT-3.5 Turbo) y devuelve la respuesta al cliente en formato JSON.

---

## 🧩 Estructura del flujo

```text
Webhook (POST /gpt)
    ↓
HTTP Request (OpenAI GPT API)
    ↓
Respond to Webhook (JSON con respuesta)
```

---

## 📬 Cómo usar

### 1. Levanta n8n localmente

```bash
docker compose up -d
```

### 2. Haz una petición POST al webhook de test

```bash
curl -X POST http://localhost:5678/webhook-test/gpt \
  -H 'Content-Type: application/json' \
  -d '{"prompt": "¿Cuál es la capital de Francia?"}'
```

### 3. Respuesta esperada

```json
{
  "message": "La capital de Francia es París."
}
```

---

## 📁 Archivos

| Archivo | Descripción |
|--------|-------------|
| `flows/gpt-basic-webhook.json` | Flujo exportado desde n8n |
| `docker-compose.yml` | Configuración Docker para levantar n8n local |
| `.gitignore` | Evita subir datos sensibles o temporales |
| `README.md` | Este archivo, con explicación técnica y uso del flujo |

---

## 🔐 Requisitos

- Cuenta en [OpenAI](https://platform.openai.com/)
- Token de API configurado como credencial en n8n (`Bearer Auth account`)
- Docker y Docker Compose instalados en tu sistema

---

## 📌 Notas

- El Webhook está en modo de prueba (`/webhook-test/gpt`). Para uso en producción, activa el flujo en n8n y usa la URL de producción.
- El `Raw Body` está habilitado, por lo que el JSON debe ir bien formateado.

---

## 🛠️ Próximos flujos

- GPT + Notion + Slack
- API externa → análisis GPT → resumen automatizado
- ETL básico con Pub/Sub + BigQuery + n8n

---

### 👨‍💻 Autor

**@gseriche**  
Lab de automatizaciones con n8n, enfocado en chatbots, APIs y flujos serverless.
