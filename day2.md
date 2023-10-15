# Day 2

## SRE for (cyber)security

Try apply SRE principles to security.

SLO for security:

- Availability
- Expected behavior changes in access logs etc.

## Tracing the Journey into Distributed Tracing

- Solve a problem, or find an opportunity
- Run a PoC phase to answer 2 questions:
  - Does this techno solve my problem?
  - What is the best tool?
- Define a rollout plan covering education, broad usage, collecting benefits
  - Educate your engineers on the technology so that they look at it with confidence, instead of distrust
  - Promote the technology to achieve broad adoption
  - Change/create processes to achieve your original goals
- Find a sponsor for the rollout.
- The more disruptive a technology is, the more detractors.
- Focus the rollout on adding value.

## Statistics for Engineers

- Charts typically show the mean aggregate
- Looking at your average latency is like looking at the average temperature in the hospital
- Histograms
  - https://opentelemetry.io/docs/specs/otel/metrics/data-model/#exponentialhistogram
  - https://www.youtube.com/watch?v=W2_TpDcess8
  - Percentiles can't be aggregated -> need histograms
- SLOs
  - Availability SLIs:
    - Start: Probe
    - Ok: Server metrics
    - Best: User metrics
  - SRE Triangle:
    - Reliability
    - On-Call health
    - Productivity
    - SLOs are a tool to balance these 3
  - 9 scale: -Log10(1-SLI)
  - Traffic light:
    - Green Error Budget: >20%
      - No investment in reliability needed.
    - Amber Error Budget: 0%...20%
      - Reliability needs attention. Increase testing efforts.
    - Red Error Budget: <0%
      - Investments in reliability need. Stop deployments.
  - Measure total burn rate: See in each minute how much did this minute burn of the error budget
- Sampling: https://heinrichhartmann.com/sampling/

## Lunch

https://r9y.dev/

## Embracing the Multi-Party Dilemma: Incident Response Across Company Boundaries

- Multi-Party Dilemma: Pattern that describes challenges at org boundaries between independent parties
  - Includes characteristics such as asymmetry, higher cost of coordination
- Recurring themes are indicators of durable features of the organization
- The dilemma was discovered by incident analysis as a theme
- Challenges and key findings
  - legal, financial and pricy concerns place barriers to **preparing to have incidents**
  - organizational boundaries expose hidden **transitive dependencies**
  - **coordination costs** increase when working across organizational boundaries
  - **mission alignment** can lead to working at cross purposes (ie. vendor wants to analyze longer and client wants to move on)
  - information sharing is key
  - recruit expertise during incident
  - awareness of friction in the system
- A **transient incident response** occurs across boundaries and bureaucracy disappear
- Dent ask why someone did something, but ask how this would have made sense for them to do in their situation.
- Ideas:
  - tracing is helpful
  - partnerships formed in advance helps shared ways of working
  - discussions both before and after incidents
  - identify existing information networks of expertise and cultivate new ones
  - can the vendor share their screen
  - can one of the experts attend a design review
  - can we shadow a support engineer for a day
  - can we invite them to our retros, design reviews, sprint planning
  - can we reveal the vendor versions in production, architectural diagrams, etc.

## The Incident Is The Way: Using Your Incidents to Win Reliability Investment

1. Map your system capabilities
   - Personal take: Group by domain
   - Percentage availability is for tourists
   - Allows to identify impacts when a service has an issue
   - Organizing around microservices is problematic because:
     - Your users are rarely using a single microservice
     - The component with an issue is not necessarily the cause
2. Bring your org in
   - No user facing incident is an engineering-only concern
   - include based on relevance not necessity
   - wider sharing of user reality
3. Agree on a definition of harm
   - Everything is the highest severity to someone
   - prefer correctness over availability
   - user context above all
   - an objective ladder of harm
4. Choose consequence over intention
   - intention and consequence don't correlate in software
   - intention is grounded in empathy for our organization
   - consequence is grounded in empathy for our users

## You depend on DNS, This is how it works and you won't believe it

Fun talk.

## 9 things you should to to get started with SLO

- Measure user journeys
- Look back to look forward
- Observability without action is just storage
- Different time windows for different folks
- Enrich dashboards with contextual information
- Document your SLOs

Cool link:

- https://www.slodlc.com

## GDPR - What if it was real?

- Recent or upcoming regulations:
  - Collective Redress - 2023
  - Digital Services Act - 2023
  - Digital Markets - 2024/03/04
  - ePrivacy - Mid 2024
  - Data Act - Mid 2025

## Lighting talks

- Status Page: Rootly
- Skip 3 pillars of observability and look at 3 phases
  - Phase 1: **Know** something is happening as fast as possible
  - Phase 2: **Triage** specific information
  - Phase 3: **Understand** to ensure never happens again
- Use quality gates in production
- Components of incidents
  - Processes
  - People
  - Artifacts
  - Processes
