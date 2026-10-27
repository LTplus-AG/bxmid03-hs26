# BXMid03 · HS26

Kursmaterial für das Minor BXMid03 (BFH, Architektur, Holz und Bau): Arbeitsmodelle und Colab-Notebooks. Die Modelle dienen nur der Kursarbeit.

```
modelle/                         IFC-Arbeitsmodelle und Demo-IDS
notebooks/
  2026-10-27_Automatisierung-I/  Notebooks pro Kurstag
  eigene/                        eigene Notebooks (aus Colab gespeichert)
```

## Notebooks 27.10. · Automatisierung I

Drei Notebooks, aufeinander aufbauend. Jedes beginnt mit **Modell wählen** (Auswahlliste mit Beispielmodellen oder eigene Datei).

| Notebook | Inhalt | Öffnen |
|---|---|---|
| 01 · Einstieg | So funktioniert Colab · Modell erkunden · ein Bauteil im Detail · eine Regel prüfen (bestanden / durchgefallen / fehlend) · Tabelle und CSV · dasselbe mit IFC-Lite | [![In Colab öffnen](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/LTplus-AG/bxmid03-hs26/blob/main/notebooks/2026-10-27_Automatisierung-I/01_Einstieg_Colab_und_IFC.ipynb) |
| 02 · Fortgeschritten | Modell als Tabelle · Dashboard mit Diagrammen · interaktiver Filter · IDS in Python schreiben und prüfen · 3D-Ansicht mit Klick zurück in Python ([ifc-anywidget](https://github.com/sanzoghenzo/ifc-viewer-anywidget), braucht Chrome oder Edge) | [![In Colab öffnen](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/LTplus-AG/bxmid03-hs26/blob/main/notebooks/2026-10-27_Automatisierung-I/02_Fortgeschritten_Dashboard_IDS_3D.ipynb) |
| 03 · Ausblick | Eigener 3D-Viewer mit Prüffarben (IFC-Lite-Geometrie) · Grundriss aus der Geometrie · Ergebnis ins IFC zurückschreiben · zwei Modellstände vergleichen · HTML-Bericht auf Knopfdruck | [![In Colab öffnen](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/LTplus-AG/bxmid03-hs26/blob/main/notebooks/2026-10-27_Automatisierung-I/03_Ausblick_Was_ist_moeglich.ipynb) |

## Notebooks speichern

In Colab: *Datei → Kopie in GitHub speichern*.
- Team-Arbeit → eigenes Team-Repository (`LTplus-AG/bxmid03-hs26-team-N`, Ordner `checks/`)
- Alles andere → dieses Repository, Ordner `notebooks/eigene/`

Ohne Speichern gehen Änderungen beim Schliessen von Colab verloren.

## Modelle (`modelle/`)

| Datei | Schema | Herkunft |
|---|---|---|
| `Team_1_Bruecke_Arbeitsmodell.ifc` | IFC4X3_ADD2 | IFC-Lite-Testkorpus (ifcbridge-model01), nach IFC4X3 migriert; Lager- und Baujahrdaten sind synthetische Lehrdaten |
| `Team_4_Snowdon_Structural_Baufortschritt.ifc` | IFC2X3 | Snowdon Towers Sample (Structural); Termin- und Montagedaten sind synthetische Lehrdaten |
| `Team_5_BIMcollab_Example_STR.ifc` | IFC2X3 | BIMcollab-Beispielmodell (Tragwerk), unverändert |
| `Demo_Holzrahmen_fehlerhaft.ifc` / `_korrigiert.ifc` / `.ids` | IFC4 | Lehrbeispiel 20.10.2026: eine Wand, Width = 0 bzw. 0.1143 m |

Das Ortbetonmodell (Team 3) ist **nicht** enthalten. Prüfsummen: `modelle/SHA256SUMS`.
