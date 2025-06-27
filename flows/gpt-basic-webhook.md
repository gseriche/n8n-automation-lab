# 🤖 GPT Basic Webhook

Este flujo utiliza n8n y OpenAI para recibir un mensaje desde un webhook, enviarlo a GPT-3.5-Turbo y devolver una respuesta generada por IA.

---

## 🧩 Estructura del flujo

```text
Webhook (POST /gpt)
    ↓
HTTP Request (OpenAI API)
    ↓
Respond to Webhook (con texto generado)
```

---

## 📬 Cómo probar

```bash
curl -X POST http://localhost:5678/webhook-test/gpt \
  -H "Content-Type: application/json" \
  -d '{"prompt": "¿Cuál es la capital de Francia?"}'
```

Respuesta esperada:

```json
{
  "message": "La capital de Francia es París."
}
```

---

## 🔐 Requisitos

- Token de API de OpenAI configurado como credencial en n8n
- Modelo usado: `gpt-3.5-turbo`
- Docker Compose con n8n levantado

---
