# Chatbot UCH

Un chatbot interactivo con reconocimiento de voz y síntesis de voz, desarrollado para la Universidad de Ciencias y Humanidades.

## Características

- Reconocimiento de voz en tiempo real
- Síntesis de voz para respuestas
- Interfaz de usuario moderna y responsiva
- Integración con IA para procesamiento de lenguaje natural

## Estructura del Proyecto

```
chatbot-uch/
├── backend/           # API FastAPI
│   ├── app/
│   │   ├── api/
│   │   ├── core/
│   │   └── main.py
│   └── requirements.txt
└── frontend/         # Aplicación React
    ├── src/
    │   ├── components/
    │   └── App.tsx
    └── package.json
```

## Requisitos

### Backend
- Python 3.8+
- FastAPI
- Uvicorn
- Google Cloud (para la API de Gemini)

### Frontend
- Node.js 14+
- React
- TypeScript

## Instalación

### Backend
```bash
cd backend
python -m venv venv
source venv/bin/activate  # En Windows: venv\Scripts\activate
pip install -r requirements.txt
```

### Frontend
```bash
cd frontend
npm install
```

## Ejecución

### Backend
```bash
cd backend
uvicorn app.main:app --reload
```

### Frontend
```bash
cd frontend
npm start
```

## Configuración

1. Crear un archivo `.env` en el directorio `backend` con:
```
GOOGLE_API_KEY=tu_api_key_aquí
```

## Licencia

Este proyecto es propiedad de la Universidad de Ciencias y Humanidades.