## Central metaphor: A restaurant launching a new dish

This one coherent scenario carries most of EBP v2.1's architecture.

---

### Door and Throne

A good restaurant has a **suggestion board** in the kitchen — any cook can pin up any dish idea, no form required, no committee needed, no justification. A sketch, a name, a vague concept. That's the **Door**: wide open, zero cost to enter.

But the **menu** is a different matter. To get onto the menu, a dish has to survive tasting sessions, costing, preparation-time checks, and consistency tests. The head chef is not kind here. The **Throne** is guarded. The suggestion board and the menu are intentionally different places with intentionally different rules.

**The failure mode this prevents:** If you apply menu-level scrutiny to the suggestion board, cooks stop suggesting. If you apply suggestion-board leniency to the menu, customers get inconsistent, untested food. EBP separates these deliberately.

---

### Three Lanes: Inbox → Workbench → Promoted

- **Inbox**: The sticky note on the suggestion board. "What if we did a miso-glazed pork belly?" Owner + claim. Nothing else required.
- **Workbench**: The test kitchen. Active debt work — someone is actually trying to make the dish, running into problems, iterating.
- **Promoted**: On the menu. All tests passed. Not declared *perfect*. Just cleared for service.

A dish can go back from Promoted to Workbench if a customer gets sick or the supplier changes an ingredient. **No shame. Just reality.**

---

### The Seven Principles, grounded

| Principle | Restaurant translation |
|---|---|
| Ideas enter free | Any cook can pin a dish idea, no approval needed |
| Debt does not kill | A failed test batch doesn't fire the cook |
| Debt is forever payable | You can revive an old idea from the board anytime |
| Promotion = current debt retired, not truth | On the menu = passed today's tests, not declared perfect forever |
| New evidence creates new debt | Customer allergy incident → dish goes back to testing |
| No final-truth claim | "Best dish in the world" can't go on the menu. "House signature pork belly" can |
| Accounting must never become the work | The paperwork serves the food. If the forms take longer than cooking, something is wrong |

---

## The six debt items — targeted analogies

Each one is a different kind of question a dish must answer before reaching the menu.

---

### needMap — the GPS route

A cook says: "I know a shortcut to the perfect texture — just trust me."

That's not a map. A **map** means: starting ingredient → specific technique → measurable outcome. If you can't show the path from A to B, you haven't claimed a shortcut — you've claimed a mystery.

**needMap fires whenever you say "X leads to Y" without showing the route.** Retire it by drawing the route explicitly: domain, codomain, translation rule. Even rough. Just draw it.

---

### needInvariant — the bridge test

A dish passes tasting on Tuesday with Chef A using summer tomatoes. Does it pass on Friday with Chef B using winter tomatoes?

A **bridge holds for any car**, not just the one used in the test. An **invariant** is whatever property must survive the crossing — same flavor profile, same texture window, same cost margin. If you can't state what's preserved across variations, you don't know if you have a dish or a lucky accident.

**needInvariant fires whenever you claim something survives translation.** Retire it by stating the invariant sharply enough that someone else can check it.

---

### needToyCheck — the small test batch

Before making 300 portions of a new dessert for a wedding, you make **one**. Then ten. Then thirty. You are not trying to prove the dish works at scale — you are trying to **kill bad structure early**, cheaply, before it reaches 300 disappointed guests.

If the small batch fails, you saved enormous waste. If it succeeds, you haven't proven scale — you've earned the right to try scale.

**needToyCheck fires when a map and invariant exist but no finite test has been run.** Toy success does not prove reality. Toy failure can kill bad structure before it costs anything.

---

### needNullModel — the placebo group

A restaurant adds a new "energy bowl" to the menu and sales go up. They conclude: the energy bowl is a hit.

But what if sales went up because they also renovated the dining room that month? Or because a competitor closed? **The null model is the control group** — what would have happened anyway, without your intervention?

In medicine this is obvious: a new pill must beat a sugar pill, not just beat nothing. In physics it's the same: a new theory must do something that the boring existing theory cannot.

