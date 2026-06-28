# HMSP Protocol

**Status:** Experimental public summary  
**Purpose:** protocol implementation for HMS-OSA

## Summary

HMSP is the protocol implementation layer that realizes the HMS-OSA architecture. It exists to provide a universal way for devices and services to announce themselves, describe their capabilities, exchange state, and receive commands without depending on brittle, one-off integration glue.

## Core Responsibilities

- discovery
- metadata exchange
- state transport
- command transport
- availability tracking
- connection lifecycle handling

## Design Goals

- transport-agnostic schema design
- practical zero-config onboarding
- predictable state availability
- a clean path for any device or service that implements the contract

## Public Shape

The public version of HMSP should be described as a protocol implementation, not as the architecture itself. The spec comes first; the implementation follows.

## Notes

The current experimental code lives in the private hub and should be treated as reference work in progress.
