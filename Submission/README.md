# Timed---TimeOut

Production planning engine for small food manufacturers (sample company: Kuih Mesra Sdn Bhd).

## Team Information

| Field                 | Details                               |
| ---                   | ---                                   |
| **Team Name**         | TimeOut                               |
| **Team Domain**       | Domain 2                              |
| **SDG Track (1–17)**  | SDG 8 Decent Work and Economic Growth |
| **Team Leader**       | M.Husein I. Rinaldi                   |
| **University**        | Sunway University                     |
| **Number of Members** | 5                                     |

## Links

| Resource              | Link                                |
| ---                   | ---                                 |
| GitHub Repository     | https://github.com/Whoosayinn/Timed |
| Replit Project        | https://replit.com/Whoosayinn/Timed |
| Live Demo             | Local                               |
| Slide Deck            | Included in Repository              |
| Demo Video            | https://youtu.be/TCKkkPqsjXk        |

## Run

```
pip install -r requirements.txt
uvicorn core.api:app --host 0.0.0.0 --port 8000
```

Docs page: `/docs`. Tests: `pytest -v`.

## AI and forecasting

- `GET /forecast/sample`: weekly demand forecast with 80% range (predicts the Deepavali gift-box rush)
- `GET /stockout/sample`: when each material runs out and the last day to reorder
- `GET /insights/sample`: plan + forecast + stockouts + plain-English explanations in one call
- `POST /insights/ask`: ask a question in English or Bahasa Melayu

Optional: copy `.env.example` to `.env` and add a free Groq or Gemini key for AI-written briefings.
Without a key, built-in explanations are used. Details: `specs/07-forecasting.md`.
