FROM python:3.9-slim-buster
EXPOSE 5000
ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONUNBUFFERED=1

# Python venv erstellen
ENV Virtual_ENV=/opt/venv
RUN python3 -m venv ${Virtual_ENV}
ENV Path="${Virtual_ENV}/bin:SPATH"

# Bibliotheken installieren und Verzeichnis Vorbereiten
COPY requirements.txt .
RUN python -m pip install --upgrade-pip; \
    python -m pip install -r requirements.txt; \
    python 