**needNullModel fires whenever you claim uniqueness, necessity, or special explanatory power.** Retire it by supplying at least one null model — a simpler explanation you have to beat — or by explicitly disclaiming uniqueness. Both are valid. Honesty about "this is one of several possible explanations" is a legitimate retirement.

---

### needObstruction — the load-bearing wall

A homeowner wants to knock down a wall to open up the kitchen. Great idea. But before swinging the hammer, a contractor checks: **is this load-bearing?**

If it is, the plan is not necessarily dead — but it needs to change. Maybe you need a steel beam. Maybe the renovation is impossible without redesigning the whole floor. Either way, **you must check before you dig**.

Known blockers in physics are like structural codes in construction: chirality problems, anomaly cancellation requirements, Lorentz invariance recovery, Born rule derivation gaps. If any apply, you don't abandon the idea — you state the obstruction, whether it applies, and what the consequence is. Sometimes the consequence is downgrade. Sometimes it's "obstruction doesn't apply here." Both retire the debt.

**needObstruction fires when known blockers exist in the relevant domain.** Retire it by honestly engaging with at least one.

---

### needFaithfulnessReview — the legal contract

Two parties shake hands on a deal. A lawyer drafts the contract. Both sign. Six months later there's a dispute — not because either party acted in bad faith, but because **what the contract says and what both parties intended are not the same thing**.

The contract can be internally consistent — every clause follows from every other — and still fail to capture the actual agreement. **Internal consistency is not faithfulness.**

In EBP, Lean proofs have this exact problem. A formal result can follow rigorously from formal assumptions and still not capture the intended physical claim. needFaithfulnessReview asks: **does the formalization match the intended claim?** The answers are yes / no / contested. Contested blocks promotion but requires a stated reason. No silent vetoes.

**needFaithfulnessReview fires whenever a formal structure is being used to retire debt toward promotion.** Lean proves the math works. It does not prove nature agrees.

---

### The Living Ledger — wine vintages

A winery has a bad harvest year. The wine from that year is not great. They don't burn the vineyard. They label the vintage honestly, cellar what they have, note what went wrong, and **come back next year**.

An idea in EBP that accumulates an obstruction it can't currently answer goes dormant — not dead. The debt stays on the ledger. If someone later finds a way to answer the obstruction, the idea returns to the workbench. No expiration date. No shame in returning.

---

### Anti-bureaucracy — brainstorming vs. shipping

There is a difference between a **whiteboard session** and a **production release**. If you apply production-release checklists to a whiteboard session, nobody writes anything down. If you apply whiteboard-session casualness to a production release, things break.

EBP's anti-bureaucracy contract is the explicit rule that **accounting must never become the work**. The six debt items are retirement conditions, not entry taxes. A mandatory profile, a mandatory theory taxonomy, a mandatory Lean formalization at entry — these are the equivalent of requiring a full engineering spec before you're allowed to say "what if we tried this?" They kill the door by turning it into the throne.

---

### Next smallest useful move — eating the frog

Any large project stalls when the next step is too big to start. **Next smallest useful move** is the rule that every idea on the workbench always has one concrete action small enough to do today.

Not "solve the Born rule problem." That's not a move. "Write down what the Born rule problem actually is, in one sentence, so I know exactly what I'm facing" — that's a move. One sentence. Today. Then the next thing is visible.

---

## The whole picture in one sentence

EBP v2.1 is the rule that **the suggestion board is free, the menu is earned, the ledger never expires, and the paperwork must never eat the kitchen.**


## This maps remarkably cleanly. Software engineering has independently reinvented most of EBP v2.1's structure — just without the unified framework naming it. The goal here is to show each EBP component has a direct, already-practiced SE analogue, then show where SE currently leaves gaps that EBP fills.

---

## Central Architecture: The SDLC as EBP v2.1

Software development already has a Door and a Throne. Most of the discipline's process machinery is about managing the gap between them.

**Door** = any engineer, PM, or stakeholder can open a GitHub Issue or Jira ticket. No architecture review, no design doc, no committee. Claim + owner. Done. That is the entire cost of entry.

**Throne** = merge to `main` and deploy to production. Gated. Reviewed. Tested. The throne does not care about intent or enthusiasm. It cares about passing the gates.

