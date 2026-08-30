# Aplikacja okienkowa oparta na PySimpleGUI (Tkinter). Kontener zapewnia
# powtarzalne srodowisko uruchomieniowe; okno wymaga serwera X z hosta —
# patrz README.md w tym katalogu.
FROM python:3.12-slim

ENV PYTHONDONTWRITEBYTECODE=1 \
    PYTHONUNBUFFERED=1

WORKDIR /app

# Tkinter nie wchodzi w sklad obrazu slim, a PySimpleGUI bez niego nie ruszy.
RUN apt-get update && apt-get install -y --no-install-recommends \
        python3-tk \
        tk \
        libx11-6 \
        fonts-dejavu-core \
    && rm -rf /var/lib/apt/lists/*

COPY src/requirements.txt ./requirements.txt

# PySimpleGUI od wersji 5 jest dystrybuowany z wlasnego indeksu, dlatego
# requirements.txt zawiera pelne polecenie pip zamiast nazwy pakietu.
RUN pip install --no-cache-dir --upgrade pip \
    && sh -c "$(cat requirements.txt)"

COPY src/ ./src/

RUN useradd --create-home --uid 1000 appuser && chown -R appuser:appuser /app
USER appuser

ENV DISPLAY=:0

CMD ["python", "src/main.py"]
