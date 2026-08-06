# MyTime: Making Time Searchable

*A Concept Paper for Universal Availability Infrastructure*

## What is MyTime?

MyTime proposes a public, searchable availability directory where anyone can discover available resources by time, location, and category --- without knowing who to ask. Current systems are person-centric ("When is John available?"). MyTime inverts this to time-centric discovery ("Who is free at 3pm Tuesday?").

The system uses a minimal three-state model:

| State | Meaning |
|-------|---------|
| Free | Available for booking or allocation |
| Busy | Unavailable, confirmed |
| Tentative | Provisionally booked or lower priority |

Nothing more is stored. No appointment details, no customer data, no transaction history. Privacy is architectural, not policy-dependent.

## The Problem

Availability data is trapped in proprietary booking platforms (10--30% commissions, vertical lock-in) or private calendar silos. Driving instructors sit idle between lessons. Wedding venues stand empty on dates couples would have booked. The information exists --- it is invisible.

Calendar interoperability standards (iCalendar, CalDAV, VFREEBUSY) handle availability exchange between known parties. What they do not provide is a way for strangers to search for available resources across providers, categories, and geographies. The closest live system — Reserve with Google — aggregates bookable availability across a few verticals, but it is partner-gated, booking-mediated, place-centric, and controlled by a single company. No *open* availability index exists.

## Design Principles

- **Infrastructure, not a marketplace** --- No transaction intermediation, no commissions, no platform lock-in
- **Built on existing standards** --- Extends iCalendar (RFC 5545), CalDAV (RFC 4791), and VAVAILABILITY (RFC 7953) with a discovery layer
- **Privacy by architecture** --- Three-state model stores no sensitive information by design
- **Variable granularity** --- From 10-minute blocks for freelancers to 180-day blocks for venues

## Status

This is a concept paper (v2.1), not a specification. It describes design principles, surveys prior art, proposes a bootstrapping strategy (the embeddable availability widget), and enumerates open design questions. A technical specification would be a separate deliverable if the concept attracts contributors.

## Documentation

See [`MyTime_WhitePaper_v2.1.pdf`](MyTime_WhitePaper_v2.1.pdf) for the full concept paper.

## Call for Contributors

We seek people who will challenge the assumptions, not validate them:

- **Calendar protocol engineers** --- Can VAVAILABILITY and CalDAV Scheduling already solve this?
- **Distributed systems architects** --- Is the storage and query model viable at scale?
- **Economists** --- Can a zero-commission infrastructure layer sustain itself?
- **Privacy engineers** --- How should GDPR-compliant calendar ingestion work?

### Key Open Questions

- **Cold-start problem** --- How to achieve provider density before the search index is useful
- **Architecture** --- Centralised service, federated network, or crawl-based index?
- **Governance** --- What structure prevents capture by a single commercial entity?
- **Economic model** --- Freemium widget features? Commercial API access? Institutional sponsorship?

## License

MIT License --- see [LICENSE](LICENSE) for details.

## Contact

Aaron Garcia
aaron@garcia.ltd