The failure mode when these blur: orgs that require a five-page design doc before anyone can open a ticket have turned the suggestion board into the menu. Engineers stop suggesting. The other failure: orgs that merge to main like they're pinning sticky notes — production breaks constantly.

EBP names this distinction explicitly. Most SDLC processes enforce it implicitly but inconsistently.

---

## Three Lanes as Ticket States

| EBP Lane | Ticket Management | SDLC Phase |
|---|---|---|
| **Inbox** | Backlog (untriaged) | Discovery / Requirements |
| **Workbench** | In Progress / Active Sprint | Design → Implementation → QA |
| **Promoted** | Shipped to Production | Deployment / Release |

The living part: a ticket can go from Done back to In Progress when a production incident reopens it. EBP names this explicitly — promoted ideas can become unpromoted. Jira has the mechanics for it. Most teams treat it as an exception and feel vaguely ashamed. EBP says: **no shame, just reality**. New evidence creates new debt. Reopen the ticket.

---

## Seven Principles — SDLC Translation

**1. Ideas enter free.**
Anyone opens a GitHub Issue. No PR attached. No design doc. No approval. This is already the norm in healthy eng cultures. Where it breaks: teams that socially penalize "half-baked" issues. The door must have no bouncers.

**2. Debt does not kill.**
A failing CI run does not delete the branch. A rejected PR does not close the ticket. The idea is alive with debt — that's what `needs-work` labels are.

**3. Debt is forever payable.**
Tech debt tickets do not expire. An issue opened in 2019 is as valid today as when it was filed. The timestamp doesn't determine relevance — the debt retirement conditions do.

**4. Promotion = current debt retired, not truth.**
Merged to `main` and shipped to production means: it passed today's gates. It does not mean bug-free, optimal, or permanent. Every team knows this intellectually. EBP requires saying it explicitly so no one conflates "shipped" with "correct forever."

**5. New evidence creates new debt.**
A production incident, an observability alert, a customer report — these reopen debt on an already-shipped feature. The ticket comes back from Done. No architectural pride should resist this.

**6. No final-truth claim may be promoted.**
"This architecture will scale infinitely" cannot go into an ADR. "This architecture satisfies our current load requirements at 10x headroom" can. The difference is a checkable claim versus a blank check.

**7. Accounting must never become the work.**
If your Jira hygiene consumes more engineer-hours than your sprint work, the protocol has eaten the product. EBP's anti-bureaucracy contract is the explicit rule that every process must justify itself by the failure mode it prevents.

---

## The Six Debt Items — SE Analogies

---

### needMap — The API Contract That Wasn't Written

A backend engineer says: "the frontend just needs to call our service and it'll get the user data."

That is not a map. A map is an OpenAPI spec: endpoint, request schema, response schema, error codes, rate limits. Domain → codomain → translation rule. Without it, the frontend team builds against their assumption of what the response looks like. Two weeks later: a JSON key changed, both sides blame each other, and nobody has a written record of what was agreed.

**needMap fires whenever someone claims a connection between two systems without specifying the interface.** In SDLC terms: no ticket moves from Workbench to Promoted without an API contract, data flow diagram, or sequence diagram that explicitly shows the route.

Other SE examples:
- An ADR that says "we should move to event-driven architecture" without specifying the event schema, producer contracts, consumer guarantees, or failure modes. That's a claim without a map.
- A migration ticket that says "move from Postgres to DynamoDB" without specifying the data model translation. The map is the schema transformation — without it, you don't have a migration, you have a wish.
- A monolith-to-microservices decomposition ticket with no bounded context diagram. You've claimed a decomposition without drawing the cut.

---

### needInvariant — The Contract Test

A microservices system has fifteen services. Service A calls Service B. Service B ships a new version. Something breaks in Service A. Nobody noticed because Service B's test suite only tests Service B's internal behavior — it never asked: **what property must survive across versions?**

The invariant is the API contract. Contract testing (Pact, for example) is exactly needInvariant retirement: you state the property that must be preserved across the boundary — specific field names, types, response shapes — and you verify it survives every deployment.

**needInvariant fires whenever you claim something survives a transition.** In SDLC:

