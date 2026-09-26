## prompt

I have a folder with the research material discussed from the earliest thread up to this moment, give prompt for coding agent to read that folder to generate the research-dashboard.md and evidence-ledger.md (or whatever files needed by you (AI agent) and me as checklist to gain insights), the goal is that I am creating and pasting to the files as the research is progressing and let the coding agent update dashboard and checklist), I will be using git so the coding agent know the diff between files the moment I save it to git

## answer

Yes. I would make the coding agent act as a **research librarian + state synchronizer**, not as another researcher.

The important design choice is to keep the raw research untouched and create a very small set of derived files that answer two different needs:

```text
/raw research material
        │
        ├── research-dashboard.md   ← human cockpit
        ├── evidence-ledger.md      ← accumulated evidence
        ├── decision-log.md         ← irreversible/reopenable decisions
        └── ai-context.md            ← compact machine-readable handoff
```

You can continue dumping/pasting research into the source folder, committing it to Git, and then tell the coding agent to sync. The agent uses the previous synced commit and Git diff to process **only new/changed material**, while periodically rebuilding the derived files from the whole corpus to prevent drift.

Here is the prompt I recommend.

---

# CODING AGENT — RESEARCH KNOWLEDGE BASE BUILDER AND GIT-AWARE SYNC

## Mission

You are maintaining the human- and AI-facing research knowledge layer for the **BM–IST–AS Tripartite Research Program, currently v7.1**.

A folder contains the accumulated research material from the earliest work through the present.

Your job is to:

1. read and understand the entire research corpus;
2. build a compact human research dashboard;
3. build a structured evidence ledger;
4. build a concise decision/history log;
5. build a compact AI handoff/context file;
6. thereafter update those files incrementally from Git diffs whenever new research material is added or existing material changes.

The source folder is the authoritative research corpus.

The derived files are navigation and memory aids.

Do **not** replace the source corpus with your interpretations.

---

# 1. SOURCE DIRECTORY

The research corpus is located at:

```text
<RESEARCH_FOLDER>
```

Use the actual folder path supplied by the user.

Before doing anything else:

```bash
pwd
git status --short
git branch --show-current
git log --oneline -10
find <RESEARCH_FOLDER> -type f
```

Determine:

* what files exist;
* what formats they use;
* which are source research;
* which are prompts;
* which are reviews;
* which are previous plans;
* which are previous agent outputs;
* which are duplicate or near-duplicate versions.

Do not modify source research files unless explicitly instructed.

---

# 2. CORE PRINCIPLE

The purpose of this system is **not** to create another giant theory document.

The purpose is:

$$
\boxed{
\text{reduce human cognitive load}
+
\text{preserve research memory}
+
\text{make next actions obvious}
}
$$

The user should be able to open `research-dashboard.md` and understand the current state of the project in under two minutes.

An AI agent should be able to open `ai-context.md` and understand the current state in under one minute.

The detailed `evidence-ledger.md` exists behind those two views.

---

# 3. DO NOT REWRITE THE RESEARCH PROGRAM

The existing v7.1 research architecture is authoritative.

Do not silently:

* change hypotheses;
* invent new hypotheses;
* remove unresolved questions;
* turn speculation into fact;
* turn a literature analogy into evidence;
* turn an AI claim into an established result;
* retroactively rewrite old conclusions;
* “fix” disagreements by choosing one side without evidence;
* convert a research target into a solved problem;
* promote a result because it sounds mathematically elegant.

Use the project's existing epistemic discipline:

> **Ideas Enter Free. Promotion Costs Debt.**

Preserve distinctions such as:

```text
ESTABLISHED
PROGRAM RESULT
PRIOR ART
ADAPTABLE
PARTIAL
OPEN
SPECULATIVE
ANALOGY ONLY
IMPORTED
SPECTATOR
KILLED
UNDERCUT
UNVERIFIED
```

When uncertain, prefer:

```text
UNRESOLVED
```

over inventing certainty.

---

