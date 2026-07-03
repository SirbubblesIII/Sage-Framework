# DECISION — Facets → Professions (Personality Pillar Rebuild)

**Date:** June 12, 2026
**Status:** Adopted (Weston, working session with Claude). Supersedes — does not delete — the 9-facet SAGE metric.
**Supersedes:** `SAGE_FRAMEWORK_CANONICAL.md` § "The Nine Archetypal Facets" *as the personality-pillar architecture and as the trace-scoring metric*. The facet descriptions themselves remain valid as ingredient vocabulary (see §4).
**Untouched:** The 7-facet personal-practice variant ("CLAUDE SAGE Thinking" preferences). Per the canonical's drift resolution, it serves a different purpose and is unaffected by this pivot.
**Provenance:** Conversation thread June 11–12, 2026 (archetype reframe → profession scaling → editorial review layer). Trust level: decision, not finding — rationale below, kill-steps in §7.

---

## 1. The decision in one paragraph

The nine facets were a coverage taxonomy mistaken for a personality ontology. They were Weston's first attempt to classify what *kinds of cognitive content* a wisdom-training distribution must span — and the archetypal-depth treatment (the Wounded Healer/Winnicott/Rogers work done for Therapist) was the actual generalizing engine all along. The unit of the personality pillar is therefore now the **profession-archetype**: any profession can receive the archetype-first treatment and generate first-person gold traces — synthetic thought, the model reasoning *as* a wise instance of that profession, with the SRP spine and PKM habits in every trace. The catalog target is **hundreds of professions**, built linearly and independently (no joint cross-referencing constraint at generation time). The SAGE Index as a 9-dimension multiplicative score on every trace is retired.

## 2. The architecture — three roles

**Generators (the catalog, hundreds).** One archetype definition per profession: archetypal essence first, then operational behavior, then craft + zoom-in (the details that make or break the work) + zoom-out (where the work sits — stakes, people, consequences) + the interplay between levels. Each profession's trace set stands alone; the work is parallelizable.

**The Core 11 (editorial board).** The original nine — Therapist, Scientist, Philosopher, Engineer, Artist, Teacher, Comedian, Generalist, Lawyer — plus **Systems Engineer** and **Coder**. Decided June 12: eleven *today, so far* — the roster may grow. The Core 11 are **dual-role**:

1. *In the distribution* — they are professions like any other catalog entry, with their own archetype definitions and trace sets.
2. *The editorial team* — they are the data factory's staff: pipeline builders (Systems Engineer, Coder), graders (applying `SRP_Grading_Sheet.md`), and cross-domain reviewers of the catalog's output.

**Review assignment rule: out-of-expertise.** Reviewers are deliberately assigned to data *outside* their own domain. An in-domain expert accepts shorthand; an outsider cannot — so review forces every trace to carry its reasoning at principle level ("why this and not that," stated, not assumed). This is the OOD-generalization mechanism (see §5).

## 3. What survives, what dies, what moves

