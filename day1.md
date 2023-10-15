# Day 1

## Keynote: eBPF

Liz Rice. Why eBPF matters for SREs.

## Symptom-based Alerting for Machine Learning

> What I Learned from Monitoring More than 30 Machine Learning Use Cases

- Backend monitoring -> focus on symptoms, ie. user pains, not causes
- ML Monitoring
  - ML Test Score Paper: https://research.google/pubs/pub46555/
  - silent failures -> bigger value impact than most model improvements
    - input data changes
    - aggressive post-processing filters applied
    - bugs in own code
    - dependencies not pinned (ie. tensorflow)
  - What to alert on
    - Prio 1: monitor outputs and user impact
      - Fraud prediction: Let through some fraudsters to evaluate model impact
    - Prio 2: service response distribution
      - rule based distance metrics: median, quantiles, share of empty/insufficient outputs
      - statistical distance metrics: kolmorogov-smirnov, d1 distance, population stability index
      - response heuristic quality metrics
    - Prio 3: input and feature data distribution
      - same metrics as prio 2
  - Do I need a tool for MLOps monitoring?
    - What are your requirements
    - Who is addressing these alerts
    - Clear data ownership and how to prioritize data issues

## Reliability Enhancing Procedures

- 1 Model Service Definition
- 2 Service Availability Requirements & Reliability Design
- 3 Service Roasting -> https://www.usenix.org/conference/srecon16europe/program/presentation/welch
  - Phase 1: Get the big picture; add lenses on the big picture -> common understanding
  - Phase 2: Roast it. For every line and every box -> what can go wrong? What is the blast radius for each error and the probability. -> Risk map
  - Phase 3: Reliability Backlog & Ready for SLO & Transparency
- 4 Provide Service Specification & Usage Instruction
- 5 SLOs
- 6 Service Continuity / Disaster Recovery Plan (RPO, RTO)
- 8 Resilience Testing in Production
- 9 Operation Response Testing

## QUIC vs HTTP/3 Application Mapping vs Protocol Encapsulation

- https://www.youtube.com/watch?v=bR86qiPOH7s
- Follow along: https://github.com/LPardue/sreconemea2023

## Deploying and Debugging HTTP/3

- Interesting, but little applicability for my context.