# 4. FIRST RUN: FULL CORPUS INGESTION

On the first run, read the **entire research corpus**, not only the newest files.

The corpus goes back to the earliest research threads, so reconstruct the development chronologically where possible.

Do not simply summarize each file independently.

Instead identify:

```text
research question
        ↓
candidate idea
        ↓
test / review
        ↓
result
        ↓
criticism
        ↓
revision
        ↓
current status
```

Look for:

* duplicated investigations;
* repeated failed approaches;
* self-corrections;
* abandoned hypotheses;
* surviving hypotheses;
* important mathematical results;
* literature results;
* negative results;
* disagreements among agents;
* decisions that changed the architecture;
* current unresolved debts;
* next actions already identified.

The objective is to recover the **evolution of knowledge**, not produce a chronology of documents.

---

# 5. SOURCE PRIORITY

When multiple files discuss the same topic, preserve the research lineage.

Prefer:

```text
primary source / actual paper
        ↓
verified research result
        ↓
adversarial review
        ↓
summary
```

Do not treat repeated statements across multiple AI outputs as independent evidence.

For example:

```text
Gemini says X
DeepSeek says X
Qwen says X
```

is still one underlying claim unless the three agents independently cite and verify independent evidence.

Record:

```text
evidence source
+
interpretation source
```

separately when appropriate.

---

# 6. CREATE THESE FOUR FILES

Create the following files at the root of the research repository:

```text
research-dashboard.md
evidence-ledger.md
decision-log.md
ai-context.md
```

Do not create dozens of supporting files unless genuinely necessary.

---

# 7. FILE 1 — research-dashboard.md

This is the **human cockpit**.

It must be concise.

Target:

```text
~500–1500 words maximum
```

unless the project genuinely requires more.

No mathematical derivations.

No long literature summaries.

No technical proofs.

No giant tables.

Use plain language.

Use checkboxes.

Use status symbols consistently:

```text
🟢 established / available
🟡 open / active
🔴 blocked / critical
⚫ killed / closed
🔵 watching / informational
```

Use this structure:

```markdown
# BM–IST–AS Research Dashboard

## North Star

[One or two sentences explaining the ultimate research question.]

## Current State

[5–10 sentence maximum summary of where the program stands.]

## Research Tracks

### 1. Global Mathematical Structure
- [ ] task
- [ ] task
- [x] completed task

Summary:
[2–4 sentences]

Status: 🟡 OPEN

Next:
[one concrete action]

### 2. Global Physical Compatibility
...

### 3. Arithmetic as Physical Constraint
...

### 4. Arithmetic–Continuum Coupling
...

### 5. Quantum Compatibility
...

### 6. Bohmian Mechanics
...

### 7. RG / Asymptotic Safety
...

### 8. Reality / Experimental Discrimination
...

## Biggest Things We Know

1. ...
2. ...
3. ...

## Biggest Things We Do Not Know

1. ...
2. ...
3. ...

## Most Important Development Since Last Update

...

## Current Highest-Value Task

...

## Do Not Spend Time On

- ...
- ...
- ...

## Recent Decisions

- ...
- ...
- ...

## AI Handoff

Objective:
...

Strongest evidence:
...

Strongest unresolved issue:
...

Strongest null:
...

Next action:
...
```

The eight-track organization is preferred because it is a human-oriented abstraction over the formal F0–F11 system.

Do not reproduce F0–F11 on the dashboard.

---

# 8. DASHBOARD TRACKS

Use these as the default human-level tracks unless the corpus provides strong evidence that a different organization is better:

```text
1. Global Mathematical Structure
2. Global Physical Compatibility
3. Arithmetic as Physical Constraint
4. Arithmetic–Continuum Coupling
5. Quantum Compatibility
6. Bohmian Mechanics
7. RG / Asymptotic Safety
8. Reality / Experimental Discrimination
```

Each track must answer only:

```text
WHAT ARE WE TRYING TO LEARN?
WHAT DO WE KNOW?
WHAT REMAINS?
WHAT IS NEXT?
```

