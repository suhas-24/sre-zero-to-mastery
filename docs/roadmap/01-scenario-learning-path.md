# The experience path

This is a proposed authoring map, not a list of completed episodes. The numbered curriculum remains the coverage catalog. Episodes introduce supporting concepts locally, so no prerequisite course is required to enter one.

| Situation | Concepts introduced when needed | Assumption to challenge |
|---|---|---|
| You tap a button and nothing happens | Client, request, server, response, user outcome, reliability | A running computer means the action worked |
| The same page is fast for one person and slow for another | Measurement, latency, distribution, percentile, network path | The average describes every user |
| The request never reaches the app | Names, DNS, addresses, connection, TLS, proxy, routing | No application errors means no failure |
| More people arrive and the wait grows | Capacity, queue, concurrency, bottleneck, resource use | More work always produces more useful throughput |
| You try again and get two results | Timeout, ambiguous outcome, idempotency, transaction, deduplication | A missing reply means nothing happened |
| Two people see different versions of the same data | Cache, replica, consistency, propagation delay | Every copy changes at the same moment |
| The dashboard looks healthy while customers complain | Indicators, eligibility, measurement boundary, missing data, logs and traces | A green dashboard proves success |
| You must decide when to wake someone | Error rate, window, objective, budget, alert, escalation | Every error needs a page |
| A new release breaks only some requests | Artifact, deployment, canary, comparison group, rollback, schema compatibility | A health check validates the whole release |
| One slow dependency affects the whole service | Deadline, connection pool, retry, jitter, backpressure, isolation | Repeating requests always improves reliability |
| The application disappears during a busy period | Process, memory, limits, container, scheduling, probes | Restarting explains or fixes the cause |
| New copies are running but capacity has not improved | Replicas, load balancing, HPA, readiness, resource requests | Replica count equals useful capacity |
| Background work falls behind | Producer, consumer, acknowledgment, lag, ordering, poison message | An empty request queue means all work is complete |
| Recovery restores service but the data is wrong | Backup, restore, integrity, RPO, RTO, reconciliation | A successful backup job proves recoverability |
| A whole location becomes unavailable | Failure domain, zone, region, failover, quorum, shared dependency | A second location guarantees independence |
| A certificate or credential stops working | Identity, authentication, authorization, expiry, rotation, trust | Security configuration is separate from availability |
| The same manual task consumes every week | Toil, automation, safe retries, dry run, verification, ownership | A script that ran successfully achieved the intended outcome |
| A platform change affects many teams | Infrastructure as code, drift, shared platform, policy, blast radius | Centralizing work automatically reduces risk |
| The service works but costs grow unexpectedly | Unit cost, telemetry volume, cardinality, storage, egress, headroom | Lower cost and higher reliability are always aligned |
| An AI assistant recommends a repair | Evidence, tool access, uncertain output, evaluation, approval boundaries | A plausible explanation proves a cause |
| The team recovers and must decide what to improve | Incident roles, timeline, causal evidence, postmortem, prioritization | One root-cause label captures the whole failure |

## Coverage obligations

Every original topic and every accepted extension must map to one or more episodes and reference sections. An episode may introduce an idea without completing the topic. Record that distinction rather than treating a mention as coverage.

Suggested coverage fields: topic/subtopic, first explanation, deeper revisit, failure cases, diagram/model, exercise, primary sources, review status, lab execution status, known gaps.

Use truthful status labels: planned, drafted, reviewed, lab-verified where a runnable lab exists. Publishing a roadmap does not make its topics complete.

## Recommended progression without gates

Start with the customer action and reveal the system as questions arise. Revisit earlier ideas in new situations. Let learners enter through a symptom or topic lookup and provide short local explanations of everything needed there.

Preserve optional reference paths for readers who want a focused Linux, networking, database or Kubernetes deep dive. These paths are additional ways to explore the resource, not entrance requirements.