- **Database migrations**: what data integrity property must survive the schema change? Foreign key constraints, non-null guarantees, referential integrity. State it before the migration runs, not after data is corrupted.
- **Blue-green deployments**: the invariant is that both environments serve consistent data. What exactly does consistent mean here? Define it before cutover.
- **Refactoring tickets**: "no behavior change" is a claimed invariant. Retire it by specifying what behavior and running tests that would catch a violation. "No behavior change" without a test suite covering the behavior is an unfunded claim.
- **Feature flags**: rolling out 10% → 50% → 100%. The invariant is that user experience degrades no more than X% at each stage. State X before the rollout.

---

### needToyCheck — The Spike Ticket

Before committing two sprints to building a new search infrastructure, a team spins up Elasticsearch on a single node, indexes 1000 representative documents, and runs the ten most common query patterns against it. Not to prove it works at scale. **To kill bad structure cheaply before it costs two sprints.**

This is a spike. EBP calls it needToyCheck. The discipline is identical: finite, representative, designed to find failure early. Toy failure ends the investigation before sunk cost accumulates. Toy success earns the right to invest in the real implementation — it does not guarantee the real implementation works.

**needToyCheck fires when map and invariant exist but no finite test has been run.** In SDLC:

- **Performance claims**: "our new caching layer will reduce p99 latency by 40%" — run it on a load test with representative traffic before committing the architecture. The load test is the toy check.
- **ML model integration**: train on a 5% sample, evaluate on a held-out set, check the integration endpoint works end-to-end before full training run. Toy check on both the model and the plumbing.
- **Third-party API integration**: build a minimal client that calls the three endpoints you actually need, handle the actual error responses you get, before writing the full integration layer. Toy check on the API's actual behavior vs. documentation.
- **Algorithm selection**: implement bubble sort and quicksort on your actual dataset distribution before claiming quicksort is better for your use case. Toy check on the actual input characteristics.
- **Infrastructure**: `terraform plan` on a single-environment minimal deployment before touching prod. The plan output is the toy check for the infrastructure change.

The critical discipline from the source: **toy success does not prove reality. Toy failure can kill bad structure early.** Asymmetric value. Run the spike before the sprint, not as an afterthought.

---

### needNullModel — The A/B Test Baseline

An engineering team ships a new recommendation algorithm. Engagement goes up 8%. They declare success.

But traffic also went up 8% that month because of a marketing campaign. The null model — the control group, the old algorithm on equivalent traffic — was never measured. The 8% might be entirely explained by external factors. The new algorithm might have done nothing or even degraded experience on the subset that saw it.

**needNullModel fires whenever you claim superiority, necessity, or special explanatory power.** In SDLC:

- **A/B testing** is needNullModel built into deployment process. Null model = control variant. You must beat the control, not just show absolute improvement.
- **Feature flag rollouts**: the 1% cohort seeing the new feature is compared against the 99% baseline. The 99% is the null model. Without it you can't attribute causation.
- **Performance optimization PRs**: "reduced query time by 200ms" — compared to what? The same query on the same data with the same load? The baseline measurement is the null model. Without it, you've measured something but attributed it to nothing rigorous.
- **Architecture replacement proposals**: "moving to Kafka will solve our reliability problems" — what would solve reliability without Kafka? More robust retry logic on the existing queue? Better error handling? State at least one null model before claiming Kafka is necessary. This is explicitly an EBP-valid retirement: you can disclaim uniqueness rather than supply a null model, but you must do one or the other.
- **Incident post-mortems**: "the deploy caused the outage" — what's the null model? Was traffic already elevated before deploy? Was a third-party dependency degraded? The null model question is the difference between a root cause analysis and a scapegoating exercise.

---

### needObstruction — The Load-Bearing Constraint

Before a team builds a distributed feature that requires strong consistency across three services, the architect asks: **does the CAP theorem apply here, and what's the consequence?**

CAP theorem is a load-bearing wall. If the network partitions — and it will — you cannot have both consistency and availability. This is a known blocker in the relevant domain. You do not avoid asking the question because the answer might be uncomfortable. You ask it, state whether it applies, and redesign accordingly.

