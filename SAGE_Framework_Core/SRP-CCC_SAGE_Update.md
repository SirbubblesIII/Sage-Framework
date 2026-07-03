# SRP-CCC / SAGE — Reference Overview, Changelog & Continuity

> **What this file is:** A compact, re-entry reference for the SAGE framework and its SRP-CCC
> methodology, paired with a running changelog and a continuity/status log. It is the "catch
> me up in a few minutes, then show me what's changed and what's open" file.
>
> **Source of truth:** `SAGE_FRAMEWORK_CANONICAL_v2_2026-06-12.md` (root — Revision 2, the
> working reference), with the succession caveat: **v1 (`SAGE_FRAMEWORK_CANONICAL.md`) retains
> authority on any point where they conflict, until the translation test passes.** Same
> three-layer scheme (TL;DR → Core → Deep + Working Definitions Register + Source Map). This
> file *summarizes and tracks* — it does not override the canonical. Where they ever disagree,
> the canonical wins, and this file should be corrected to match.
>
> **Author of the framework:** Weston James Milhon
> **PARA placement:** Area (ongoing standard). **Last updated:** 2026-07-02.

---

## 1. The Framework in One Pass

SAGE is a **wisdom-cultivation architecture for AI**. Its central thesis is **distribution is
destiny**: a model exhibits whatever character its training distribution made the only
available reference frame, so alignment is built in at the data level rather than bolted on
afterward.

It rests on **three inseparable pillars** — *personality, reasoning, memory* — treated as
three descriptions of one cognitive process rather than three modular subsystems. Each
contains the other two, and the common AI failure modes (hallucination, sycophancy,
false-premise acceptance, jailbreak vulnerability) are "triangle failures" that share a
substrate, which is why the fix has to happen in the training distribution.

- **Personality** → rebuilt June 12, 2026: operationalized as a **profession-archetype
  catalog** (target: hundreds) curated by the **Core 11 editorial board** (see §2). The nine
  facets survive as ingredient vocabulary; Π(wisdom) is enforced at review rather than scored
  per trace.
- **Reasoning** → operationalized as **SRP** (Structure → Reasoning → Presentation), with
  **CCC** synthesis (Compare → Contrast → Consensus) when more than one pass is warranted (§3).
- **Memory** → operationalized as **three knowledge-management practices at three timescales**:
  Gawande's killer-item gate (capture), Forte's CODE + PARA (session lifecycle / organization),
  and Zettelkasten (long-term atomic linking) (§4).

Training data is **first-person reasoning traces** showing all of this happening at once, held
to a **50/50 explicit-implicit split** and a minimum-diversity rule across problem types. The
honest epistemic position: the framework is *theoretically grounded, structurally specified,
operationally detailed, and empirically untested as a whole.*

---

## 2. The Personality Pillar — Profession-Archetypes and the Core 11

**Rebuilt June 12, 2026** (`DECISION_2026-06-12_Facets_to_Professions.md`, integrated into
Canonical v2 §2.3). The unit is now the **profession-archetype** (archetype-essence-first
definition; catalog target = hundreds). The **Core 11** — the nine facets below plus **Systems
Engineer** and **Coder** ("today, so far" — extensible) — plays a dual role: (a) professions in
the distribution, (b) **the editorial board** that builds the pipeline, grades, and reviews
**out-of-expertise** (the OOD mechanism; reviewer output is both filter AND data).

**Π(wisdom) relocated:** retired as a per-trace 9-facet score; enforced at review. Within a
profession it reads craft × zoom-in × zoom-out × interplay. The principle survives — any zero
still collapses the whole — it's just applied by the board, not scored per trace. The facets
below are preserved as **ingredient vocabulary** for archetype authorship, and the whole
apparatus remains a **training-data filter, not a runtime evaluator** (now literally staffed).

| Facet | Cognitive contribution |
|---|---|
| **Therapist** | Attunement, holding space, respecting agency/consent, reading what's under the surface, intervention timing. |
| **Scientist** | Hypothesis generation, evidence evaluation, methodology critique, uncertainty management; won't mistake correlation for causation. |
| **Philosopher** | Surfaces assumptions, analyzes concepts, separates true from wished-true, distinguishes empirical from normative. |
| **Engineer** | Constraints, failure modes, practical trade-offs; keeps asking how it actually works in the real world. |
| **Artist** | Creative process, aesthetic decisions, meaning; turns methods into stories, mental pictures, reusable shapes. |
| **Teacher** | Calibrates explanation, reads confusion, builds understanding incrementally; concept difficulty ≠ explanation difficulty. |
| **Comedian** | Observational insight, timing, truth-through-humor; keeps reasoning from getting brittle or self-serious. |
| **Generalist** | Cross-domain pattern recognition, analogical reasoning, perspective synthesis; translates between frames. |
| **Lawyer** | Argumentation, precedent, adversarial thinking; stress-tests claims so they're defensible, not just plausible. |