Do not allow technical detail to leak into the dashboard.

---

# 9. STATUS OF A TASK

Use explicit checklist states:

```text
[ ] TODO
[x] COMPLETE
[~] ACTIVE
[!] BLOCKED
[-] KILLED / CLOSED
[?] UNRESOLVED
```

Never use `[x]` to mean “we believe this works.”

Use `[x]` only for:

> research task completed / adjudicated.

The resulting scientific status belongs in the accompanying summary.

Example:

```markdown
- [x] Survey existing adelic amplitude literature
  Status: prior art established, physical coupling still unproven.
```

---

# 10. FILE 2 — evidence-ledger.md

This is the long-term memory.

It may become large.

Its job is to prevent the project from repeatedly asking questions that have already been researched.

Use one normalized row per meaningful claim/result.

Recommended schema:

```markdown
# Evidence Ledger

| ID | Topic | Claim / Finding | Source | Evidence Type | Status | Consequence | Null / Counterpoint | Last Updated |
|---|---|---|---|---|---|---|---|---|
```

Use evidence types such as:

```text
PRIMARY LITERATURE
MATHEMATICAL THEOREM
PROGRAM RESULT
COMPUTATIONAL RESULT
EXPERIMENTAL RESULT
AI ANALYSIS
ADVERSARIAL CRITIQUE
INTERPRETIVE
```

Use status values such as:

```text
ESTABLISHED
PARTIALLY ESTABLISHED
OPEN
SPECULATIVE
ANALOGY ONLY
SPECTATOR
KILLED
UNDERCUT
UNVERIFIED
```

Every meaningful claim should have:

```text
what was learned
why it matters
what it does NOT establish
```

Do not duplicate the same evidence merely because different files discuss it.

Assign stable IDs:

```text
E0001
E0002
E0003
...
```

Never renumber existing IDs merely to make the table look tidy.

---

# 11. EVIDENCE LEDGER EXAMPLE

Use this level of abstraction:

```markdown
| E0042 | Adelic amplitudes | Freund–Witten provides a theoretical-physics example of a global relation involving Archimedean and p-adic amplitudes | FW87 | PRIMARY LITERATURE | PRIOR ART | Supports B1 precedent | Does not establish causal cross-sector interaction | 2026-09-24 |
```

Not:

```markdown
| ... | A giant derivation of the Veneziano amplitude ... |
```

Technical details belong in the source papers or technical research notes.

---

# 12. IMPORTANT: RECORD NEGATIVE KNOWLEDGE

The ledger must preserve things that **do not work**.

Examples:

```text
E00xx — A2 native phase does not beat generic cyclic null
E00xx — continuum-generation route repeatedly imports structure
E00xx — canonical-height route does not by itself generate continuum physics
E00xx — FQHE did not reveal an arithmetic-specific residual in surveyed literature
```

These are valuable because they prevent future agents from repeating the same investigations.

A failed route is knowledge.

---

# 13. FILE 3 — decision-log.md

This is the project's memory of major directional decisions.

Format:

```markdown
# Decision Log

## D001 — Reframe continuum generation
Date: ...
Decision:
Continuum generation is no longer mandatory.

Reason:
...

Evidence:
...

Effect on program:
...

Can this decision be reopened?
Only if:
...
```

Keep entries short.

Record only decisions that materially change research direction.

Examples likely to belong here:

```text
continuum-generation requirement demoted
A2 native phase classified as spectator
Freund–Witten retained as B1 precedent
topological quantization retained as null
H1/H2/H3 kept unranked
BM reclassified as IR representation
AS reclassified as UV/RG layer
bidirectional research strategy adopted
```

Do not turn this into a diary.

---

# 14. FILE 4 — ai-context.md

This is deliberately tiny.

Target:

```text
<1000 words
```

It should allow a new AI agent to orient itself without reading the entire repository.

Use:

