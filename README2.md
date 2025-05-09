# chatbot-institucional
Demo 1

<!-- import speech_recognition as sr
import pyttsx3
import time
import os
from dotenv import load_dotenv
import google.generativeai as genai

# Cargar variables de entorno
load_dotenv()
GEMINI_API_KEY = os.getenv("GEMINI_API_KEY")

# Inicializar Gemini
genai.configure(api_key=GEMINI_API_KEY)
model = genai.GenerativeModel("gemini-1.5-flash")  # O el modelo que prefieras

# Inicializar motor de voz
engine = pyttsx3.init()
engine.setProperty('voice', 'spanish')
engine.setProperty('rate', 150)

# Inicializar reconocedor de voz
recognizer = sr.Recognizer()
microphone = sr.Microphone()

def hablar(texto):
    print(f"Asistente: {texto}")
    engine.say(texto)
    engine.runAndWait()

def escuchar():
    with microphone as source:
        print("Habla ahora (o di 'salir' para terminar)...")
        recognizer.adjust_for_ambient_noise(source)
        audio = recognizer.listen(source)
    try:
        texto = recognizer.recognize_google(audio, language="es-ES")
        print(f"Tú: {texto}")
        return texto.lower()
    except sr.UnknownValueError:
        print("No entendí, intenta de nuevo.")
        return None
    except sr.RequestError:
        print("Error con el servicio de reconocimiento de voz.")
        return None

def obtener_respuesta_gemini(mensaje):
    try:
        response = model.generate_content(mensaje)
        return response.text
    except Exception as e:
        return f"Error al conectar con Gemini: {e}"

def main():
    hablar("Hola, soy tu asistente virtual. ¿En qué puedo ayudarte?")
    while True:
        texto = escuchar()
        if texto is None:
            continue
        if "salir" in texto:
            hablar("Hasta luego!")
            break
        respuesta = obtener_respuesta_gemini(texto)
        hablar(respuesta)
        time.sleep(0.5)

if __name__ == "__main__":
    main() -->


# backend/.env
GEMINI_API_KEY=AIzaSyDBHp2QxaVJ6LuRk0xVHyeKZXguf_sMXcI