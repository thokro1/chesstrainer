
---

# 2) `BUILD_STOCKFISH.md` (ins Repo-Root)

```md
# BUILD_STOCKFISH.md

Dieses Dokument beschreibt **zwei** Wege, Stockfish für den Browser zu nutzen.

## Weg A — „Fertigpaket“ aus dem npm-Ökosystem (empfohlen)

1) Installiere/verwende `stockfish@17.1.0` (JS/WASM, GPL).  
   Quelle/Info: jsDelivr npm Seite (Version 17.1.0).  
2) Kopiere die ausgelieferten Artefakte (z. B. `stockfish.js`, `stockfish.wasm`, evtl. Worker-Dateien)
   in dein Webverzeichnis, z. B. `/vendor/stockfish/`.
3) Achte darauf, dass Dateien aus **demselben Verzeichnis** geladen werden (relative Pfade passen).

> Hinweis: 17.1 ist die aktuelle Linie (Release 2025-03-30). Siehe Stockfish-Blog.  
> UCI/Kommandos (inkl. `speedtest`) sind in 17.1 offiziell.  
> Belege: Blog/Docs.  
*(Quellen siehe Ende dieses Dokuments)*

## Weg B — selbst bauen (WASM, Threads)

### Voraussetzungen
- **Emscripten SDK (emsdk)** installiert/aktiviert  
- Git, Node (für manche Buildskripte)

### Option B1: Lichess-Port bauen (bequemer)
Der Lichess-Port `stockfish.wasm` bringt erprobte Emscripten-Setups mit.

```bash
git clone https://github.com/lichess-org/stockfish.wasm.git
cd stockfish.wasm
# ggf. emsdk aktivieren
# Build (siehe Repo-README)
npm run prepare
