# Architecturally-significant requirement

An Architecturally-significant requirement (ASR) is a requirement that has a measurable effect on a software system’s architecture.

{% embed url="https://en.wikipedia.org/wiki/Architecturally_significant_requirements" %}

{% embed url="https://www.ozimmer.ch/practices/2020/09/24/ASRTestECSADecisions.html" %}

## Why?

> As a software engineer with architecture responsibilities, I want to prioritize technical issues quickly so that architecturally significant issues are addressed at their most responsible moment and we do not have to revise decisions and designs unnecessarily later. When doing so, I want to be as objective as possible to avoid that loud voices receive more attention than they deserve so that the truly urgent and important things are tackled first.
>
> [https://www.ozimmer.ch/practices/2020/09/24/ASRTestECSADecisions.html](https://www.ozimmer.ch/practices/2020/09/24/ASRTestECSADecisions.html)

## Seven Criteria for Architectural Significance

{% hint style="info" %}
The following Criteria is copied from Olaf Zimmermann (ZIO)'s article - [https://www.ozimmer.ch/practices/2020/09/24/ASRTestECSADecisions.html](https://www.ozimmer.ch/practices/2020/09/24/ASRTestECSADecisions.html)
{% endhint %}

1. The requirement is directly associated with high business value (benefit vs. cost) or business risk.
2. The requirement is a concern of a particularly important stakeholder such as the project sponsor or an external compliance auditor.
3. The requirement includes _runtime Quality-of-Service (QoS) characteristics_ (such as performance needs) that deviate from those already satisfied by the evolving architecture substantially.
4. The requirement causes new or deals with one or more existing _external dependencies_ that might have unpredictable, unreliable and/or uncontrollable behavior.
5. The requirement has a _cross-cutting_ nature and therefore affects multiple parts of the system and their interactions; it may even have _system-wide impact_, short term and/or in the long run (examples: security, monitoring).
6. The requirement has a _First-of-a-Kind_ (FOAK) character: For instance, this team has never built a component or subsystem that satisfies this particular requirement before.
7. The requirement has been _troublesome_ and caused critical situations, budget overruns or client dissatisfaction _on a previous project_ in a similar context.