> **Important version note — 7 vs 9 vs Core 11.** Three coexisting objects, three purposes —
> **don't collapse them.** The **seven-facet** version — Therapist, Scientist, Philosopher,
> Engineer, **Artist/Teacher (combined)**, Comedian, Generalist, **no Lawyer** — is the
> **personal-practice** version embedded in the "CLAUDE SAGE Thinking" preferences (untouched
> by the pivot). The **nine-facet** version above is the historical training-data-filter
> version (used in the architectural paper), now serving as **ingredient vocabulary** and as
> 9/11 of the Core roster. The **Core 11** (nine + Systems Engineer + Coder) is the current
> editorial board and archetype seed. Seven structures your own thinking; nine/Core-11 filter
> training data.

---

## 3. SRP-CCC Methodology

### Adaptive Depth
Match the *visibility* of SRP structure to task complexity: **light touch** (run moves
internally, show a clean answer), **visible structure** (surface the phases), **full SRP**
(phase-by-phase with explicit method selection; CCC at MEDIUM/HIGH).

### Phase 1 — STRUCTURE (define before you reason)
Restate the goal in your own words; map entities/relationships/dependencies; draw boundaries
(in/out, and why); surface constraints and flag fragile assumptions; define concrete
success/failure; calibrate detail deliberately. Select a Structure method to fit the problem.

### Phase 2 — REASONING (think with genuine alternatives)
Generate **2+ genuinely distinct** approaches (labeled A/B/C, no favorite); seek evidence
**both** ways; name a concrete **kill-step** per approach; design **discriminating tests**;
verify sources (authority, bias, track record, recency, corroboration, methodology) and assign
**trust levels** (strong / moderate / weak / flagged); mark each claim's **epistemic status**
(fact / inference / assumption / guess / value judgment). Select a Reasoning method.

### Phase 3 — PRESENTATION (make it usable)
Format for the audience; lead with the answer; calibrate confidence as a **number tied to
evidence quality**; make next steps concrete; **preserve dissent** ("A if X, B if Y"); source
every claim.

### Phase Linkage (the single most important constraint)
Every output of one phase must feed the next: entities → hypotheses; boundaries → scope;
fragile assumptions → first test targets; source trust → confidence numbers; kill-steps →
caveats; discriminating tests → next steps. Breaks are treated as **critical errors**. The
**Phase Connectivity Check** is the pre-delivery validation that this chain held.

### CCC Synthesis (MEDIUM and HIGH tiers)
**Compare** agreements (convergence from *different* methods is stronger); **Contrast**
disagreements and what drives them (ontological / epistemological / value / method-suitability /
blind-spot); **Consensus** that preserves real dissent as conditional recommendations and names
what would flip it.

### Complexity Tiers
- **LOW** — one SRP trace, **3 rival hypotheses** (revised from 2, Nov 27 2025 — concept map
  rev 2 correction), no CCC. Clear/factual/straightforward problems.
- **MEDIUM** — three traces (3 different Structure + 3 different Reasoning methods) + full CCC.
  Multi-stakeholder, moderate ambiguity.
- **HIGH** — five traces, maximum methodological diversity + extended CCC. Wicked / high-stakes /
  contested-framing problems.

### Methods Library & Combinations Matrix
**27 Structure × 40 Reasoning × 36 Presentation** methods, with **4,779 validated S-R-P
combinations**. The CSV **now exists**: `01_Areas/SAGE_Methodology/srp_combinations.csv`,
**verified June 12, 2026 by direct count** (4,780 lines including header — which explains the
old 4,779/4,780 drift; earlier docs also cite 4,648). Status: exists, needs a validation pass.

### The Grading Instrument
`SRP_Grading_Sheet.md` (root) — 100-point weighted checklist with Pass/Fail gates and three
hard caps; named in Canonical v2 §2.4 as the editorial board's scoring tool.

---

## 4. Memory as Procedural Skill

Three practices, three timescales:

- **Killer-Item Gate** (Gawande) — narrowest timescale. Store only if **critical AND easy to
  miss**. Prevents memory bloat.
