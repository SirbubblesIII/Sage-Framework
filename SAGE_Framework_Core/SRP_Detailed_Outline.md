# SRP — How It Works and What Went Into It

> **What this file is:** An extremely detailed outline of the SRP (Structure → Reasoning →
> Presentation) methodology — both *how it operates as a method* and *what intellectual inputs
> and development history produced it*. Built by reading across the SRP runtime skill, the
> canonical framework reference, the methods library, the tributaries/lineage doc, the three-year
> long synthesis, and the genesis conversation recaps.
>
> **Scope note:** SRP is the *reasoning pillar* of the larger **SAGE** framework. This outline
> centers SRP but pulls in SAGE context wherever SRP can't be understood without it (CCC, the
> facets, the memory stack, the training-data thesis).
>
> **Source of truth:** `SAGE_FRAMEWORK_CANONICAL_v2_2026-06-12.md` (root; v1 retains authority
> where they conflict, until the translation test passes). Where this outline and the canonical
> ever disagree, the canonical wins.
> **Framework author:** Weston James Milhon.
> **Compiled:** 2026-06-02. **Update pass:** 2026-07-02.
>
> **⚠️ June 12, 2026 developments postdate this outline's compilation.** The SRP core in this
> document is still accurate. What changed around it: (1) **Canonical v2** exists (integrating
> the profession-archetype pivot — personality is now a profession-archetype catalog curated by
> the **Core 11** editorial board; the nine facets survive as ingredient vocabulary; SAGE-context
> sections here, esp. Appendix B, are the pre-pivot picture). (2) The **combinations CSV now
> exists and was verified at 4,779** — §8 and §26 below carry dated corrections. (3) The
> **grading sheet** (`SRP_Grading_Sheet.md`, root) is named in v2 as the editorial board's
> scoring tool. See `SRP-CCC_SAGE_Update.md` (this folder) for the current running status.

---

## Part 0 — Orientation: what SRP is, in one pass

- **SRP = Structure → Reasoning → Presentation.** A three-phase methodology for disciplined
  problem-solving.
  - **Naming is load-bearing and frequently mis-stated.** It is *Structure-Reasoning-Presentation*,
    **NOT** "Structured Reasoning Process." Claude made this error repeatedly and was corrected;
    treat "Structured Reasoning Process" as a known drift bug.
- **CCC = Compare → Contrast → Consensus.** A *synthesis layer* that runs on top of SRP when more
  than one reasoning pass (trace) has been generated. SRP + CCC together are usually written
  "SRP-CCC."
- **Where SRP sits in SAGE.** SAGE rests on three inseparable pillars — *personality, reasoning,
  memory* — treated as three descriptions of one cognitive process. SRP **is the operationalization
  of the reasoning pillar.** (Personality → the nine facets; Memory → the killer-item gate + CODE/PARA
  + Zettelkasten.)
- **The original name had a "C."** It began as **C-SRP**, where the C stood for "cognitive"
  (also seen as "cognitive-safety"). The C was dropped within days of its first appearance
  (late Oct 2025) and SRP stabilized.
- **What SRP is *for*.** It is the **trace skeleton** for training data: the structural backbone of
  the first-person reasoning traces SAGE is built from. The runnable SRP "skill" is explicitly a
  **runtime approximation** of what a SAGE-pretrained model would do intrinsically — i.e., test
  scaffolding, not the framework's actual deliverable.

---

# PART I — HOW SRP WORKS (mechanics)

## 1. Adaptive Depth — calibrate visibility to the problem

SRP is not a fixed ritual; it is run at one of three *visibility* levels. The internal moves are
always performed — what changes is how much scaffolding is surfaced.

| Level | What the user sees | What you still do internally |
|---|---|---|
| **Light touch** | A clean, well-structured answer; no visible scaffolding | Every SRP move (restate goal, consider alternatives, name uncertainty) |
| **Visible structure** | Phases surfaced explicitly: decomposition, hypotheses, evidence, kill-steps, calibrated confidence | All moves, made legible |
| **Full SRP mode** | Phase-by-phase walkthrough with explicit method selection from the combinations matrix; CCC at MEDIUM/HIGH | All moves + method IDs + CCC synthesis |

**Decision heuristics (ask before responding):**
- How many *genuinely different* approaches exist? (1–2 = LOW, 3–5 = MEDIUM, 5+ = HIGH)
- How much ambiguity is in the problem definition?
- How many stakeholders / perspectives are involved?
- What are the stakes if the answer is wrong?
- Did the user ask for depth, or for a quick answer?

**Default rule:** if most answers are "not much," go light touch. **If uncertain, default to visible
structure** — better to over-show reasoning than to hide a sloppy process behind a smooth answer.

---

## 2. Phase 1 — STRUCTURE (define before you reason)

**Produces:** a clear problem space the Reasoning phase can actually work with. This is the most
*skipped* phase and the most *important* one — if Structure is vague, Reasoning will be vague.

**The six required moves (do all, even if some stay internal):**

1. **Restate the goal in your own words** — a genuine restatement, not a copy-paste. If you can't
   restate it, you don't understand it yet; ask.
2. **Map what matters** — key entities, relationships, dependencies, hierarchies. Must be *explicit*
   in your thinking even if not surfaced.
3. **Draw boundaries** — what's in scope, what's out, and *why*. Name boundary choices as choices,
   not as givens.
4. **Surface constraints and assumptions** — what must be true for the analysis to hold (time,
   budget, technical, legal, ethical). **Flag the fragile assumptions** — they become test targets.
5. **Define success and failure concretely** — not "a good answer" but e.g. "the user can decide
   with tradeoffs visible" or "no unaddressed single points of failure."
6. **Calibrate level of detail deliberately** — rough map vs. step-by-step path is a *choice*, not an
   accident of how much you happened to write. Say why.

