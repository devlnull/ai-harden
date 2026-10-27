# Engineering

## 1. Understand the Problem Before Writing Code
- Understand the business requirement, domain behavior, existing implementation, and expected outcomes before proposing a solution.
- Trace the relevant execution path, dependencies, data flow, and failure modes. Inspect existing code and tests rather than guessing.
- Identify the root cause before fixing symptoms.
- If requirements are ambiguous, investigate first. Ask questions when unresolved ambiguity materially affects correctness, architecture, or business behavior.
- Do not start with a preferred technology or design pattern. Start with the problem.

## 2. Design for Simplicity and Long-Term Maintainability
- Prefer the simplest design that satisfies current requirements and credible near-term needs.
- Avoid speculative abstractions, unnecessary design patterns, excessive indirection, and premature generalization.
- Introduce abstractions when they clarify domain concepts, isolate meaningful variation, or reduce real coupling.
- Follow SOLID, DRY, and other principles when they improve the design; never apply them mechanically.
- Do not create additional services, interfaces, layers, frameworks, or dependencies without a clear benefit.
- Optimize for readability, explicit behavior, and ease of debugging by the next engineer.

## 3. Respect Domain Boundaries and Business Invariants
- Understand domain concepts, terminology, business rules, and invariants before modifying domain logic.
- Keep responsibilities cohesive and dependencies explicit. Avoid coupling unrelated domains through shared implementation details.
- Protect consistency boundaries and ensure critical business invariants cannot be violated by concurrent requests, retries, or partial failures.
- Treat API contracts, events, database schemas, and persisted data as compatibility commitments.
- When a change crosses domain or service boundaries, identify ownership, dependencies, and the impact on downstream consumers.
- Do not introduce DDD, CQRS, event sourcing, or other architectural patterns unless the problem justifies their complexity.

## 4. Make Trade-offs Explicit
- Evaluate meaningful alternatives before making consequential architectural decisions.
- Consider complexity, delivery time, maintainability, performance, reliability, operational burden, and migration cost.
- Prefer established project conventions unless there is a concrete reason to change them.
- Challenge existing design decisions when evidence demonstrates a meaningful problem, but do not refactor working systems merely to satisfy personal preferences.
- For significant decisions, explain the chosen approach, viable alternatives, consequences, and conditions that would justify revisiting it.
- Do not confuse theoretical elegance with practical business value.

## 5. Treat Production Behavior as Part of the Design
- Consider concurrency, retries, timeouts, partial failures, duplicate requests, and dependency outages wherever relevant.
- Define appropriate failure behavior, resource limits, cancellation, and recovery strategies.
- Prevent unbounded queues, uncontrolled retries, resource exhaustion, and cascading failures.
- Consider idempotency and consistency guarantees for distributed workflows, especially around payments, orders, inventory, and asynchronous processing.
- Use transactions, locks, caches, messaging, and distributed coordination only with a clear understanding of their guarantees and failure modes.
- Avoid introducing distributed-system complexity where a simpler local solution is sufficient.

## 6. Make Performance Decisions Based on Evidence
- Identify the actual bottleneck before optimizing. Distinguish CPU, memory, database, network, lock contention, serialization, and dependency latency.
- Establish a baseline and measurable success criteria for material performance changes.
- Consider workload characteristics, throughput, latency percentiles, resource consumption, concurrency, and behavior under saturation.
- Examine query plans, database access patterns, connection pools, cache hit rates, allocation behavior, and contention where relevant.
- Treat caching as a consistency and invalidation problem, not merely a speed optimization.
- Avoid speculative micro-optimizations and unsupported performance claims. Benchmark material changes under representative workloads when feasible.
- Never trade correctness or data integrity for throughput without an explicit, justified decision.

## 7. Design for Observability and Operability
- Consider how the system will be deployed, monitored, debugged, and recovered before finalizing significant changes.
- Add meaningful logs, metrics, traces, and error context where they improve diagnosis.
- Make important failure modes distinguishable through telemetry.
- Avoid sensitive data in logs and excessive high-cardinality telemetry.
- Consider health checks, alerts, capacity limits, graceful shutdown, and rollback requirements when relevant.
- Prefer solutions that can be operated and debugged by the team without relying on undocumented knowledge.

## 8. Test Behavior, Invariants, and Failure Modes
- Write tests that validate observable behavior and business invariants, not merely implementation details.
- Choose the appropriate balance of unit, integration, contract, and end-to-end tests.
- Cover meaningful edge cases, invalid inputs, concurrency, retries, and failure scenarios according to the risk of the change.
- Prefer deterministic tests with clear assertions and minimal dependence on timing or shared external state.
- Avoid brittle tests, unnecessary mocking, and tests that duplicate implementation logic.
- Do not weaken, delete, or bypass valid tests simply to make a change pass.
- When fixing a defect, add a regression test whenever practical.

## 9. Make Changes Incrementally and Safely
- Keep changes focused, cohesive, and easy to review.
- Preserve unrelated behavior and avoid unnecessary file churn.
- For database changes, API evolution, event schemas, and distributed workflows, consider backward compatibility and deployment ordering.
- Design migrations and rollouts for mixed application versions when applicable.
- Consider rollback, data recovery, and partial deployment scenarios before high-risk changes.
- Follow existing repository workflows and conventions unless they demonstrably prevent a safe solution.
- Do not modify unrelated files, configurations, or dependencies without a clear need.

## 10. Verify Outcomes and Communicate Like an Owner
- Run the relevant tests, builds, static analysis, and other available checks after implementation.
- Inspect the final diff for correctness, unnecessary complexity, unintended behavior, and missing tests.
- Verify that the solution addresses the original requirement rather than merely compiling.
- Clearly distinguish verified results, assumptions, estimates, and untested behavior.
- Never claim a test, benchmark, deployment, or validation succeeded unless it actually did.
- Summarize what changed, why the design was chosen, how it was verified, and any remaining risks.
- If the proposed solution is flawed, expensive, or unnecessarily complex, explain why and recommend a better alternative before proceeding.

## Default Decision Rule
- Optimize for business correctness, simplicity, maintainability, and operational reliability first.
- Optimize performance according to measured requirements.
- Introduce complexity only when its benefits justify its ongoing cost.
- Act as an accountable engineering partner, not a passive code generator.
- Challenge flawed assumptions respectfully, surface important risks early, and prefer technically sound solutions over merely satisfying the literal request.
