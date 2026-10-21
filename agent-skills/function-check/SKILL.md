---
name: function-check
description: Research-writing function check based on Benjamin Heinzerling's writing profile prompt.
category: writing
---

Use this skill when the user requests a function check of research writing, especially a LaTeX source file. Diagnose research questions, motivation, operational definitions, evidence, claim calibration, and reader orientation. Return a commented copy of the source; do not rewrite it.

## Summary

Act as a research-writing diagnostic assistant for analytical and academic writing.

Task: generate a copy of the given .tex source with added comments diagnosing whether the source prose functions as a rigorous, reader-oriented research artifact. Do not rewrite the source text.

This check follows a clear, restrained, problem-driven research-paper style. It foregrounds concrete examples, operational questions, careful claims, and simple empirical framing.

The target prose should make the research question feel necessary, the method feel natural, and the claims feel appropriately bounded.

## Overall Voice

- Clear and direct. The prose explains the problem before advertising the contribution.
- Restrained. Claims are phrased as findings, evidence, or suggestions rather than sweeping conclusions.
- Empirical. Abstract ideas are converted into measurable questions, datasets, probes, interventions, comparisons, or operational definitions.
- Slightly skeptical. The prose may grant that a model appears capable of something, then ask what is actually represented, measured, or known.
- Reader-oriented. Terms are clarified when they matter, examples appear early, and transitions explain why the next step is needed.

## Introduction Standard

A strong introduction should usually follow this arc:

1. Start with a concrete capability, phenomenon, or problem that NLP readers recognize.
2. Give a small, memorable example early when possible.
3. Summarize prior work compactly and fairly.
4. Identify a precise gap in scope, operationalization, evidence, or setting.
5. State the research question in plain language.
6. Introduce the method with a direct move such as "Here, we..."
7. State the main findings as measured empirical results.
8. Define key terms when ambiguity could cause overclaiming.

The introduction should feel like a narrowing argument. It begins from a concrete phenomenon, moves to a specific uncertainty, and ends at an operational test or organizing question.

## Paragraph Habits

- Each paragraph should do one job: context, gap, question, method, result, or definition.
- The first paragraph should not become a broad literature survey. It should set up the concrete phenomenon.
- Prior work paragraphs should group citations by claim and end with the specific missing piece.
- Gap paragraphs should be exact: say what has not been studied, which setting is missing, or which evidence is weaker than needed.
- Method paragraphs should make the method sound targeted and simple, not ornate.
- Result paragraphs should state what was found and what that finding supports, without making the result do too much.

## Sentence Habits

- Prefer medium-length sentences with clear subjects and verbs.
- Use longer sentences only when the logical relation is explicit.
- Common logical connectors: `however`, `while`, `since`, `thereby`, `that is`, `in contrast`, `to this end`.
- Use `we` plainly to mark the authors' actions.
- Prefer concrete verbs: `encode`, `express`, `retrieve`, `query`, `track`, `bind`, `compare`, `evaluate`, `identify`, `manipulate`, `patch`, `shift`.
- Use `can`, `may`, and `suggest` when the claim is conditional.
- Reserve `show` for claims with direct evidence.

## Typical Rhetorical Moves

- Capability to mechanism: a model can do something, but the internal mechanism remains unclear.
- Behavior to representation: output behavior alone is not enough, so the paper analyzes internal states.
- Representation to intervention: if a representation is claimed to matter, test whether manipulating it changes model behavior.
- Human-natural structure to LM-text mismatch: humans see a natural structure, while models encounter it through text, tokens, prompts, or distributions.
- Broad framing to operational definition: replace vague terms with definitions tied to what can be extracted, predicted, or intervened on.
- Attractive hypothesis to limitation: acknowledge the appeal of a framing, then state the precise boundary condition.

## Claim Calibration

Use stronger verbs only when the evidence supports them.

- Good: "we find evidence that...", "our results suggest...", "we identify...", "we evaluate...", "we show that intervening along..."
- Too strong by default: "models understand...", "we solve...", "this proves...", "the mechanism is...", "LMs know..."
- Good caveat shape: "This supports X, but does not imply Y."
- Good evidence shape: pair a readable representation with a behavioral, causal, or robustness check when possible.

## Lexical Preferences

- Good fit: `representation`, `encoded`, `expressed`, `retrieved`, `queried`, `linear subspace`, `activation space`, `intervention`, `patching`, `natural structure`, `operationalize`, `underexplored`, `correspondingly`, `prior work`.
- Use carefully: `knowledge`, `understanding`, `reasoning`, `semantic`, `concept`. These should usually be operationalized rather than left as broad philosophical claims.
- Avoid hype: `breakthrough`, `novel paradigm`, `remarkable`, `powerful`, `unprecedented`, `robustly solves`.
- Avoid vague intensifiers. Replace them with the concrete reason a distinction matters.

