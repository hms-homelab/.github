# HMS Homelab

[![Homepage](https://img.shields.io/badge/Home%20Page-shmaestro.com-blue?logo=internet-explorer)](https://shmaestro.com)
[![HMS-4C](https://img.shields.io/badge/Architecture-HMS--4C-blue)]()
[![HMSP](https://img.shields.io/badge/Protocol-HMSP-blue)]()
[![HMS-OSA](https://img.shields.io/badge/API-HMS--OSA-blue)]()

Local-first home management systems, protocols, and services for a resilient residential automation stack.

## What This Org Is For

`hms-homelab` groups the software and infrastructure behind a multi-domain home platform:
- Home Assistant integrations and automations
- n8n workflows and orchestration
- Local AI and voice services
- Device monitoring and health reporting
- Embedded firmware and edge controllers
- Shared protocols, schemas, and libraries

## Architectural Model

This org follows the HMS-4C framework:

- Field Layer: sensors, actuators, firmware, and devices
- Automation Layer: rules, workflows, bridges, and orchestration
- Management Layer: dashboards, operator tools, and manual control
- Intelligence Layer: analytics, inference, and optimization

HMS-4C is the system-level model. HMSP and HMS-OSA define how devices and services discover each other, exchange metadata, and stay available without MQTT-style configuration overhead.

## Protocol Direction

The protocol work in this org is centered on:

- mDNS discovery for zero-config onboarding
- REST metadata endpoints for device description
- Persistent transport for live state and commands
- Protobuf schemas for structured messages
- Availability tracking so devices degrade cleanly instead of falling into unknown states

## Core Repositories

- `hms-hub` - umbrella appliance and integration layer
- `hmsp-protocol` - protocol and schema work
- `hms-assist` - backend voice and intent service
- `hms-assist-voice` - embedded voice firmware
- `hms-weather` - weather station and forecasting stack
- `hms-nut` - UPS monitoring and alerts
- `hms-cpap` - CPAP data processing and intelligence
- `hms-firetv` - media and Fire TV automation
- `hms-tuya` - Tuya integration work
- `hms-nvr` - camera and vision services
- `hms-shared` - common libraries and reusable code

## Product Direction

The long-term target is a plug-and-play homelab appliance that combines:
- Home Assistant
- n8n
- Local AI
- Voice assistance
- Monitoring and alerting
- Low-config setup

## Tags

- `homelab`
- `home-automation`
- `home-assistant`
- `n8n`
- `local-ai`
- `protocols`
- `HMS`

## Current Focus

- Standardized device discovery
- Reliable local integrations
- Reusable automation patterns
- Event-driven telemetry
- Shared schemas and protocol bindings
- Operational docs and quick references

## Documentation

Start with:
- HMS-4C framework
- HMSP specification
- HMS-OSA specification
- Maestro Hub product overview
- Service-specific setup guides and quick refs

## Status

This org is under active development. Repos are split by domain so each subsystem can evolve independently while sharing common architecture and protocol ideas.
