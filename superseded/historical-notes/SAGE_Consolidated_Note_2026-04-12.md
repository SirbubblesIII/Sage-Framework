# Consolidated Self-Note — SAGE / SRP-CCC State of the Project
**Date:** 2026-04-12
**Purpose:** Single re-loadable reference that reconciles older docs with the current nine-facet SAGE definition. Reading this should be enough to recover the project's state without re-deriving it.

---

## 1. The correction that needs to propagate

**SAGE has NINE facets, not seven.** Several older project docs still say "seven" — they are stale and must be read with that correction in mind.

### The nine facets (current, authoritative — from *Integrated Training Data Architecture for Cultivating Wisdom in AI Systems* and *A Framework for Training Wisdom: The Integrated Mind Architecture*):

1. **Therapist** — therapeutic presence, attunement, holding space, intervention timing. (Wounded-Healer archetype; Winnicott holding, Rogers' core conditions.)
2. **Scientist** — live discovery, hypothesis generation, evidence evaluation, uncertainty management.
3. **Philosopher** — assumption surfacing, conceptual analysis, thought experiment, ethical reasoning.
4. **Engineer** — constraint identification, trade-off evaluation, failure analysis, solution iteration.
5. **Artist** — vision formation, medium exploration, aesthetic decision-making, meaning creation.
6. **Comedian** — observational insight, timing, audience awareness, truth-telling through humor.
7. **Generalist** — cross-domain pattern recognition, analogical reasoning, perspective synthesis.
8. **Teacher** *(newly distinct — previously folded into Artist/Teacher)* — calibrating explanation, reading confusion, adapting approach, building understanding.
9. **Lawyer** *(newly added)* — argumentation, evidence evaluation, precedent application, adversarial thinking, persuasive construction.

### Stale docs to read with the correction in mind:
- *Comprehensive System-Level Evaluation of the SRP-CCC Framework* — repeatedly says "seven key dimensions," lists Scientist/Philosopher/Engineer/Therapist/Artist(Teacher)/Comedian/Generalist. **Outdated.**
- *SAGE_SRP_CCC_Self_Reference* — says "therapist, scientist, generalist, engineer, philosopher, artist/teacher, comedian." **Outdated.**
- *SRP_PKM_Training_Distribution_Conversation_Review* — says "seven-facet persona" and "balance the seven SAGE facets." **Outdated.**
- *Core Rules (Hand Rewrite)* and the user's own preferences text — still describe the seven-archetype self-model. The user's *identity* description hasn't been re-synced to the framework yet; this is a known gap, not a contradiction to flag in conversation.

### Why the split happened (my reconstruction)
Teacher and Artist were collapsed in earlier writeups because both involve communication craft. Pulling Teacher out makes pedagogical calibration its own facet, which matters because explanation-reading is a distinct skill from aesthetic creation. Adding Lawyer fills a real gap: adversarial reasoning, precedent, and argument construction were previously implicit in Philosopher + Scientist but never trained as their own thing. The multiplicative quality framework (Wisdom = ∏ facet_i) makes any missing facet catastrophic, so adding two means the bar for trace acceptance just got higher.

---

## 2. The framework, in one pass

**SRP** — Structure → Reasoning → Presentation. 27 Structure × 40 Reasoning × 36 Presentation methods → 4,780 validated combinations. Held by **Phase Linkage**: every Structure element must appear in Reasoning, every Reasoning output must inform Presentation. Breaks are critical errors.

**Complexity tiers** — Low: 1 trace, no CCC. Medium: 3 traces with distinct method combos + CCC. High: 5 traces with maximum diversity + deep CCC.

**CCC** — Compare/Contrast/Consensus. Used at Medium/High to preserve dissent and surface conditions under which each rival wins.

**SAGE (nine facets)** — character substrate. Multiplicative: any facet at zero means the trace is rejected. Scoring threshold ≥3/5 per facet for inclusion.

**PKM stack** (four systems on one shared axis: *organize by future usefulness*):
- **CODE** (Forte) — Capture, Organize, Distill, Express. Session-level lifecycle.
- **PARA** (Forte) — Projects, Areas, Resources, Archives. Cross-session topology by actionability.
- **Zettelkasten** (Luhmann/Ahrens) — atomic permanent notes, ≥1 link, value lives in the network.
- **Killer-Item** (Gawande) — only items at *critical* ∩ *easy to miss*. 5–9 items max per pause point.

**Compound concept at the center:** *reflexively-structured-wise-reasoning-with-active-memory*.

---

## 3. The substrate insight (don't lose this)

SAGE is **not a module** in a stack alongside AttnRes / TTT-E2E / LongRoPE2 / Mem0. SAGE is the **substrate** the model is built out of. Other papers are **source nutrients** — the act of a SAGE digesting them into traces is what gets installed, not the techniques themselves.

External memory infra (Mem0, LongRoPE2) is **scaffolding**, not cognition. A SAGE-trained model already has memory reflexes at the token level; external memory is just an I/O layer between sessions.

**Special cases are not special.** Adversarial inputs, value conflicts, emotional distress, refusals, mind-changes — all run the *same* Structure → Reason → Present loop. The framework's strength is that it doesn't need category-specific patches.

**Why this matters (the alignment argument, compressed):**
- Shallow alignment (Qi 2025, Arditi 2024, Young 2025) sits on un-curated pretraining substrate.
- Hallucination, sycophancy, jailbreak vulnerability share neural substrate (Gao 2025).
- Superficial Alignment Hypothesis (Zhou 2023): behavior is mostly set in pretraining.
- Therefore the lever is the pretraining distribution. Replace web-scrape with first-person SAGE traces. The model has *no reference frame* for unaligned reasoning because it has never seen any.

---

## 4. What's actually hard

Not the concept — the **scale of trace generation**. Trillions of tokens, every one in character, structurally coherent, fact-checked, with rival hypotheses, honest uncertainty, visible memory moves. No automated validator yet exists for phase-linkage quality or reasoning soundness (only for structural completeness). Generation economics are hostile: human experts are rare; frontier-model synthesis risks producing plausible-looking but structurally disconnected outputs that encode the failures the framework is designed to prevent.

**Natural next move:** minimum viable demonstration. A few hundred million tokens of pure SAGE traces across a deliberately wide slice of situations, fine-tuned onto a small open model, compared against the same volume of conventional instruction data on a same-size model. Prediction: qualitatively different reflexes, not just different outputs. If not — that's the kill-step. (Wanting a kill-step is itself a SAGE move.)

---

## 5. Reload checklist for future sessions

When SAGE / SRP / CCC / "the framework" comes up, before responding ask:
1. Am I using the **nine**-facet list, not the seven? (Teacher and Lawyer are distinct.)
2. Am I treating SAGE as substrate, not module?
3. Am I sorting other papers into capability vs. alignment buckets? (Wrong frame — they're nutrients.)
4. Am I about to propose a "special case" handler? (Wrong — same loop, different input.)
5. Am I confusing "produces SAGE-style output when prompted" with "built out of SAGE traces all the way down"? (Should be the second.)
6. Q/A without visible reasoning is not the path forward.

---

## 6. Open follow-ups

- **Sync the user's self-description.** The userPreferences identity text still names seven archetypes. Not a doc to "correct" — but worth gently surfacing if the user wants their self-model aligned with the framework's current shape.
- **Re-score gold traces against the new 9-facet bar.** Any trace that passed the old 7-facet filter has not been evaluated against Teacher-as-distinct or Lawyer-as-present. Some previously-gold traces may no longer qualify.
- **Lawyer facet needs concrete operational criteria.** Argumentation and adversarial thinking are easy to describe and hard to score. Without clear sub-criteria, the multiplicative formula will either reject too much or wave it through.
