# 🌤️ Weather GPT Summary

Este flujo en n8n recibe el nombre de una ciudad, consulta su clima actual vía WeatherAPI, y solicita a GPT-3.5 un resumen en lenguaje natural. Devuelve un mensaje amigable para el usuario.

---

## 🧩 Estructura del flujo

```text
Webhook (POST /weather)
    ↓
HTTP Request (WeatherAPI)
    ↓
HTTP Request (OpenAI GPT)
    ↓
Respond to Webhook
```

---

## 📬 Cómo probar

```bash
curl -X POST http://localhost:5678/webhook-test/weather \
  -H "Content-Type: application/json" \
  -d '{ "city": "Valdivia" }'
```

Respuesta esperada:

```json
{
  "message": "Hoy en Valdivia el clima está despejado con una temperatura de 12°C..."
}
```

---

## 🔐 Requisitos

- API Key válida de [WeatherAPI](https://www.weatherapi.com/)
- Token de OpenAI
- Docker Compose con n8n corriendo local

---
