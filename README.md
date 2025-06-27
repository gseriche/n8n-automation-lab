# 🧠 n8n Automation Lab

Laboratorio personal de automatización usando [n8n](https://n8n.io/), integrando APIs, GPT y flujos útiles para experimentación y aprendizaje.

---

## 📂 Flujos disponibles

| Nombre del flujo           | Descripción breve                                                    | JSON | Documentación |
|----------------------------|-----------------------------------------------------------------------|------|----------------|
| `gpt-basic-webhook`        | Webhook básico que recibe un prompt y responde con GPT-3.5           | [`gpt-basic-webhook.json`](flows/gpt-basic-webhook.json) | [`gpt-basic-webhook.md`](flows/gpt-basic-webhook.md) |
| `weather-gpt-summary`      | Consulta una ciudad en WeatherAPI y responde con un resumen GPT      | [`weather-gpt-summary.json`](flows/weather-gpt-summary.json) | [`weather-gpt-summary.md`](flows/weather-gpt-summary.md) |

---

## 🚀 Cómo usar

1. Clona este repositorio
2. Levanta n8n con Docker Compose:

   ```bash
   docker compose up -d
   ```

3. Importa el flujo deseado desde la pestaña **Import Flow** en la UI de n8n
4. Configura las credenciales necesarias (OpenAI, WeatherAPI, etc.)
5. Activa el flujo y realiza una prueba (ver documentación específica por flujo)

---

## 📁 Estructura del proyecto

```bash
.
├── flows/                     # Flujos exportados desde n8n y sus documentación
│   ├── gpt-basic-webhook.json
│   ├── gpt-basic-webhook.md
│   ├── weather-gpt-summary.json
│   └── weather-gpt-summary.md
├── .gitignore
├── docker-compose.yml
└── README.md
```

---

## 🔐 Requisitos

- Cuenta en [OpenAI](https://platform.openai.com/)
- Cuenta en [WeatherAPI](https://www.weatherapi.com/)
- Docker y Docker Compose instalados en tu sistema

---

## ✍️ Autor

**Gonzalo Seriche**  
[🌐 gonzaloseriche.rocks](https://gonzaloseriche.rocks) · [💼 LinkedIn](https://www.linkedin.com/in/gseriche)