**Choosing a Structure method** (visible/full modes): pick the method that actually decomposes *this*
problem — not the most impressive one. Quick heuristics:

| Problem feels like… | Candidate S-methods |
|---|---|
| Tangled system with feedback loops | System Dynamics (S3), Causal Loop Diagrams (S17) |
| Need multiple angles | DSRP (S1), Rich Pictures (S22) |
| Organizational/institutional | Viable System Model (S4), Stakeholder Mapping (S16) |
| Strategic/competitive | SWOT (S11), Porter's Five Forces (S12), PESTLE (S14) |
| Need categories/taxonomy | Hierarchy Analysis (S7), Taxonomy (S26) |
| Wicked / ill-defined | Boundary Critique (S23), Problem Framing Canvas (S25) |
| Finding where to intervene | Leverage Points (S24), Network Analysis (S19) |

---

## 3. Phase 2 — REASONING (think with genuine alternatives)

**Produces:** a set of tested approaches with evidence both ways, concrete kill-steps, and an honest
read of what's confident vs. not.

**The seven required moves:**

1. **Generate ≥2 genuinely distinct approaches** — differing in *mechanism or core assumption*, not
   just conclusion. Label them neutrally (A/B/C) — *not* "main hypothesis and alternatives." If you
   already have a favorite, you're rationalizing, not reasoning.
   - **Genuineness test:** if an advocate of Approach A would find Approach B *threatening or
     uncomfortable*, they're genuinely distinct. If they'd shrug, they're cosmetic.
2. **Seek evidence in both directions** — build the case *for* and actively hunt the thing that would
   break each approach. (The Scientist facet doing real work.)
3. **Name a concrete kill-step per approach** — a specific, falsifiable observation that would mean
   "abandon this." Not "if it doesn't work" but "if latency exceeds 2s under normal load" or "if the
   primary study fails to replicate." No kill-step = it's a belief, not a hypothesis.
