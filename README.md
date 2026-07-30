# KATTOO v12 — Path Sync

Diese Version korrigiert die Hero-Animation entsprechend der markierten Bewegungslogik.

## Animation

1. Die Tätowiermaschine bewegt sich zunächst **von Norden nach Süden** auf den vorhandenen Signaturstrich zu.
2. Der goldene Strich unter „Kathi“ liegt bereits vollständig **östlich/rechts der Nadel**.
3. Sobald die Nadel den Strich berührt, folgt sie einer **zusammenhängenden Bahn nach Südwesten**.
4. Die goldene Linie wird dabei direkt an der Nadelspitze fortgesetzt.
5. Es gibt keine zwei voneinander getrennten Linienanimationen mehr.

## Hero-Buttons

Die grafischen Buttons im Hero besitzen vergrößerte echte HTML-Klickflächen:

- Kostenloses Erstgespräch
- Portfolio ansehen
- Home
- Galerie

## Upload auf GitHub Pages

Den kompletten Inhalt des ZIP-Archivs in das Repository übernehmen. Der Ordner `assets` muss erhalten bleiben.

Geänderte beziehungsweise neue Kerndateien:

- `index.html`
- `assets/hero-hand-machine-v12.webp`

Die neuen Assets werden mit `?v=12` geladen, damit Safari nicht wieder die vorherige Version aus dem Cache verwendet.
