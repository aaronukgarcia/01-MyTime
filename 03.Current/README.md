# MyTime

**A Protocol for Universal Availability — The "Time Layer" of the Internet**

## What is MyTime?

MyTime is a global availability directory that makes time searchable. Just as HTTP made information discoverable, MyTime makes availability discoverable across any resource type.

The protocol uses a minimal three-state model:

| State | Meaning |
|-------|---------|
| Free | Available for booking or allocation |
| Busy | Unavailable, confirmed |
| Tentative | Provisionally booked or lower priority |

## The Problem

Commerce depends on discovering when resources are available, yet no universal system exists. Availability data is trapped in proprietary booking platforms or private silos.

The inefficiency is measurable: driving instructors sit idle between lessons, venues stand empty, consultants have unutilised hours. The resource provider knows their availability but cannot advertise it efficiently.

Current systems are person-centric ("When is John available?"). MyTime inverts this to time-centric discovery ("Who is free at 3pm Tuesday?").

## Design Principles

- **Infrastructure, not a marketplace** — No transaction intermediation, no commissions, no platform lock-in
- **Privacy preservation** — Only availability states are stored; no appointment details, customer data, or transaction history
- **Universal granularity** — From 10-minute blocks for freelancers to 180-day blocks for venues
- **Federation-ready** — Designed for integration with iCal, CalDAV, and Exchange

## Status

This project is in the specification phase. Implementation is planned for early 2026.

## Call for Contributors

We're seeking founding contributors to refine the specification:

- Systems architects
- Calendar protocol experts
- Database engineers
- Economists

### Key Challenges

- **Trust mechanics** — Sybil-resistance to prevent inventory squatting
- **Privacy standards** — Proving availability without leaking pattern-of-life data
- **Economic modelling** — Sustainability for zero-transaction-fee infrastructure
- **Federation protocols** — Integration with existing calendar ecosystems

## Documentation

See `docs/MyTime_WhitePaper_v1_0.pdf` for the full specification.

## License

MIT License — see [LICENSE](LICENSE) for details.

## Contact

Aaron Garcia  
aaron@garcia.ltd