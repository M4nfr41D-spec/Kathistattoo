# KATTOO — finale technische Baseline v6

Deploy-fertiges GitHub-Pages-Paket mit **einer Hauptseite**, einer separaten **Tattoo-Galerie** und der vorbereiteten kleinen **Beyond-Ink-Galerie** für Malerei und Zeichnungen.

## Dateien

- `index.html` — vollständige Mainsite; bestehende Navigation, Kalender und Kontaktlogik bleiben erhalten
- `galerie.html` — filterbare, progressiv nachladende Masonry-Galerie mit Lightbox und Swipe
- `artworks.html` — kompakte Offtopic-Galerie „Beyond Ink“
- `assets/patina.webp` — Seitenhintergrund
- `assets/kattoo-seal.webp` — Header-Logo
- `assets/kattoo-artist.webp` — freigestelltes Artist-Portrait
- `assets/hero-motif.svg` — **austauschbares transparentes Blackline-Motiv hinter dem Portrait**

## Galerie-Logik

Die vier übergeordneten Stile sind:

- `C1.webp`, `C2.webp` … — Color
- `SW1.webp`, `SW2.webp` … — Black & Grey
- `LA1.webp`, `LA2.webp` … — Fine Line / Lineart
- `SP1.webp`, `SP2.webp` … — Special / Cover-up

Die Dateien liegen in `assets/gallery/`. Reihenfolge, Titel und Kategorie werden in `assets/gallery-data.js` festgelegt. **Ein Bild kann jederzeit ausgetauscht werden, ohne den HTML-Code anzufassen**, solange der Dateiname gleich bleibt.

## Neue Tattoo-Arbeit ergänzen

1. Bild als WebP in `assets/gallery/` ablegen, z. B. `C5.webp`.
2. In `assets/gallery-data.js` einen Eintrag ergänzen:

```js
{"file":"C5.webp","code":"C5","category":"C","title":"Motivtitel","order":15}
```

## Hero-Motiv austauschen

Das florale Placeholder-Motiv liegt unter `assets/hero-motif.svg`. Es ist eine transparente Blackline-Datei. Später einfach durch Kathis Lieblingsmotiv ersetzen und den Dateinamen beibehalten. PNG, WebP oder SVG mit Alpha funktionieren; bei PNG/WebP muss im HTML/CSS lediglich die Dateiendung angepasst werden.

## Beyond Ink ergänzen

1. Werke als `ART1.webp`, `ART2.webp` … in `assets/artworks/` ablegen.
2. `assets/artworks-data.js` ergänzen, z. B.:

```js
window.KATTOO_ARTWORKS = [
  {"file":"ART1.webp","title":"Freie Zeichnung"},
  {"file":"ART2.webp","title":"Acryl auf Leinwand"}
];
```

## GitHub Pages

Den **kompletten Inhalt dieses Ordners** in die Repository-Wurzel hochladen. `index.html` muss dort auf oberster Ebene liegen. GitHub Pages übernimmt Änderungen nach dem Commit gewöhnlich automatisch.

## Status der Bildauswahl

Die enthaltenen Tattoo-Bilder sind eine funktionierende Erstbestückung und vollständig austauschbar. Die finale kuratorische Auswahl kann später ohne Strukturänderung eingespielt werden.


## v7 – flache Asset-Struktur für iPad/iPhone

Alle Bilder liegen direkt im Ordner `assets/`. Es werden keine Unterordner für `gallery`, `editorial` oder `artworks` benötigt.

Beispiele:

```text
assets/C1.webp
assets/SW1.webp
assets/artist-at-work.webp
assets/artist-detail.webp
assets/ART1.webp
```

Die HTML-Dateien dieser Version verweisen bereits auf diese flache Struktur.


## v8 Motion Baseline

- `assets/hero-final.webp`: approved hero artwork.
- `assets/hero-hand-machine.webp`: separate, softly feathered hand/machine motion layer.
- Scroll motion completes the signature by a maximum of 10 px.
- Background parallax is deliberately limited to 14 px.
- Gold particles are sparse and disabled with `prefers-reduced-motion`.
- Gallery now uses a true reflow grid with fade transitions; hidden categories leave no gaps.


## v9 Motion Fix

- `hero-final.webp` is now the approved flower-based hero without the hand/machine baked in.
- `hero-hand-machine.webp` contains only the tightly isolated glove and tattoo machine with transparency.
- No button, background panel, torso block or signature fragment moves with the hand.
- The hand moves no more than 8 px and the final signature segment is drawn separately as SVG.


## v10 Live-Fix
- Neues, cache-sicher benanntes Hand-Asset: `assets/hero-hand-machine-v10.webp`
- UI-/Schattenreste aus dem bewegten Asset entfernt
- Galerie-Bildpfade korrigiert (`assets/<Dateiname>`)
- Galerie-Hero abgedunkelt und weichgezeichnet statt grob hochskaliert
- Beyond-Ink-Bildausschnitt für iPad/iPhone korrigiert
- Kritische Assets tragen `?v=10`, damit Safari/GitHub nicht die alte Version aus dem Cache verwendet
