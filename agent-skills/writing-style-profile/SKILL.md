---
name: writing-style-profile
description: Source-free drafting and revision prompts for writing research papers in Ana Brassard's style.
category: writing
---

Use this skill when the user asks to draft, revise, outline, or check the claims of research-paper text in Ana Brassard's writing style, or invokes “writing style profile.” Apply the matching prompt below (drafting, revision, outline, or calibrated claims) to the user's text.

# Ana Brassard Writing Style Guide
## Source-Free Drafting & Revision Prompts

Use these prompts with ChatGPT, Claude, or any LLM writing assistant to draft or revise in this research-paper style.

---

## 1. Core Drafting Prompt

**Use this when starting a new section, paper, or research write-up:**

```
Write in research-paper style with these characteristics:

VOICE & TONE:
- Formal, restrained, empirically grounded
- Problem-driven; focus on measurement and diagnosis
- Direct and clear; avoid hedging on empirical facts
- Confident in framing research questions; cautious in claim strength
- Use "we" throughout (never "I" except in acknowledgments)
- No exclamation marks, intensifiers ("very," "clearly"), or editorializing ("interestingly," "surprisingly")

INTRODUCTION STRUCTURE:
- Start with a concrete, recognizable problem (not abstract)
- Acknowledge what prior work has achieved
- Identify the specific gap or limitation (what remains unsolved)
- State the research question or objective explicitly
- List contributions as numbered, parallel items (bullet points or enumeration)

PARAGRAPH PATTERNS:
- Each paragraph has an explicit topic sentence
- Move from motivation → method → findings → implication
- Use strong transitions: "Specifically," "To verify this," "The results show," "In summary"
- Avoid soft transitions; make the logical connection explicit

SENTENCE LEVEL:
- Use active voice (subject → verb → object)
- Mix sentence length purposefully: complex for explanation, short for key claims
- Use em-dashes and colons for subordination; avoid run-on coordination
- Subordinate less important information; keep main idea in main clause
- Ground all examples in actual data or methods, never hypothetical

CLAIMS & HEDGING:
- Empirical facts: "We found," "Results show," "The correlation was 0.72"
- Well-supported conclusions: "suggests," "indicates," "is consistent with"
- Method capability: "can serve," "is capable of," "enables"
- Limitations: "may," "could," "remains unclear," "warrants further investigation"
- Never use: "appears to," "seems," "one might say," "it could be argued"

VOCABULARY & TERMS:
- Prefer: "compare," "measure," "evaluate," "investigate," "propose," "demonstrate"
- For data work: "collect," "extract," "aggregate," "curate"
- Connectives: "Moreover," "Furthermore," "However," "Still," "Despite this"
- Use consistent terminology throughout (don't switch between "raters," "annotators," "workers" randomly)
- Avoid: "just," "simply," "merely," "hopefully"

EXAMPLE & DATA PRESENTATION:
- Ground all examples in actual datasets or observations
- Label examples (e.g., "best," "worst," "top-rated," "high-quality")
- Present data naturally: "Dataset X contains 1,000 samples. Each sample has five ratings."
- Use figures and tables early in relevant sections with detailed captions
- Preserve data as it appears (don't clean up ungrammatical explanations if that's authentic)

METHODS & REPRODUCIBILITY:
- Every detail needed for reproduction should be in the text
- Don't assume readers have access to your code or materials
- Specify versions, hyperparameters, random seeds, software libraries
- Explain choices: why this method? Why this threshold? Why this subset?

DISCUSSION & LIMITATIONS:
- Lead with limitations, not strengths
- Frame as: "While X is limited by Y, this still suggests Z"
- Avoid: "Our results show X is great because Y" without caveats
- End with implications or future work (brief, grounded in findings)

---
```

## 2. Revision Prompt

**Use this on an existing draft to tighten it toward this style:**

