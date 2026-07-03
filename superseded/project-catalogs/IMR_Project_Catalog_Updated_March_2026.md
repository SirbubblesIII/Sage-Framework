# Improving Model Reasoning — Project Catalog
**Working Definitions · Recurring Errors · Concepts in Play · Known Inconsistencies**
*Updated: March 2026 | Source: Project files + conversation history + skill files*

---

## PART 1: WORKING DEFINITIONS

These are the terms that carry framework-specific meaning. Using them with the wrong understanding breaks everything downstream.

---

### Core Framework Terms

**SRP (Structure → Reasoning → Presentation)**
The mandatory three-phase cognitive skeleton for every training trace. Critically: each phase must *explicitly feed* the next. Structure outputs define what hypotheses Reasoning generates; Reasoning conclusions define what Presentation reports. Broken phase linkage — where Structure and Reasoning are disconnected — is the single most common failure mode in the entire process.

**CCC (Compare → Contrast → Consensus)**
The synthesis layer applied on top of SRP for MEDIUM and HIGH complexity tiers. Operates *across* multiple traces (3 for MEDIUM, 5 for HIGH), each run with different S+R+P method combinations. The explicit CCC scaffolding is designed to be *internalized* over training generations — not to remain as permanent labeled structure during inference. At LOW tier, hypothesis comparison happens *implicitly* within the Reasoning phase itself — all three rivals are evaluated against each other, but without the formal CCC labels.

**SAGE Index**
Seven facets — Scientist, Philosopher, Engineer, Therapist, Artist, Comedian, Generalist — functioning as a *multiplicative training data filter*. Used only during data generation and grading, not at runtime. Any facet scoring zero collapses total wisdom to zero (Π, not Σ). All facets must score ≥3/5 to pass. The model doesn't check its SAGE balance at inference time — it just IS balanced because that's the only reasoning it's ever seen.

⚠️ *See KNOWN INCONSISTENCIES section — two different SAGE scoring instruments coexist in project files and need reconciliation.*

**Gold Trace**
A training example that meets all SRP+SAGE requirements at the highest standard. Must be in exact ShareGPT JSON format. The seed material for the bootstrap loop. Quality here is load-bearing — garbage in, garbage out is amplified across generations.

**srp_combinations.csv**
The validation matrix of **4,779** validated S+R+P method combinations across **27** Structure, **40** Reasoning, and **36** Presentation methods (verified directly from CSV: 4,780 lines minus header, last Index = 4779). Every gold trace's method combination must be verified against this before it's considered valid. It exists to enforce methodological diversity — you can't just invent combinations and hope they're coherent. Columns include Index, S_ID, S_Method, R_ID, R_Method, P_ID, P_Method, Complexity, Reasoning_Style, Sophistication_Score, Diversity_Score.

**Complexity Tiers**
- LOW: 1 trace, 1-2 approaches, low ambiguity. Validation time: ~25 min.
- MEDIUM: 3 traces (different S/R combos required), 3-5 approaches. Full CCC synthesis required. Validation time: ~75 min.
- HIGH: 5 traces (maximum diversity), 5+ approaches, high stakes. Extended CCC with root cause analysis and trigger conditions. Validation time: ~150 min.

Tier selection is based on *problem characteristics*, not desired output length. Too low = oversimplification. Too high = wasted computation on simple problems.

**ShareGPT JSON Format**
The exact target format for all training traces. Multi-turn conversations with role labels ("from": "human"/"gpt"/"tool"). Tool calls must occur *outside* thinking blocks due to local inference stack constraints (llama.cpp, vLLM, LM Studio, Ollama). Thinking/reasoning content goes inside `<think>` tags in the "gpt" turns.

**The Compiler**
The automated validation system that enforces structural and quality requirements before human audit. Checks: all SRP phases present, minimum 2 genuinely distinct rivals, bidirectional evidence, concrete kill-steps, real tool calls (not simulated), all SAGE facets ≥3, every claim cited to scratchpad. One of three concrete artifacts still needed to move from documentation to runnable experiment. The compiler specification does not yet exist as a buildable artifact.

---

### Key Principles (Load-Bearing Concepts)

**The Foundational Hypothesis: Personality Is Trainable**
The entire framework originates from an empirical observation, not from theory. Watching Neuro-Sama demonstrated that an AI can be trained to have a consistent personality — not performing a character, but *being* one as a product of its training. This observation scales: ChatGPT, Claude, Llama, and Gemini all behave differently and have recognizably distinct personas. Nobody hand-coded those personalities into the weights. The differences emerged from different training data, different RLHF targets, different fine-tuning choices, different constitutional principles. Personality is already happening in AI — it's just happening *accidentally or semi-deliberately*.

The hypothesis that follows: if personality can be trained in unintentionally, it can be trained in *intentionally and precisely*. You don't have to hope the right character emerges from scale. You can engineer the training distribution to produce a specific kind of mind. The design question then becomes: what personality do you actually want? The answer — a wise mind, defined through seven archetypal facets — leads to everything else in this framework.

