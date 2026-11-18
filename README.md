# Exposé Reel

Arbeitsstand einer Produktidee: eine Software, mit der Immobilienmakler aus Grundriss und Fotos selbst ein Objektvideo, ein 3D-Puppenhaus und einen begehbaren Rundgang erstellen und auf ihrer Website einbinden.

Stand: 18.11.2026. Alles hier ist Prototyp und Konzept, nichts davon ist mit echten Kunden getestet.

## Wie es dazu kam

1. Ausgangspunkt war ein Plan für eine europäische KI-Produktvideo-Plattform für E-Commerce ([docs/01](docs/01-businessplan-original.md)).
2. Recherche zu kommerziell nutzbaren Datensätzen und Modellen auf Hugging Face ([docs/02](docs/02-recherche-datensaetze-modelle.md)).
3. Zwei Runden "LLM Council" mit fünf Beratern. Ergebnis: Produktfotos sind Commodity, die Nische ist Makler-Exposé zu Video ([docs/03](docs/03-council-entscheidungen.md)).
4. Produktkonzept für Makler, Self-Service statt Dienstleistung ([docs/04](docs/04-produktkonzept.md)).
5. Kosten pro Objekt und Einbindung auf Makler-Websites ([docs/05](docs/05-kosten-und-einbindung.md)).

## Demo-Link

Nach dem Merge veröffentlicht der Workflow `.github/workflows/pages.yml` die Prototypen bei jedem Push auf `main` unter:

https://yasinserdar6666-hash.github.io/Immo-Seite/

- `index.html` ist die Startseite mit allen vier Prototypen.
- `einbettung-test.html` ist eine erfundene Makler-Seite, die den Kombi-Rundgang per iframe einbindet.

Einmalig nötig: unter Settings → Pages bei „Source“ die Option „GitHub Actions“ wählen.

## Prototypen

Die Dateien in `prototypes/` lassen sich direkt im Browser öffnen.

| Datei | Was sie zeigt |
|---|---|
| `01-expose-reel-video.html` | Self-Service-Ablauf: Grundriss hochladen, Räume anlegen, Fotos pro Raum, Stil wählen, Storyboard, Video im Browser rendern |
| `02-puppenhaus.html` | 3D-Puppenhaus einer Beispielwohnung, Räume anklickbar, automatischer Rundgang |
| `03-rundgang-streetview.html` | Rundgang in Ich-Perspektive wie Street View, mit Pfeilen und Mini-Grundriss |
| `04-rundgang-kombi.html` | Puppenhaus und Ich-Perspektive kombiniert, 360°-Fotos pro Raum, Rundgang als Video, Einbettungs-Schnipsel |

Hinweise:
- Die KI-Funktionen in `01` (Grundriss lesen, Fotos prüfen, Storyboard) laufen nur als Claude-Artifact, weil sie Claude über die Artifact-Schnittstelle aufrufen. Lokal geöffnet arbeitet die Seite mit Vorlagen und manueller Zuordnung, das Video wird trotzdem gerendert.
- Download-Knöpfe funktionieren ebenfalls nur als Artifact. Lokal lässt sich das Video im Player abspielen und per Rechtsklick speichern.
- `02` bis `04` laden three.js 0.128.0 von jsDelivr und brauchen dafür Internet.
- Die Beispielwohnung (Maße, Möbel) ist erfunden.

## Offene Punkte

- Mit Maklern sprechen, bevor weiter gebaut wird (siehe [docs/04](docs/04-produktkonzept.md#nächste-schritte)).
- Grundriss-Erkennung mit echten Plänen testen, vor allem für genaue Wandmaße.
- Echtes Hosting für Rundgänge (EU), damit der Einbettungs-Schnipsel funktioniert.
- Lizenzen der gewählten Modelle juristisch prüfen lassen.
