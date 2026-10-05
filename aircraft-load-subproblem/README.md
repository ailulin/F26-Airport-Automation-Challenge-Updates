# Aircraft Load Subproblem
## Table of Contents

- [Challenge](#challenge)
- [Potential Solutions](#potential-solutions)
- [Resources](#resources)

## The Problem
A mechanical issue causes the airline to replace the originally scheduled aircraft with a smaller aircraft shortly before departure. The new aircraft has different seating, baggage capacity and weight-and-balance-limits. 

Passengers have already checked in, seats have been assigned, and baggage is being prepared for loading. Because the new aircraft has less capacity and different loading constraints, the existing passenger and baggage plan can no longer be used directly. Staff must quickly determine how to recognize passengers, baggage and available capacity while avoiding unnecessary delays. 

Your challenge is to develop a solution that quickly adapts the existing passenger and baggage plan to the replacement aircraft while maintaining safety weight-and-balance limits and minimizing operational disruption. 

### Inputs and Expected Outputs

You'll likely be working with aircraft layouts, baggage records, scan events, document fields, and schedules. As it is difficult to find perfect datasets, some of it will be missing, late, or contradictory. Design for that instead of around it.

## Potential Solutions

A few possible scopes below. You can extend one or build something else entirely.

| Potential solution | Description | Starting point |
| --- | --- | --- |
| Aircraft load control | Assign passenger and cargo load to aircraft zones while respecting weight and balance limits. | [`load-control/`](load-control/) |