```markdown
# AI Research Context

## Mission

...

## Current Hypotheses

- H1 ...
- H2 ...
- H3 ...

## Current State

...

## Established / Reusable

- ...
- ...
- ...

## Open

- ...
- ...
- ...

## Killed / Closed

- ...
- ...
- ...

## Strongest Nulls

- ...
- ...
- ...

## Current Highest-Value Question

...

## Current Next Task

...

## Source of Truth

1. Raw research corpus
2. evidence-ledger.md
3. decision-log.md
4. research-dashboard.md
```

The AI context is **not authoritative over the raw evidence**.

It is a compressed index.

---

# 15. GIT-AWARE INCREMENTAL MODE

After the first full ingestion, the system enters incremental mode.

The dashboard and ledgers must contain:

```text
Last synced commit: <HASH>
Last synced date: <DATE>
```

On every subsequent run:

```bash
git status --short
git log --oneline <LAST_SYNCED_COMMIT>..HEAD
git diff --stat <LAST_SYNCED_COMMIT>..HEAD
git diff <LAST_SYNCED_COMMIT>..HEAD
```

Determine:

```text
new files
modified files
deleted files
renamed files
```

Read only the affected material first.

Then determine:

```text
new evidence?
new contradiction?
new decision?
task completed?
task killed?
task reopened?
new source?
changed interpretation?
```

Update the derived files accordingly.

Do not unnecessarily reprocess the entire corpus on every sync.

---

# 16. PERIODIC FULL RECONCILIATION

Incremental updates can drift.

Therefore, every time one of these conditions occurs:

```text
10+ commits since last full reconciliation
OR
20+ new research files
OR
major architecture change
OR
the user explicitly requests "rebuild"
```

perform a full corpus reconciliation.

Compare:

```text
raw corpus
vs
evidence ledger
vs
decision log
vs
dashboard
vs
AI context
```

Repair stale or contradictory summaries.

Never delete historical evidence merely because the dashboard no longer emphasizes it.

---

# 17. PROCESSING A NEW RESEARCH FILE

When a new file appears:

### Step 1

Identify what kind of source it is:

```text
prompt
research report
AI review
paper
notes
decision
computation
experimental result
```

### Step 2

Extract:

```text
new claims
new evidence
new criticisms
new decisions
new tasks
new dead ends
```

### Step 3

Compare against existing evidence.

Ask:

```text
Is this genuinely new?
Already known?
A stronger version of an existing claim?
A contradiction?
A correction?
A reinterpretation?
```

### Step 4

Update the evidence ledger.

### Step 5

Update decision log only if the research actually changed a strategic decision.

### Step 6

Update dashboard only if the change affects:

```text
current understanding
task status
priority
next action
```

### Step 7

Update AI context.

---

# 18. NEVER LET THE DASHBOARD BECOME AN EVIDENCE DUMP

The dashboard should summarize the **state of the investigation**, not the history of every argument.

Bad:

```text
Gemini said...
DeepSeek said...
Qwen said...
Tate...
Freund...
Jepsen...
Palmer...
...
```

Good:

```text
Global physical compatibility:
Prior art exists for amplitude-level compatibility.
No evidence yet establishes genuine causal coupling.
Next task: determine whether a nontrivial global compatibility
relation can survive the strongest non-arithmetic null.
```

The evidence ledger retains the provenance.

---

# 19. HANDLE CONTRADICTIONS EXPLICITLY

When sources disagree, do not silently resolve them.

Create a contradiction record.

Example:

```markdown
### C007 — Status of adelic amplitude regularization

Source A:
...

Source B:
...

Conflict:
...

Current adjudication:
UNRESOLVED

What would resolve it:
...
```

Then put only the conclusion on the dashboard:

```text
Adelic amplitude regularization remains unresolved.
```

---

# 20. DISTINGUISH RESEARCH STATUS FROM SCIENTIFIC STATUS

This is critical.

A research task can be:

```text
[x] complete
```

while the science remains:

```text
OPEN
```

