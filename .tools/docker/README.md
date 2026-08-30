# Docker — DataFusion App (Python)

Obraz zawiera Pythona 3.12 wraz z Tkinterem, ktorego wymaga PySimpleGUI.
Katalog `database/` jest zamontowany z hosta, wiec dane przezywaja restart
kontenera.

## Wymagania

- Docker Engine 24+ z wtyczka `docker compose`
- Serwer X, jesli chcesz zobaczyc interfejs (patrz nizej)

## Uruchomienie

```bash
cd .tools/docker
docker compose up --build
```

## Samo budowanie

```bash
docker compose build
```

## Aplikacja okienkowa a kontener

To jest aplikacja z graficznym interfejsem, wiec kontener **nie serwuje jej
przez przegladarke**. Okno musi zostac narysowane na serwerze X hosta.

**Linux** — jednorazowo zezwol kontenerowi na dostep do X:

```bash
xhost +local:docker
docker compose up --build
```

**macOS** — wymagany jest XQuartz (`brew install --cask xquartz`), z wlaczona
opcja *Allow connections from network clients*:

```bash
xhost + 127.0.0.1
DISPLAY=host.docker.internal:0 docker compose up --build
```

**Windows** — uzyj serwera X (VcXsrv lub X410) i ustaw `DISPLAY` na adres IP
hosta.

Jesli zalezy Ci wylacznie na sprawdzeniu, ze projekt sie kompiluje, samo
`docker compose build` wystarczy — nie wymaga serwera X.

## Zatrzymanie

```bash
docker compose down
```
