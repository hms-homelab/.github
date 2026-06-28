# HMS-4C Framework

**Status:** Experimental public summary  
**Purpose:** architectural discipline for home-lab interactions

## Summary

HMS-4C is the design frame for how systems in the homelab should behave. It is not the transport, not the implementation, and not a product integration. It defines the principles that should shape every interaction between devices, services, and operators.

The four pillars are:

- **Components** - the replaceable parts of the system
- **Connectors** - the interactions and links between parts
- **Constraints** - the limits that shape acceptable behavior
- **Context** - the domain-specific meaning behind an interaction

## What HMS-4C Does

- gives the system a consistent design language
- keeps interactions understandable across device classes
- forces explicit thinking about limits and environment
- makes room for multiple domains without collapsing them into one opaque automation layer

## What HMS-4C Does Not Do

- it does not define a wire protocol
- it does not prescribe a specific vendor platform
- it does not require any single home-automation product
- it does not expose private network details

## Relationship to the Stack

`HMS-4C` is the outer frame.
`HMS-OSA` is the formal architecture definition.
`HMSP` is the protocol implementation path.

The public project is intentionally architecture-first and implementation-second.
