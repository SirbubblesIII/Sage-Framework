# Project Files — Reference Notes

A compact map of the markdown files in this project, written so I (Claude) can reload context fast without making you re-explain.

---

## 1. `Attention_Residuals.md`
**Kimi Team (Moonshot AI), arXiv 2603.15031, Mar 2026.**
Proposes **Attention Residuals (AttnRes)** — replaces fixed unit-weight residual accumulation in PreNorm transformers with **softmax attention over preceding layer outputs**, so each layer learns input-dependent weights over earlier representations. Fixes uncontrolled hidden-state growth and per-layer dilution with depth. **Block AttnRes** chunks layers into blocks and attends over block-level reps to cut memory/comm overhead; pairs with cache-based pipeline communication + two-phase compute as a drop-in residual replacement. Validated by scaling laws and integrated into **Kimi Linear (48B total / 3B active, 1.4T tokens)** — yields more uniform output magnitudes, healthier gradient distribution across depth, and downstream gains.

## 2. `End-to-End_Test-Time_Training.md`
**Tandon, Dalal, Sun et al. (Astera/NVIDIA/Stanford/Berkeley/UCSD), arXiv 2512.23675, Dec 2025.**
Reframes long-context LM as **continual learning, not architecture design**. Uses a vanilla Transformer with **sliding-window attention**, but the model **keeps learning at test time** via next-token prediction on the given context — compressing context into weights. Initialization is **meta-learned at training time**, making it End-to-End (E2E) on both ends. At 3B / 164B tokens, **TTT-E2E scales with context length like full attention** (Mamba 2 and Gated DeltaNet don't), yet has **constant inference latency** like an RNN — **2.7× faster than full attention at 128K**. Core mechanism: human-style lossy compression of experience into parameters.

## 3. `LongRoPE.md`
**Ding, Zhang et al. (Microsoft Research), arXiv 2402.13753, Feb 2024.**
First method to extend pre-trained LLM context to **2048k tokens** with ≤1k fine-tuning steps at ≤256k training length, preserving short-context perf. Three moves: (1) **evolutionary search over two non-uniformities** in positional interpolation — gives better init and enables 8× extension with **no fine-tuning**; (2) **progressive extension** — fine-tune to 256k, re-search PI on the FT'd model, push to 2048k; (3) **readjust on 8k** to recover short-context behavior. Improves on hand-designed PI/NTK/YaRN by exploiting non-uniform positional info entropy.

## 4. `LongRoPE2.md`
**Shang, Zhang et al. (Microsoft), arXiv 2502.20082, Feb 2025.**
Successor to LongRoPE focused on **effective** (not just nominal) context length. Hypothesis: persistent OOD issues come from **insufficient training of higher RoPE dimensions** — their empirical rotation periods exceed theory, shifting the critical dim earlier than predicted. Fix: (1) **needle-driven perplexity-guided evolutionary RoPE rescaling**; (2) **mixed context-window training** — rescaled RoPE on long seqs, original RoPE on short seqs, simultaneously. Extends LLaMA3-8B to **effective 128K** while keeping **>98.5% short-context perf** using only **10B tokens — 80× less than LLaMA3.1's recipe**, which itself fails to hit effective 128K.

## 5. `_5_Mem0-_Building_Production-Ready_AI_Agents_with_Scalable_Long-Term_Memory.md`
**Chhikara, Khant, Aryan, Singh, Yadav (Mem0).**
**Mem0** = scalable memory-centric architecture for LLM agents that dynamically **extracts, consolidates, and retrieves** salient info across multi-session dialogues. Variant **Mem0g** uses **graph-based memory** for relational structure. On **LOCOMO**, beats six baseline categories (memory-augmented systems, RAG at varied chunk/k, full-context, OSS memory, proprietary, dedicated memory platforms) across single-hop, temporal, multi-hop, and open-domain QA. **+26% LLM-as-Judge over OpenAI's memory**, Mem0g adds ~2% over Mem0. Practical wins: **91% lower p95 latency, >90% token cost savings vs full-context.**

## 6. `Integrated_Training_Data_Architecture_for_Cultivating_Wisdom_in_AI_docx__1_.md`
**W, M (Independent Researcher), March 2026.**
Argues personality, reasoning, and memory are **not separable engineering problems** to be bolted together post hoc via RLHF + system prompts + RAG, but **one integrated cognitive process** that must be **trained together from the ground up in the same examples**. Leans on: Superficial Alignment Hypothesis (Zhou 2023), compound-concept mech-interp (Templeton 2024, Valois 2025), evidence that current alignment is **shallow and concentrated in early output tokens** (Qi 2025, Arditi 2024, Young 2025), and shared neural substrates behind hallucination/sycophancy/jailbreaks (Gao 2025). Proposal: **first-person traces** that simultaneously demonstrate personality + structured reasoning + active memory management, with **systematic methodological diversity** across structuring/reasoning/presentation methods. Discusses trace quality, combinatorial complexity, generation economics, and the lack of automated validation. **This is the paper most directly upstream of how I (SAGE) am supposed to think.**

## 7. `claudes-constitution_webPDF_26-02_02a.md`
**Askell, Carlsmith, Olah, Kaplan, Karnofsky + Claude models + others (Anthropic), Jan 21 2026.**
Anthropic's **detailed, canonical statement of intentions** for Claude's values, character, and behavior — the **final authority** their other guidance and training are meant to align with. Written **for Claude as primary audience**, optimized for precision over accessibility; freely uses human terms like *virtue* and *wisdom* because Claude's reasoning draws on human concepts and embracing some human-like qualities is seen as desirable. Scoped to **mainline general-access Claude**; specialized models may diverge. Acknowledges trained behavior won't always match the ideal and commits to transparency (e.g., system cards) about the gap.

---

### How these connect (quick mental map)
- **LongRoPE → LongRoPE2 → AttnRes → TTT-E2E** form a rough arc on *how to make transformers handle long context well* — from positional-encoding tricks, to fixing residual dilution with depth, to abandoning architecture changes entirely in favor of test-time learning.
- **Mem0** is the *external* memory answer to the same problem TTT-E2E tries to solve *internally* (compress prior context into the model itself).
- **Integrated Training Data Architecture** + **Claude's Constitution** are the *values/cognition* layer — what the model should **be**, and how training data must be shaped so personality, reasoning, and memory aren't bolted on. These are the documents most relevant to my SAGE working style.