**needObstruction fires when known blockers exist in the relevant domain.** In SDLC:

- **Concurrency and race conditions**: a ticket proposes a feature that reads then writes a shared resource. needObstruction fires immediately — TOCTOU (time-of-check-to-time-of-use) is a known class of blocker here. State whether it applies. If it does: add a lock, use an atomic operation, or explicitly downgrade the feature's consistency guarantee.
- **Security review blockers**: a feature ships to Workbench. Security scan finds an injection vulnerability. That finding is a needObstruction item — it doesn't kill the ticket, but it blocks promotion. The ticket cannot reach Promoted until the obstruction is answered.
- **Browser compatibility**: a frontend feature uses a Web API not supported in Safari. That's a needObstruction item. State it, decide whether the feature degrades gracefully or is blocked, and document the consequence.
- **Third-party rate limits**: "we'll call the Stripe API per user action" — Stripe has rate limits. That's a known blocker. State it before the integration, not after hitting the 429.
- **Database schema constraints**: a migration requires dropping a column that turns out to have a foreign key dependency six layers deep. The dependency graph is a known obstruction class for migration tickets. State it before running `ALTER TABLE` on production.
- **Regulatory/compliance**: GDPR right-to-erasure requirement creates an obstruction for any feature that writes user data to immutable audit logs. Known blocker in the relevant domain. State whether it applies and what the consequence is — maybe you need a separate erasure layer.

The retirement pattern: state the obstruction, whether it applies, and the consequence. Sometimes the consequence is architectural downgrade — "this feature will be eventually consistent rather than strongly consistent." That's honest retirement. The feature isn't dead; it's honestly scoped.

---

### needFaithfulnessReview — The Spec That Drifted

A team writes an OpenAPI spec. A team writes tests against the spec. The tests pass. The spec passes linting. But three months ago during an urgent hotfix, an engineer changed the response payload shape without updating the spec. The spec now describes the old behavior. The tests cover the spec. The tests pass. **The system does not match the spec. The spec does not match the requirement. Nobody noticed.**

This is the faithfulness gap. Internal consistency — spec compiles, tests pass — does not imply faithfulness to the intended behavior. The two are independent questions.

**needFaithfulnessReview fires whenever a formal structure is used to retire debt.** In SDLC:

- **Type systems**: TypeScript compiles with no errors. The types are internally consistent. But the `UserProfile` type has a field marked non-optional that the business rule says is optional for free-tier users. The type system proves the code compiles. It does not prove the types match the business domain. That's a faithfulness gap.
- **Test coverage metrics**: 92% line coverage. Looks good. But the 92% covers implementation paths, not requirement branches. A critical edge case — what happens when a user has zero balance and attempts a transaction — is covered by lines that exist but the test doesn't assert the right output. Coverage metric passed. Faithfulness to the requirement: failed.
- **ADR approval**: an Architecture Decision Record is approved by the tech lead. The implementation ships. Six months later a new engineer reads the ADR and the code — they describe different systems. The ADR was faithful at merge time. Faithfulness drifted. needFaithfulnessReview means periodic checks: does the formal record still match the intended behavior?
- **Documentation**: the README says the service accepts ISO 8601 dates. The service actually accepts Unix timestamps after a refactor eight months ago. The documentation is internally consistent (no contradictions within itself). It is not faithful to the actual system.
- **Formal verification in critical systems**: you formally verify a protocol implementation in TLA+. The TLA+ model proves the protocol is deadlock-free. But the model omits network timeouts because they were "out of scope." The formal proof is correct for the model. The model is not faithful to the production environment. That gap is needFaithfulnessReview.

The resolution: yes / no / contested. Contested blocks promotion but requires a stated reason. No silent vetoes — if you believe a test suite doesn't faithfully cover a requirement, say so explicitly in the PR review, not as a vague "I'm not sure about this."

---

## The Living Ledger — The Backlog That Never Purges

A ticket opened in 2021 about a subtle memory leak in a rarely-used export feature. Triaged as low priority. Never fixed. Never closed.

