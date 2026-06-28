# HMS Homelab

[![Homepage](https://img.shields.io/badge/Home%20Page-shmaestro.com-blue?logo=internet-explorer)](https://shmaestro.com)
[![Architecture](https://img.shields.io/badge/Architecture-HMS--4C-blue)]()
[![Protocol](https://img.shields.io/badge/Protocol-HMSP%20(draft)-orange)](https://github.com/hms-homelab/hmsp-protocol)

Local-first home management systems and services for a resilient residential automation stack.

## What This Org Is For

`hms-homelab` groups the software and firmware behind a multi-domain home platform:
- Home Assistant integrations and automations
- n8n workflows and orchestration
- Local AI and voice services
- Device monitoring and health reporting
- Embedded firmware and edge controllers
- Shared libraries and reusable code

Most services are C++ (Drogon) microservices or ESP32 firmware that integrate with
Home Assistant over MQTT and REST. They are split by domain so each subsystem can
evolve independently while sharing common patterns.

## Architecture — HMS-4C

The stack follows the **HMS-4C** framework: four operational layers, so concerns stay
separated and the system degrades cleanly instead of failing as a monolith.

- **Field** — sensors, actuators, firmware, cameras, UPS, weather station
- **Automation** — Home Assistant, n8n, data collectors, protocol bridges
- **Management** — dashboards, operator tools, manual control
- **Intelligence** — analytics, ML inference, optimization

## Protocol — HMSP (draft)

Today these services integrate over **MQTT + Home Assistant auto-discovery**. The
planned successor is **[HMSP](https://github.com/hms-homelab/hmsp-protocol)** — a
zero-config protocol that drops the broker in favor of:

- mDNS discovery (`_hmsp._tcp.local`)
- a REST metadata endpoint (`GET /api/hmsp/info`)
- a WebSocket carrying Protobuf messages, with sequence numbers, command
  acknowledgements, and explicit availability

> **Status:** HMSP is a `v1.0.0-draft` design with a reference C++ library, Python SDK,
> ESP-IDF component, and HA integration — **not yet production-deployed.** The current
> production transport is still MQTT.

## Repositories

**CPAP / Sleep**
- [`hms-cpap`](https://github.com/hms-homelab/hms-cpap) — ResMed CPAP data collection for Home Assistant
- [`hms-cpapdash-parser`](https://github.com/hms-homelab/hms-cpapdash-parser) — shared C++ CPAP parser (ResMed + Lowenstein)
- [`hms-cpapdash-charts`](https://github.com/hms-homelab/hms-cpapdash-charts) — shared Angular chart components
- [`hms-cpap-arduino`](https://github.com/hms-homelab/hms-cpap-arduino) — ESP8285 CPAP data bridge (FYSETC SD-WiFi v2.1)
- [`hms-fysetc`](https://github.com/hms-homelab/hms-fysetc) — HTTP file server firmware for FYSETC SD WiFi Pro
- [`hms-mm`](https://github.com/hms-homelab/hms-mm) — dual ESP32-C3 miner/mule WiFi SD card bridge

**Voice / Assist**
- [`hms-assist-api`](https://github.com/hms-homelab/hms-assist-api) — backend voice and intent service (3-tier classification)

**Monitoring / Power**
- [`hms-nut`](https://github.com/hms-homelab/hms-nut) — UPS monitoring and alerts
- [`hms-esp-apc`](https://github.com/hms-homelab/hms-esp-apc) — ESP32-S3 USB Host to MQTT bridge for APC UPS

**Cameras / Vision**
- [`hms-nvr`](https://github.com/hms-homelab/hms-nvr) — Amcrest camera event stream monitor
- [`hms-detection`](https://github.com/hms-homelab/hms-detection) — RTSP capture and YOLO object detection
- [`hms-timeline`](https://github.com/hms-homelab/hms-timeline) — YOLO detection timeline viewer

**Media / Automation**
- [`hms-firetv`](https://github.com/hms-homelab/hms-firetv) — Fire TV Lightning Protocol service

**Devices / Bridges**
- [`hms-tuya`](https://github.com/hms-homelab/hms-tuya) — Tuya WiFi MQTT bridge with HA auto-discovery
- [`nanotuya`](https://github.com/hms-homelab/nanotuya) — C++ library for the Tuya WiFi local protocol
- [`hms-esp-tuya-ble`](https://github.com/hms-homelab/hms-esp-tuya-ble) — ESP32-C3 BLE to MQTT bridge for Tuya breakers
- [`hms-scale`](https://github.com/hms-homelab/hms-scale) — smart scale service with ML user identification
- [`hms-scale-esp`](https://github.com/hms-homelab/hms-scale-esp) — ESP32-C3 BLE gateway for Etekcity scale
- [`nordictrack_t5`](https://github.com/hms-homelab/nordictrack_t5) — ESP32-S3 bridge for NordicTrack/iFit treadmills

**Baby**
- [`hms-baby-tracker`](https://github.com/hms-homelab/hms-baby-tracker) — newborn care tracking for Home Assistant

**Protocol / Shared**
- [`hmsp-protocol`](https://github.com/hms-homelab/hmsp-protocol) — HMSP spec, C++ lib, SDKs (draft)
- [`hms-shared`](https://github.com/hms-homelab/hms-shared) — common libraries and reusable code
- [`hms-claude-mem`](https://github.com/hms-homelab/hms-claude-mem) — semantic memory MCP server (C++ / Redis / Ollama)
- [`hms-gmail`](https://github.com/hms-homelab/hms-gmail) — self-hosted Gmail backup and semantic search

## Tags

`homelab` · `home-automation` · `home-assistant` · `n8n` · `local-ai` · `HMS`

## Status

Under active development. Repos are split by domain so each subsystem can evolve
independently while sharing common architecture ideas. HMS-4C is the production model;
HMSP is the in-design protocol direction.
