<p align="center">
  <a href="https://www.divera247.com">
    <img src="https://www.divera247.com/downloads/grafik/divera247_logo_800.png" alt="Divera 24/7">
  </a>
</p>

---

[![English](https://img.shields.io/badge/🇬🇧%20-English-blue)](README.en.md)

---

# Divera 24/7

Diese Integration verbindet dein persoenliches Divera-Konto mit Home Assistant
und stellt Alarme, News, Termine, Fahrzeugstatus und deinen Benutzerstatus als
Entitaeten bereit.

## Funktionen

- Einrichtung ueber den Konfigurationsdialog direkt in der Home Assistant UI
- Unterstuetzt Divera Cloud und benutzerdefinierte Server-URL
- Unterstuetzt Konten mit einer oder mehreren Einheiten (Cluster)
- Sensor-Entitaeten:
  - Letzter Alarm
  - Letzte News
  - Fahrzeugstatus (ein Sensor pro Fahrzeug)
- Binary-Sensor:
  - Aktiver Alarm (an, wenn offene Alarme vorhanden sind)
- Kalender-Entitaet:
  - Termine
- Select-Entitaet:
  - Benutzerstatus (aendere deinen Divera-Status aus Home Assistant)

## Voraussetzungen

- Home Assistant mit aktivierten benutzerdefinierten Integrationen
- Ein gueltiger persoenlicher Divera Benutzer-Accesskey

Wichtig: Gruppen-Accesskeys werden nicht unterstuetzt. Verwende einen
Benutzer-Accesskey.

## Installation

### Option 1: Manuelle Installation

1. Kopiere den Ordner `custom_components/divera` aus diesem Repository.
2. Lege ihn in deinem Home Assistant Konfigurationsverzeichnis ab unter:
   `config/custom_components/divera`
3. Restart Home Assistant.

### Option 2: Entwicklung mit symbolischem Link

Wenn du lokal entwickelst, verlinke deinen Integrationsordner in Home Assistant:

```bash
ln -s /path/to/ha-divera/custom_components/divera /path/to/ha/config/custom_components/divera
```

Danach Home Assistant neu starten.

## Einrichtung in Home Assistant

1. Oeffne `Einstellungen -> Geraete & Dienste -> Integration hinzufuegen`.
2. Suche nach `Divera 24/7`.
3. Gib ein:
   - `Accesskey` (erforderlich)
   - `Server Address` (optional, Standard ist `https://app.divera247.com`)
4. Wenn dein Konto zu mehreren Einheiten gehoert, waehle die aktiven
   Einheiten aus.
5. Einrichtung abschliessen.

## Einheiten neu konfigurieren

Wenn du spaeter aendern moechtest, welche Einheiten aktiv sind:

1. Oeffne die Integration in Home Assistant.
2. Waehle `Neu konfigurieren`.
3. Waehle die gewuenschten Einheiten aus.

## Entitaeten

Diese Integration erstellt Entitaeten pro aktiver Einheit.

### Sensoren

- `alarm`: letzter Alarm
- `news`: letzte News
- `vehicle`: ein Sensor pro Fahrzeug mit aktuellem Fahrzeugstatus

### Binary-Sensor

- `active_alarm`: zeigt an, ob mindestens ein Alarm aktuell offen ist

### Kalender

- `events`: stellt Divera-Termine bereit

### Select

- `user_status`: liest und setzt deinen persoenlichen Divera-Status

## Fehlerbehebung

- `Error during authentication`:
  - Pruefe deinen Accesskey
  - Stelle sicher, dass du einen Benutzer-Key und keinen Gruppen-Key nutzt
- `Error during connection`:
  - Pruefe die Internetverbindung
  - Pruefe die benutzerdefinierte Server-URL, falls du eine verwendest

Nach Aenderungen Home Assistant neu starten und die Integration neu laden.

## Projektstatus

Dieses Repository wird aktiv weiterentwickelt. Issues und Pull Requests sind
willkommen.
