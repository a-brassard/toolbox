---
title: "Ana Brassard Writing Style Profile"
type: analysis
status: active
source_weighting: "Dissertation_2025 (anchor) > COLM_2024 > EMNLP_2023 > CSKB_2021 > Master_2018"
summary: "Systematic, empirically rigorous style for NLP research. Clear problem setup with concrete examples, structured argumentation, methodical methodology reporting, and nuanced discussion of limitations."
---

# Ana Brassard Writing Style Profile

## Summary
You write in a **methodical, empirically-grounded research style** that prioritizes **clarity and rigor over flourish**. Your prose is direct, formally structured, and guided by a strong commitment to reproducibility and transparent reasoning. You move from concrete motivations through systematic analysis to carefully calibrated claims.

## Source Weighting
- **Primary anchor (dominates profile):** Dissertation_2025 — most developed voice, comprehensive chapters with refined technical writing
- **Strong secondary:** COLM_2024 — conference paper showing consolidated approach to complex evaluation design
- **Supporting:** EMNLP_2023 — similar conference paper, validates patterns across publication venues
- **Earlier foundations:** CSKB_2021, Master_2018 — shows stability of voice across 7 years

## Overall Voice
**Formal, restrained, problem-driven, systems-focused.**
- Not promotional or persuasive; instead, oriented toward diagnosis and measurement
- Confident in framing (you state research questions directly), but cautious in claim strength
- Tone: professional, detail-minded, aware of methodological limitations
- Audience: other NLP researchers; assumes strong technical background

Key voice markers:
- Opens with concrete problem or example ("The primary objective is to assess...")
- Avoids hedging phrases like "seems," "perhaps," "may be"—you commit to statements about what you *found*
- Uses "we" throughout (collaborative framing), never "I" except in very personal contexts (acknowledgments)
- Rarely uses exclamation marks; emphasis comes through structural emphasis, not punctuation

## Introduction Structure

**Pattern (observed across all works):**

1. **Concrete capability or challenge (opening move)**
   - Example: "Natural language processing systems that not only generate correct output, but also provide an explanation... are desirable"
   - You anchor to a real, recognizable problem before abstracting

2. **Recognition of existing weakness**
   - "Since explanations are typically free-form text, automatic evaluation suffers the well-known, but as of yet unresolved, weaknesses..."
   - You acknowledge prior art and what remains unsolved

3. **Gap identification (specific, not vague)**
   - Not: "More work is needed"
   - Instead: "We investigate whether LLMs can serve as a viable alternative... To see whether these benefits are realized, we first formulate specific requirements..."
   - You articulate *what specific question* you're addressing

4. **Research question or objective stated explicitly**
   - Dissertation intro: "(i) When do models learn to explain? (ii) How do models explain? (iii) Are LLMs reliable judges?"
   - Questions are numbered and parallel in structure

5. **Contributions stated as discrete, enumerated items**
   - Bulleted list of what the work delivers
   - Example: "Two new datasets... A new evaluation method... Meta-evaluation methods..."

## Paragraph-Level Habits

**Consistent structure within body sections:**
- Paragraph 1: Motivation or framing for subsection
- Paragraph 2: Your approach or method (what you actually did)
- Paragraph 3: Results or findings (factual, minimal interpretation)
- Final paragraph: Implication or transition to next idea

**Connective tissue:**
- Topic sentences are explicit and often repeat key terms from previous paragraph
- You favor "Specifically," "We," "Our," and "The results show" over softer transitions
- Rarely opens paragraphs with questions (you state, then expand)

**Data presentation paragraphs:**
- Move seamlessly from method description to data statistics
- Numbers are embedded naturally: "COPA-SSE contains 9,747 commonsense explanations for 1,500 Balanced COPA questions. Each question has up to nine explanations..."
- No separate "Results" sentence; the data IS the result

## Sentence-Level Habits

**Length:** Mixed, but purposeful
- Complex sentences reserve subordination for explanatory material: "We created this dataset with several uses in mind: it can serve as training data for... or as representations of ideal subgraphs..."
- Shorter sentences for key claims: "Our goal is to add high-quality explanations to Balanced COPA."
- Run-on coordination avoided; instead use em-dashes or colons

**Passive voice: Almost never**
- "We collected" not "Explanations were collected"
- Even in methodology sections, you maintain agent visibility: "Workers were asked to provide..." (passive here, but followed by active framing)

**Hedging in claims:**
- You use **very little hedging** for empirical findings: "The correlation... ranged between 0.54 and 0.93"
- When uncertainty is warranted, you use: "may," "can," "suggests," "could," "appears"
- Never speculative: avoid "might suggest" or "seems to indicate"

**Preferred verbs:**
- Action-oriented: "compare," "measure," "evaluate," "investigate," "propose," "demonstrate"
- Minimal: "show," "suggest," "indicate" (used only when evidence is indirect)
- "Collect," "extract," "aggregate" for data work
- Rarely use: "analyze" alone; instead "analyze differences" (more specific)

**Example clauses:**
- Frequent, grounded in your actual data: "For example, in a manual inspection of 1,200 CoS-E samples most explanations were judged to be..."
- Never hypothetical examples; always from your dataset

