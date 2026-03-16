<p align="center">
  <a href="https://www.divera247.com">
    <img src="https://www.divera247.com/downloads/grafik/divera247_logo_800.png" alt="Divera 24/7">
  </a>
</p>

---

[![German](https://img.shields.io/badge/🇩🇪%20-German-red)](README.md)

---

# Divera 24/7

This integration connects your personal Divera account to Home Assistant and
provides alarms, news, events, vehicle states, and your user status as entities.

## Features

- Config flow setup directly in Home Assistant UI
- Supports Divera cloud and custom server URL
- Supports accounts with one or multiple units (clusters)
- Sensor entities:
  - Last alarm
  - Last news
  - Vehicle status (one sensor per vehicle)
- Binary sensor:
  - Active alarm (on when open alarms exist)
- Calendar entity:
  - Events
- Select entity:
  - User status (change your Divera status from Home Assistant)

## Requirements

- Home Assistant with custom integrations enabled
- A valid personal Divera user access key

Important: Group access keys are not supported. Use a user access key.

## Installation

### Option 1: Manual installation

1. Copy the folder `custom_component/divera` from this repository.
2. Place it into your Home Assistant config directory as:
   `config/custom_components/divera`
3. Restart Home Assistant.

### Option 2: Development with symbolic link

If you develop locally, link your integration folder into Home Assistant:

```bash
ln -s /path/to/ha-divera/custom_component/divera /path/to/ha/config/custom_components/divera
```

Then restart Home Assistant.

## Setup in Home Assistant

1. Open `Settings -> Devices & Services -> Add integration`.
2. Search for `Divera 24/7`.
3. Enter:
   - `Accesskey` (required)
   - `Server Address` (optional, defaults to `https://app.divera247.com`)
4. If your account belongs to multiple units, select the active units.
5. Finish setup.

## Reconfigure units

If you want to change which units are active later:

1. Open the integration in Home Assistant.
2. Choose `Reconfigure`.
3. Select the desired units.

## Entities

This integration creates entities per active unit.

### Sensors

- `alarm`: last alarm
- `news`: last news
- `vehicle`: one sensor per vehicle with current vehicle status

### Binary sensor

- `active_alarm`: indicates if at least one alarm is currently open

### Calendar

- `events`: exposes Divera events

### Select

- `user_status`: read and set your personal Divera status

## Troubleshooting

- `Error during authentication`:
  - Verify your access key
  - Ensure you are using a user key, not a group key
- `Error during connection`:
  - Check internet connectivity
  - Check custom server URL if you use one

After changes, restart Home Assistant and reload the integration.

## Project status

This repository is under active development. Issues and pull requests are welcome.