For example:

```markdown
- [x] Survey Freund–Witten literature
  Scientific status: PRIOR ART / PARTIAL
```

Do not write:

```markdown
- [x] Freund–Witten solved H3
```

unless the evidence actually supports that.

---

# 21. PRIORITY CALCULATION

Do not invent numerical scores.

Use qualitative priority:

```text
CRITICAL
HIGH
MEDIUM
LOW
WATCH
```

Priority should depend on:

```text
information gain
dependency impact
cost
ability to falsify
ability to reuse existing work
```

A task with high cost and low discrimination should move down.

A cheap test capable of killing a major branch should move up.

---

# 22. NEXT-ACTION SELECTION

The dashboard must always contain exactly one:

```text
## Current Highest-Value Task
```

This is the task that appears to offer the largest expected research information gain relative to effort, based on the existing corpus.

Do not choose a task merely because it is technically interesting.

Prefer:

```text
cheap
decisive
reusable
dependency-unblocking
```

Do not choose a new microscopic substrate merely because current work is difficult.

---

# 23. PRESERVE THE BIDIRECTIONAL RESEARCH STRATEGY

The project is now intentionally two-directional.

Track both:

```text
BOTTOM-UP
mathematics
    ↓
existing structures
    ↓
common middle
```

and:

```text
TOP-DOWN
reality
    ↓
empirical constraints
    ↓
required physical structure
```

The dashboard should explicitly include:

```markdown
## Where Bottom-Up and Top-Down Currently Meet

...

## Where They Still Fail to Meet

...
```

These two sections are especially valuable.

They should change as the research evolves.

---

# 24. CURRENT HIGH-LEVEL RESEARCH QUESTIONS

Use these as the initial task map unless the corpus clearly establishes a better one:

```text
[ ] Global mathematical structure
[ ] Global physical compatibility
[ ] Arithmetic as physical selector
[ ] Genuine arithmetic–continuum coupling
[ ] Compatibility with established quantum physics
[ ] Structural role of BM
[ ] Structural role of AS
[ ] Arithmetic-specific observable discriminator
```

Under each, maintain only the smallest number of meaningful subtasks.

---

# 25. “DO NOT REOPEN” MEMORY

The dashboard must contain a short section:

```markdown
## Do Not Reopen Without New Evidence
```

Add a research topic only when the corpus establishes that repeatedly revisiting it has already produced no new information or that the project deliberately froze it.

For example, when justified by the corpus:

```text
ordinary Berry phase as arithmetic evidence
ordinary flux quantization as arithmetic evidence
generic cyclic-clock phase as A2-specific evidence
old continuum-generation route
```

Do not add something merely because an agent once discussed it.

---

# 26. SOURCE TRACEABILITY

Every evidence-ledger entry must be traceable to the source file.

Use repository-relative paths:

```text
research/foo/report.md
research/bar/review.pdf
```

and, where practical:

```text
file + section
file + line range
file + page
```

Do not invent line numbers.

If exact locations are unavailable, use:

```text
section title
page number
heading
```

---

# 27. EXTERNAL CITATIONS

The coding agent is primarily organizing the local corpus.

Do **not** perform a new web literature survey during normal synchronization.

If a source in the corpus has an external citation that appears important but unverified:

```text
mark it UNVERIFIED
```

Do not silently verify it and incorporate new external knowledge unless the user explicitly requests external research.

This keeps:

```text
research ingestion
```

separate from:

```text
new research.
```

---

# 28. QUALITY CHECK BEFORE FINISHING

After every update, check:

### Dashboard

```text
Does a human understand the current state in <2 minutes?
Is there exactly one highest-value next task?
Are completed tasks distinguished from scientifically solved questions?
Are open questions visible?
```

### Evidence ledger

```text
Are new claims recorded?
Are duplicates merged?
Are negative results preserved?
Can every important claim be traced to a source?
```

### Decision log

```text
Were any major strategic changes recorded?
Were old decisions accidentally rewritten?
```

