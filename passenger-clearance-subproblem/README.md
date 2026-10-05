# Passenger Clearance Subproblem

## Table of Contents
- [The Problem](#the-problem)
- [Potential Solutions](#potential-solutions)
- [Resources](#resources)

## The Problem
A school group of 32 passengers arrives at the airport to check in for the same flight less than an hour before the check-in deadline. Although the passengers are travelling together, each person has different document requirements, seat assignments and baggage information. Most passengers are cleared immediately, but several require additional document review.

Processing every passenger individually creates a long queue and increases the risk that the group will not complete check-in on time. However. Treating the entire group as one unit could cause individual document or baggage issues to be overloaded. Staff need a way to see which passengers are ready, which require attention and what issues remain unsolved. 

Your challenge is to develop a solution that helps airport staff process large groups efficiently while maintaining accurate clearance information for each individual passenger.

Your challenge is to develop a solution that quickly adapts the existing passenger and baggage plan to the replacement aircraft while maintaining safety weight-and-balance limits and minimizing operational disruption.

### Inputs and Expected Outputs 
You'll likely be working with passenger lists, bookings, seat maps, aircraft layouts, baggage records, scan events, document fields, and schedules. As it is difficult to find perfect datasets, some of it will be missing, late, or contradictory. Design for that instead of around it.

Whatever you build should make departure readiness legible at a glance: current status, what was decided, what still needs attention, and why.

## Potential Solutions
A few possible scopes below. You can extend one or build something else entirely.

| Potential solution | Description | Starting point |
| --- | --- | --- |
| Unified identity gateway | Combine booking lookup, document checks, seat selection, baggage declaration, boarding passes, and agent review. | [Working implementation](unified-identity-gateway/README.md) |
| Document-review assistant | Validate required fields, identify mismatches, and route uncertain cases to an agent. | [Identity-gateway rules](unified-identity-gateway/apps/api/src/rules/) |
| Boarding-readiness dashboard | Combine document, seat, baggage, and boarding state into one operator view. | [Unified Identity Gateway](unified-identity-gateway/README.md) |
| Baggage reconciliation tool | Link accepted bags to passengers and explain missing or unexpected scans. | [Baggage Handling System](../baggage-handling-system/README.md) |

### Evaluation

Worth checking your solution against:

| Area | What to look for |
| --- | --- |
| Workflow completeness | Does the process work from input to result? |
| Data modelling | Are passengers, bags, flights, and seats represented clearly? |
| Decision quality | Are recommendations, predictions, and review flags useful? |
| Exception handling | Does the system handle missing, inconsistent data, and edge cases? |
| Dashboard clarity | Can an operator understand readiness and outstanding work from a glance? |
| Privacy and accessibility | Is sensitive data minimized, and is feedback usable by people with different needs? |
| Code quality | Is the implementation modular, readable, and maintainable? |
| Demonstration | Does the demo make the value and limitations clear? |

### Challenge Resources

- [Unified Identity Gateway implementation](unified-identity-gateway/README.md)
- [Passenger-processing project ideas](passenger-processing/README.md)
- [Identity-gateway challenge specification](unified-identity-gateway/docs/challenge-spec.md)

### Safety, Privacy, and Industry References

- [IATA Resolution 753 baggage-tracking implementation guide](https://www.iata.org/contentassets/5c4aa8b8b3b1432697d2bf3301450684/reso753-implementation-guide---2023_issue-4.02.pdf): baggage tracking at defined handoff points
- [ICAO Doc 9303 machine-readable travel documents](https://www.icao.int/publications/pages/publication.aspx?docnum=9303): international specifications for machine-readable passports and identity documents
- [ICAO Annex 9: Facilitation](https://www.icao.int/facilitation-programmes/Annex9): international passenger, border, and document-control context
- [ICAO Annex 6: Operation of Aircraft](https://store.icao.int/en/annex-6-operation-of-aircraft): international aircraft-operation context, including mass and balance responsibilities
- [IATA Weight and Balance Manuals](https://www.iata.org/en/publications/manuals/weight-balance-manuals/): airline load-control procedures and data standards
- [Canadian Aviation Security Regulations, 2012](https://laws-lois.justice.gc.ca/eng/regulations/SOR-2011-318/index.html)
- [Secure Air Travel Regulations](https://laws-lois.justice.gc.ca/eng/regulations/SOR-2015-181/FullText.html)
- [Personal Information Protection and Electronic Documents Act](https://laws-lois.justice.gc.ca/eng/acts/P-8.6/index.html)
- [Accessible Transportation for Persons with Disabilities Regulations](https://laws-lois.justice.gc.ca/eng/regulations/SOR-2019-244/index.html)

