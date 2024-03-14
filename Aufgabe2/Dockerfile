# Basierend auf einem offiziellen Python-Image
FROM python:3.9-slim

# Arbeitsverzeichnis im Container festlegen
WORKDIR /app

# Kopiere die Anforderungen und installiere Python-Abhängigkeiten
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Kopiere den gesamten Service-Code (inklusive des templates Ordners) in das Arbeitsverzeichnis
COPY Aufgabe1/ .

# Starte den FastAPI-Server, wenn der Container läuft
CMD ["uvicorn", "microservice:app", "--host", "0.0.0.0", "--port", "8000"]

