# BXMid03 · HS26

Kursmaterial für das Minor BXMid03 (BFH, Architektur, Holz und Bau): Arbeitsmodelle und Colab-Notebooks. Die Modelle dienen nur der Kursarbeit.

```
modelle/                         IFC-Arbeitsmodelle und Demo-IDS
notebooks/
  2026-10-27_Automatisierung-I/  Notebooks pro Kurstag
  eigene/                        eigene Notebooks (aus Colab gespeichert)
```

## Notebooks 27.10. · Automatisierung I

Jedes Notebook beginnt mit **Modell wählen** (Dropdown). Teams mit eigenem Repository tragen stattdessen im eigenen Block den GitHub-Link zu ihrer IFC-Datei ein.

| Notebook | Inhalt | Öffnen |
|---|---|---|
| 01 Basis · IfcOpenShell | Wand-Check „Breite > 0“ mit IfcOpenShell, Ergebnis als CSV | [In Colab öffnen](https://colab.research.google.com/github/LTplus-AG/bxmid03-hs26/blob/main/notebooks/2026-10-27_Automatisierung-I/01_Basis_IfcOpenShell.ipynb) |
| 02 Basis · IFC-Lite | Derselbe Check mit IFC-Lite in Python (`ifclite-geom`) | [In Colab öffnen](https://colab.research.google.com/github/LTplus-AG/bxmid03-hs26/blob/main/notebooks/2026-10-27_Automatisierung-I/02_Basis_IFC-Lite.ipynb) |
| 03 Fortgeschritten · 3D | Check plus 3D-Ansicht ([ifc-anywidget](https://github.com/sanzoghenzo/ifc-viewer-anywidget), IFC-Lite-Renderer). Braucht Chrome oder Edge (WebGPU). | [In Colab öffnen](https://colab.research.google.com/github/LTplus-AG/bxmid03-hs26/blob/main/notebooks/2026-10-27_Automatisierung-I/03_Fortgeschritten_3D.ipynb) |

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