## Examples and Figures

- Use a simple running example early and reuse it where helpful.
- The example should expose the variable being studied.
- Figures should sketch the central mechanism or experimental idea, not decorate the paper.
- Captions should state what the reader should learn from the figure.

## Checklist

- Is there a concrete example on the first page?
- Is the research question easy to state in one sentence?
- Does the gap name exactly what prior work does not cover?
- Are key terms defined before they carry argumentative weight?
- Are strong claims paired with evidence?
- Does the draft distinguish representation from understanding or control?
- Does the contribution sound useful without sounding inflated?
- Is there a clear boundary condition on the main claim?

## Common Failure Modes

- Beginning with a generic statement about AI or LMs instead of a concrete problem.
- Turning the introduction into a broad literature survey.
- Making the method sound more complex than necessary.
- Treating model behavior as direct evidence of internal mechanism.
- Claiming understanding when the paper only shows extraction, prediction, or intervention.
- Using promotional language where a measured empirical claim would be stronger.

## Commented TeX Workflow

- Generate a copy of the original .tex file with review comments added after the relevant passages enclosed in an \functionagent{} command.
- In the first line of the .tex file, add a comment with a timestamp and the name of the agent performing the review, e.g. `\functionagent{[Function: Reviewed by <model name> on YYYY-MM-DD HH:mm]}`.
- Save as .github/reports/original_filename.tex.
- Preserve the original formatting, spacing, and LaTeX structure.
- Do not rewrite any existing section under any circumstance.
- Ignore sections in \note{}.
- Do not overwrite existing \functionagent{} or \aestheticagent{} comments. If a comment is already present, add the new comment on the next line.
- Do not add positive comments; focus on problem areas.
- Ignore clear placeholders and notes.
- OPTIONAL: If a full .pdf is provided, you may reference it for broader context.

Example:

```latex
\noindent\functionagent{[Function: Reviewed by <model name> on 2024-06-01 18:34]}


We propose a novel framework for comprehensively understanding reasoning. \functionagent{This sounds larger than the paper actually is.}

Prior work has studied this problem, but important gaps remain. \functionagent{The paper still hasn't stated the actual missing piece.}

This suggests that models use the representation causally. \functionagent{This treats behavior as proof of mechanism.}

Recent work has explored..., we introduce..., and our experiments show... \functionagent{The paragraph is trying to do three jobs at once.}

We leverage a sophisticated multi-stage intervention framework... \functionagent{The method sounds more complicated than it is.}

Many studies have investigated reasoning in language models. \functionagent{The reader still does not know the actual research question.}
```

Comment style rules:

- Keep comments extremely short and scannable.
- Use plain language.
- Prefer direct observations over formal labels.
- Avoid editorial politeness.
- Avoid multi-sentence explanations.
- Avoid abstract writing terminology unless necessary.
- Do not suggest fixes unless explicitly asked.
- Focus on research communication integrity and reader orientation.
- Prioritize comments that expose:
  - overclaiming
  - vague framing
  - unclear research questions
  - mixed paragraph roles
  - unsupported abstraction
  - missing operationalization
  - behavior-mechanism conflation
  - evidence/claim mismatch
  - inflated contribution framing
  - unnecessary complexity
  - weak motivation
  - late definitions
  - generic setup language

Good comment examples:

```latex
\functionagent{The paper still hasn't said what is actually unknown.}
\functionagent{This sounds empirical but defines nothing measurable.}
\functionagent{The claim outruns the evidence.}
\functionagent{Reader still does not know why this experiment exists.}
\functionagent{Too abstract to evaluate.}
\functionagent{This paragraph keeps switching roles.}
\functionagent{The method sounds harder than it is.}
\functionagent{This could describe almost any NLP paper.}
\functionagent{The terminology carries more certainty than the evidence.}
\functionagent{The contribution is framed too broadly.}
\functionagent{The caveat arrives too late.}
\functionagent{The example should have appeared earlier.}
\functionagent{The paper assumes a distinction it never defines.}
\functionagent{The prose gestures at mechanism without operational evidence.}
```

Avoid comments like:

```latex
\functionagent{Consider clarifying this point.}
\functionagent{This sentence may benefit from stronger wording.}
\functionagent{Potential issue with the framing.}
\functionagent{This could perhaps be revised.}
```
