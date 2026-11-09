# BXMid03 · HS26

Kursmaterial für das Minor BXMid03 (BFH, Architektur, Holz und Bau): Arbeitsmodelle und Colab-Notebooks. Die Modelle dienen nur der Kursarbeit.

```
modelle/                         IFC-Arbeitsmodelle und Demo-IDS
notebooks/
  2026-10-27_Automatisierung-I/  Notebooks pro Kurstag
  2026-11-03_Validierung/        Notebook 04: Daten ausserhalb des IFC (Airtable)
  eigene/                        eigene Notebooks (aus Colab gespeichert)
```

## Notebooks 27.10. · Automatisierung I

Drei Notebooks, aufeinander aufbauend. Jedes beginnt mit **Modell wählen** (Auswahlliste mit Beispielmodellen oder eigene Datei).

| Notebook | Inhalt | Öffnen |
|---|---|---|
| 01 · Einstieg | So funktioniert Colab · Modell erkunden · ein Bauteil im Detail · eine Regel prüfen (bestanden / durchgefallen / fehlend) · Tabelle und CSV · dasselbe mit IFC-Lite | [![In Colab öffnen](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/LTplus-AG/bxmid03-hs26/blob/main/notebooks/2026-10-27_Automatisierung-I/01_Einstieg_Colab_und_IFC.ipynb) |
| 02 · Fortgeschritten | Modell als Tabelle · Dashboard mit Diagrammen · interaktiver Filter · IDS in Python schreiben und prüfen · 3D-Ansicht mit Klick zurück in Python ([ifc-anywidget](https://github.com/sanzoghenzo/ifc-viewer-anywidget), braucht Chrome oder Edge) | [![In Colab öffnen](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/LTplus-AG/bxmid03-hs26/blob/main/notebooks/2026-10-27_Automatisierung-I/02_Fortgeschritten_Dashboard_IDS_3D.ipynb) |
| 03 · Ausblick | Eigener 3D-Viewer mit Prüffarben (IFC-Lite-Geometrie) · Grundriss aus der Geometrie · Ergebnis ins IFC zurückschreiben · zwei Modellstände vergleichen · HTML-Bericht auf Knopfdruck | [![In Colab öffnen](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/LTplus-AG/bxmid03-hs26/blob/main/notebooks/2026-10-27_Automatisierung-I/03_Ausblick_Was_ist_moeglich.ipynb) |

## Notebook 03.11. · Daten ausserhalb des IFC

| Notebook | Inhalt | Öffnen |
|---|---|---|
| 04 · Airtable und Tabellen | Modell mit Airtable-Links erkunden · eigene Tabelle aus dem IFC (CSV, GlobalId als Schlüssel) · in Airtable oder Google Sheets bearbeiten · zurück ans Modell hängen und Zuordnung prüfen (Mapping-Fehler finden). Teil A, B und D laufen ohne Konto. | [![In Colab öffnen](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/LTplus-AG/bxmid03-hs26/blob/main/notebooks/2026-11-03_Validierung/04_Airtable_Daten_ausserhalb_IFC.ipynb) |

Ohne Colab: `modelle/STR_mit_Airtable_Links.ifc` in [ifclite.com](https://www.ifclite.com) öffnen, Bauteil anklicken → `CPSet_Airtable`.

**Airtable-Daten zum Modell:** [Basis „BFH IFC Demo“](https://airtable.com/appNGbI0mNP8RhZzZ/shrhbra4Qz7Lc4fnS) – ansehen ohne Konto; zum Bearbeiten oben **Copy base** (gratis Airtable-Konto).

## Notebooks speichern

In Colab: *Datei → Kopie in GitHub speichern*.
- Team-Arbeit → eigenes Team-Repository (`LTplus-AG/bxmid03-hs26-team-N`, Ordner `checks/`)
- Alles andere → dieses Repository, Ordner `notebooks/eigene/`

Ohne Speichern gehen Änderungen beim Schliessen von Colab verloren.

## Modelle (`modelle/`)

| Datei | Schema | Herkunft |
|---|---|---|
| `Team_1_Bruecke_Arbeitsmodell.ifc` | IFC4X3_ADD2 | IFC-Lite-Testkorpus (ifcbridge-model01), nach IFC4X3 migriert; Lager- und Baujahrdaten sind synthetische Lehrdaten |
| `Team_1_Bruecke_BFH_Minor.ifc` | IFC4X3_ADD2 | Bereinigte Kopie des Team-1-Arbeitsmodells, ein Pset `BFH_Minor` pro Bauteil (fiktive Lehrdaten). Details: `Team_1_Elementplan.md` |
| `Team_4_Snowdon_Structural_Baufortschritt.ifc` | IFC2X3 | Snowdon Towers Sample (Structural); Termin- und Montagedaten sind synthetische Lehrdaten |
| `Team_5_BIMcollab_Example_STR.ifc` | IFC2X3 | BIMcollab-Beispielmodell (Tragwerk), unverändert |
| `STR_mit_Airtable_Links.ifc` | IFC2X3 | BIMcollab-Tragwerksmodell; 225 Bauteile mit `CPSet_Airtable` und `IfcDocumentReference` auf die Airtable-Basis „BFH IFC Demo“ (öffentlicher Lesezugriff über den Link oben), Lehrbeispiel 2025 |
| `airtable_export_beispiel.csv` | CSV | Simulierter Airtable-Export zu diesem Modell, mit zwei absichtlichen Zuordnungsfehlern (für Notebook 04) |
| `Demo_Holzrahmen_fehlerhaft.ifc` / `_korrigiert.ifc` / `.ids` | IFC4 | Lehrbeispiel 20.10.2026: eine Wand, Width = 0 bzw. 0.1143 m |

Das Ortbetonmodell (Team 3) ist **nicht** enthalten. Prüfsummen: `modelle/SHA256SUMS`.
