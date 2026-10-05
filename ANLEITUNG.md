# Miguels Tracker – als App installieren

Dieses Paket ist eine installierbare Web-App (PWA). Sie läuft offline, bekommt ein eigenes
Symbol auf dem Startbildschirm und öffnet sich ohne Browserleiste.

## Inhalt
- `index.html` – die App
- `manifest.webmanifest` – Name, Farben, Symbole
- `sw.js` – Offline-Modus
- `icons/` – App-Symbole

## 1. Online stellen (kostenlos mit GitHub Pages)
Eine PWA muss über https erreichbar sein. Einfach doppelklicken reicht nicht.

1. Konto auf github.com anlegen (falls noch nicht vorhanden).
2. Oben rechts auf „+“ → „New repository“. Name z. B. `tracker`, Sichtbarkeit „Public“, erstellen.
3. Im neuen Repository auf „uploading an existing file“ klicken und **alle Dateien und den Ordner
   `icons`** aus diesem Paket hineinziehen (nicht die ZIP-Datei selbst). „Commit changes“.
4. „Settings“ → „Pages“ → bei „Branch“ `main` und `/ (root)` wählen → „Save“.
5. Nach ein bis zwei Minuten ist die App erreichbar unter
   `https://DEINNAME.github.io/tracker/`

Alternative ohne Konto-Einrichtung bei GitHub: den Ordner auf app.netlify.com/drop ziehen.

## 2. Auf dem Handy installieren
- **iPhone (Safari):** Link öffnen → Teilen-Symbol → „Zum Home-Bildschirm“.
- **Android (Chrome):** Link öffnen → Menü (⋮) → „App installieren“ bzw. „Zum Startbildschirm hinzufügen“.

## 3. Deine Daten
- Alles wird **nur auf dem Gerät** gespeichert, auf dem du die App benutzt. Kein Konto, kein Server.
- Unter **Ziele → Daten** kannst du eine **Sicherung herunterladen** (JSON-Datei) und auf einem
  anderen Gerät wieder **einspielen**. Mach das ab und zu, z. B. einmal pro Woche.
- Wenn du die Website-Daten im Browser löschst, ist auch der Tracker leer – dann hilft nur die Sicherung.
- iPhone: Die installierte App und Safari haben getrennte Speicher. Trag deine Daten immer in der
  installierten App ein.

## 4. App ändern
Wenn du `index.html` später austauschst, erhöhe in `sw.js` die Zeile
`const CACHE = "tracker-v1";` auf `"tracker-v2"`, damit Handys die neue Version laden.

Alle Werte sind Schätzungen und ersetzen keine ärztliche Beratung.
