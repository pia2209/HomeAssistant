# Home Assistant Packages

Dieses Verzeichnis enthält organisierte Konfigurationspakete für Home Assistant.

## Ordnerstruktur

```
packages/
├── climate/           # Klimasteuerung (Heizung, Kühlung, Thermostat)
│   └── climate_package.yaml
├── dashboard/         # Dashboard-Konfigurationen und UI-Einstellungen
│   └── dashboard_package.yaml
├── lighting/          # Beleuchtungssteuerung und Szenen
│   └── lighting_package.yaml
├── media/             # Mediensteuerung (TV, Musik, Streaming)
│   └── media_package.yaml
├── security/          # Sicherheitssysteme (Alarm, Kameras, Sensoren)
│   └── security_package.yaml
└── system/            # Systemverwaltung (Backups, Updates, Wartung)
    └── system_package.yaml
```

## Was enthält jedes Paket?

Jedes Paket kann folgende Konfigurationen enthalten:

- **input_boolean** - Schalter für Automatisierungen
- **input_number** - Zahlenwerte (z.B. Temperaturen, Helligkeiten)
- **input_select** - Auswahloptionen
- **input_datetime** - Datum/Zeit-Einstellungen
- **sensor** - Template-Sensoren
- **automation** - Automatisierungen
- **script** - Skripte

## Pakete hinzufügen

Um ein neues Paket hinzuzufügen:

1. Erstelle einen neuen Ordner unter `packages/`
2. Erstelle eine YAML-Datei mit der Konfiguration
3. Füge das Paket in `configuration.yaml` hinzu:

```yaml
homeassistant:
  packages:
    neues_paket: !include packages/neues_paket/neues_paket_package.yaml
```

## Vorhandene Pakete

| Paket | Beschreibung |
|-------|-------------|
| climate | Heizung, Kühlung, Thermostatsteuerung |
| dashboard | UI-Themes, Ansichten, Widget-Einstellungen |
| lighting | Beleuchtung, Szenen, Bewegungssteuerung |
| media | TV, Musik, Streaming, Party-Modus |
| security | Alarm, Türsensoren, Urlaubsmodus |
| system | Backups, Wartung, Systemüberwachung |