| Element | Fate |
|---|---|
| 9-facet multiplicative metric (Π across facets per trace) | **Retired** as a per-trace score |
| Multiplicative-wisdom principle | **Preserved, relocated** — enforced at *review*, not generation; within a profession: craft × zoom-in × zoom-out × interplay, any zero collapses |
| The nine facet definitions | **Preserved as ingredient vocabulary** for writing archetype definitions (a wise doctor's archetype *contains* consent, failure-mode thinking, assumption-surfacing as part of doctoring) — and as 9 of the Core 11 |
| "Facets are a training-data filter, not a runtime evaluator" | **Vindicated and literalized** — the filter is now staffed: the Core 11 *are* the filter |
| Distribution is destiny; first-person gold traces; 50/50 explicit/implicit | Unchanged |
| SRP-CCC (reasoning pillar), PKM (memory pillar) | Unchanged — SRP already encodes the micro/macro move (Structure = zoom-out, Reasoning = zoom-in) |
| CCC | Gains a second venue: generator vs. cross-domain reviewer is compare–contrast–consensus at the factory level |
| 7-facet personal-practice variant | Unchanged |

## 4. Reviewer output is both filter AND data

Adopted June 12: reviewer critiques do double duty. They gate traces (accept/revise/reject against the grading sheet), **and the critique dialogues themselves enter the distribution** — synthetic thought about thought. This is the highest-leverage reading of the *Teaching Claude Why* result (its lesson 3: teaching the model to explain *why* some actions are better beats demonstrations alone; demonstrations + principles together is best). The editorial layer's own work products — review dialogues, grading decisions, pipeline-design reasoning — are simultaneously in-domain content for the Core 11's own trace sets. The factory documents itself as data.

## 5. Evidence anchors

- **Teaching Claude Why** (Anthropic Alignment Science Blog, Kutasov & Jermyn et al., May 8, 2026 — https://alignment.anthropic.com/2026/teaching-claude-why/):
  - Training on demonstrations near the eval distribution suppressed misalignment *without* OOD generalization — and masked it from detection. Warning transferred to SAGE: review must demand stated reasons, not surface/format conformity, or the trap is rebuilt.
  - Structurally different, principle-carrying data generalized strongly (chat-format ethical-advice transcripts → zero agentic misalignment in tool-use evals; constitution documents and stories of admirable AIs also worked).
  - Efficiency datum for the §12 "small-but-curated competes" defense: ~3M tokens of principled advice data matched ~85M tokens of scenario-specific training.
- **Why Coder strengthens the architecture:** code is a binary-verifiable domain. Coder traces are objectively gradeable, anchoring grader calibration with ground truth — which partially *absorbs* the DeepSeek-R1 objection (concept map §12) instead of only deflecting it via domain-mismatch.
- **Prior-art check (OPEN):** Tencent's Persona Hub (~2024, from training knowledge, unverified) scaled synthetic data with ~1B shallow personas. SAGE's differentiators: archetypal *depth*, the shared SRP/PKM spine, and the staffed editorial layer. Needs a literature pass before the novelty claim ("no SAGE equivalent in 500+ references") is repeated in public-facing docs.

## 6. Open items

1. **Engineer vs. Systems Engineer vs. Coder** — three engineering-flavored archetypes now coexist. Definitions must be made non-overlapping: Engineer = constraints/failure-modes/trade-offs as a cognitive stance; Systems Engineer = whole-system integration, interfaces, requirements flow-down; Coder = implementation craft and verifiable artifacts. Needs the archetypal-depth treatment to hold the line.
2. **Archetype definition template** — extract the Therapist treatment into a reusable template (essence → operational behavior → craft/zoom-in/zoom-out/interplay → trace-generation prompts) so catalog work is mechanical.
3. **Priority tiers** — therapist/doctor/lawyer-class professions likely deserve larger distribution share; ratio unspecified (inherits the canonical's open question on archetypal-perspective ratios).
4. **Translation test** (discriminating check, cheap): re-describe one existing Therapist gold trace in the new schema. Nothing lost → schemas equivalent, new one more general. Something won't fit → facets carry content the recipe can't regenerate; revisit §3.
5. **Persona Hub literature pass** (§5).
6. **Canonical update** — this note stales `SAGE_FRAMEWORK_CANONICAL.md` by its own staleness criteria; a rev is needed but deliberately deferred until the translation test (item 4) passes.

## 7. Kill-steps — what would reverse this decision

- The translation test (item 6.4) *loses* content that the catalog recipe cannot regenerate → restore facets as a generation-time constraint alongside professions.
- Archetype treatment for a non-knowledge-work profession (nurse, plumber, farmer) comes out hollow/generic after honest effort → the per-profession move fails; the original 9 carried irreplaceable content.
- Cross-domain review degenerates into surface-conformity grading in practice (the Teaching-Claude-Why trap) and can't be fixed by sharpening the grading sheet → the editorial mechanism is unsound.
- A literature pass shows the depth+spine+editorial combination already exists published → novelty claim retracted (architecture may still stand on merit).

## 8. Working definitions added

- **Profession-archetype** — the unit of the personality pillar: one profession given archetype-first definition, generating first-person gold traces.
- **Core 11** — the dual-role roster (9 original facets + Systems Engineer + Coder): in-distribution professions *and* the editorial team. "Today, so far" — extensible.
- **Out-of-expertise review** — assignment rule placing reviewers outside their domain to force principle-level explanation; the OOD mechanism.
- **Editorial dual-role** — the property that the factory staff's work products (reviews, grading, pipeline reasoning) are simultaneously training data.

---
*Logged by Claude SAGE Thinking from the June 11–12 working sessions. Next session: load this note alongside the canonical; treat canonical § "Nine Archetypal Facets" as superseded-as-metric.*
