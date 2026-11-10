# Research Questions

## PCC (Population, Concept, Context) Mapping

This review uses the PCC framework, which is appropriate for
methodological/architectural reviews where the aim is to map and synthesize
practice rather than compare interventions.

| Element | Specification |
|---|---|
| **Population (P)** | Software systems originally implemented using a microservices architecture that have undergone a documented process of consolidation into a modular monolith, macro-services, or similar post-microservices architecture |
| **Concept (C)** | The consolidation process itself: drivers, decision frameworks, migration strategies, architectural refactorings, tooling support, and reported outcomes |
| **Context (C)** | Industrial software systems and/or open-source projects, across any application domain; any organization size; any language/runtime stack |

## Research Questions

**RQ1.** What data consistency patterns are reported in microservices architectures, and what consistency guarantees do they provide?

**RQ2.** What technical, organizational, and economic factors influence the selection of data consistency patterns in microservices?

**RQ3.** How are these patterns evaluated, and what benefits, limitations, and trade-offs are reported regarding consistency, performance, availability, scalability, and operational complexity?

**RQ4.** What open challenges and research gaps are reported in implementing and evaluating data consistency patterns in microservices?

## Justification of question framework choice

PCC (rather than PICO) is used because this is a mapping-type review of
architectural practice rather than an intervention-effectiveness review.
Primary studies describe consolidation experiences and do not randomize
architectural choices across comparable populations. This follows PRISMA
2020 item 4, which permits alternative frameworks where appropriate.
