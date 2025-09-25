# Chesstrainer

Ein HTML/JavaScript-Schachtrainer mit **chessboard.js**, **chess.js** und **Stockfish (WASM)**.  
Produktivseite: **tkchess.com** (IONOS Hosting).

## Features
- Interaktives Brett (drag & drop), Züge/PGN laden
- Engine-Analyse via Stockfish (WebAssembly)
- Übungs-/Positionsdateien (z. B. LucasChess-Sätze)
- Lizenz- und Quellcode-Nachweise: [/licenses.html](/licenses.html)

## Schnellstart (lokal)
> Wegen WASM solltest du *einen lokalen Webserver* nutzen (sonst CORS/COOP/COEP-Probleme).

```bash
git clone https://github.com/thokro1/chesstrainer.git
cd chesstrainer
# einfacher Dev-Server, z. B.:
python -m http.server 8000
# dann http://localhost:8000/index.html öffnen
