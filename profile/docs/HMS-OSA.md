# HMS-OSA Specification

**Status:** Experimental public summary  
**Purpose:** formal architecture definition for open homelab integration

## Summary

HMS-OSA defines how the HMS-4C pillars should be implemented in practice. It describes the structure that participating devices and services should expose so they can be discovered, understood, and integrated consistently.

## What It Defines

- a consistent architecture contract
- discovery and metadata expectations
- state and command surfaces
- availability semantics
- the relationship between a device, its capabilities, and its operating context

## What It Avoids

- private network assumptions
- vendor-locked behavior
- product-specific integration rules
- hard dependencies on any single home-automation platform

## Relationship to HMSP

`HMS-OSA` is the formal definition.
`HMSP` is the implementation path.

The protocol work exists to make the spec usable across devices, services, and future community implementations.
