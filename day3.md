# Day 3

## Should I Use OTel (collectors), or Is Prometheus Good Enough?

- Always articulate which OTel you mean
- OTel is not a silver bullet. Pay attention trade off
- Don't reinvent the wheel

## Implementing Open-source Observability within Maersk

- o11y platform with Grafana open source services
- Read proxy (wizard):
  - Validates the queries and checks for best practices (prevent bad queries bringing down the system)
  - Enforces metric name in query
  - Checks if label selector is present
- Write proxy (guard):
  - Checks the written telemetry.
    - Require `env` label
  - Retention control
  - Usage tracking
  - cardinality tracking
  - traffic routing
  - metrics on what is being dropped

## Journey from Fluent Bit, Fluentd and Prometheus to OpenTelemetry Collector - Lessons Learned

- Metadata API in k8s? Need to check this further.
- Collector for Logs:
  - Pretty much okay to use.
- If you are brave enough, you can use the collector for metrics, logs, traces and metadata.

## Continuous Profiling in the Cloud-Native era

- SLO & Prometheus: https://github.com/pyrra-dev/pyrra
- Continuous Profiling: https://www.parca.dev/
- Videos: https://www.youtube.com/@PolarSignalsIO/streams
- Cross-language development platform for in-memory analytics: https://arrow.apache.org/

## How to Use Prometheus's Native Histograms

- Instrument first, ask questions later
- New param:
  - `NativeHistogramBucketFactor`, ex. `1.1` means buckets grow 10% from the previous bucket
- Still experimental behind a flag.
- Progress: https://github.com/prometheus/prometheus/milestone/10

## A Dual Approach to Accountability Engineering

- 100% match of FAIRTIQ's strategy
- Framework for Accountability in Engineering
- Don't model, focus project and goals.
- Give recognition

## Should an SRE Care About FinOps? Using Observability to Enable Resources Optimization

- FinOps teams are a thing
  - Promote interactions among teams
  - Central optimization
- Kubecost https://www.kubecost.com/
  - https://docs.kubecost.com/
- Everyone should care. Not only SRE / DevOps
- Case study: 35% savings with applying FinOps (spend $1.7M)
- Quote: You build it, you run it, you pay it
- Reference: https://www.oreilly.com/library/view/cloud-finops/9781492054610/
- KubeCost is not free: Open version https://www.opencost.io/

## Looking at SRE Needs and Trends over Two Decades with a Single Service (Google Chubby)

## How to Make Your Automation a Better Team Player

- Paper worth reading: Ironies of automation, Lisanne Bainbridge
- Patterns to avoid:
  - Don't create surprises with automation: "Why did it do that??"
    - Automation processes don't behave as intended
    - Human triggered processes that do things the user didn't want
    - Avoid scattered autonomous processing
      - Out of sight and out of mind is bad
      - Run as a service, status pages, alerting
      - Predictable and as simple as possible
      - Avoid modes and other complexity
      - Example: Unattended upgrades
      - Clearly display intended actions
  - Don't make strong recommendations that aren't warranted
    - https://snafucatchers.github.io/
    - Try to build amplifiers and not prostheses
    - Amplifiers:
      - Summarize to avoid overwhelming operators
      - Provide ability to drill down and explore all the details (including exact times)
      - Try to expose how things really work
- Question to Ask: How does this system help the operator to build an accurate mental model of how the system works?
