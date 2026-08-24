# ESP32 BLE Configuration System

Embedded firmware project implementing a Bluetooth Low Energy configuration
interface for an ESP32-based connected device.

## Overview

The goal was to allow device parameters to be configured wirelessly through BLE
instead of modifying and reflashing the firmware whenever network or communication
settings change.

## Technologies

- ESP32
- ESP-IDF
- Embedded C
- NimBLE
- BLE / GATT
- NVS Flash
- Wi-Fi
- MQTT
- nRF Connect

## Features

- Custom BLE GATT configuration service
- Read/Write GATT characteristics
- Device ID configuration
- Wi-Fi SSID and password configuration
- MQTT URI and credentials configuration
- Transmission interval configuration
- Persistent parameter storage using NVS
- Configuration restored automatically from Flash at boot
- BLE interface validation using nRF Connect

## Architecture

BLE Client  
↓  
ESP32 NimBLE GATT Server  
↓  
Runtime Configuration  
↓  
NVS Flash Storage  
↓  
Wi-Fi / MQTT Services

## Validation

The GATT interface was tested using nRF Connect to validate characteristic
discovery, Read/Write operations and persistent configuration behavior.

## Note

This repository presents the architecture and technical work developed during
an embedded firmware internship. Proprietary company firmware and confidential
source code are not included.<img width="682" height="1263" alt="télécharger" src="https://github.com/user-attachments/assets/ac2c03bf-fe44-45d8-8a1a-f7afe5a15bb8" />