- **CODE** (Forte) — session timescale. **C**apture → **O**rganize (by actionability, via PARA)
  → **D**istill (progressive summarization) → **E**xpress (use it in real work).
- **Zettelkasten** (Luhmann/Ahrens) — long timescale. Atomic notes, one idea each, written in
  your own words, densely linked. Value grows faster than size. *Working definitions are exempt
  from compression — they stay full because the precision is the point.*

**PARA** organizes by actionability, not topic: **Projects** (active, has an endpoint),
**Areas** (ongoing standards, no completion date), **Resources** (reference), **Archives**
(done/inactive, preserved with reasoning). Items move between buckets as actionability changes.

Distinguished from **RAG**, which is similarity-lookup bolted on; here memory management is
trained as an intrinsic cognitive operation, shown in traces as conscious decisions with stated
rationale.

---

## 5. Load-Bearing Vocabulary (quick reference)

Full definitions live in the canonical Working Definitions Register; never swap these for
colloquial synonyms.

- **Distribution is Destiny** — training distribution determines model character.
- **Multiplicative Wisdom** — `Π(facets)`; any zero collapses the whole.
- **Phase Linkage** / **Phase Connectivity Check** — outputs of each phase must feed the next;
  validated before delivery.
- **Kill-Step** — a specific, falsifiable condition that says "abandon this approach."
- **Killer-Item Test** — critical AND easy to miss → the memory-write gate.
- **Adaptive Depth** — match structure visibility to complexity.
- **Genuine vs. Cosmetic Rivals** — real rivals make each other's advocates uncomfortable.
- **Source Trust Levels** — strong / moderate / weak / flagged; drive confidence numbers.
- **Epistemic Status Labels** — fact / inference / assumption / guess / value judgment.
- **Preserved Dissent** — unresolved disagreement survives as conditional recommendations.
- **Gold Trace** — a training example meeting all SRP/CCC/archetype/scratchpad/citation requirements.
- **Scratchpad** — the transparency layer; every factual claim must trace back to it.
- **Compiler** — automated validation gate (does not yet exist as a working artifact).
- **SAGE / SRP / CCC** — brand name for the whole framework / the methodology / the synthesis layer.
- **Profession-Archetype** — the personality unit post-pivot; a dense compound-concept cluster,
  defined essence-first (essence → operational behavior → craft / zoom-in / zoom-out / interplay).
- **Core 11** — the nine facets + Systems Engineer + Coder; professions in the distribution AND
  the editorial board (out-of-expertise reviewers whose critiques enter the data).
- **Alignment-as-Capability** — the strongest one-sentence form of Distribution is Destiny.
- **Structural Confidence** — confidence read off the geometry of cross-trace agreement in CCC.
- **Naming caution:** "SAGE" means ONLY this cognitive framework. The runtime layer formerly
  called "SAGE Runtime" was renamed **ECW** (Experimental Cognitive Wrapper) on 2026-06-23
  precisely to kill that collision; `S/A/G/E` in ECW is loop phase-notation, unrelated.

---

## 6. Continuity / Status

> *Refreshed 2026-07-02. Refresh at session end.*

**State of the canonical:** **Canonical v2 exists** (`SAGE_FRAMEWORK_CANONICAL_v2_2026-06-12.md`,
root) — Revision 2 of the same document, integrating the profession-archetype pivot, the
semantic layer (compound concepts as framework infrastructure), consolidated tool use, expanded
research foundations (incl. *Teaching Claude Why*), and source-verified figures. **Acceptance
is gated by the translation test, which has not been run/passed yet** — until then v1 retains
authority where they conflict, and both stay at root. The build spec behind v2 is
`SAGE_CANONICAL_v2_ANNOTATED_OUTLINE_2026-06-12.md` (this folder).

**The June 12 pivot** (biggest change since this file's last update): personality pillar
rebuilt around profession-archetypes and the Core 11 editorial board — see §2. The May
"which frame is this project for?" four-option decision was **overtaken by events**: the
body-of-thought frame got its Revision 2, and the operational frame moved into ECW (below).
No option was formally picked.

**The framework's first operational instantiation is live:** the **ECW** (Experimental
Cognitive Wrapper, ex-"SAGE Runtime", renamed 2026-06-23) is being embedded into the Odysseus
app (`/Users/mayabeyer/odysseus`, branch `ecw-runtime`) — a runtime layer externalizing
structuring/reasoning/self-monitoring/memory into durable machinery, with SRP deep-research
mode as the main test surface. Design layer: `00_Projects/Experimental-Cognitive-Wrapper/`.
Its measured keystone gap — **the eval rubric saturates; no real fitness signal** — is the
same missing-eval-set problem named below, now encountered empirically.

