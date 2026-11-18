# Recherche: Datensätze und Modelle

Stand: 16.11.2026. Drei parallele Recherchen zu kommerziell nutzbaren Datensätzen und offenen Modellen. Lizenzen wurden aus den Dataset- und Model-Cards gelesen, nicht aus vollständigen Rechtstexten. Vor einem Produktstart juristisch prüfen lassen.

## Grundriss und 3D

| Name | Inhalt | Lizenz | Kommerziell |
|---|---|---|---|
| [CubiCasa5K](https://zenodo.org/records/2613548) | 5.000 annotierte Grundrisse | CC BY-NC-SA 4.0 | Nein |
| [Modified Swiss Dwellings](https://doi.org/10.4121/e1d89cb5-6872-48fc-be63-aadd687ee6f9) | gut 4.000 Grundrisse (Schweiz) | CC BY 4.0 laut Metadaten | Ja, vorher prüfen |
| [Structured3D](https://github.com/bertjiazheng/Structured3D) | 3.500 synthetische Häuser | eigene Terms of Use | Nicht verifiziert |
| [ZInD (Zillow)](https://github.com/zillow/zind) | Panoramen und Grundrisse | nur akademisch | Nein |
| [Matterport3D](https://niessner.github.io/Matterport) | 90 Gebäude, RGB-D | signierte Terms | Nicht verifiziert, vermutlich nein |
| [TRELLIS-image-large](https://huggingface.co/microsoft/TRELLIS-image-large) | Bild zu 3D | MIT | Ja |
| [Hunyuan3D-2](https://huggingface.co/tencent/Hunyuan3D-2) | Bild zu 3D | Community License ohne EU, UK, Südkorea | In der EU nein |
| [VGGT-1B-Commercial](https://huggingface.co/facebook/VGGT-1B-Commercial) | Kameras, Tiefe, Punktwolken aus Fotos | eigene Lizenz, gated | Ja, außer militärisch |

Fazit: Die fachlich besten Grundriss-Datensätze sind nicht kommerziell nutzbar. Ein Produkt braucht eigene Daten oder einen Ansatz ohne Training (Grundriss per Vision-Modell lesen, Geometrie per Regeln).

Konkurrenz (Preise aus Drittquellen, nicht geprüft): Matterport ab ca. 12 USD pro Monat, Polycam Pro ca. 27 USD pro Monat, Planner 5D 20 bis 50 USD pro Monat.

## Produktbild und Video

| Name | Zweck | Lizenz | Kommerziell |
|---|---|---|---|
| [BiRefNet](https://huggingface.co/ZhengPeng7/BiRefNet) | Freistellen | MIT | Ja |
| [RMBG-2.0](https://huggingface.co/briaai/RMBG-2.0) | Freistellen | nur mit Bria-Vertrag | Nein |
| [FLUX.1 schnell](https://huggingface.co/black-forest-labs/FLUX.1-schnell) | Text zu Bild | Apache 2.0 | Ja |
| [FLUX.1 dev](https://huggingface.co/black-forest-labs/FLUX.1-dev) | Text zu Bild | nicht kommerziell (Modell) | Nein |
| [Wan2.2 I2V](https://huggingface.co/Wan-AI/Wan2.2-I2V-A14B-Diffusers) | Bild zu Video | Apache 2.0 | Ja |
| [LTX-2](https://huggingface.co/Lightricks/LTX-2.3) | Video | Community License, Umsatzgrenze | Bedingt |
| [HunyuanVideo-I2V](https://huggingface.co/tencent/HunyuanVideo-I2V) | Bild zu Video | ohne EU | In der EU nein |
| [CogVideoX-5B-I2V](https://huggingface.co/THUDM/CogVideoX-5b-I2V) | Bild zu Video | eigene Lizenz | Unklar |

Fazit: Sauberer Stack ist BiRefNet, FLUX.1 schnell und Wan2.2. Eigenes Training lohnt höchstens für Stil-LoRAs mit eigenen Bildern.

## Weitere Datensätze mit Geschäftspotenzial

| Name | Inhalt | Lizenz | Idee |
|---|---|---|---|
| [openlegaldata/court-decisions-germany](https://huggingface.co/datasets/openlegaldata/court-decisions-germany) | ca. 697.000 deutsche Urteile | ODbL | Urteils-Recherche per RAG |
| [ds4sd/DocLayNet](https://huggingface.co/datasets/ds4sd/DocLayNet) | 80.000 Seiten mit Layout-Boxen | CDLA-Permissive | Dokumenten-Pipeline |
| [katanaml-org/invoices-donut-data-v1](https://huggingface.co/datasets/katanaml-org/invoices-donut-data-v1) | 501 englische Rechnungen | MIT | Rechnungs-Extraktion |
| [DiscoResearch/germanrag](https://huggingface.co/datasets/DiscoResearch/germanrag) | 3.362 deutsche RAG-Beispiele | widersprüchlich, BY-SA annehmen | RAG-Feintuning |
| [deepset/germanquad](https://huggingface.co/datasets/deepset/germanquad) | 13.722 Fragen | CC BY 4.0 | Evaluation |
| [google/fleurs](https://huggingface.co/datasets/google/fleurs) | Sprachaufnahmen, auch Deutsch | CC BY 4.0 | Spracherkennung |

Offene Bau- oder Immobiliendatensätze mit klarer Lizenz wurden nicht gefunden.

## Kernaussage

Datensätze sind nicht der Engpass. Für die meisten Ideen reichen Prompting, RAG oder fertige offene Modelle. Der Vorsprung entsteht durch Nische, Workflow und eigene Daten, nicht durch eigenes Training.