```
Revise this passage to match research-paper style with these priorities:

1. FACTS & EMPIRICISM:
   - Replace vague claims with measured, specific statements
   - If reporting findings: include numbers, not just directions
   - Keep assertions grounded in what you actually did or observed

2. CLARITY & DIRECTNESS:
   - Make agents visible (prefer active voice; if passive, explain why)
   - Strengthen topic sentences; make logical flow explicit
   - Remove hedging on empirical facts (hedge only on interpretation)

3. STRUCTURE & FLOW:
   - Check each paragraph has a topic sentence
   - Verify transitions move the argument forward
   - Ensure examples are from real data, not hypothetical

4. TERMINOLOGY & CONSISTENCY:
   - Use the same term throughout (don't switch synonyms)
   - Replace folksy language with technical precision
   - Remove intensifiers, editorializing, and speculation markers

5. METHODOLOGY & REPRODUCIBILITY:
   - Add missing details (versions, hyperparameters, datasets sizes, etc.)
   - Make every procedure explicit enough to reproduce without external materials
   - Explain *why* each choice, not just *that* you made it

6. CLAIMS & HEDGING:
   - Empirical findings: report without hedging
   - Interpretations: use "suggests," "indicates," "is consistent with"
   - Limitations: use "may," "could," "warrants investigation"
   - Remove: "seems," "appears," "might suggest," "one could argue"

---
```

## 3. Paper Outline Prompt

**Use this to structure a full paper or long document:**

```
Structure your paper using this framework:

INTRODUCTION:
- [Concrete problem or capability]
- [Current state of prior work (what's been solved)]
- [Specific gap or limitation (what remains unclear)]
- [Your research question(s) — stated explicitly, often numbered]
- [Your contributions — enumerated, parallel structure]

RELATED WORK / BACKGROUND:
- Survey existing approaches to this problem
- Emphasize what they achieved and what they left unresolved
- Position your work relative to prior art (what's different/new)

METHODS / DATA / DESIGN:
- What you built, collected, or set up
- Step-by-step reproducibility detail
- Why each choice (justify non-obvious decisions)
- Dataset statistics (size, composition, distributions)

EXPERIMENTS / RESULTS:
- Report findings with numbers; minimal interpretation here
- Use tables/figures; reference them explicitly
- Compare systematically (e.g., model size, dataset source, human vs. LLM)
- Present both positive and negative findings

ANALYSIS / DISCUSSION:
- Lead with limitations of your method or findings
- Interpret what results mean: why did X happen? What does it tell us?
- Compare to prior work: are results aligned? Do they contradict?
- Brief implications or future directions

CONCLUSION:
- Restate your research question
- Summarize your main findings (1-2 sentences)
- Reiterate contributions

---
```

## 4. Calibrated Claim Prompt

**Use this to check whether your hedging matches your evidence:**

```
For each claim in your draft, ask:

IF YOU'RE CLAIMING: "X is true / happened / was found"
- EVIDENCE: Did I measure/observe/collect this myself?
- LANGUAGE: "We found," "Results show," "X occurred in Y% of cases"
- Don't hedge: Report the fact.

IF YOU'RE CLAIMING: "X suggests / indicates / is consistent with Y"
- EVIDENCE: Is the connection logical but not directly proven?
- LANGUAGE: "suggests," "indicates," "is consistent with," "implies"
- OK to hedge slightly here.

IF YOU'RE CLAIMING: "X is possible / could happen / may indicate"
- EVIDENCE: Am I speculating or discussing limitations?
- LANGUAGE: "may," "could," "might," "appears possible"
- Use only for genuine uncertainty, not vagueness.

IF YOU'RE CLAIMING: "X is notable / interesting / surprising"
- STOP. Don't editorializ. Instead, report what X *is* and let readers judge.
- Replace: "Surprisingly, X correlated with Y" → "X correlated with Y (r=0.72), above the prior average of 0.45"

CHECKLIST:
- [ ] Every claim has evidence attached (data, method, prior work)
- [ ] Hedging matches uncertainty level
- [ ] No claims are speculation dressed as finding
- [ ] Positive and negative findings are reported equally
- [ ] Limitations are stated upfront, not hidden

---
```

## 5. Quick-Reference: Vocabulary & Connectives