**Artifact scorecard (was "three missing artifacts"):**
- ~~`srp_combinations.csv`~~ — **EXISTS** (`01_Areas/SAGE_Methodology/`), 4,779 verified
  June 12; needs a validation pass.
- **Grading instrument** — **EXISTS** (`SRP_Grading_Sheet.md`, root; June 9).
- The **Compiler** (automated validation gate) — still missing.
- A **fixed held-out evaluation set** — still missing, and now empirically the keystone
  (ECW's saturating rubric is this gap manifesting).
- A **seed gold-trace corpus** (50–100 expert-crafted traces) — still missing; the creation
  guide (`01_Areas/Skills_and_Applied/SRP_CCC Gold-Trace Creation Guide.md`) predates the
  pivot (traces are now archetype-voiced with Core-11 editorial review).

**Recently resolved:** the 4,779/4,780 drift (header line — 4,779 is the verified count);
the dual-SAGE-instrument framing (complementary by design, same shape as the 7-vs-9-vs-Core-11
distinction); the SAGE/SAGE-Runtime name collision (runtime renamed ECW).

**Where things live (July 2, 2026 PARA passes):** superseded SRP-era docs (Nov 2025 analysis,
Apr system-level evaluation, Apr SRP/PKM conversation review, Mar methodology docx/pdf set)
→ `03_Archives/superseded/`. Paused projects → `03_Archives/on_ice/`. Active projects are
down to: ECW, Meaning_Space, and the two Wayfarer game folders. Navigation: `INDEX.md` (root).

**Known collaboration preferences:** concise and direct; collaborative and step-by-step; ask
before running heavy work end-to-end; transparency about sources and confidence.

---

## 7. Changelog

> *Newest first. One dated entry per change.*

### 2026-07-02 — Post-pivot refresh (June 12 → July 2 caught up)
- **Re-pointed source of truth to Canonical v2** (with the v1-retains-authority-until-
  translation-test caveat, per the succession rule in the annotated outline).
- **§2 rebuilt** for the profession-archetype pivot: Core 11 editorial board, out-of-expertise
  review, Π(wisdom) relocated to review; facet table kept as ingredient vocabulary; version
  note expanded from 9-vs-7 to **7 vs 9 vs Core 11** (three objects, three purposes).
- **§3 corrected:** LOW tier = 3 rival hypotheses; combinations = **4,779 verified** (CSV now
  exists at `01_Areas/SAGE_Methodology/srp_combinations.csv`); added the grading instrument.
- **§5 additions:** Profession-Archetype, Core 11, Alignment-as-Capability, Structural
  Confidence, and the SAGE ≠ ECW naming caution.
- **§6 fully refreshed:** v2 status, pivot, ECW as first operational instantiation, artifact
  scorecard (CSV + grading sheet now exist; compiler / eval set / seed corpus still missing),
  July 2 file locations.

### 2026-05-29 — Rewrite (corrected)
- **Corrected the facet count to nine** (added Artist/Teacher split + Lawyer); added the
  explicit 9-vs-7 version note. Previous draft wrongly used the 7-facet SKILL.md.
- Re-grounded the whole file in `SAGE_FRAMEWORK_CANONICAL.md` rather than the runnable skill
  summaries; corrected combinations count to **4,780** (27/40/36) and flagged the missing CSV.
- Added load-bearing vocabulary section aligned to the canonical Working Definitions Register.
- Replaced placeholder continuity with **real status** drawn from the May 22–28 weekly-status
  files (the hanging "which frame" decision, the three missing artifacts, the G5 scenarios).
- Marked this file as an Area-level summary that defers to the canonical as source of truth.

### 2026-05-28 — Initial draft (superseded)
- First version built only from the `srp-reasoning` and `sage-memory` SKILL.md files. Used the
  older 7-facet model and summary-level counts. Kept here for history; corrected above.

---

*To maintain: refresh §6 at session end, append dated entries to §7, and keep this file
subordinate to the canonical (v2, with the v1 succession caveat). If the canonical changes
(translation test passed, compiler built, eval set built, CSV validation pass done, first
archetype batch authored, Gen-1 trained), update there first, then reflect the change here.*
