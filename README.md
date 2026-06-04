# 🤖 Labyrinth · Calliope-Sicht

Eine kleine Web-App, um den **Wandfolger-Algorithmus** (Rechte-Hand-Regel) aus der
Sicht eines „dummen" Calliope mini zu verstehen.

Reines Frontend — eine einzige `index.html`, kein Build, kein Backend.
Der Zustand lebt „sticky" im `localStorage` des Browsers.

## Routen (Hash-basiert)

| Route       | Zweck                                                                 |
|-------------|-----------------------------------------------------------------------|
| `#display`  | Top-Down-Ansicht (Vogelperspektive) — die der Roboter nie sieht       |
| `#solve`    | First-Person: **nur die Zelle vorne** (Wand / frei). Pfeiltasten.     |
| `#refresh`  | Neues, perfektes (schleifenfreies) Labyrinth — immer lösbar           |

**Steuerung im Solve-View:** `↑` vor · `←` links drehen · `→` rechts drehen · `↓` umdrehen.

Der Roboter „fühlt" strikt nur nach vorne. Wer die Rechte-Hand-Regel umsetzen will,
muss sich also drehen, fühlen und ggf. zurückdrehen — genau dieser Dreh-Fühl-Tanz
ist der Lerneffekt.

## Lokal starten

Einfach `index.html` im Browser öffnen — oder:

```bash
python3 -m http.server 8123
# http://localhost:8123
```

## Auf GitHub Pages veröffentlichen

1. Repo auf GitHub anlegen und pushen (siehe unten).
2. **Settings → Pages → Build and deployment → Source: „Deploy from a branch"**.
3. Branch `main`, Ordner `/ (root)` wählen, **Save**.
4. Nach ~1 Minute ist die App unter `https://<user>.github.io/<repo>/` erreichbar.

Die Datei `.nojekyll` sorgt dafür, dass GitHub die Dateien unverändert ausliefert.
