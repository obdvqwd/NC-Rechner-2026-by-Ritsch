# Medizinstudium Zentrale (Ritsch Test Vercel)

Statische Single-File-Website: `index.html` enthält HTML, CSS und JavaScript komplett inline.
Externe Abhängigkeiten werden nur per CDN nachgeladen:

- Leaflet 1.9.4 (unpkg) für die interaktive Karte
- OSRM Public API (`router.project-osrm.org`) für die Fahrzeit-Berechnung

## Deployment auf Vercel

Kein Build-Schritt nötig – Vercel serviert das Repo direkt als statische Seite.

1. Auf [vercel.com/new](https://vercel.com/new) dieses Repository importieren.
2. Framework Preset: **Other**.
3. Build Command und Output Directory leer lassen (Root-Verzeichnis `.`).
4. Deploy.

Pushes auf `main` erzeugen ab dann automatisch ein Production-Deployment,
Pushes auf andere Branches ein Preview-Deployment.

## Lokal testen

```bash
python3 -m http.server 8000
# http://localhost:8000
```
