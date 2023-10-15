# Notes on [SREcon EMEA Dublin 2023](https://www.usenix.org/conference/srecon23emea) 2023

## Key Takeaways

- MLOps: Focus on monitoring outputs and user impact.
- Monitoring/SLOs: Utilize histograms for better analysis.
- SLOs: Maintain a balance between reliability, on-call health, and productivity with SLOs.
- Automation as a Team Player:
  - Ensure automation processes are predictable and transparent.
  - Avoid creating surprises with automation and maintain simplicity.
- FinOps: Use tools like OpenCost/Kubecost to analyze and optimize cloud resource usage.
- Profiling: Utilize tools like Parca for continuous profiling and analysis.

## Favorite Quotes

> Looking at your average latency is like looking at the average temperature in the hospital.

> "Percentage availability" is for tourists.

> Instrument first, ask questions later.

> Try to build amplifiers and not prostheses.

## [Day 1](day1.md)

- Liz Rice's keynote highlighted the significance of eBPF technology.
- Symptom-based alerting for machine learning emphasized monitoring outputs, user impact, and input data distribution. Resources include a Google research paper and various metrics for monitoring ML systems.
- Reliability-enhancing procedures included steps such as service definition, SLOs, and operational response testing.
- Understanding QUIC vs HTTP/3 and its application mapping was also discussed, providing a GitHub resource for further exploration.
- Deploying and debugging HTTP/3 was briefly touched upon.

## [Day 2](day2.md)

- SRE principles applied to cybersecurity highlighted the importance of SLOs for security.
- The significance of distributed tracing and the importance of statistics for engineers were discussed. Resources included explanations on histograms and SLO measurement tools.
- Incidents as a means to enhance reliability investment were emphasized, focusing on mapping system capabilities and understanding user context.

## [Day 3](day3.md)

- Various talks covered topics such as OTel implementation, open-source observability, continuous profiling, Prometheus histograms, accountability engineering, and FinOps.
- The importance of automation being a good team player was stressed, citing the "Ironies of Automation" paper and the need to avoid creating surprises with automation.