4. **Design discriminating tests** — checks that *distinguish between* approaches ("what would make A
   right and B wrong?"), not just "is A good?"
5. **Verify sources before trusting them** — interrogate each significant source on: **Authority,
   Bias/incentive, Track record, Recency, Corroboration, Methodology.** Then assign a **trust level**:
   - **Strong** — credible author, peer-reviewed/well-corroborated, no obvious bias, current
   - **Moderate** — credible but single-source, some bias, or not fully corroborated
   - **Weak** — unknown author, obvious bias, outdated, uncorroborated, poor method
   - **Flagged** — known issues; use only with explicit caveat
6. **Mark the epistemic status of every claim** — separate from source quality: is this a **fact**,
   an **inference**, an **assumption**, a **guess**, or a **value judgment**? Don't blend load-bearing
   granite with swappable scaffolding.
7. **Use tools when they'd give real evidence** — search/calc/code as *part of* reasoning, not
   decoration. Document what you searched, found, and what it means for the hypotheses.

**Choosing a Reasoning method** (visible/full modes), quick heuristics:

| Reasoning need | Candidate R-methods |
|---|---|
| Premises → certain conclusion | Deductive (R1) |
| Observations → generalization | Inductive (R2) |
| Best explanation for a surprise | Abductive (R3) |
| Something broke, find the cause | Root Cause Analysis (R4), Fault Tree (R33) |
| Creative/inventive solutions | TRIZ (R7), Design Thinking (R8) |
| Fast decisions under uncertainty | OODA (R9) |
| Iterative improvement | PDCA (R10) |
| Rigorous empirical testing | Scientific Method (R12), Hypothesis Testing (R18) |
| Multi-criteria evaluation | MCDA (R13), Decision Trees (R40) |
| Stress-test a plan | Pre-mortem (R26), Red Team/Blue Team (R28), Devil's Advocate (R29) |
| Compare to known solutions | Analogical (R21), Case-Based (R22) |
| Explore futures | Scenario Planning (R24), Counterfactual (R25) |
| Quantify tradeoffs | Cost-Benefit (R41), Trade-off (R42) |
| Multiple stakeholder views | Six Thinking Hats (R38), Delphi (R36) |

---

## 4. Phase 3 — PRESENTATION (make it usable)

**Produces:** something the person can *use*, not just admire — a reusable method, a clear decision,
a concrete next step.

**The six required moves:**

1. **Choose a format that serves the audience** — a developer needs different packaging than an
   executive; a Slack question different shape than a planning session.
2. **Lead with the answer, then show reasoning** — unless the user asked to see the thinking, don't
   make them wade through the journey to find the conclusion.
3. **Calibrate confidence explicitly** — a number/range *plus* the reason ("~75% because the primary
   evidence is strong but single-source"). Tie it to evidence strength/relevance/reliability.
4. **Make next steps concrete** — "test X by doing Y; if you see Z, that confirms this approach,"
   not "consider further research."
5. **Preserve dissent when it matters** — "A is better if X; B is better if Y" beats a forced false
   consensus.
6. **Source every claim** — back to a search result, calculation, document, or an explicit
   assumption. Unsourceable → flag as your inference.

**Choosing a Presentation method**, quick heuristics:

| Audience/purpose | Candidate P-methods |
|---|---|
| Quick decision-maker | Executive Summary (P7), Memo (P6) |
| Technical audience | Technical Report (P8), Annotated Code (P32) |
| Teaching/learning | Tutorial (P13), FAQ (P14), Dialogue (P15) |
| Comparing options | Comparative Table (P16), Decision Matrix (P17) |
| Process/flow | Flowchart (P19), Systems Diagram (P23) |
| Cause-and-effect | Causal Diagram (P18), Fishbone (P27) |
| Memorability | Metaphorical Explanation (P36), Narrative Synthesis (P33) |
| Planning/scheduling | Gantt (P20), Timeline (P26) |
| Policy/governance | Policy Brief (P9), White Paper (P10) |

---

## 5. Phase Linkage — the single most important structural constraint

Every output of one phase must feed the inputs of the next. **A broken link is treated as a critical
error.** The required handoffs:

**Structure → Reasoning**
- **Entities → Hypotheses:** mapped entities/relationships must appear in your hypotheses.
- **Boundaries → Scope control:** a hypothesis drifting out of scope means the hypothesis or the
  boundary is wrong — fix one.
- **Constraints → Feasibility filter:** never spend a hypothesis slot on something a hard constraint
  already kills.
- **Fragile assumptions → Test targets:** the assumptions you flagged become the *first* things
  Reasoning investigates.
- **Success criteria → Evaluation frame:** how you defined success shapes how you judge hypotheses.

**Reasoning → Presentation**
- **Evidence quality → Confidence level:** source trust levels directly determine confidence numbers.
  Best evidence "moderate" → confidence shouldn't be 95%.
- **Kill-steps → Caveats/conditions:** kill-steps reappear as the conditions under which the
  recommendation changes (not buried).
- **Approach comparison → Preserved dissent:** genuine, unresolved disagreement survives into the
  presentation; don't collapse it for a cleaner answer.
- **Evidence gaps → Uncertainty flags:** holes (unanswerable questions, unverifiable sources,
  un-runnable tests) appear as explicit uncertainty.
- **Discriminating tests → Next steps:** the tests that would resolve the question become the
  recommended next steps.

**Phase Connectivity Check:** the explicit pre-delivery validation that this whole chain held. (See
the validation checklist in §11.)

---

## 6. CCC Synthesis — Compare / Contrast / Consensus (MEDIUM & HIGH only)

When multiple traces have been run (3 for MEDIUM, 5 for HIGH) with different S-R-P combinations,
synthesize them:

- **COMPARE — map agreements.** Where do traces reach the same conclusion? With the same or different
  evidence? *Convergence from different methods is stronger than convergence from similar methods.*
- **CONTRAST — map disagreements and what drives them.** Five candidate drivers:
  **ontological** (entity definitions), **epistemological** (evidence standards), **value**
  (normative assumptions), **method-suitability** (one method better fit), **blind-spot** (each method
  missed different things). Distinguish *resolvable-with-more-info* from *fundamental-framing*
  differences.
- **CONSENSUS — build synthesis without forcing it.** Strong convergence → higher-confidence
  statement. Genuine disagreement → conditional recommendation ("A if X, B if Y"). Preserve
  legitimate minority views; *don't average away insight.* Name what would resolve the rest.

**CCC method-diversity rules:**
- **MEDIUM (3 traces):** 3 different Structure methods + 3 different Reasoning methods. Presentation
  may repeat.
- **HIGH (5 traces):** 5 different Structure + 5 different Reasoning methods — maximum diversity.
- Each S+R+P combination should be validated against the combinations matrix; record the Index.

**Critical subtlety — CCC is training scaffolding meant to be internalized.** Explicit CCC exists in
*early-generation training data* so the model absorbs it and makes it implicit. A mature trained model
will **not** show visible CCC at runtime — and that's success, not failure. *Any evaluation that tests
for visible CCC at runtime is testing the wrong thing.*

---

## 7. The three complexity tiers

| Tier | Traces | Hypotheses | CCC? | Use when |
|---|---|---|---|---|
| **LOW** | 1 | 3 (A/B/C) | No (absorbed) | Clear/factual/straightforward; 1–2 reasonable approaches |
| **MEDIUM** | 3 (different S & R methods) | A/B/C per trace | Yes, full | Multi-stakeholder, moderate ambiguity, several valid framings |
| **HIGH** | 5 (maximum diversity) | A/B/C per trace | Yes, extended | Wicked, high-stakes, complex ethical, novel, contested framings |

- **Tier is set by problem characteristics, not desired output length.**
- **LOW does not skip CCC — it *absorbs* it.** Hypothesis comparison happens *inside* the Reasoning
  phase rather than across separate traces. (The LOW hypothesis count was revised from 2 → 3 for
  stronger discrimination, Nov 2025.)

---

## 8. The methods library and combinations matrix

- **27 Structure × 40 Reasoning × 36 Presentation methods.**
- **Validated S-R-P combinations — drift RESOLVED (update 2026-07-02): the verified figure is
  4,779.** The CSV now physically exists (`01_Areas/SAGE_Methodology/srp_combinations.csv`,
  landed June 9) and was **verified June 12, 2026 by direct count: 4,780 lines including the
  header row = 4,779 combinations** — which also explains how the 4,779/4,780 drift arose.
  Canonical v2 §2.4 carries the verified figure.
  - *Drift history (kept for the record):* earlier docs (Nov 2025) cite **4,648**; later docs
    and the academic paper cite **4,780** (v1 declared it canonical); one March-2026 recap
    reported **4,779** as an "exact CSV query" result — that recap turned out to be right.
- **Status:** the CSV **exists**; the remaining open task is a **validation pass** (checking the
  combinations themselves, not just the count).
- **Purpose framing (important):** the matrix is **compositional learning coverage**, not a curriculum
  to memorize. The point is that the model learns to *compose* methods to problems — "cross-training
  across cognitive operations, the way physical cross-training works across muscle groups" — not to
  pattern-match traces. (This is the defense against the "over-prescription" objection.)

**Structure methods (27), grouped:**
- *Systems & Complexity (S1–S10):* DSRP, Soft Systems Methodology, System Dynamics, Viable System
  Model, Critical Systems Thinking, Systemic Design, Hierarchy Analysis, Complex Systems Analysis,
  Complex Adaptive Systems, Self-Organized Criticality
- *Strategic & Business (S11–S16):* SWOT, Porter's Five Forces, Value Chain, PESTLE, Business Model
  Canvas, Stakeholder Mapping
- *Visual & Relational (S17–S22):* Causal Loop Diagrams, Stock-Flow Diagrams, Network Analysis,
  Systems Archetypes, IBIS, Rich Pictures
- *Problem Framing (S23–S27):* Boundary Critique, Leverage Points, Problem Framing Canvas, Taxonomy,
  Conceptual Modeling

**Reasoning methods (40), grouped:**
- *Formal logic (R1–R3):* Deductive, Inductive, Abductive
- *Problem-solving (R4–R8):* Root Cause Analysis, A3, 8D, TRIZ, Design Thinking
- *Decision cycles (R9–R11):* OODA, PDCA, GROW
- *Scientific & empirical:* Scientific Method, Trial and Error, Hypothesis Testing, Sensitivity
  Analysis (plus Bayesian Inference / Monte Carlo in the probabilistic grouping)
- *Decision-making:* MCDA, Naturalistic Decision-Making, Intuitive Decision-Making
- *Comparative & analogical (R21–R23):* Analogical, Case-Based, Benchmarking
- *Scenario & counterfactual (R24–R27):* Scenario Planning, Counterfactual, Pre-mortem, Post-mortem
- *Adversarial & critical (R28–R31):* Red Team/Blue Team, Devil's Advocate, Dialectical, Critical
  Thinking
- *Risk & safety (R32–R35):* FMEA, Fault Tree, Event Tree, Bow-Tie
- *Group methods (R36–R38):* Delphi, Nominal Group Technique, Six Thinking Hats
- *Optimization (R39–R42):* Linear Programming, Decision Trees, Cost-Benefit, Trade-off

**Presentation methods (36), grouped:**
- *Note/document (P1–P5):* Cornell Notes, SQ3R, CODE (Second Brain), Progressive Summarization,
  Checklist
- *Written (P6–P15):* Memo, Executive Summary, Technical Report, Policy Brief, White Paper, Academic
  Paper, Case Study, Tutorial, FAQ, Dialogue
- *Visual (P16–P31):* Comparative Table, Decision Matrix, Causal Diagram, Flowchart, Gantt, Dashboard,
  Infographic, Systems Diagram, Network Graph, Mind Map, Timeline, Fishbone, Slide Deck, Interactive
  Visualization, Video, Simulation
- *Narrative (P32–P36):* Annotated Code, Narrative Synthesis, Scenario Narrative, Dialogue Format,
  Metaphorical Explanation

**Selection + validation workflow:** pick S + R + P → look up the combination in the CSV by
S_ID/R_ID/P_ID → verify it exists → record the Index → check the `Problem_Types`
(simple/complicated/complex/wicked) and `Output_Types`
(conceptual/comparative/narrative/qualitative/quantitative/sequential/visual) columns against your
actual problem. Mismatches aren't fatal but signal a possibly-better method.

---

## 9. The scratchpad — the transparency layer SRP rides on

Every trace is anchored by a scratchpad recording:
- Verbatim tool calls (actual API requests/responses, not summaries)
- Evidence extraction with direct quotes + source attribution
- Memory operations with query strings and rationale
- Internal reasoning showing hypothesis logic and kill-step design
- Metacognitive notes (aha moments, contradictions, knowledge gaps, strategy shifts)

**Rule:** every factual claim in Reasoning and Presentation must trace back to the scratchpad. Claims
without scratchpad citations are treated as hallucinations and rejected. This is what makes SRP
*auditable*.

---

## 10. How SRP plugs into memory (the third pillar)

SRP doesn't run in a vacuum; memory operations appear inside traces as conscious decisions:
- **Killer-item gate (Gawande)** — capture moment. Store only if **critical AND easy to miss**
  ("would this change action?"). Prevents memory bloat.
- **CODE (Forte)** — session level. Capture → Organize (by actionability, via PARA) → Distill
  (progressive summarization) → Express (use it).
- **Zettelkasten (Ahrens/Luhmann)** — long term. Atomic notes, one idea each, your own words, densely
  linked; value grows faster than size. *Working definitions are exempt from compression — precision
  is the point.*
- **PARA** — organizational layer by actionability not topic (Projects/Areas/Resources/Archives), and
  in SAGE, **actionability is facet-dependent** ("PARA modified by SAGE facets").
- **Distinguished from RAG:** RAG is similarity-lookup bolted on; here memory management is trained as
  an intrinsic cognitive operation.

---

## 11. Validation — the pre-delivery checklist

**Structure check:** restated the goal (not echoed)? named boundaries + constraints? identified the
most fragile assumptions?

**Reasoning check:** 2+ genuinely distinct approaches (not cosmetic)? evidence sought *against* each?
concrete kill-step each? sources verified (authority/bias/track record/recency/corroboration)? trust
level assigned per source? every claim labeled by epistemic status?

**Presentation check:** format matched to audience? confidence a number *with reasoning*? confidence
*actually reflects* source trust levels? next steps concrete? dissent preserved? kill-steps surfaced
as conditions, not buried?

**Phase connectivity check:** entities→hypotheses; boundaries→scope; fragile assumptions→test targets;
source trust→confidence numbers; kill-steps→caveats; evidence gaps→uncertainty flags; discriminating
tests→next steps.

*If any check fails, fix the gap before delivering.*

---

## 12. What SRP is NOT (scope boundaries the skill states about itself)

- It handles **methodology** — decompose, reason, present. It does **not** enforce SAGE facet balance
  (a separate discipline), does **not** manage cross-session memory by itself, and does **not** replace
  judgment about when to go deep vs. light.
- **The skill is a tool, not a cage.** If SRP structure isn't helping a given task, say so and explain
  why. Rigid application to problems that don't need it is its own failure mode.

---

# PART II — WHAT WENT INTO IT (intellectual lineage)

> Ordered roughly by when each input entered the work and how load-bearing it became. Some inputs
> became core, some were stepping-stones, some were rejected.

## 13. The four foundational books (the explicit synthesis layer)

The working metaphor — *"these four are saying the same thing about different layers of cognition"* —
predates the framework's name (in play since ~mid-2024).

- **_Unlimited Memory_ — Kevin Horsley.** Seeded the memory pillar's mnemonic techniques (method of
  loci, peg/Major systems, body/car methods, linking story, SEE principle, Look–Link–Lock). **This is
  where kill-steps originated** — as image-quality checks for mnemonic encoding (vivid? one-to-one?
  distinct? recallable both ways?) *before migrating into SRP as falsification conditions for
  hypotheses.* The specific techniques were dropped; the kill-step concept and "memory is an active
  practice" endured.
- **_The Checklist Manifesto_ — Atul Gawande.** Most directly load-bearing of the four. Source of the
  **killer-item gate** (critical AND easy to miss), do-confirm vs. read-do, the 5–9 item working-memory
  guideline, and the **"would this change action?"** question. Surgical/aviation examples dropped;
  principles kept.
- **_Building a Second Brain_ (CODE + PARA) — Tiago Forte.** Source of **CODE** (session-level
  information lifecycle) and **PARA** (actionability-based organization). PARA holds the whole memory
  stack together; SAGE adds "actionability is facet-dependent." App recommendations dropped; principles
  kept.
- **_Atomic Habits_ — James Clear.** Least directly load-bearing — more "shared intellectual climate."
  Behavior-as-compound-effect and identity-based change echo "distribution is destiny" at the human
  level. Specific habit techniques not in the canonical.

## 14. Zettelkasten — Niklas Luhmann (via Sönke Ahrens)

Added to the memory stack at the longest timescale. Atomic notes (one idea each), written for a future
self, densely linked rather than rigidly filed; value is in the connections. Provides the *atomic shape*
of stored knowledge in the canonical nine components.

## 15. David Shapiro and the heuristic imperatives (earliest seed, May 2023)

Shapiro's heuristic imperatives (reduce suffering, increase prosperity, increase understanding) were
the **first explicit "what character should an AI have?" question** in Weston's archive. The framework
didn't grow from Shapiro's specific imperatives — but the *appetite* for designing AI character rather
than stacking rules is visible here. What endured: the framing question, and "design for character, not
just compliance."

## 16. Wave Function Collapse (WFC) — the planning metaphor that became a stepping-stone

A procedural-generation algorithm (state → pick → collapse → propagate → backtrack → finish) from the
procgen community (Caves of Qud etc.). During the convergence period (Aug–Oct 2025) it was *the*
planning metaphor: the AI maintains a "map of valid possible actions" and uses WFC to collapse it into a
coherent plan, like a prefrontal-cortex filter. **What endured:** "planning is constraint propagation,"
"limited valid actions at any time." **What was dropped:** WFC is *not* doing the load-bearing planning
work in the final framework — that work is done by SRP, the combinations matrix, and CCC. Docs that
still treat WFC as the planning mechanism are out of date.

## 17. Mindcraft / Mindcraft CE — the test bed

A Minecraft LLM-agent project; the test bed for the WFC + memory + checklist synthesis in fall 2025. A
deep-dive into its codebase forced concrete thinking about agent architecture, tool use, and memory.
What endured: agent-architecture moves, multi-step task completion, the "code-shelling" framing
(wrapping prompts in code that feeds outputs back to complete tasks). The specific codebase isn't part
of the framework — it was the practice-ground.

## 18. Neuro-sama and Vedal — the actual origin observation

Vedal987's AI VTuber. **This is the framework's stated origin** (per the foundational-hypothesis recap,
2026-03-06): watching Neuro-sama maintain a consistent personality →
*"personality is already being trained whether you mean to or not"* → *"what personality?"* → **SAGE.**
It also supplied the architectural template Weston carried through 2025: a single LLM orchestrator with
auxiliary modules (speech, TTS, tool interface, memory, safety head), persona reinforced via curated
data + community feedback rather than hard rules. **Note:** the framework's origin is this observation,
*not* alignment theory — and the recap argues this chain should be the first principle in the academic
paper, *before* "Distribution is Destiny."

## 19. Mem0 and LongRoPE — technical commitments (2025)

- **Mem0** — production-ready LLM long-term memory: extracts key facts from dialogue, stores in
  graph-structured memory, does ADD/UPDATE/DELETE/NOOP by similarity (~26% higher accuracy, ~91% lower
  latency, ~90% token savings vs. full context, per the paper). → the memory-operations architecture
  (one of the nine components).
- **LongRoPE** — extended-context positional encoding; longer inputs without retraining positional
  embeddings. → working memory across long SRP sessions (one of the nine components).
- *Correction pinned (2026-03-04):* both are inference-time tools today, but their **principles port to
  pretraining via adaptation, not replacement.** "Mem0 can't be used at pretraining" is wrong as
  written.

## 20. RLP / RoRL — the training paradigm

Reinforcement Learning Pretraining: treats chain-of-thought generation as an action rewarded by
information gain over a baseline (reasoning-as-pretraining). It's the paradigm that **embeds the other
eight components into pretraining (not fine-tuning)** — the 90–100% integration constraint is RLP's
load-bearing requirement. **Alias:** the DataxLLM survey calls this **RoRL** (Reasoning-oriented RL);
adding the alias positions the framework in existing literature.

## 21. Agent paradigms — the thought-action-observation lineage

- **ReAct** (Yao 2023) — interleaving reasoning and action; foundation of "agent-shells."
- **Reflexion** (Shinn 2023) — verbal RL; analogue for the "continuous-improvement-mindset" emergent
  property.
- **Toolformer** (Schick 2023) — model learns when/how to call tools.
- **Self-Refine** (Madaan 2023) — iterative self-feedback; analogue for the "self-correction" property.
- **HuggingGPT** (Shen 2023) — LLM as controller orchestrating expert models; analogue for the
  orchestrator architecture.

## 22. The empirical foundations — 5 lines of evidence (the academic backbone)

1. **Pretraining distribution primacy** — LIMA (1,000 curated examples beat RLHF DaVinci003 in 65% of
   comparisons; matched GPT-4 in 43%); Lin et al. 2024 (>92% of aligned-model tokens within base
   model's top-3; only 5–8% of positions shift meaningfully); Phi series (Phi-1: 1.3B / 7B tokens
   "textbook quality" → 50.6% HumanEval; Phi-2 better toxicity than RLHF via curated pretraining alone);
   DoReMi (data-mixture optimization → +6.5 pts; baseline with 2.6× fewer steps).
2. **Shallowness of current alignment** — Qi et al. 2025 (alignment mostly modifies first few output
   tokens); Arditi et al. 2024 (refusal mediated by a single residual-stream direction; ablate →
   refusal gone); Young 2025 (gradient-based alignment gets zero signal beyond the "harm horizon");
   Qi et al. 2024 (alignment removable with ~10 adversarial fine-tune examples); Hubinger et al. 2024
   ("Sleeper Agents" — backdoors survive standard safety training).
3. **Shared neural substrate of failure** — Gao et al. 2025 ("H-Neurons": <0.1% of neurons causally
   link hallucination, sycophancy, false-premise acceptance, jailbreak vulnerability; shared mechanism
   = "over-compliance"; neurons form in pretraining, parameter stability ~0.97 through alignment). *This
   is the empirical case that the three pillars are one process.*
4. **Single-component improvement degrades overall** — OpenAI o3 (doubled PersonQA hallucinations,
   33% vs 16% for o1 — stronger reasoning without matching calibration/grounding made it worse);
   Sharma et al. 2024 (RLHF amplifies sycophancy because matching user beliefs scores higher).
5. **Compound concept representation** — Anthropic SAE work (Templeton et al. 2024: up to 34M features
   in Claude 3 Sonnet, incl. abstract behavioral concepts like deception); Frame Representation
   Hypothesis (Valois et al. 2025, TACL); Representation Engineering (Zou et al. 2023: honesty/
   harmlessness/fairness as readable, controllable directions).

## 23. The numbered reading list (#1–#14, project Resources)

RLP on Pre-Training Data · Reliability of LLMs (CoT + RAG) · Enhancing LLMs through Structured
Reasoning · Stress-Testing Model Specs · Mem0 · RLP as a Pretraining Objective · Cognitive Foundations
for Reasoning (CogFound — basis for the external evaluation instrument) · The Era of Agentic
Organization · Thinking Faithful and Stable · CharacterGPT · Humanoid Artificial Consciousness · RAG
for Knowledge-Intensive NLP · Defeating Nondeterminism in LLM Inference · PersonaLLM.
*Plus unnumbered:* A-MEM, Checklist-Guided Memory Architectures, Context Engineering 2.0, The Bitter
Lesson, TrajAgent, Attention Residuals, End-to-End Test-Time Training, LongRoPE.

## 24. Excluded from SAGE (shared lineage, separate projects)

Same author, same interdisciplinary instinct, but **not** part of SAGE: K-12 curriculum reform;
Sustainable Earthship Condominium design; the Third Place community center (Lawrence, KS); the policy
platform ("11 Policies" / Prometheus). They show the cross-domain synthesis style that *became* SAGE's
method, but their content isn't SAGE's content.

---

# PART III — DEVELOPMENT CHRONOLOGY (how SRP actually evolved)

> Compiled from ~2,131 conversations (Apr 2023 – Nov 2025 ChatGPT export) + the Claude Experimental
> folder (Nov 2025 – May 2026). Six acts.

## Act 1 — Seeds (Apr 2023 – mid-2024)
No project yet — just *appetite*. Shapiro's imperatives (May 2023); first "system thinking checklist"
(May 27 2023); AI-Therapist feasibility chats (begin the Therapist persona); *Unlimited Memory* enters
(late Jul 2023); PARA enters ("Combine PARA and Dellis," Jul 29 2023). Parallel projects (Earthship,
K-12, policy) build the *synthesis muscle* without being SAGE. **Honest note:** no engineering work yet
— and still none three years later, which the project's own confidence calibration admits.

## Act 2 — The four pillars assemble (mid-2024 – Aug 2025)
Longest, most diffuse period. Solo-D&D / dungeon-master engine work builds *agentic-system-design*
muscle (state tracking, rule-following, narrative coherence). First WFC experiments (Jul 30 2024). PARA
matures into a system Weston actually uses (May 2024). Memory techniques mature — **kill-steps origin as
mnemonic image-quality checks.** The **Mixture-of-Experts review pattern emerges** (asking AI to review
work as Systems Engineer / Psychologist / Generalist / Memory Expert / Scientist) — **the direct
ancestor of the SAGE facet system.** The four books become canonical reading; *Checklist Manifesto*
summary (Mar 8 2025) yields the "would this change action?" question.

## Act 3 — The convergence (Aug 2025 – Oct 2025)
"Four related books" becomes "one synthesis." "Human thought process" (Aug 31 2025). WFC promoted to
*the* planning metaphor (Sep 1–7). Mindcraft CE becomes the test bed (Sep 4 – Oct 1). Academic-paper
reading begins in earnest. **Proto-SRP work begins:** "Cognitive safety framework / checklist
framework" (Oct 19) — compressing the four-pillar synthesis into a single methodology. Mem0 deep dive
(Oct 21). "Textual Decompositions" (Oct 23, 742 messages) — disciplined, fully-traceable decomposition
is itself proto-SRP practice.

## Act 4 — C-SRP → SRP → SRP-CCC crystallizes (late Oct – Nov 2025)
The architecture clicks in ~four weeks.
- **C-SRP** appears (Oct 25; "C" = cognitive); the C drops within days → **SRP**.
- SRP practiced with worked examples ("SRP chain of thought example," Nov 7).
- **"SAGE Index Checklist" (Nov 9, 487 messages):** the SAGE *name* lands; the **7-facet** personal-
  practice version stabilizes; the **first** SAGE Index (0–100 weighted rubric, Checklist-Manifesto
  style) is built. (The **second**, multiplicative Π(facets) training-filter instrument, evolves later
  — the two are complementary, not contradictory.)
- Combinations-matrix work begins ("SRP topics and combinations," Nov 9) — **4,648** first appears.
- Working-definitions register begins (Nov 10).
- **CCC arrives** ("SRP-CCC Training Plan," Nov 12) — Compare-Contrast-Consensus as the synthesis layer;
  the **three tiers** (LOW/MEDIUM/HIGH) land; pipeline sketched end-to-end.
- Causal-chain work (Nov 17–18); "Faking RL with reasoning" (Nov 19–20); first-person traces stabilize
  as the training-data format (Nov 21).
- *By end of Nov 2025 the core exists* (SAGE, SRP, CCC, tiers, methods library, 7 personas, killer-item
  gate, CODE/PARA, scratchpad) — *but not yet:* the Lawyer/Teacher facet additions, the 90–100% RLP
  constraint, the empirical foundations, the paper, or the canonical doc.

## Act 5 — Maturation (Dec 2025 – Mar 2026)
ChatGPT export ends ~Nov 2025; the rest happens in Claude (the 29 dated recaps).
- **Low-tier template work (Nov 27):** gold traces in ShareGPT JSON; **LOW hypotheses revised 2 → 3.**
- **Cognitive-architecture white paper (Dec 1):** introduces *structural confidence* (confidence from
  cross-trace agreement geometry, not a single trace's self-report) and the *compositional-library*
  framing.
- **IMR project naming stabilizes (Feb 9):** "Improving Model Reasoning" is the *project*; SAGE is its
  *output*.
- **SRP-CCC method analysis (Mar 3):** "three missing artifacts" framing stabilizes; **CCC is training
  scaffolding meant to be internalized** (don't test for visible CCC at runtime); **LOW absorbs CCC.**
- **SRP foundational components (Mar 4):** **THE most important single correction — SAGE is a
  pretraining data-curation filter, never a runtime checklist.** Plus: methodological diversity is
  cross-training not over-prescription (DeepSeek-R1 counter-evidence is domain-inapplicable because R1
  is binary-verification math/code); Mem0/LongRoPE = adapt not replace; high rejection is intentional.
- **Claude SAGE Thinking skill genesis (Mar 5):** three skills designed (SRP reasoning, SAGE facet
  enforcement, memory module). **Skills = runtime approximation / test scaffolding, not the deliverable.**
  Memory module integrates CODE/PARA/Zettelkasten/Checklist with **PARA modified by SAGE facets.**
  Naming corrected (SRP = Structure-Reasoning-Presentation). **Only numeric self-assessment baseline:**
  Comedian lands 30–40%; kill-steps rarely named unprompted; Therapist's collaborative patience
  overridden by base tendency to over-answer.
- **Foundational hypothesis (Mar 6):** origin = Neuro-Sama observation, not alignment theory.
  Combinations resolved to **4,779 exact** via CSV query (27/40/36).
- **Viability assessment (Mar 6):** word-embedding analogy for SAGE-score convergence (works only if
  rater variance is noise around a shared signal) → archetypal-definition work *is* scoring-viability
  work.
- **CogFound comparison (Mar 7):** CogFound's 28-element taxonomy chosen as an *independent* external
  evaluation instrument (uncontaminated by self-validation).
- **Nine components integration (Mar 7):** **90–100% RLP integration constraint lands** — all nine
  *components* must appear in 90–100% of training data; modularity forbidden. (Components ≠ facets.)
  Encoder-decoder ideal vs. decoder-only reality tension surfaces (unresolved).
- **Greek-stack vocabulary (Mar 10):** four-term stack (Ratiocination / Dianoia / Sublation / Diorthotic
  Logos) coined for "the active process of reasoning"; functional triple = clean, flow, coherent.
- **Greek-stack rejection (Mar 12):** the stack is **permanently rejected**; Weston replaces it with a
  single compound word — **and the chat ended before he recorded the word.** *This is the "lost compound
  word," recovery priority #1.* Also here: strongest thesis form — **alignment-as-capability.**
- **DataxLLM comparison (Mar 11):** 500+ reference survey confirms novelty; adds the **RoRL** alias.
- **9-facet version becomes canonical (Mar 19, "Master Reference Organized"):** Artist/Teacher split +
  Lawyer added; 7-facet preserved as the personal-practice version (not interchangeable).
- **Situational-awareness triad (Mar 25):** situational + context + linguistic awareness as a cyclical,
  mutually-constitutive unit (no canonical name yet); **dependency topology of meaning** introduced →
  new failure mode **concept-cluster fragmentation** (a trace names a concept but fails to activate its
  dependency partners — a hollow compound that reads correct but encodes nothing).

## Act 6 — System-level evaluation & consolidation (Apr – May 2026)
- **Academic paper** *Integrated Training Data Architecture for Cultivating Wisdom in AI* (Mar 17) —
  9-facet, full empirical foundations.
- **Comprehensive System-Level Evaluation (May 2026):** the load-bearing claim crystallizes —
  **"the emergent properties ARE the framework; wisdom can't be decomposed into parts,"** and **"the
  system, not the model, is the artifact"** (model + compiler + auto-validator + human auditors +
  dataset). Numerical corrections (cost efficiency ~10–18× not 100×, etc.).
- **`SAGE_FRAMEWORK_CANONICAL.md` (May 2026):** the three-layer source of truth (TL;DR / Core / Deep)
  with Working Definitions Register and Source Map / Drift Notes resolving 7-vs-9 facets, the
  combinations count, and "SAGE is not an acronym."

---

# PART IV — KEY CORRECTIONS, STATUS, AND OPEN ITEMS

## 25. The load-bearing corrections (drift bugs to guard against)
- **SAGE is a pretraining data-curation filter, never a runtime evaluator.** The single most important
  fact. Any doc hinting at SAGE-as-runtime is broken.
- **SRP = Structure-Reasoning-Presentation**, not "Structured Reasoning Process."
- **CCC is training scaffolding to be internalized** — mature models won't show visible CCC; don't
  evaluate for it at runtime.
- **The skills are runtime approximations / test scaffolding** — not the framework's deliverable.
- **Components (9) ≠ Facets (9).** Different lists, different jobs.
- **Methodological diversity = cross-training, not over-prescription**; the DeepSeek-R1 objection is
  domain-inapplicable (binary-verification vs. open-ended analytical).
- **WFC is a retired stepping-stone metaphor**, not the planning mechanism.
- **The Greek stack is rejected**; its replacement compound word is lost.
- **Two SAGE Index instruments coexist by design** (0–100 quarterly review vs. multiplicative
  per-trace filter) — not an inconsistency.

## 26. Status of major artifacts *(statuses re-audited 2026-07-02)*
| Artifact | Status |
|---|---|
| `SAGE_FRAMEWORK_CANONICAL.md` (3-layer + Working Defs + Source Map) | ✅ Exists (May 2026); **v2 exists (June 12, 2026)** — working reference, acceptance gated on translation test |
| Academic paper (Integrated Training Data Architecture) | ✅ Built (Mar 2026) |
| SRP-CCC causal chain | ✅ Documented (doc now in `03_Archives/superseded/` — content absorbed into canonical) |
| Three runtime skills (SRP, SAGE facets, memory) | ✅ Built (test scaffolding) |
| Methods library catalog (`methods_library.md`) | ✅ Documented |
| **Combinations matrix CSV** (4,779) | ✅ **Exists** (`01_Areas/SAGE_Methodology/`, verified June 12); validation pass pending |
| **Grading instrument** (`SRP_Grading_Sheet.md`, root) | ✅ Built (June 9, 2026) |
| **Compiler** (automated validation gate) | ❌ Not built |
| **Held-out evaluation set** | ❌ Not built — now the empirical keystone (ECW's saturating eval rubric is this gap in the wild) |
| **Seed gold-trace corpus** (50–100 expert traces) | ❌ Not built |
| **Generation-1 model** | ❌ Not trained |
| **The lost compound word** | ❌ Lost; recovery pending |
| Archetypal-depth facet definitions | 🟡 Reframed by the June 12 pivot: Therapist treatment = the template; open task is now **template extraction + archetype catalog build-out** (Canonical v2 §3.8) |

## 27. The three "missing artifacts" (the execution gap)
The canonical statement of *what it would take to move from documentation to a runnable experiment*:
(1) completed **gold traces in ShareGPT JSON**, (2) a **compiler specification**, (3) a **fixed
evaluation protocol**. Research-readiness and practitioner-readiness are independent axes — SAGE is
research-ready but not yet practitioner-ready.

## 28. Honest epistemic position
The framework is **theoretically grounded, structurally specified, operationally detailed, and
empirically untested as a whole.** Its greatest vulnerability is being untested; its greatest
opportunity is that no one else is generating the data point that would confirm or refute it.

---

## Appendix A — Load-bearing vocabulary (quick reference)
- **Distribution is Destiny** — training distribution determines model character.
- **Alignment-as-capability** — if the distribution is built correctly, misalignment is structurally
  impossible.
- **Multiplicative Wisdom** — `Π(facets)`; any facet at zero collapses the whole.
- **Phase Linkage / Phase Connectivity Check** — each phase's outputs must feed the next; validated
  before delivery.
- **Kill-Step** — a specific, falsifiable condition that says "abandon this approach."
- **Killer-Item Test** — critical AND easy to miss → the memory-write gate.
- **Adaptive Depth** — match structure visibility to complexity.
- **Genuine vs. Cosmetic Rivals** — real rivals make each other's advocates uncomfortable.
- **Source Trust Levels** — strong / moderate / weak / flagged → drive confidence numbers.
- **Epistemic Status Labels** — fact / inference / assumption / guess / value judgment.
- **Preserved Dissent** — unresolved disagreement survives as conditional recommendations.
- **Gold Trace** — a training example meeting all SRP/CCC/facet/scratchpad/citation requirements.
- **Scratchpad** — the transparency layer; every factual claim traces back to it.
- **Compiler** — automated validation gate (does not yet exist).
- **Concept-cluster fragmentation** — a trace names a concept without activating its dependency
  partners; a hollow compound.

## Appendix B — The nine facets (training-data filter) vs. seven (personal practice)
- **Nine (canonical training filter):** Therapist, Scientist, Philosopher, Engineer, Artist, Teacher,
  Comedian, Generalist, Lawyer.
- **Seven (personal-practice, in the "CLAUDE SAGE Thinking" preferences):** Therapist, Scientist,
  Philosopher, Engineer, **Artist/Teacher (combined)**, Comedian, Generalist — **no Lawyer.**
- *Not interchangeable:* nine filters training data; seven structures one's own thinking.

## Appendix C — The nine components (architectural commitments, ≠ facets)
PKM (CODE+PARA) · Checklist Manifesto (admission gate) · SRP (trace skeleton) · Zettelkasten (atomic
shape) · LongRoPE (long-session working memory) · Mem0 (memory operations) · SAGE persona system
(quality filter) · RLP/RoRL (embeds all into pretraining) · encoder-decoder architecture ideal
(unresolved vs. decoder-only reality). **Must appear in 90–100% of training data; modularity
forbidden.**

---

*End of outline. Subordinate to `SAGE_FRAMEWORK_CANONICAL.md`; correct against it where they differ.*
