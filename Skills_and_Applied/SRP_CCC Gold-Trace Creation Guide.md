

SRP/CCC Gold-Trace Creation Guide

> **Status note (2026-07-02):** Still the how-to for the seed gold-trace corpus (50–100 traces
> — one of the three missing artifacts). Two things have moved under it since it was written:
> (1) **"GRaPE-Flash" is a retired name** (see the retired-names registry, Canonical v2 §3.6) —
> read it below as "the Generation-1 model." (2) The **June 12 profession-archetype pivot**:
> traces are now **archetype-voiced** and pass **Core-11 out-of-expertise editorial review**,
> whose critiques are themselves captured as a data class (Canonical v2 §2.9); "SAGE balance"
> below is enforced at that review, not as a per-trace 9-facet score. The combinations CSV it
> depends on now exists: `01_Areas/SAGE_Methodology/srp_combinations.csv` (4,779 verified).

Working Backward from the End Goal
The Collapsed State (What We're Building Toward):
Perfect gold traces that teach GRaPE-Flash to natively reason in structured SRP/CCC
format, automatically selecting the appropriate complexity level (Low/Medium/High)
based on problem characteristics.
Global Constraints (What MUST be true):
- Distribution is destiny: Every trace demonstrates complete SRP pipeline + tool use +
SAGE balance
- Tier differentiation: Model learns WHEN to use Low vs Medium vs High thinking
- Method validity: All SRP combinations exist in
srp_combinations.csv
- Perfect execution: No partial implementations, no shortcuts, no simulations

## 1. Thinking Tiers: Backward Constraint Propagation
Working Backward: What requires what?
END GOAL: Model selects appropriate thinking tier automatically
↓ requires
Model has learned the pattern: problem characteristics → tier selection
↓ requires
Training data shows clear tier differentiation
↓ requires
Each tier has distinct structure while sharing core SRP elements
↓ requires
Tier-specific checklists and validation
## Tier Definitions & Constraints
Tier SRP
## Traces
## CCC
## Required
When to Use Constraints

Low 1 No Simple, clear solution path,
low ambiguity
Must still have rivals, tests,
kill-steps within single trace
## Medi
um
3 Yes Moderate complexity,
benefits from multiple
perspectives
Each trace uses different SRP
combination
High 5 Yes Complex, high ambiguity,
multiple valid approaches
Maximum methodological
diversity, deep synthesis

- Tier-Specific Checklist Templates
##  LOW THINKING CHECKLIST
## Problem Characteristics:
● Clear problem definition
● Low ambiguity (≤2 reasonable approaches)
● Limited stakeholder complexity
● Straightforward scope
Required Elements in Single Trace:
## Structure Phase:
● Single SRP combination verified in srp_combinations.csv (Index noted: ______)
● Method selection justified
● Ontology: Entities and relationships defined
● Boundaries: In/out of scope explicit
● Constraints: Time, budget, technical limits stated
● Assumptions: What must be true listed
● Level of detail: Appropriate for problem scope
## Reasoning Phase:
● Minimum 2 rivals (even for "simple" problems)
● Each rival has:
○ Clear hypothesis statement
○ Supporting evidence with provenance
○ Contradicting evidence with provenance
○ Discriminating test (falsifiable)
## ○ Kill-step (indicator/threshold/action/owner)
● Winner selected with justification

## Scratchpad:
● ≥1 real tool call with verbatim API response
● Evidence extraction with provenance
● Memory operation (if reusable knowledge present)
## Presentation:
● Format matches problem type from CSV
● All 7 SAGE facets present (score ≥3 each)
● Confidence calibrated (numeric + justification)
● Evidence citations link to scratchpad
● Next steps actionable
CCC Synthesis: None required
Validation Time: ~25 minutes

##  MEDIUM THINKING CHECKLIST
## Problem Characteristics:
● Moderate complexity
● 3-5 reasonable approaches exist
● Multiple stakeholder perspectives relevant
● Some ambiguity in problem definition or solution space
## Required Elements Across 3 Traces:
Trace-Level Requirements (Each of 3 traces):
● Distinct SRP combination verified in srp_combinations.csv (Indices: _____,
## _____, _____)
● Different Structure methods across traces (no repeats)
● Different Reasoning methods across traces (no repeats)
● Presentation methods may vary or repeat (based on audience needs)
● All elements from Low Thinking Checklist present in EACH trace
Cross-Trace Methodological Diversity:
● Trace 1: [S_Method: ______] + [R_Method: ______] + [P_Method: ______]
● Trace 2: [S_Method: ______] + [R_Method: ______] + [P_Method: ______]
● Trace 3: [S_Method: ______] + [R_Method: ______] + [P_Method: ______]
● No repeated S or R methods (P can repeat if appropriate)

CCC Synthesis (Required):
## Compare Section:
● Convergence documented: Where do all 3 traces agree?
● Divergence documented: Where do traces differ?
● Key insights from each trace listed
## Contrast Section:
● Root cause analysis: WHY do traces differ?
○ Different structural assumptions identified
○ Different evidence weighted
○ Different stakeholder priorities
● Evidence quality comparison: Which trace has strongest support?
● Method appropriateness: Which SRP combinations work best for this problem?
## Consensus Section:
● Best current answer synthesized from all 3 traces
● Confidence stated (numeric, with reasoning about cross-trace agreement)
● Preserved dissent: Conditions under which minority view would prevail
○ Format: "Trace X's conclusion holds if [specific condition]"
● Conditions that would change the answer specified
Meta-Commentary:
● Which SRP combination was most effective? Why?
● Which combination revealed blind spots in others?
● What did methodological diversity add?
Validation Time: ~75 minutes (3 × 25 min per trace + 0 min for CCC)

##  HIGH THINKING CHECKLIST
## Problem Characteristics:
● High complexity
● >5 reasonable approaches exist
● Many stakeholder perspectives with conflicting interests
● Significant ambiguity or "wicked problem" characteristics
● High stakes (safety, ethics, large-scale impact)
## Required Elements Across 5 Traces:

Trace-Level Requirements (Each of 5 traces):
● Distinct SRP combination verified in srp_combinations.csv (Indices: _____,
## _____, _____, _____, _____)
● Different Structure methods across traces (no repeats)
● Different Reasoning methods across traces (no repeats)
● Presentation methods selected for audience appropriateness
● All elements from Low Thinking Checklist present in EACH trace
Cross-Trace Methodological Diversity:
● Trace 1: [S_Method: ______] + [R_Method: ______] + [P_Method: ______]
● Trace 2: [S_Method: ______] + [R_Method: ______] + [P_Method: ______]
● Trace 3: [S_Method: ______] + [R_Method: ______] + [P_Method: ______]
● Trace 4: [S_Method: ______] + [R_Method: ______] + [P_Method: ______]
● Trace 5: [S_Method: ______] + [R_Method: ______] + [P_Method: ______]
● Maximum methodological diversity (S, R methods span different categories)
CCC Synthesis (Required - Extended):
## Compare Section:
● Full convergence map: Agreement across all 5 traces
● Divergence map: Pairwise and group disagreements
● Pattern analysis: Clusters of similar conclusions
## Contrast Section:
● Deep root cause analysis: WHY each disagreement exists
○ Ontological differences (entities/relationships framed differently)
○ Epistemological differences (what counts as evidence)
○ Value differences (normative assumptions)
● Evidence quality ranking: Best to weakest support
● Method appropriateness ranking: Most to least suitable
● Blind spot analysis: What did each approach miss?
## Consensus Section:
● Sophisticated synthesis: Not just majority vote, but integrated insight
● Confidence calibrated across 5 perspectives
● Preserved dissent with conditions: Each minority view gets explicit conditions
○ Dissent 1: "Trace X holds if [condition A]"
○ Dissent 2: "Trace Y holds if [condition B]"
● Trigger conditions: What evidence would flip the consensus?
● Residual uncertainty acknowledged

Meta-Commentary:
● Methodological effectiveness ranking with justification
● Synergies identified: Which combinations complemented each other?
● Diminishing returns assessment: Did 5 traces add value beyond 3?
● Recommendations for future similar problems
Validation Time: ~150 minutes (5 × 25 min per trace + 25 min for CCC)

- Global Requirements (All Tiers)
✅ STRUCTURE PHASE (Every trace, every tier)
● Method from
srp_combinations.csv
- Record S_ID and S_Abbrev
● Ontology defined (entities + relationships)
● Boundaries stated (in/out of scope)
● Constraints listed (time, budget, technical, legal, ethical)
● Assumptions explicit (what must be true)
● Level of detail justified
● Stakeholders identified (if relevant)

✅ REASONING PHASE (Every trace, every tier)
● Method from
srp_combinations.csv
- Record R_ID and R_Abbrev
● Minimum 2 rivals (even in Low thinking)
● Each rival must have:
○ Clear statement
○ Supporting evidence + provenance
○ Contradicting evidence + provenance
○ Discriminating test (falsifiable)
○ Kill-step: indicator/threshold/action/owner
Kill-Step Format:
Indicator: [Specific measurable]
Threshold: [Numeric or clear qualitative trigger]
Action: [Concrete response]
Owner: [Named role or person]


✅ SCRATCHPAD (Every trace, every tier)
● Real tool calls (never simulated)
○ Query shown
○ API response captured verbatim
○ Evidence extracted with attribution
○ Timestamp + URL preserved
## Tool Call Format:
xml
<tool_call id="1">
<query>exact search query</query>
<api_response>[LITERAL RESPONSE - unedited]</api_response>
## <evidence_extracted>
<claim>Specific claim</claim>
<provenance>Source, URL, timestamp</provenance>
<confidence>0.XX - justification</confidence>
## </evidence_extracted>
## </tool_call>
● Memory operations (when appropriate)
○ Key + value
○ Value score (0-1: reuse potential)
○ Confidence (0-1: certainty)
○ Expiry + justification
○ Provenance + tags
## Memory Format:
xml
<memory_write id="1">
## <key>descriptive_key</key>
<value>Information</value>
<provenance>Source</provenance>
<confidence>0.XX</confidence>
<value_score>0.XX - why worth storing</value_score>
<expiry>Duration - why this timeframe</expiry>
<tags>retrieval, hooks</tags>
## </memory_write>
## ```

## ---


### ✅ PRESENTATION PHASE (Every trace, every tier)

- [ ] **Method from `srp_combinations.csv`** - Record P_ID and P_Abbrev
- [ ] **Complete SRP combination validated** - Record Index from CSV
- [ ] Format appropriate for Problem_Type and Output_Type
- [ ] All citations link to scratchpad
- [ ] Confidence calibrated (numeric + bounds)
- [ ] Next steps actionable

## ---

### ✅ SAGE BALANCE (Every trace, every tier)

**Score each facet 0-5. Minimum 3 for all facets.**

## | Facet | Score | Evidence |
## |-------|-------|----------|
| **Therapist** (empathy, agency, consent) | /5 | |
| **Scientist** (rivals, tests, calibration) | /5 | |
| **Generalist** (cross-domain, first principles) | /5 | |
| **Engineer** (concrete plans, edge cases) | /5 | |
| **Philosopher** (explicit assumptions, is/ought) | /5 | |
| **Artist** (clarity, detail calibration, metaphor) | /5 | |
| **Comedian** (appropriate levity, engagement) | /5 | |

**Acceptance Criteria:** No facet below 3, most at 4-5

## ---

## 4. Validation Protocol by Tier

###  Low Thinking Validation (25 min)

- **SRP Combination** (3 min):
- [ ] Find in `srp_combinations.csv`
- [ ] Verify Problem_Type matches
## - [ ] Record Index: ______

- **Structure** (4 min):
- [ ] All required elements present?
- [ ] Justification clear?

- **Reasoning** (8 min):
- [ ] 2+ rivals genuinely distinct?

- [ ] Evidence bidirectional (support + contradict)?
- [ ] Tests discriminating?
- [ ] Kill-steps concrete?

- **Scratchpad** (4 min):
- [ ] Tool calls real (verbatim responses)?
- [ ] Provenance complete?

- **Presentation** (4 min):
- [ ] Format matches CSV expectations?
- [ ] SAGE score all ≥3?

- **Overall** (2 min):
- [ ] Appropriate for Low tier? (could this be simpler?)
- [ ] Ready for synthetic templating?

## ---

###  Medium Thinking Validation (75 min)

**For each of 3 traces** (25 min × 3 = 75 min):
- Follow Low Thinking validation protocol
- **Additional**: Verify no S or R method repeats across traces

**CCC Validation** (10 min):
- [ ] Compare: Convergence/divergence clear?
- [ ] Contrast: Root causes of differences identified?
- [ ] Consensus: Synthesis genuine (not just vote)?
- [ ] Dissent preserved with conditions?
- [ ] Meta-commentary: Method effectiveness discussed?

**Overall** (5 min):
- [ ] Appropriate for Medium tier?
- [ ] Does multi-perspective analysis add value?
- [ ] Ready for synthetic templating?

## ---

###  High Thinking Validation (150 min)

**For each of 5 traces** (25 min × 5 = 125 min):
- Follow Low Thinking validation protocol
- **Additional**: Verify maximum methodological diversity


**CCC Validation** (20 min):
- [ ] Compare: Full convergence/divergence map?
- [ ] Contrast: Deep root cause analysis?
- [ ] Consensus: Sophisticated synthesis?
- [ ] Dissent: Each minority view has conditions?
- [ ] Meta-commentary: Effectiveness ranking + synergies?

**Overall** (5 min):
- [ ] Appropriate for High tier? (does this need 5 perspectives?)
- [ ] Does diminishing returns analysis show value?
- [ ] Ready for synthetic templating?

## ---

## 5. Tier Selection Guide (For Trace Creators)

### When to Use Each Tier:
## ```
## Problem Assessment
## ↓
How many reasonable approaches exist?
## ↓
├─ 1-2 approaches → LOW
├─ 3-5 approaches → MEDIUM
└─ 5+ approaches → HIGH

How ambiguous is the problem definition?
## ↓
├─ Clear scope, constraints → LOW
├─ Some ambiguity → MEDIUM
└─ Wicked problem → HIGH

How many stakeholders with conflicting interests?
## ↓
├─ Single perspective sufficient → LOW
├─ 2-3 perspectives valuable → MEDIUM
└─ Many conflicting views → HIGH

What are the stakes?
## ↓
├─ Low stakes, reversible → LOW
├─ Moderate stakes → MEDIUM
└─ High stakes, safety/ethics → HIGH
## ```


## ### Decision Matrix:

## | Characteristic | Low | Medium | High |
## |----------------|-----|--------|------|
## | Approaches | 1-2 | 3-5 | 5+ |
## | Ambiguity | Low | Moderate | High |
| Stakeholders | Single view | Multiple views | Conflicting views |
## | Stakes | Low | Moderate | High |
| **Recommendation** | **1 SRP** | **3 SRP + CCC** | **5 SRP + CCC** |

## ---

## 6. Critical Failure Modes by Tier

## ### ❌ Low Thinking Failures:
- **Over-simplification**: Only 1 rival considered (always need ≥2)
- **Missing complexity**: Problem actually requires Medium/High
- **Incomplete execution**: Skipping elements because "it's simple"

## ### ❌ Medium Thinking Failures:
- **Repeated methods**: Same S or R method in multiple traces
- **Fake diversity**: 3 traces that are cosmetically different but conceptually identical
- **Weak CCC**: Compare/Contrast superficial, consensus is just majority vote
- **Wrong tier**: Problem is actually Low (overkill) or High (insufficient)

## ### ❌ High Thinking Failures:
- **Method repetition**: Not maximizing diversity across 5 traces
- **Diminishing returns**: Traces 4-5 add no new insight
- **Shallow synthesis**: CCC doesn't integrate 5 perspectives meaningfully
- **Wrong tier**: Problem doesn't warrant 5 traces (could be Medium)
- **Missing dissent conditions**: Minority views dismissed instead of preserved

## ---

## ## 7. Example Tier Assignments

## ### Low Thinking Examples:
- "What's the capital of France?" ❌ Too simple - not suitable for ANY tier
- "Calculate optimal inventory reorder point given demand curve" ✅ 1 clear method
- "Should Company X use MySQL or PostgreSQL for this workload?" ✅ 2 clear rivals

## ### Medium Thinking Examples:

- "Design a content moderation policy balancing free speech and safety" ✅ Multiple
perspectives needed
- "Evaluate congestion pricing vs transit expansion for urban traffic" ✅ 3-4 reasonable
approaches
- "Recommend technology stack for mid-size e-commerce platform" ✅ Several valid options

## ### High Thinking Examples:
- "Develop national AI governance framework balancing innovation and safety" ✅ Many
stakeholders, high stakes
- "Design climate adaptation strategy for coastal city over 50 years" ✅ Wicked problem, high
complexity
- "Resolve ethical tensions in autonomous vehicle crash algorithms" ✅ Deep value conflicts, no
clear answer

## ---

## 8. Prompt Template for Frontier Models
## ```
You are generating a gold-standard reasoning trace at the [LOW/MEDIUM/HIGH] thinking level.

## === THINKING TIER ===
[LOW]: Generate 1 complete SRP trace
[MEDIUM]: Generate 3 complete SRP traces with different S/R methods + CCC synthesis
[HIGH]: Generate 5 complete SRP traces with maximum S/R diversity + deep CCC synthesis

## === TASK ===
[Insert specific task here]

## === TIER JUSTIFICATION ===
This task requires [LOW/MEDIUM/HIGH] thinking because:
- Number of reasonable approaches: [1-2 / 3-5 / 5+]
- Ambiguity level: [Low / Moderate / High]
- Stakeholder complexity: [Single / Multiple / Conflicting]
- Stakes: [Low / Moderate / High]

## === MANDATORY REQUIREMENTS ===
- Use ONLY SRP combinations from srp_combinations.csv
- For each trace:
- Complete Structure phase (ontology, boundaries, constraints, assumptions)
- Generate ≥2 rival hypotheses with bidirectional evidence
- Include discriminating tests and kill-steps for each rival
- Execute REAL tool calls (capture verbatim API responses)
- Include memory operations when reusable knowledge present
- Present with all 7 SAGE facets (each scored ≥3/5)

- [MEDIUM/HIGH only]: CCC synthesis with preserved dissent + conditions

## === SRP COMBINATION CONSTRAINTS ===
[For MEDIUM]: Use 3 different Structure methods and 3 different Reasoning methods
[For HIGH]: Use 5 different Structure methods and 5 different Reasoning methods

Suggested combinations from srp_combinations.csv for this task:
[List 3-5 valid Index values here]

## === OUTPUT FORMAT ===
[Include tier-specific checklist from above]

Begin generation:
## ```

## ---

## 9. The WFC Collapse Path
## ```
Perfect gold traces for training
↑ requires
Validated against tier-specific checklists
↑ requires
Tier-appropriate complexity (Low/Medium/High)
↑ requires
Problem characteristics match tier selection guide
↑ requires
Complete SRP pipeline in every trace
↑ requires
Valid combinations from srp_combinations.csv
↑ requires
All global requirements met (structure, reasoning, scratchpad, presentation, SAGE)
↑ requires
No shortcuts, no simulations, no compromises
Every constraint must hold. Violation at any level = trace rejected.