## Rhetorical Moves to Imitate

1. **Concrete → Abstract → Concrete (throughout)**
   - Start with a real COPA question ("The documents were loose. Effect?")
   - Generalize about what this shows
   - Return to similar examples to reinforce

2. **Problem Diagnosis → Systematic Measurement → Actionable Finding**
   - Acknowledge evaluation is subjective and manual
   - Design quantitative framework to measure specific aspects
   - Report findings with nuance about what the numbers mean

3. **Explicit Comparison (human vs. LLM, across model sizes, across datasets)**
   - You love side-by-side numerical comparison
   - Figure 4.2 juxtaposing GPT-3.5 vs GPT-4 is quintessential
   - Always contextual: *why* the difference matters

4. **Limitation-First Framing in Discussion**
   - Instead of: "Our results are great because..."
   - You: "While correlation between LLMs and human judges was high but not perfect, they did not negatively impact inter-annotator agreement. This suggests..."
   - Leads with the caveat, then interprets it

5. **Operational Definition Before Measurement**
   - State your working definition explicitly: "A good explanation is a minimal set of relevant commonsense statements that coherently connect..."
   - Then measure against that definition
   - Justifies your criteria

## Preferred Claim Strength

**How you calibrate assertions:**

| Claim Type | Your Language |
|-----------|---------------|
| Empirical fact | "We found," "Results show," "The correlation was 0.72" |
| Well-supported conclusion | "This suggests," "indicates," "is consistent with" |
| Method capability | "can serve," "is capable of," "enables" |
| Limitation or open question | "may," "could," "remains unclear," "warrants further investigation" |
| Hypothesis (not yet tested) | Rare; you avoid this unless explicitly framed as future work |

**Rarely use:** "appears to," "seems," "it could be argued," "one might say"
**Frequently use:** "quantify," "measure," "verify," "confirm"

## Lexical Preferences

**Favorite technical markers:**
- "Aspect-wise" (repeats across papers: "aspect-wise quality labels")
- "Fine-grained analysis"
- "Diagnostic" (Dissertation title embraces this)
- "Faithfulness," "explainability," "reasoning"
- "Benchmark," "dataset," "criteria" (institutional terms, not folksy)

**Connecting words you rely on:**
- "Moreover," "Furthermore" (builds on prior point)
- "To verify this," "To see whether" (moves toward evidence)
- "In summary," "In short" (rare; when used, signals wrap-up)
- "However," "Still," "Despite this" (nuance and contrast)

**Words you avoid:**
- "Very," "clearly," "obviously" (no intensifiers)
- "Hopefully," "interestingly," "surprisingly" (no editorializing)
- "Just," "simply," "merely" (no false minimization)

**Terminology precision:**
- Distinguish consistently: "gold labels" vs. "majority-voted labels"
- "Workers" not "annotators" or "raters" (though you use all three, workers is primary in methodological sections)
- "Crowdsourced" for human collection; "generated" or "prompted" for LLM-produced text

## Figure and Example Style

**How you use examples:**
- **Early in section:** Concrete Q&A with explanations shown verbatim
- **Labeled with "best" and "worst" categories** to illustrate quality range
- Tables show multiple examples from the same source to demonstrate consistency
- Explanations are presented as they appear in data (sometimes ungrammatical; you preserve fidelity)

**Figure captions:**
- Explicit about what the figure shows: "Figure 1.1 A commonsense reasoning question and an example output with the answer and a justification."
- Longer captions (2-3 sentences); not relying on inline text alone

**Tables:**
- Dense, information-rich
- Column headers are precise: "Criterion" (not "Type"), "Avg. score" (not "Score")
- Row labels are systematic: consistent naming across related tables

## How To Draft In This Style

**Pre-writing:**
1. Identify your **concrete anchor**—the actual problem or dataset that motivated the work
2. State **what question you're answering** explicitly; don't bury it
3. List **three main findings** you'll report; structure sections around these

**Drafting:**
1. **Introduction:** Concrete problem → Literature gap → Your research question → Contributions (numbered)
2. **Methods/Data:** What you did, step-by-step, without editorializing. Focus on reproducibility.
3. **Results:** Report measurements and comparisons with minimal interpretation
4. **Discussion:** Lead with limitations, then what the findings suggest

**Sentence work:**
1. Ensure each sentence is **active voice** (subject → verb → object)
2. If you use subordination, subordinate the less important information
3. Avoid hedging on empirical claims; save hedging for interpretation ("suggests," not on the measurement itself)
4. One idea per sentence; don't force multiple claims

**Revision:**
1. Check: Does each paragraph have a **topic sentence**?
2. Check: Is every **number grounded** in what you actually measured or collected?
3. Check: Have you **named your dataset/corpus** consistently throughout?
4. Check: Is every **methods subsection reproducible** without your paper in hand?

## Revision Prompt For Mimicking Your Style

```text
Revise this passage to match Ana Brassard's research-paper style:
- Replace any vague claims with measured statements
- Make agents visible (use active voice)
- Ground all examples in concrete data
- Add explicit topic sentences to paragraphs
- Remove hedging on facts; save hedging for interpretation
- Check that methodology is reproducible from text alone
- Ensure transitions move the argument forward, not just connect ideas