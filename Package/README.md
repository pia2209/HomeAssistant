# Package/
Diese Struktur dient dazu, Home-Assistant-Konfiguration thematisch zu bündeln.

## Wie es eingebunden ist
In `configuration.yaml` ist Folgendes aktiviert:
- `homeassistant.packages: !include_dir_named Package`

Wichtig: Home Assistant lädt **nur** die YAML-Dateien direkt in `Package/` (z.B. `climate.yaml`).
Die Unterordner (`Package/climate/`, `Package/dashboard/`, …) werden über `!include ...` aus den
jeweiligen Package-Dateien eingebunden.

## Ordner
- `Package/climate/`: Climate-Skripte/Automationen (z.B. `script_climate.yaml`)
- `Package/dashboard/`: Ablage/Notizen zu Dashboards (optional)
- `Package/system/`: Systemnahe Dinge (optional)
- `Package/common/`: Gemeinsame Helfer/Blöcke (optional)