Three years later a customer starts using the export feature heavily. The 2021 ticket is still there. It is not stale — it is **dormant**. The debt was always real. The attention was elsewhere. Now it's the most important ticket in the sprint.

**Dormant means inactive, not dead.** Closing old tickets to "clean up the backlog" is the anti-pattern EBP explicitly names. You are not cleaning debt — you are hiding it. The leak still exists. You've just removed the record that it was ever noticed.

The living ledger discipline: tickets only close when the debt is retired, not when the team gets tired of seeing them. Won't-fix is a valid closure — but it requires stating the decision and the rationale, not just archiving.

---

## Next Smallest Useful Move — Ticket Decomposition

An epic: "migrate authentication system from legacy JWT to OAuth2."

That is not a move. That is a destination. No engineer can start working on "migrate authentication system." They can start working on:

> "Document all current JWT validation paths in the codebase — find every callsite."

That is a move. One ticket. One afternoon. When it's done, the next move is visible: "identify which callsites can be migrated independently vs. which have dependencies."

**Every ticket on the workbench always has one next action small enough to do today.** This is the discipline behind story pointing, ticket decomposition, and definition of done. Where it fails: epics that stay as epics indefinitely because nobody has decomposed them into moves. The epic has debt — needMap for what the migration path looks like, needToyCheck for whether OAuth2 integrates with the existing session store — but the debt isn't being worked because the ticket is too large to start.

The EBP rule: **every idea always has one visible next move small enough to do now.** If a ticket is blocked, the move is: "state explicitly what is blocking it." That's a move.

---

## Anti-Bureaucracy — The Process That Ate the Sprint

A team adopts a new engineering excellence initiative. Every PR now requires:
- A Jira ticket linked
- An ADR if any infrastructure changes
- A design doc for any change over 50 lines
- A security review checklist
- A performance impact statement
- Sign-off from two senior engineers

Sprint velocity drops 60%. Engineers spend Friday afternoons filling out forms for changes that took thirty minutes to implement. The Monday retrospective discusses whether the forms are filled out correctly. Nobody ships anything.

**The ruthless test from EBP:** what failure mode does each process requirement prevent? Is that failure mode worse than the overhead the process creates?

- Linked Jira ticket: prevents orphan work with no context. Overhead: 30 seconds. Worth it.
- ADR for infrastructure changes: prevents undocumented architectural drift. Overhead: 20 minutes for significant changes. Worth it for significant changes. Not worth it for bumping a dependency version.
- Design doc for any change over 50 lines: prevents... what, exactly? A 55-line change to fix a null pointer dereference now requires a design doc. That failure mode is not real. The process is overhead with no corresponding protection.

The anti-bureaucracy contract applied to ticket management specifically: ticket hygiene must cost less than the cost of the problems it prevents. If sprint planning ceremonies consume more time than development, the ceremony has become the work.

---

## The Full Picture Across the SDLC

| SDLC Phase | EBP Component Active | Primary SE Analogue |
|---|---|---|
| Discovery | Door | GitHub Issue / Jira ticket creation — zero cost |
| Requirements | needMap, needNullModel | User story with acceptance criteria, A/B test baseline |
| Architecture/Design | needMap, needInvariant, needObstruction | ADR, API contract, CAP theorem / security constraints |
| Implementation | needToyCheck, needFaithfulnessReview | Spike, PoC, type system vs. business domain check |
| Testing/QA | needInvariant, needFaithfulnessReview | Contract tests, coverage vs. requirement alignment |
| Deployment | Throne, needObstruction | Merge gates, security scans, compliance blockers |
| Operations | New evidence creates new debt | Production incidents reopen closed tickets |
| Maintenance | Living ledger, dormant | Tech debt backlog that never expires |
| Retrospective | needFaithfulnessReview | Does the ADR still match what was actually built? |

The through-line: every SDLC gate is a Throne. Every suggestion, issue, or idea is a Door. The six debt items are the specific questions any artifact must answer before passing through a gate. The living ledger is the backlog with no expiration date. The anti-bureaucracy contract is the rule that the gates must justify their own existence or be removed.

EBP v2.1 doesn't add new process to software engineering. It names the process that good engineering teams already practice — and makes the gaps visible where they don't.


