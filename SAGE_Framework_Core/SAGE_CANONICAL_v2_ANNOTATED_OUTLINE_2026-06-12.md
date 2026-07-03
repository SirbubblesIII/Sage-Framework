# SAGE Canonical v2 — Annotated Outline (Build Spec)

**Date:** June 12, 2026 · **Author of underlying work:** Weston James Milhon
**Purpose:** Section-by-section build spec for the full v2 rewrite. Each section notes WHAT goes there, what CHANGED vs. v1, and which SOURCE feeds it.
**Succession rule (resolves v1's anti-fork clause):** v1 says "update, don't duplicate into a v2 that recreates drift." v2 is therefore written as *Revision 2 of the same canonical*, not a parallel document. On acceptance (gated by the translation test, decision note item 6.4), v1 moves to `03_Archives/superseded/` with an `_OLD` suffix and v2 takes the root slot. Until then v2 carries a status banner: *working reference; v1 retains authority on any point where they conflict.*

---

## FRONT MATTER
Title, author, revision history (v1 May 2026 → v2 June 2026), status banner, scope (SAGE + SRP-CCC + PKM + training architecture + vocabulary; adjacent projects excluded), How-to-Read (keep v1's three-layer scheme — it works).
*Changed vs v1:* adds revision history and the succession banner.

## LAYER 1 — TL;DR (one page, rewritten)
Same job as v1: five-minute re-entry, hand to any new collaborator. Must now state: distribution is destiny → alignment-as-capability; three pillars; **personality = profession-archetype catalog curated by the Core 11 editorial board** (no longer "nine facets are the personality"); SRP-CCC; PKM at four timescales; tool use inside reasoning (flagged); first-person traces, 50/50 split, reviewer critiques as a data class; candid epistemic position (untested as a whole; completion frames ~90–95% / ~50–60% / ~5–10%).
*Sources:* v1 TL;DR + DECISION_2026-06-12 + concept map §1, §2 ("Where it stands").

## LAYER 2 — CORE

### 2.1 The Core Thesis — Distribution is Destiny
Carry v1 nearly intact (it's the stable heart). Add the strongest one-sentence form: **alignment-as-capability** (Mar 12, 2026). Add the foundational-hypothesis origin: Neuro-sama observation → "personality is already being trained" → "what personality?" (leads the academic paper before the thesis).
*Sources:* v1 Core Thesis; concept map §2 (origin), §3.

### 2.2 The Three Inseparable Pillars (+ tool use, flagged)
Carry the mutually-constitutive triangle and triangle-failure diagnosis (hallucination/sycophancy/context collapse). Tool use gets explicit treatment: five reasoning properties include tool-integrated; **DECISION POINT for Weston** — v1 keeps tool use inside Reasoning with a fourth-pillar flag; v2 outline assumes *kept inside Reasoning but given its own section (2.7)* with stated promotion criteria (if tool-use patterns require their own archetype treatments, distribution quotas, and failure taxonomy, promote).
*Sources:* v1 Pillars; concept map §3.

### 2.3 The Personality Pillar, Rebuilt — Profession-Archetypes and the Core 11  ★ biggest change
The June 12 decision, fully integrated:
- Unit = **profession-archetype**; catalog target = hundreds; archetype-essence-first definition (Therapist treatment as template: essence → operational behavior → craft / zoom-in / zoom-out / interplay).
- **The Core 11** — Therapist, Scientist, Philosopher, Engineer, Artist, Teacher, Comedian, Generalist, Lawyer + **Systems Engineer + Coder** ("today, so far" — extensible). Dual role: (a) in the distribution as professions, (b) **the editorial board** — pipeline builders, graders, reviewers.
- **Out-of-expertise review** as the OOD mechanism; reviewer output = **filter AND data**.
- **Π(wisdom) relocated:** retired as per-trace 9-facet score; enforced at review; within a profession: craft × zoom-in × zoom-out × interplay.
- Facet descriptions preserved as *ingredient vocabulary* for archetype authorship.
- Keep: "training-data filter, not runtime evaluator" (now literally staffed); 7-facet personal-practice variant untouched; both SAGE Index instruments (checklist = personal quarterly; multiplicative = data filter) complementary by design.
- Open: Engineer/SysEng/Coder differentiation; priority tiers (therapist/doctor/lawyer-class weighting); "Researcher" facet (silently dropped in lineage) reviewed for catalog re-entry.
*Sources:* DECISION_2026-06-12; v1 facet section; concept map §3, §9.3–9.5.

### 2.4 The Reasoning Pillar — SRP-CCC
Carry v1 structure with concept-map precision corrections: **LOW tier = 3 rival hypotheses** (revised from 2, Nov 27 2025); genuineness test; phase linkage as the most important constraint + Phase Connectivity Check; CCC with **structural confidence** (confidence from cross-trace agreement geometry — promote from recovery files into canonical); adaptive depth (CCC scaffolding internalized, invisible at runtime); naming caution (SRP ≠ "Structured Reasoning Process").
Methods library: 27/40/36; **combinations = 4,779 — VERIFIED June 12, 2026 by direct count of the now-existing CSV** (`01_Areas/SAGE_Methodology/srp_combinations.csv`, 4,780 lines incl. header — which also explains the 4,779/4,780 drift). The CSV moves from "missing artifact" to "exists, needs validation pass."
The grading instrument: `SRP_Grading_Sheet.md` (100-pt, gates, three hard caps) named as the editorial board's scoring tool.
*Sources:* v1 SRP/CCC/tiers/methods; concept map §4, §9.1–9.2; June 12 CSV verification; grading sheet.

### 2.5 The Memory Pillar — PKM at Four Timescales
Carry v1's three-practices content, upgraded to the concept map's **four-system / four-timescale table** (Killer-Item · CODE · PARA · Zettelkasten). Keep: killer-item dual gate (DO-CONFIRM vs READ-DO modes), progressive summarization power law, working-definitions exemption, network-is-the-knowledge, not-RAG distinction, memory ops as conscious decisions with rationale. Add: **PARA-modified-by-facets** as a testable claim (what counts as actionable shifts with dominant archetype).
*Sources:* v1 memory section; concept map §5.

### 2.6 The Semantic Layer — Compound Concepts as Framework Infrastructure  ★ new section
Elevates compound concepts from one register entry to a load-bearing section, and answers the explicit request: the toolset for the Core 11.
- The four definitions (operational): **Concept** (stable co-activating feature cluster ≠ word ≠ dictionary entry), **Compound Concept** (binding with emergent meaning; co-occurrence is the binding mechanism), **Context Dependence** (multi-scale: lexical/sentence/discourse/domain/register), **Working Definition** (compound deliberately pinned to scope; revisable; reshapes the compound within scope).
- Why it's load-bearing for training: compound-concept formation through co-occurrence IS the mechanism full-stack trace integration relies on (v1 already says this); a **profession is a dense compound-concept cluster** — archetype definition is deliberate engineering of that cluster (the doctor "chest pain radiating to left arm" example).
- **As Core-11 tooling:** out-of-expertise reviewers, lacking the domain compound, are structurally positioned to detect shorthand; their toolkit = demand working definitions, check context dependence across scales, test for **concept-cluster fragmentation** (trace names a concept but fails to activate its dependency partners — hollow compound; promote this from "unnamed constructs" into the canonical failure-mode list).
- The binding compound concept: **reflexively-structured-wise-reasoning-with-active-memory** (each word load-bearing; remove-one analysis). Related: "the system is the artifact"; "the emergent properties ARE the framework."
- Open: the **lost compound word** (recovery priority #1); the cognitive triad {situational, context, linguistic awareness} — name and canonize or keep flagged; dependency topology of meaning (graph/hypergraph/lattice undecided).
*Sources:* compound-concepts SKILL.md; v1 register; concept map §7, §9.8–9.10.

### 2.7 Tool Use — Inside Reasoning, Watched for Promotion
Consolidate what v1 scatters: tools used as natural extensions of thought; bare-bones tool loop (search/fetch/calculate/memory-retrieve → evidence assessment → follow-ups); scratchpad rule — verbatim calls, simulated tool calls = checked failure mode; **gold-trace format constraint: tool calls outside thinking blocks** (llama.cpp/vLLM/LM Studio/Ollama compatibility — hard rule); Tools × Memory × Reasoning synergy. Promotion criteria stated (see 2.2).
*Sources:* v1 (scattered); concept map §6 format constraint.

### 2.8 The Training Data Specification (updated)
Carry v1: first-person traces, recursive loop, full-stack integration, 50/50 explicit-implicit (with the genuinely-rigorous constraint), ≥20% × five problem categories, scratchpad anchoring.
Add — the *Teaching Claude Why* integrations:
- **Principle-carrying data class:** traces must state the *why* at principle level, not only demonstrate behavior (demonstrations + principles together = most effective).
- **Reviewer-critique dialogues as a named data class** (the editorial board's out-of-expertise reviews enter the distribution).
- **The OOD warning as a design rule:** never train on the eval distribution; structurally-different principled data is the generalization mechanism; surface-conformity grading rebuilds the trap.
- Efficiency anchor: ~3M tokens of principled data ≈ ~85M of scenario training.
Also: the **nine components table** (≠ nine facets — keep §8's disambiguation): PKM, Checklist, SRP, Zettelkasten, LongRoPE, Mem0, persona filter (now: archetype catalog + Core 11), RLP/RoRL, encoder-decoder ideal — with the 90–100% co-presence constraint that defines RLP-style integration.
*Sources:* v1 spec; concept map §6, §8; DECISION_2026-06-12; Teaching Claude Why (alignment.anthropic.com/2026/teaching-claude-why/).

### 2.9 The Pipeline and Bootstrap Loop (updated)
Carry v1 stages, re-cast with the staffed editorial layer: sourcing → complexity classification → method selection (matrix) → archetype-voiced generation → **compiler** (structural) → **Core-11 editorial review** (out-of-expertise; substantive; critiques captured as data) → human audit → formatting → composition. Seed 50–100 gold traces; 1.5–7B Gen-1; 80–95% early rejection; budget $2M–$6M, ~10–18× efficiency claim (100× retracted). Bootstrap caveat: needs the fixed eval set to distinguish improvement from mode collapse.
*Sources:* v1 pipeline; concept map §6; decision note.

### 2.10 Emergent Properties (carry, lightly updated)
Self-correction, hallucination resistance (~10–15% vs 40–50%), contextual adaptation, intrinsic alignment, transparent reasoning, calibrated confidence, continuous improvement. Add cross-reference: intrinsic alignment claim now has the Teaching-Claude-Why generalization evidence shape behind it.

## LAYER 3 — DEEP

### 3.1 Research Foundations and the Reading List  ★ expanded per request
- The five empirical lines, carried from v1 with citations intact: pretraining primacy (LIMA, Lin, Phi-1/2, DoReMi); alignment shallowness (Qi, Arditi, Young, Sleeper Agents); shared substrate (H-Neurons, ~0.97 stability, over-compliance); single-component degradation (o3 hallucination doubling, RLHF sycophancy); compound-concept representation (Templeton SAE 34M features, Frame Representation Hypothesis, Representation Engineering).
- **2026 additions:** *Teaching Claude Why* (principles > demonstrations; OOD generalization; eval-distribution warning) — slots into lines 2 and 5. **Open check:** Persona Hub (breadth-without-depth precedent; novelty-claim audit before public use).
- **The numbered reading list mapped to components** (#1 RL on Pre-Training Data → RLP; #2 CoT+RAG reliability; #3 Structured Reasoning → SRP; #4 Stress-Testing Model Specs → character consistency; #5 Mem0 → memory ops; #6 RLP; #7 CogFound → external eval; #8 Agentic Organization; #9 Hallucination mitigation; #10 CharacterGPT + #14 PersonaLLM → persona/archetype precedent; #11 psychoanalysis/personality theory → archetype depth; #12 RAG (the contrast case); #13 Nondeterminism → eval reliability; plus A-MEM, Checklist-Guided Memory, Context Engineering 2.0, LongRoPE, Attention Residuals, Bitter Lesson as the counter-weight argument).
- External validation instruments: CogFound 28-element taxonomy (mapping table still needed); DataxLLM (independent Distribution-is-Destiny convergence; "no SAGE equivalent in 500+ references" — pending Persona Hub audit).
- Theoretical defenses (promote from concept map §12 into canonical): word-embedding convergence (+ caveat), domain-mismatch vs. DeepSeek-R1 (now partially *absorbed* by Coder-in-Core-11), scale anchors.
*Sources:* v1 Layer 3; concept map §12; Research_Papers folder; decision note §5.

### 3.2 Component Interactions (carry from v1)
Structure×Diversity, SAGE×SRP, Iteration×QC, Tools×Memory×Reasoning, Compiler×Human-audit — updated so "SAGE×SRP" reads as "archetype-balance×SRP" and Compiler×Human-audit becomes Compiler×Editorial-board×Human-audit.

### 3.3 The Operational Sequence (bare-bones, carry from v1)
Runtime walkthrough essentially unchanged; note LOW = 3 rivals; adaptive-depth governs surfacing.

### 3.4 Quality Gates and Failure Modes (updated)
Carry six: mode collapse, cosmetic rivals, simulated tool calls, superficial engagement (now: superficial *archetype* engagement), compiler overfitting, distribution drift. **Add two:** concept-cluster fragmentation (semantic hollowness — detected via the 2.6 toolkit) and **surface-conformity review** (the Teaching-Claude-Why trap, named as a gate on the editorial board itself). Carry the validation gap and inter-rater reliability discussion (word-embedding defense cross-ref); bootstrap problem + eval-set criticality.

### 3.5 The Open Strategic Fork — Path A vs Path B
Promote from concept map §10 into the canonical (v1 omitted it): SRP-dominant pretraining vs two-stage; kill-steps for each; the empirical crux (how late can reflex be installed); poisoning reframe (shape-corruption, not fact-density); decoder-only multi-token-planning question gating encoder-decoder.

### 3.6 History — Six Acts (compact)
New in canonical (one page): Apr 2023 seeds → MoE-review ancestor of the facets → convergence → SRP/SAGE/CCC crystallization (Nov 2025) → maturation + 9-facet canonical (Mar 2026) → consolidation + system-is-the-artifact (May 2026) → **profession-archetype pivot (June 2026)**. Neuro-sama origin stated as the foundational hypothesis. Retired names registry: C-SRP, PCC, SRL→P, SYNTH-Mind, GRaPE-Flash, AWSI, Greek stack (rejected; dianoia/noesis survives).
*Sources:* concept map §2, §9.7, §9.9.

### 3.7 Confidence Calibration of Major Claims (carry, re-audit)
Carry v1's four bands; re-audit each claim against June state (e.g., "facet filter creates different optimization target" → restate for archetype catalog; add calibration entries for the pivot itself: out-of-expertise review mechanism = moderate confidence pending pilot).

### 3.8 Known Open Questions (updated roll-up)
Minimum viable dataset; archetype ratio (was facet ratio); 50/50 validation; RLP↔review reward integration; CSV validation pass; compiler; eval set; seed traces; five missing archetype-depth treatments → now: **template extraction + catalog build-out**; lost compound word; cognitive triad naming; ontology of AI vs human reasoning; Engineer/SysEng/Coder boundaries; Persona Hub audit.

### 3.9 What This Framework Does Not Do (carry, add)
Carry v1's honest boundaries. Add: does not claim the Core 11 list is final; does not claim archetype catalogs eliminate the need for the compiler or human audit.

## WORKING DEFINITIONS REGISTER (updated)
Carry all v1 entries (full-detail, never compressed). **Add:** Profession-Archetype; Core 11; Editorial Dual-Role; Out-of-Expertise Review; Reviewer-Critique Data Class; Structural Confidence; Concept; Compound Concept (upgrade existing entry with operational definition); Context Dependence; Working Definition (self-referential entry); Concept-Cluster Fragmentation; Alignment-as-Capability; Nine Components (vs Nine Facets disambiguation); RLP/RoRL; Path A / Path B. **Amend:** Multiplicative Wisdom (relocated to review); The Nine Archetypal Facets (historical + ingredient vocabulary + 9/11 of Core roster).

## SOURCE MAP AND DRIFT NOTES (updated)
Carry v1's source map; add: DECISION_2026-06-12, concept map rev 2, grading sheet, compound-concepts skill, Teaching Claude Why, CSV verification (June 12). Drift resolutions updated: 4,779 verified at source (header-line explanation); facets 7 vs 9 vs **Core 11** (three coexisting objects, three purposes); dual SAGE Index complementary. Staleness triggers re-listed (translation test result; template built; first archetype batch; compiler; eval set; Gen-1 model; Persona Hub audit).

---
*Build notes: full rewrite target ~35–45KB, tight prose, v1's voice. Hard figures to use: 4,779 (verified) · 27/40/36 · LOW=3 rivals · tiers 1/3/5 · ≥20%×5 · 50/50 · 90–100% components · seed 50–100 · 1.5–7B · 80–95% rejection · $2M–$6M · ~10–18× · ~3M≈85M tokens.*