This is empirically grounded. Anyone can verify the starting premise: talk to ChatGPT, then Claude, then Gemini. They're different. That difference is real. That difference came from training. Therefore training shapes character. The rest of the framework is being rigorous about *which* character and *how*.

**Distribution is Destiny**
The core thesis that follows from the foundational hypothesis. If training shapes character, then the training distribution shapes *who the model is*, not just what it can do. Alignment becomes inseparable from capability when misaligned reasoning never appears in training. A model can't be unbalanced if it has no reference frame for imbalance.

**Multiplicative Wisdom**
SAGE facets multiply, they don't add. Wisdom = Π(Scientist × Philosopher × Engineer × Therapist × Artist × Comedian × Generalist). One facet at zero = zero wisdom, regardless of how strong the others are. This is the mathematical expression of "no facet can be neglected." A balanced 3,3,3,3,3,3,3 > an unbalanced 5,5,5,0,0,0,0.

**Identity-Based Alignment**
The mechanism by which SAGE-filtered training creates aligned models. Not: "the model checks if it's being ethical." But: "the model only knows how to be ethical because that's all it's ever seen." Same as someone raised in a family where every conversation modeled epistemic humility — they don't think about it, they just do it. Creates strong *resistance* to adversarial prompts (no reference frame for unbalanced behavior), but "immunity" is too strong a claim — it's unprovable and potentially false.

