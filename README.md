<p align="center">
  <a href="https://www.divera247.com">
    <img src="https://www.divera247.com/downloads/grafik/divera247_logo_800.png" alt="Divera 24/7">
  </a>
</p>

---

[![English](https://img.shields.io/badge/🇬🇧%20-English-blue)](README.en.md)

---

![update-badge](https://img.shields.io/github/last-commit/moehrem/ha-divera?label=last%20update)

[![GitHub Release](https://img.shields.io/github/v/release/moehrem/ha-divera?sort=semver)](https://github.com/moehrem/ha-divera/releases)

![GitHub commit activity](https://img.shields.io/github/commit-activity/m/moehrem/ha-divera)
![GitHub last commit](https://img.shields.io/github/last-commit/moehrem/ha-divera)
![GitHub issues](https://img.shields.io/github/issues/moehrem/ha-divera)

![HA Analytics](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fanalytics.home-assistant.io%2Fcustom_integrations.json&query=%24.ha-divera.total&label=Active%20Installations)
[![hacs](https://img.shields.io/badge/HACS-Integration-blue.svg)](https://github.com/hacs/integration)
[![HASS QS](https://github.com/moehrem/ha-divera/actions/workflows/hass.yml/badge.svg)](https://github.com/moehrem/ha-divera/actions/workflows/hass.yml)
[![HACS QS](https://github.com/moehrem/ha-divera/actions/workflows/hacs.yml/badge.svg)](https://github.com/moehrem/ha-divera/actions/workflows/hacs.yml)

---

# Divera 24/7

> Hinweis: Diese Integration basiert auf der Arbeit von @fwmarcel. Leider ist seine originale Integration nicht mehr verfügbar und wird daher hier vorrübergehend bereit gestellt. Vielen Dank für deine Mühen!

Dies ist eine Divera-Integration zur persönlichen Nutzung. Es sind keine erweiterten Berechtigungen erforderlich. Diese Integration deckt den üblichen Heimbedarf komplett ab. Es werden Alarme, News, Termine, Fahrzeugstatus und eine Funktion zum Setzen des Status bereit gestellt.

Eine Integration mit erweiterten Funktionen, u.a. der Alarmerstellung, dem Setzen des Fahrzeugstatus etc findet sich hier: [DiveraControl](https://github.com/moehrem/DiveraControl)

## Funktionen

- Einrichtung ueber den Konfigurationsdialog direkt in der Home Assistant UI
- Unterstuetzt Divera Cloud und benutzerdefinierte Server-URL
- Unterstuetzt Konten mit einer oder mehreren Einheiten (Cluster)
- Sensoren:
  - Letzter Alarm
  - Letzte News
  - Fahrzeugstatus (ein Sensor pro Fahrzeug)
  - Aktiver Alarm (an, wenn offene Alarme vorhanden sind)
- Kalender:
  - Termine
- Auswahl:
  - Benutzerstatus (ändere deinen Divera-Status aus Home Assistant)

Wichtig: Gruppen-Accesskeys werden nicht unterstuetzt. Verwende einen Benutzer-Accesskey.

## Installation

### Option 1: HACS (empfohlen)

Divera 24/7 ist via HACS (Home Assistant Community Store) verfügbar.

1. [HACS installieren](https://www.hacs.xyz/docs/use/)
2. [![HACS Repo hinzufügen](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=moehrem&repository=ha-divera&category=Integration)
3. **Installation:** Unten rechts auf "Herunterladen" klicken.

### Option 2: Manuelle Installation

1. Kopiere den Ordner `custom_components/divera` aus diesem Repository.
2. Lege ihn in deinem Home Assistant Konfigurationsverzeichnis ab unter:
   `config/custom_components/divera`
3. Restart Home Assistant.

## Einrichtung in Home Assistant

1. Öffne `Einstellungen -> Geraete & Dienste -> Integration hinzufuegen`.
2. Suche nach `Divera 24/7`.
3. Gib ein:
   - `Accesskey` (erforderlich)
   - `Server Address` (optional, Standard ist `https://app.divera247.com`)
4. Wenn dein Konto zu mehreren Einheiten gehört, wähle die aktiven Einheiten aus.
5. Einrichtung abschliessen.

## Projektstatus

Dieses Projekt wird nicht aktiv weiter entwickelt. Lediglich bugfixing bzw durch HA notwendige Codeanpassungen werden vorgenommen.
In Zukunft soll dieses Projekt mit [DiveraControl](https://github.com/moehrem/DiveraControl) zusammengeführt werden.
