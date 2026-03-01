# Stremio Prehrajto Addon

Jedná se o fork původního Stremio addonu pro službu Prehrajto, upravený pro podporu Dockeru.  
Aplikace běží na Python serveru na portu 5000 (lze změnit pomocí proměnné prostředí `PORT`).

## Spuštění pomocí Dockeru

### 1) Lokální build

```bash
docker build -t stremio-prehrajto-addon .
docker run -p 5000:5000 stremio-prehrajto-addon
```

Aplikace poběží na:
http://localhost:5000


### 2) Spuštění z GHCR

```bash
docker pull ghcr.io/jondycz/stremio-prehrajto-addon:latest
docker run -p 5000:5000 ghcr.io/jondycz/stremio-prehrajto-addon:latest
```

Opět dostupné na:
http://localhost:5000


### Změna portu

```bash
docker run -e PORT=8080 -p 8080:8080 ghcr.io/jondycz/stremio-prehrajto-addon:latest
```