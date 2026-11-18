# Kosten und Einbindung

Stand: 17.11.2026. Schätzungen aus Listenpreisen, keine gemessenen Werte.

## Kosten pro Objekt

Annahmen: Claude Sonnet 5.5 über die API (2 USD pro Million Input-Token, 10 USD pro Million Output-Token), ein Foto entspricht ca. 1.500 Token, 15 Fotos, 30 Sekunden Video.

| Baustein | Kosten |
|---|---|
| Grundriss lesen | ca. 0,01 USD |
| 15 Fotos prüfen und sortieren | ca. 0,06 USD |
| Storyboard schreiben | ca. 0,02 USD |
| Sprecherstimme 30 bis 60 s (ElevenLabs Multilingual, 0,10 USD pro 1.000 Zeichen) | ca. 0,05 bis 0,10 USD |
| Video aus Fotos mit Zoom und Schwenk | praktisch 0 |
| **Variante A gesamt** | **ca. 0,15 bis 0,20 €** |
| KI-Bewegtbilder statt Zoom (ca. 40 s Rohmaterial, 720p) | ca. 2 bis 5 USD |
| **Variante B gesamt, mit Fehlversuchen** | **ca. 3 bis 7 €** |

Videopreise pro Sekunde bei 720p laut [devtk.ai](https://devtk.ai/en/blog/ai-video-generation-pricing-2026/): MiniMax Hailuo 2.3 ca. 0,05 USD, Veo 3.1 Lite 0,05 USD, Kling 3.0 0,08 USD, Seedance 2.0 Fast 0,12 USD. Bei KI-Clips mit etwa 30 % Fehlversuchen rechnen.

Bei 40 bis 60 € pro Objekt bleibt in beiden Varianten viel Marge. Hinzu kommen Hosting, Zahlungsgebühren und Support.

## Einbindung beim Makler

Rundgang auf der eigenen Website:
- Jeder Rundgang bekommt eine eigene Adresse, z. B. `https://rundgang.deinedomain.de/t/abc123`.
- Der Makler fügt einen iframe-Schnipsel ein:

```html
<iframe src="https://rundgang.deinedomain.de/t/abc123"
        width="100%" height="560" style="border:0;border-radius:8px"
        allow="fullscreen; gyroscope; accelerometer"
        loading="lazy" title="3D-Rundgang"></iframe>
```

- WordPress: Block "Individuelles HTML". Wix und Jimdo: "Einbetten/Code". Makler-CRMs wie onOffice: meist ein Feld für Rundgang- oder Video-Links, im Einzelfall prüfen.

Portale:
- ImmoScout24 erlaubt pro Exposé ein Video bis 1 GB ([Quelle](https://www.immobilienscout24.de/anbieten/gewerbliche-anbieter/tipps/anwender-handbuch/multimedia.html)). Der Makler lädt das MP4 dort hoch.
- Den Rundgang als Link zusätzlich angeben. Ob ein eigener Rundgang-Link wie die 360°-Partner gekennzeichnet wird, ist nicht geklärt.

## Technik für den echten Betrieb

- Server in der EU, der pro Objekt Grundrissdaten, Fotos und 360°-Fotos ausliefert.
- Viewer-Seite (wie `prototypes/04-rundgang-kombi.html`), die diese Daten lädt.
- Löschung nach Verkauf oder Vermietung, kein Tracking ohne Einwilligung, da Fotos aus privaten Wohnungen.

## Quellen

- [Claude API Pricing](https://platform.claude.com/docs/en/about-claude/pricing)
- [Claude Vision](https://platform.claude.com/docs/en/build-with-claude/vision)
- [AI Video API Pricing 2026](https://devtk.ai/en/blog/ai-video-generation-pricing-2026/)
- [ElevenLabs API Pricing](https://developer.puter.com/tutorials/elevenlabs-api-pricing/)
- [ImmoScout24: Bilder, Grundrisse und Videos](https://www.immobilienscout24.de/anbieten/gewerbliche-anbieter/tipps/anwender-handbuch/multimedia.html)