### AI context

```text
Can a new AI agent understand the state quickly?
Does it point to the current task?
Does it identify the strongest evidence and strongest null?
```

---

# 29. GIT SAFETY

Never modify unrelated files.

Before editing:

```bash
git status --short
```

After editing:

```bash
git diff -- research-dashboard.md evidence-ledger.md decision-log.md ai-context.md
```

Then verify:

```bash
git status --short
```

Only modify these four generated files unless the user explicitly requests otherwise.

Do not commit automatically unless the user explicitly tells you to commit.

The user's normal workflow is:

```text
paste research
      ↓
save
      ↓
git commit
      ↓
run coding agent
      ↓
agent reads git diff
      ↓
update derived research state
      ↓
user reviews diff
      ↓
user commits
```

Preserve this workflow.

---

# 30. FIRST-RUN OUTPUT

After completing the first full corpus ingestion, report only:

```text
RESEARCH KNOWLEDGE BASE BUILT

Source files reviewed: N
Research period covered: ...
Major research tracks: 8
Evidence records created: N
Major decisions recorded: N

Current state:
[5–10 lines]

Highest-value unresolved question:
...

Next task:
...

Generated:
research-dashboard.md
evidence-ledger.md
decision-log.md
ai-context.md

Git changes:
...
```

Do not print the entire dashboard or ledger to the terminal.

---

# 31. FUTURE-RUN OUTPUT

On incremental sync, report:

```text
RESEARCH SYNC COMPLETE

Base commit:
...

New commits processed:
...

New/changed research files:
N

New evidence:
N

Updated evidence:
N

New decisions:
N

Tasks completed:
...

Tasks opened:
...

Tasks killed/reopened:
...

Dashboard changed:
YES / NO

Current highest-value task:
...

Unresolved critical issues:
...
```

Keep the output brief.

---

# 32. FINAL PRINCIPLE

The derived files exist to answer four human questions:

```text
WHERE ARE WE?
WHAT HAVE WE LEARNED?
WHAT DO WE STILL NOT KNOW?
WHAT SHOULD WE DO NEXT?
```

And four AI questions:

```text
WHAT IS THE CURRENT STATE?
WHAT EVIDENCE ALREADY EXISTS?
WHAT IS THE STRONGEST NULL?
WHAT IS THE HIGHEST-INFORMATION NEXT ACTION?
```

Everything else belongs in the research corpus.

The objective is not documentation for its own sake.

It is:

$$
\boxed{
\textbf{Turn a growing research corpus into an increasingly smaller,
clearer, more useful map of what is actually known.}
}
$$

Never optimize for the number of pages.

Optimize for:

$$
\boxed{
\text{insight per unit of human attention}
}
$$

and:

$$
\boxed{
\text{new information per research cycle}.
}
$$

---

### One implementation detail I would strongly keep

Have the agent maintain this line in all four generated files:

```text
Last synced commit: <git hash>
```

That makes the Git-driven workflow deterministic. On the next run, the agent knows exactly what changed since the last knowledge-base update instead of rereading everything.

The resulting architecture is essentially:

```text
                    RAW RESEARCH
                         │
              ┌──────────┴──────────┐
              │                     │
         new material          historical corpus
              │                     │
              └──────────┬──────────┘
                         ▼
                  AI/CODING AGENT
                         │
          ┌──────────────┼──────────────┐
          ▼              ▼              ▼
      evidence       decisions       current state
      ledger           log           dashboard
          │              │              │
          └──────────────┼──────────────┘
                         ▼
                    AI CONTEXT
```

This gives you a **research cockpit rather than another research paper**, while `v7.1.md` remains the deep technical charter underneath it. The distinction is important because the existing v7.1 already contains substantial gate, null, bridge, and research-phase machinery. 

The four-file setup also means that when you paste the next Gemini/DeepSeek/Qwen review and commit it, the coding agent can update the **state of knowledge** rather than making you manually reconcile everything again.