### Strong Action Verbs (Use These)
```
compare    measure     evaluate    investigate
propose    demonstrate  establish   quantify
verify     confirm     identify    extract
collect    curate      aggregate   analyze
```

### Connectives That Move Arguments
```
Specifically        To verify this      However
Moreover            Furthermore         Still
The results show    In summary          Despite this
To address this     Conversely          Additionally
```

### Words to Avoid
```
very        clearly    obviously   hopefully
just        simply     merely      arguably
interestingly       surprisingly  seemingly
appears    seems      might suggest   one could say
```

### Hedging: Use Only When Appropriate
```
may         could       suggests    indicates
is consistent with      appears possible     warrants investigation
```

---

## 6. Usage Instructions

### **For Drafting New Text:**
1. Copy the **Core Drafting Prompt** into your LLM (ChatGPT, Claude, etc.)
2. Add: `[Your topic/section title]. Here's what I want to cover: [bullet points]`
3. Request: "Draft this section following the style guide above."
4. Revise the output using the **Revision Prompt** if needed

### **For Revising Existing Drafts:**
1. Copy the **Revision Prompt** into your LLM
2. Paste your draft
3. Request: "Revise this using the priorities above. Keep my ideas; improve clarity and style."

### **For Structuring a Full Paper:**
1. Use the **Paper Outline Prompt** to organize sections
2. For each section, use the **Core Drafting Prompt** to write that section
3. Use the **Revision Prompt** on the full draft after assembly

### **For Checking Claims:**
1. Extract all major claims from your draft
2. Use the **Calibrated Claim Prompt** to verify hedging matches evidence
3. Adjust language as needed

### **Tips:**
- **Don't over-rely on LLMs.** These prompts guide style; *your ideas and findings* come from you.
- **Iterate.** First draft with LLM assistance, then read and revise by hand.
- **Customize.** Adjust the prompts if your specific paper needs different structure (e.g., position papers, reviews).
- **Preserve your voice.** These prompts describe a style, not a voice-replacement. Your unique perspective should still shine through the structure.

---

## Examples

### Example 1: Vague → Specific

**Before (vague):**
> "We investigated whether language models could evaluate explanations. The results were interesting and suggested potential for future use."

**After (following this style):**
> "We investigated whether large language models could reliably evaluate free-text explanations by comparing LLM ratings against five independent human raters. LLM ratings correlated with majority-voted human judgments at r=0.72 (GPT-4o), though this falls below full replacement of human annotation."

### Example 2: Passive → Active with Detail

**Before (incomplete):**
> "A dataset was created with 3,000 explanations."

**After (following this style):**
> "We crowdsourced 3,000 explanations using Amazon Mechanical Turk. Workers were instructed to write detailed, contrastive explanations (focusing on key differences between answer choices) and were compensated at $0.89 per explanation, matching $20/hour. All workers passed a qualification round ensuring 59% match rate on gold-standard examples."

### Example 3: Hedging Too Much → Appropriate Calibration

**Before (over-hedged):**
> "The results seem to suggest that LLMs may possibly indicate some capability for evaluation, which could imply future potential."

**After (calibrated):**
> "LLMs demonstrated moderate capability for explanation evaluation. Spearman correlations with human ratings ranged from 0.54 to 0.93 depending on the evaluation criterion. However, LLMs did not reliably replace human annotation, suggesting they are best used as additional raters in limited-budget scenarios."

---

## Notes

- This guide emphasizes **empirical clarity and rigor** — appropriate for research papers, methods documentation, and technical writing.
- **Not suitable for:** Opinion pieces, creative writing, marketing copy, or casual communication (would need different guidance).
- **Customization:** Adjust vocabulary or structure if your field uses different conventions (e.g., qualitative research, humanities).
- **Tone variation:** This guide aims for "restrained" and "formal." If your audience expects more accessibility or directness, dial back the formality slightly.

---

**Last updated:** 2026-05-25  
**Purpose:** Reusable drafting guidance for research-paper writing  
**Status:** Ready to use; update if your style evolves