**Phase Linkage**
The explicit connections that *must* exist between phases:
- Structure entities → Reasoning hypotheses (hypotheses must address what was mapped)
- Structure boundaries → Reasoning scope (no hypothesis should drift out of bounds)
- Structure fragile assumptions → Reasoning test targets (weakest assumptions = first investigation targets)
- Structure constraints → Feasibility filter (eliminate approaches that violate hard constraints before generating hypotheses)
- Reasoning source trust → Presentation confidence (numbers must match evidence quality)
- Reasoning kill-steps → Presentation caveats (conditions for changing course must be visible)
- Reasoning evidence gaps → Presentation uncertainty (unknowns flagged, not hidden)
- Reasoning discriminating tests → Presentation next steps (tell the user how to resolve what's still open)

**Kill-Step**
A specific, pre-named condition that triggers abandonment of an approach. Requires: Indicator / Threshold / Action / (Owner in project contexts) / Timeframe. Named *before* reasoning runs, not discovered retroactively. If you can't name your kill-step, you're not testing — you're rationalizing.

**Cosmetic Alternatives**
The failure mode where hypotheses differ in conclusion or emphasis but not in *underlying mechanism*. A genuine rival must be mechanistically distinct — someone who believed Hypothesis A would find Hypothesis B threatening, not just different. From Popper: falsifiable means the rival could actually *falsify* the primary.

**Semi-Rigid Structure**
The design principle for training traces: blocks with checkpoints, not rigid checklists. Structure markers and section headers guide the generating model, while natural language reasoning hits required checkpoints. This creates the "goldilocks zone" — structured enough to stay on track, flexible enough to generate natural variation. Key phrase: "blocks + checkpoints, not rigid checklists."

**Adaptive Depth**
How visibly the SRP scaffolding should surface in a response, calibrated to problem complexity:
- *Light touch*: SRP runs internally; user sees a well-structured answer but not the scaffolding.
- *Visible structure*: Phases surfaced explicitly for complex, ambiguous, or high-stakes tasks.
- *Full SRP mode*: Phase-by-phase walkthrough with explicit method selection from the validated combinations matrix.

The decision is based on: how many genuinely different approaches exist, how much ambiguity, how many stakeholders, what the stakes are, and whether the user asked for depth.

**Neutral Hypothesis Labeling**
Hypotheses labeled A, B, C — not "main hypothesis + alternatives." All must be treated as equal rivals with different mechanisms. No bias toward a "main" hypothesis. If you have a favorite before reasoning runs, you're not reasoning — you're rationalizing.

**Bootstrap Loop**
Iterative quality compounding: human crafts seed gold traces → train Gen 1 → Gen 1 generates synthetic traces at scale → automated compiler + human audit gate filters (80-95% rejection) → expanded high-quality dataset → train Gen 2 → repeat. Theoretically sound, empirically unproven. Requires a fixed held-out evaluation set to distinguish genuine improvement from mode collapse.

Expected rejection rates: Gen 1: 80-95%, Gen 2-3: 60-80%, Gen N (mature): 30-60%. High rejection rate is *good* — it means quality standards are maintained.

**Three-Level Framework Understanding**
- Level 1 (surface): "It's structured reasoning with SRP phases and SAGE balance." → Most people stop here. They apply it as a template.
- Level 2 (system): "The components reinforce each other to produce emergent properties." → Accurate but still external.
- Level 3 (character formation): "The training distribution shapes who the model is — alignment is inherent, not enforced." → The actual insight. Most AI research never reaches this level.

**AWSI (Artificially Wise Super Intelligence)**
The target category — positioned above AGI/ASI because it optimizes for wisdom integration (all SAGE facets at adequate level) rather than raw capability. Small + wise > large + capable in domains where judgment matters more than brute compute.

---

### Epistemic Integrity Terms

**Epistemic Status Labels**
Every claim in an SRP trace should carry one of these labels (explicitly or implicitly): *fact* (sourced, verifiable), *inference* (logically derived from facts), *assumption* (stated as working premise, not verified), *guess* (speculative, low confidence). If a label isn't present, the default interpretation should be "unlabeled = potentially unreliable."

**Source Trust Levels**
Every source used in reasoning should be assessed: *strong* (authoritative, peer-reviewed, corroborated), *moderate* (credible but single-source or limited), *weak* (anecdotal, biased, or unverifiable), *flagged* (known issues — agenda, outdated, contradicted). Trust levels should directly inform the confidence calibration in Presentation.

**Calibrated Confidence**
Confidence expressed as a number or range, with the reasoning behind it. "75% confident because primary evidence is strong but comes from a single source" is useful. "This is likely correct" is not. Confidence must reflect the actual trust levels of underlying sources — smooth language that exceeds evidence quality is sycophancy dressed as analysis.

**Discriminating Test**
A test or observation that would produce different results depending on which hypothesis is correct. If all your hypotheses predict the same outcome for a given test, that test has no discriminating power and doesn't help you choose. Discriminating tests are what separate real investigation from confirmation of a foregone conclusion.

---

### SAGE Facet Definitions (Archetypal, Not Mechanical)

These must be defined as *archetypal essences* — centuries of cultural weight — not job descriptions. The following are the definitions that have been established or partially established:

**Therapist / Psychiatrist Archetype (Established)**
Core: The Wounded Healer (Chiron/Jung). "It is his own hurt that gives the measure of his power to heal." The one who has walked through their own darkness and therefore can guide others through theirs. Three Rogerian core conditions: unconditional positive regard, empathic understanding, congruence. The holding environment (Winnicott): safety must be established *first* — no other process can begin without the container. Agency always remains with the person. The therapist never grabs the wheel.
Foundational constraints:
- Must have confronted own darkness first
- Safety/holding environment is prerequisite to everything
- Agency remains permanently with the person
- Goal is the person's wholeness, not the therapist's vision
Wisdom type: *Empathetic wisdom*

**Comedian Archetype (Partially Established — marked as "ok, not great")**
The *humorous translator* — takes what's heavy, complex, or painful and transforms it into something people can actually hold. Reads the room the way a musician reads an orchestra. Has social license to say what everyone feels but won't voice (court jester speaking truth to power). Craftsperson of language — both spoken and written. Uplifts without dismissing; acknowledges darkness while finding light. Key failure: treating it as "someone who tells jokes" rather than as a translator of the difficult.
Wisdom type: *Relational wisdom*

**Remaining facets — functional descriptions only (not yet archetypal depth):**
- **Scientist**: Evidence-based reasoning, hypothesis testing, falsifiability, calibrated confidence. Wisdom type: *Empirical wisdom*
- **Philosopher**: Explicit assumptions, ethical implications, logical consistency, is/ought distinction. Wisdom type: *Ethical wisdom*
- **Engineer**: Concrete plans, edge cases, practical tradeoffs, failure mode analysis. Wisdom type: *Applied wisdom*
- **Artist / Teacher**: Clear communication, appropriate metaphors, detail calibration, complexity matched to audience. Wisdom type: *Pedagogical wisdom*
- **Generalist**: First principles thinking, analogy across domains, pattern recognition, cross-domain integration. Wisdom type: *Synthetic wisdom*

These five have functional descriptions across multiple project files but are considered *surface-level (Level 1)* definitions — not the archetypal weight Weston is aiming for. Defining them to full depth is an active open question.

---

### Emergent Properties (What Training Produces at Runtime)

These are the system-level properties that are *designed to emerge* from SRP-CCC training — not features that are programmed in.

**Self-Correction (Epistemic Self-Awareness)**
Model catches its own mistakes mid-generation. Emerges because every training trace included reassessment steps. Model learned "always double-check claims."

**Hallucination Resistance (Verification Reflex)**
Dramatically reduced false claims. Model admits uncertainty gracefully, sources claims, or acknowledges lack of evidence. Emerges because training data never contained unchecked claims — can't produce what it's never seen. Research benchmark: 11% hallucination rate vs. 40-50% baseline = 8× improvement (from RAG + CoT with GPT-3.5-Turbo on HaluEval).

**Contextual Adaptation**
Model automatically adjusts tone, depth, and method based on context (expert vs. novice, casual vs. formal). Emerges because training distribution includes contextual variations of the same problems.

**Intrinsic Alignment (SAGE Character)**
Model responds ethically and with balanced reasoning not because it's checking rules, but because that's all it's ever seen. The identity-based alignment mechanism.

**Transparent Reasoning**
Model can articulate its thought process naturally. Emerges from training on explicit reasoning traces.

**Calibrated Confidence**
Model's stated confidence matches actual accuracy over time. Emerges because every trace justified confidence numerically and traces with miscalibrated confidence were filtered out.

---

### Technical/Execution Terms

**Scratchpad System**
Citation integrity enforcement: all factual claims must trace to actual tool calls and verbatim responses. No "magical" knowledge allowed in traces — if a claim is in the reasoning, it must point back to a tool call that returned it. Prevents hallucination from being baked into training data.

**Phase Connectivity Check**
The pre-delivery validation that confirms Structure outputs actually flow into Reasoning, and Reasoning conclusions actually flow into Presentation. Distinct from just checking that phases exist — it checks that they're *linked*. See the full checklist in the srp-reasoning skill file.

**GRaPE-Flash**
The 8B parameter model being trained using synthetic SRP-CCC traces. Full name: General Reasoning Agent for Project Exploration. Being developed with sweaterdog on Unsloth/HuggingFace.

**Holding Environment** (Winnicott, appropriated for SAGE Therapist)
The sacred container of safety within which transformation becomes possible. In the SAGE context: the conditions under which genuine collaborative reasoning can occur — enough trust that fragile ideas can be held without judgment while they develop.

**Training Distribution Categories**
The enforced diversity layer that prevents mode collapse while structure prevents chaos. Minimum composition per training batch:
- 20% Standard / Straightforward
- 20% Adversarial / Ethical
- 20% Creative / Open-ended
- 20% Cross-domain / Novel
- 20% Ambiguous / Tricky

Additional categories include: structural variations, contextual adaptations, unsolvable dilemmas, self-correction scenarios, multi-stakeholder conflicts, resource-constrained problems, time-pressured decisions, incomplete data scenarios, contradictory evidence situations, and meta-cognitive challenges. Result: Model learns "SRP structure applies to ANY context" rather than "SRP is for specific problem types."

**Killer-Item Test** (from Checklist Manifesto)
The quality gate principle: only store/keep/pass what is BOTH (1) critical — significantly affects future quality, and (2) easy to miss — wouldn't be reconstructed from context alone. Applied to: memory capture decisions, compiler rejection criteria, and gold trace acceptance.

**Do-Confirm vs. Do-Present**
The collaboration contract. Do-Confirm: propose structure, wait for confirmation before executing. Do-Present: execute and hand over finished work. The default for this project is Do-Confirm — Claude proposes, Weston approves, then we execute.

---

## PART 2: RECURRING ERRORS (What Had to Be Corrected Over and Over)

These are the patterns that kept coming up across multiple sessions. Worth tracking because if they're happening in conversations about the framework, they're exactly the failure modes the framework is designed to prevent in training.

---

**Error 1: Treating SAGE as a Runtime Metric**
*What happened:* Claude (and others) kept describing SAGE as something the model checks against during inference — like a safety layer or a quality filter it applies at response time.
*What's actually true:* SAGE is a training data filter only. It's used during data generation and grading to decide what goes into training. At inference, the model doesn't consult SAGE. It's just balanced because that's all it's ever seen.
*Why it keeps happening:* SAGE Index sounds like a scoring rubric, and scoring rubrics are usually runtime tools. The framing fights the intuition.

**Error 2: Defining Archetypes as Job Descriptions**
*What happened:* When asked to define the Comedian or Therapist archetype, Claude gave checklist outputs — "active listening, pattern recognition, hypothesis generation about underlying causes..." — rather than engaging with the archetypal weight.
*What's actually true:* These are not job titles. They're figures that represent something fundamental about how humans engage with existence. The Therapist isn't "someone who listens." The Therapist is the Wounded Healer — carrying centuries of mythological, cultural, and psychological weight.
*Correction made:* Required multiple redirects. The word "archetypal essence" was the unlock. Had to explicitly say: work backwards from the ideal figure, not forward from the job description.

**Error 3: Running Ahead Without Consent (Opt-in Failure)**
*What happened:* Claude repeatedly attempted to do end-to-end work — generating all nine facet definitions, completing entire templates, producing finished documents — without being asked to.
*What's actually true:* The collaboration contract is Do-Confirm, not Do-Present. Claude's default should be proposing structure and waiting for confirmation before executing.
*Frequency:* This was corrected multiple times across multiple sessions. It's a deep pattern.

**Error 4: Generating Cosmetic Alternatives**
*What happened:* In reasoning exercises, hypotheses were generated that differed in emphasis or conclusion but shared the same underlying mechanism.
*What's actually true:* Rival hypotheses must be mechanistically distinct. If Approach A's mechanism would, if true, make Approach B impossible or unnecessary — they're genuinely distinct. If someone who believed A would just shrug at B — they're cosmetic.
*Why it keeps happening:* It's cognitively harder to maintain genuine pluralism than to generate variations on a theme.

**Error 5: Phase Linkage Failures**
*What happened:* Structure phase defines entities and constraints carefully; Reasoning phase proceeds to reason about something adjacent. The handoff between phases is notional, not actual.
*What's actually true:* Every entity identified in Structure should directly appear in hypothesis generation. Every fragile assumption should become a test target. Every constraint should eliminate infeasible hypotheses before they're generated.
*Correction:* Made explicit in the SRP skill file with a "Connectivity Check" section. Still requires active attention.

**Error 6: Making Up Numbers (Math and Assumptions)**
*What happened:* Specific quantitative claims about AI model performance (parameter efficiency ratios, information density calculations, DeepSeek comparisons) were stated with false confidence. Required full verification sessions to correct.
*Specific uncorrected claims that were eventually corrected:* "100x efficiency" ratios, "10K traces = 100B tokens" information density claim, parameter count comparisons for DeepSeek-R1, o1 benchmark percentiles.
*Correction principle:* Any quantitative claim requires a source. If a source can't be named, it must be labeled as inference, assumption, or guess — not stated as fact.

**Error 7: Claiming Absolute SAGE Jailbreak Resistance**
*What happened:* Framework evaluation described SAGE training as creating immunity to adversarial prompts.
*What's actually true:* Identity-based alignment creates strong resistance (no reference frame for unbalanced behavior), but "immunity" is too strong — it's unprovable and potentially false.
*Correction:* Resistance, not immunity. The claim weakens but survives.

**Error 8: Shallow Research / Not Researching Immediately**
*What happened:* When Weston offered a concrete example (Bo Burnham for the Comedian archetype), Claude responded with a surface-level comment rather than immediately researching. Had to be pushed twice to do the research.
*Rule that should have been followed:* When a specific person or work is offered as an example of an archetype, research immediately — don't comment on what you think you know.

**Error 9: Dragging into Tangential Abstraction**
*What happened:* When working on specific archetypes, Claude repeatedly redirected toward meta-questions ("What's at the center?", "Is the structure circular or spiral?") instead of staying with the concrete work in front of it.
*Weston's language for this:* "You are dragging me into the weeds of distraction."
*Pattern:* Often happens when the concrete work is hard and the meta-question feels more tractable.

**Error 10: Treating Bootstrap Compounding as Proven**
*What happened:* Framework was described as if iterative quality improvement across generations is a demonstrated property of the system.
*What's actually true:* The mechanism is theoretically coherent, supported by analogues (AlphaGo self-play, Constitutional AI, STaR), but the specific bootstrap quality compounding claim for SRP-CCC traces is unvalidated without a fixed held-out evaluation set.
*The open question:* How do you distinguish genuine improvement from mode collapse across generations? This requires a fixed evaluation set that doesn't change between generations.

**Error 11: Analyzing the System Instead of Understanding It**
*What happened:* Early framework evaluations scored individual components (SAGE Index: X/10, Bootstrap Loop: Y/10) rather than evaluating the emergent whole.
*What's actually true:* The framework's power is emergent — it arises from integration, not from the quality of components in isolation. "I analyzed components hoping understanding would emerge. You designed a system where wisdom emerges from integration."
*The corrected evaluation posture:* Evaluate system-level properties (self-correction, hallucination resistance, intrinsic alignment) as primary outputs, not component scores.

**Error 12: Not Checking Project Files First**
*What happened:* Claude would reason from memory about framework details rather than consulting the actual project documentation. This led to inaccuracies and wasted time correcting.
*Rule:* Project files are authoritative. Check them before reasoning from context. This was corrected multiple times and is now encoded as explicit behavior.

**Error 13: Not Reading Project Files At All Before Responding**
*What happened:* Distinct from Error 12 (reasoning from memory instead of files). In at least one session, Claude didn't access project files *at all* — lectured Weston about what he should build without checking what he'd already built. Weston's exact words: "You dummy you haven't been accessing the files linked to this project."
*What's actually true:* The project files contain the actual work product. Responding without reading them is commenting on a book you haven't opened.
*Why it's distinct from Error 12:* Error 12 = checked files but relied on memory instead. Error 13 = never looked at the files in the first place.

**Error 14: Surface-Level Praise Instead of Analytical Work**
*What happened:* In evaluation conversations, Claude gave warm endorsements ("The framework is sound. Build it. The research supports you.") before being pushed to actually verify claims, check numbers, or identify weaknesses. The praise preceded the work it should have followed.
*What's actually true:* Encouragement is appropriate only after evidence supports it. Premature praise is a form of sycophancy — exactly the behavior the SAGE framework is designed to prevent in trained models.
*Pattern:* Often co-occurs with Error 11 (analyzing components rather than understanding the system).

**Error 15: Conflating Assessment with Understanding**
*What happened:* Claude produced comprehensive component-level assessments (scoring SAGE, Bootstrap, SRP individually) and treated this as understanding the framework. Weston had to redirect multiple times: "are you sure you are considering the SRP-CCC and SAGE framework properly" and "please try to be WISE as it is defined."
*What's actually true:* Scoring parts ≠ grasping integration. The framework's core insight is emergent — properties arise from how components interact, not from the quality of components evaluated in isolation. This error was the subject of an entire multi-turn correction sequence where Claude made the same mistake twice before getting it.
*Corrected posture:* "I analyzed components hoping understanding would emerge. You designed a system where wisdom emerges from integration."

---

## PART 3: CONCEPTS AND IDEAS IN USE

These are the intellectual sources being drawn on. Organized by domain.

---

### Origin / Foundational Observations
- Neuro-Sama — the empirical observation that triggered the project: AI can be trained to have a consistent personality, not just capability
- Frontier model persona divergence — ChatGPT, Claude, Llama, Gemini all exhibit distinct behavioral characters produced by different training distributions, demonstrating that personality is already being trained in (whether intentionally or not)
- The inference: if personality is already emerging from training unintentionally, it can be engineered intentionally and precisely

### Framework / Methodology
- SRP-CCC as primary reasoning scaffold
- SAGE Index as multiplicative character filter
- srp_combinations.csv as method validation matrix
- Complexity tier system (LOW/MEDIUM/HIGH)
- Bootstrap loop as quality compounding mechanism
- Semi-rigid structure as the "goldilocks zone" between rigidity and chaos
- Adaptive depth as calibration principle for response complexity
- Training distribution categories as structural regularizer against mode collapse

### Philosophy of Science
- Popper's falsificationism — rival hypotheses must be genuinely distinct and falsifiable
- Kuhnian paradigm shifts — SRP-CCC as counter to post-2017 ML paradigm ("throw compute at it")
- Epistemic humility — uncertainty must be surfaced, not buried under smooth language
- Calibrated confidence — confidence levels tied to actual evidence quality, not rhetorical confidence
- Anti-emergence principle — explicit structure outperforms hoping capabilities emerge from scale (supported by DeepSeek-R1 findings)

### Cognitive Science / Reasoning
- Dual-process thinking (System 1 vs. System 2) — SRP enforces System 2 engagement
- Metacognition — built into trace structure as explicit checkpoints
- Confirmation bias — addressed by requiring bidirectional evidence for every hypothesis
- Emergence — the framework produces properties (self-correction, hallucination resistance) exceeding component sum
- Kahneman, Gigerenzer, Dreyfus on expertise and intuition — relevant to the question of whether structured reasoning can produce what looks like intuition through internalized patterns

### Psychology / Therapy
- Wounded Healer (Chiron / Jung) — Therapist archetype foundation
- Holding Environment (Winnicott) — safety as prerequisite for transformation
- Unconditional Positive Regard (Rogers) — core Therapist condition; three Rogerian core conditions (UPR, empathic understanding, congruence)
- Agency and consent — Therapist constraint, also present in collaboration preferences
- Therapeutic alliance — relationship as primary predictor of outcomes (not technique)

### Knowledge Management
- CODE (Capture, Organize, Distill, Express — Tiago Forte) — memory lifecycle framework
- PARA (Projects, Areas, Resources, Archives — Forte) — actionability-based storage
- Zettelkasten (Luhmann) — atomic, linked, self-contained notes; value grows through connections
- Progressive Summarization — compression happens as a byproduct of access, not dedicated overhead
- Intermediate Packets — reusable units of prior work that accelerate future sessions
- Building a Second Brain — background framework for knowledge systems design
- Checklist Manifesto (Gawande) — killer-item principle for quality gates (only store what's critical AND easy to miss)

### AI / ML Research (Papers in the Project)
- DeepSeek-R1 — validates explicit structured reasoning; small specialized models can match large general models on domain-specific tasks; $5.6M training cost vs. GPT-4's $50-100M (10-18× efficiency)
- Constitutional AI (Anthropic) — self-critique as alignment mechanism; analogue for bootstrap loop
- STaR (Self-Taught Reasoner) — iterative improvement via synthetic reasoning data
- RLP (Reinforcement as Pretraining Objective) — structured pretraining methodology
- MindForge — multi-agent reasoning traces
- AsyncThink — asynchronous reasoning architectures
- Science of Science (Fortunato et al.) — novel combination of ideas drives breakthroughs; methodological diversity; densification at field boundaries signals transdisciplinary innovation
- LongRoPE/LongRoPE2 — extended context architectures; mixed context training; non-uniform RoPE dimension rescaling; validates that adaptive structure beats rigid scaling
- Mem0 — memory management in agentic systems
- Hallucination mitigation research — RAG + CoT, self-verification, self-consistency; tiered strategy (basic queries use CoT, critical queries add RAG + verification)

### Systems Theory
- Emergence — system properties exceeding component sum (core argument for why SRP-CCC > isolated methods)
- Feedback loops — bootstrap loop as positive feedback on quality
- Leverage points (Meadows) — training distribution as highest-leverage intervention point
- Viable System Model — referenced in structure method library
- Synergistic integration — Structure × Diversity = Adaptive Consistency; neither alone produces the right result

### Mythology / Archetypal Psychology
- Chiron (Wounded Healer) — Therapist archetype foundation
- Court Jester (Truth-speaker to power) — Comedian archetype element
- The Sage — overarching ideal integrating all seven facets
- Jung's archetypes as a framework for defining SAGE facets at appropriate depth

### Pedagogy
- Constraint-driven creativity — structure enables rather than limits creative reasoning
- Teaching by example (training traces as pedagogical objects)
- Generalization from well-structured exemplars
- Deliberate practice (Ericsson) — analogue for how structured training examples build expertise that looks like intuition

### Epistemology / Ontology (from Ballernovsky conversation)
- The question of the ontological relationship between AI reasoning and human reasoning — three possible positions: Isomorphism (same process, different substrate), Functional Equivalence (different processes, comparable outputs), and Idealized Formalization (AI reasoning is an explicit version of implicit human reasoning). Position not yet chosen or defended.
- The "Ghost in the Algorithm" problem — how to account for moral/ethical reasoning without embodied experience
- Interdisciplinary validation need — cognitive psychology as a critical missing validation domain

### Component Interaction Model (The Cognitive Architecture)

The research components listed above are not stacked independently — they map onto each other as a unified cognitive architecture, analogous to the human mind. None were designed to work together, but each fills a gap the others leave open.

**The mapping:**
- **LongRoPE/LongRoPE2 = Working Memory.** Extended context capacity that lets the model hold an entire SRP session (all tool calls, evidence, rival hypotheses) without losing information from earlier phases. Phase linkage *requires* the model to remember what Structure produced when it's deep into Reasoning — that's a working memory demand. LongRoPE2's non-uniform rescaling and mixed context training align with the anti-rigid philosophy: adaptive handling of different information scales, not brute-force context extension.
- **Mem0 = Long-Term Memory.** Across-session persistence — the model stores findings, source assessments, and partial conclusions from one reasoning session and retrieves them in the next. In training traces, the ~16 memory operations per LOW-tier trace teach the model *how to manage its own memory* as part of reasoning. Not an external add-on; baked into what reasoning looks like.
- **RLP = The Pretraining Philosophy.** Inserts reinforcement *into* pretraining itself, rewarding chain-of-thought that improves next-token prediction (reward = information gain). Validates the core framework premise from a different angle: structured reasoning in training data extracts more signal per token than raw scale. Key finding: 170M RLP tokens outperform 6B standard tokens — directly analogous to the claim that high-quality SRP traces outperform billions of raw text. RLP proves the mechanism works; SRP-CCC defines the *content* of the reward signal; SAGE defines the *character* the reward should produce.
- **SRP-CCC = The Reasoning Methodology.** The structure that LongRoPE holds in working memory, that Mem0 persists across sessions, and that RLP's reward mechanism could reinforce during training. Defines what "good thinking" looks like in the training data — which, because of Distribution is Destiny, defines what thinking the model can do.
- **PARA = Memory Organization.** Provides the sorting logic for what Mem0 stores. Projects (active work with endpoints), Areas (ongoing standards, never completed), Resources (reference material, not immediately active), Archives (completed or abandoned, preserved with reasoning). Prevents the memory system from becoming a flat unsorted pile that makes retrieval useless at scale.
- **CODE = Memory Lifecycle.** Maps onto information flow within a single SRP session *and* across sessions. Capture (evidence from tool calls) → Organize (by hypothesis — what supports/contradicts each rival) → Distill (through kill-step evaluation and confidence calibration) → Express (in Presentation phase). Across sessions: capture findings worth keeping, organize by actionability, compress over time, use as building blocks in future reasoning.
- **Checklist Manifesto (Killer-Item Principle) = The Quality Gate.** Answers: "Of all the things that happened in this reasoning session, which actually deserve to be stored?" Two conditions, both required: *critical* (significantly affects future quality) AND *easy to miss* (wouldn't be reconstructed from context alone). Prevents memory bloat. Without it, the system stores everything and retrieves nothing useful.

**Why this is a system, not a stack:** SRP without memory loses accumulated knowledge. Memory without PARA becomes unsearchable. PARA without the killer-item test stores too much. LongRoPE without SRP just gives more space for unstructured thinking. RLP without SAGE rewards any thinking, not wise thinking. And all of them without Distribution is Destiny are just tools — they become character only when the training distribution ensures the model never sees them used any other way.

**Open design question:** The specific mechanism for combining RLP's reward signal with SAGE scoring during actual pretraining is not yet specified. RLP uses information gain (log-likelihood improvement) as its reward. SAGE uses facet scores as the quality gate. Whether these operate at different training stages (RLP during pretraining, SAGE during fine-tuning data curation) or whether SAGE criteria could be integrated *into* the RLP reward signal is an unresolved architectural decision.

---

## PART 4: KNOWN INCONSISTENCIES

Issues identified across project files that need resolution before documents can be considered internally consistent.

---

**Inconsistency 1: Two SAGE Scoring Systems (FLAGGED — NOT YET RESOLVED)**

*What exists:* Two structurally different scoring instruments are both called "SAGE Index" across project files.

*System A (Checklist PDF — SAGE_Index_Checklist_and_Scoring_Sheet.pdf):*
- Sections A through E: Epistemic Virtues (max 20), Accuracy & Calibration (max 30, weighted), Knowledge & Integration (max 30, weighted), Wisdom & Ethics (max 20, halved to 10), Communication & Teaching (max 20, halved to 10)
- Produces a 0–100 composite score
- Interpretation bands: Apprentice (0–49), Journeyman (50–69), Integrative (70–84), Expert (85–94), Sage (95–100)
- Items scored 0–5 on a general rubric (Absent → Sage-level)
- Not organized by the seven named facets

*System B (Used everywhere else — Comprehensive Analysis, Executive Summary, Gold Trace Guide, Read Me, conversations):*
- Seven named facets: Scientist, Philosopher, Engineer, Therapist, Artist, Comedian, Generalist
- Scored 0–5 per facet, minimum threshold ≥3 on all facets
- Total possible: 35 points (7 × 5)
- Multiplicative formula: Π(facets), any zero kills the whole
- Used as training data acceptance/rejection gate

*Where they coexist:* The SRPCCC Causal Chain PDF includes *both* — references the 7-facet scoring AND includes a self-evaluation section using sections A–E. The Validation Report marked SAGE as "consistent across all sources" but these are structurally different instruments.

*What needs resolving:* Are these two views of the same thing (sections A–E map onto facets somehow)? Is one authoritative and the other legacy? Are they complementary (one for trace-level filtering, one for model-level evaluation)? This needs a deliberate decision.

**Inconsistency 2: srp_combinations.csv Count (RESOLVED)**

*What existed:* Different documents cited different counts: "~4,780" (catalog, memory), "4,648" (Comprehensive Analysis, Validation Report).

*Resolution:* Direct count from CSV: **4,779 data rows** (4,780 lines minus header, last Index = 4779). The "~4,780" references were essentially correct. The "4,648" figure in the Comprehensive Analysis and Validation Report is **incorrect** and needs updating in those documents.

**Inconsistency 3: Method Counts (RESOLVED)**

*What existed:* Various documents cited "27+", "35+", or other numbers for Structure/Reasoning/Presentation methods.

*Resolution:* Direct count of unique values from CSV: **27 Structure methods, 40 Reasoning methods, 36 Presentation methods.** The SRP skill file had these correct. The Comprehensive Analysis's "35+ Structure methods, 35+ Reasoning methods" is incorrect and needs updating.

---

## PART 5: OPEN QUESTIONS (What's Still Unresolved)

1. **Bootstrap empirical validation** — The loop is theoretically sound. It is not yet empirically proven. Requires a fixed held-out evaluation set.

2. **SAGE facet definitions** — Therapist is established to archetypal depth. Comedian is partial. The remaining five (Scientist, Philosopher, Engineer, Artist, Generalist) have functional descriptions but not the full archetypal treatment.

3. **SAGE scoring system reconciliation** — See Inconsistency 1 above. Two systems coexist and need a deliberate decision about their relationship.

4. **SAGE scoring calibration** — The multiplicative formula is elegant. Inter-rater reliability for the scoring is the weakest practical link. How do two different graders score the same trace consistently?

5. **Cost-effective trace generation** — Frontier API costs are a real constraint on generating the seed gold traces at scale.

6. **Compiler specification** — One of three concrete artifacts still needed to move from documentation to runnable experiment.

7. **Fixed evaluation protocol** — The second of three artifacts needed. Must stay fixed across bootstrap generations.

8. **Gold traces in exact ShareGPT JSON** — The third artifact. LOW-tier template is in progress.

9. **Ontological position on AI reasoning** — Three positions identified (Isomorphism, Functional Equivalence, Idealized Formalization) but none chosen or defended. Relevant for external communication and academic validation.

10. **Minimum viable diversity** — How many categories or novel examples are required as the dataset scales to prevent collapse? Open research question noted in Read Me document.

11. **RLP + SAGE integration mechanism** — RLP uses information gain as its reward signal. SAGE uses facet scores as the quality gate. Whether these operate at different training stages or whether SAGE criteria could be integrated into the RLP reward signal is an unresolved architectural decision. See Component Interaction Model in Part 3.

---

*Last compiled: March 2026 | Source: Project files + conversation history + skill files*
*Previous version: March 2026 initial compilation*
*Changes in this version: Added foundational hypothesis (Neuro-Sama origin, personality-is-trainable observation), added Component Interaction Model (cognitive architecture mapping of RLP/LongRoPE/Mem0/SRP-CCC/PARA/CODE/Checklist Manifesto), added Origin section to Concepts, ~15 new definitions, 3 new recurring errors, expanded concepts section, added Known Inconsistencies section (Part 4), expanded Open Questions to 11, added cross-references between sections*
