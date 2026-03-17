<p align="center">
	<a href="https://www.divera247.com">
		<img src="https://www.divera247.com/downloads/grafik/divera247_logo_800.png" alt="Divera 24/7">
	</a>
</p>

---

[![Deutsch](https://img.shields.io/badge/Deutsch-available-blue)](README.md)

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

> Note: This integration is based on the work of @fwmarcel. Unfortunately, the original integration is no longer available and is therefore temporarily provided here. Thank you for your work.

This is a Divera integration for personal use. No extended permissions are
required. It fully covers typical home use cases. It provides alarms, news,
events, vehicle states, and functions to change your status.

An integration with advanced features, including alarm creation and setting
vehicle status, can be found here:
[DiveraControl](https://github.com/moehrem/DiveraControl)

## Features

- Setup through the config flow directly in the Home Assistant UI
- Supports Divera cloud and custom server URL
- Supports accounts with one or multiple units (clusters)
- Sensors:
  - Last alarm
  - Last news
  - Vehicle status (one sensor per vehicle)
  - Active alarm (on when open alarms exist)
- Calendar:
  - Events
- Select:
  - User status (change your Divera status from Home Assistant)

Important: Group access keys are not supported. Use a user access key.

## Installation

A HACS integration is planned. Until then, only manual installation is
available.

### Option 2: Manual installation

1. Copy the folder `custom_components/divera` from this repository.
2. Place it in your Home Assistant configuration directory as:
   `config/custom_components/divera`
3. Restart Home Assistant.

## Setup in Home Assistant

1. Open `Settings -> Devices & Services -> Add integration`.
2. Search for `Divera 24/7`.
3. Enter:
   - `Accesskey` (required)
   - `Server Address` (optional, default is `https://app.divera247.com`)
4. If your account belongs to multiple units, select the active units.
5. Finish setup.

## Project status

This project is not under active feature development. Only bug fixes and
Home Assistant compatibility changes are being made.
In the future, this project is planned to be merged with DiveraControl.
