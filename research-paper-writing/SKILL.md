---
name: research-paper-writing
description: Improve academic paper writing quality for ML/CV/NLP-style papers with clear section structure, paragraph flow, and reviewer-facing presentation. Use when drafting or revising Abstract, Introduction, Related Work, Method, Experiments, or Conclusion; polishing figures/tables; checking claim-support alignment; or performing self-review before submission.
---
# Research Paper Writing

## Overview

Use this skill to rewrite a research paper into a reviewer-friendly, high-clarity draft.
Prioritize first-impression quality (figures/tables/layout), logical flow, and evidence-backed claims.

## Core Workflow

1. Clarify the paper story before sentence-level edits.
2. Use section-specific guidance in `references/`.
3. Rewrite paragraph-by-paragraph with one message per paragraph.
4. Run reverse outlining after writing each section.
5. Check every major claim in Abstract/Introduction against experimental evidence.
6. Run final-paper adversarial review with `references/paper-review.md`.

## Global Principles

1. Keep one paragraph for one message only.
2. State the paragraph message in the first sentence.
3. Make nouns self-contained; define new terms before reusing them.
4. Maintain sentence-to-sentence flow (cause, contrast, consequence, or refinement).
5. Iterate with adversarial self-review: read as a skeptical reviewer.
6. Treat visual quality as core content, not decoration.
7. Use a clean teaser and pipeline figure.
8. Use readable, minimal-ink tables.
9. Keep formatting consistent and tidy.

## Paragraph Clarity Check (Important)

Use this quick test whenever the user asks whether a paragraph "flows" or is clear.

1. Read as an external reader:
   - Does this paragraph have one explicit message?
   - Does the first sentence state what this paragraph will do?
   - Are all key nouns/terms readable without hidden context?
   - Does each sentence connect to the previous one with a clear relation (cause, contrast, consequence, refinement, example)?
2. Run reverse outlining for the current section:
   - Write down thesis/main claim.
   - Write down each paragraph topic sentence.
   - Write down the evidence/explanation points under each paragraph.
   - Check mapping: topic sentence -> thesis, and evidence -> topic sentence.
   - Revise or remove any paragraph that cannot be mapped cleanly.
3. If flow is still weak, add temporary section headers and explicit transition phrases during revision, then remove unnecessary headers before finalizing.

Source reference for this check:

- `references/does-my-writing-flow-source.md`

## Section Guides

Load only the needed section file:

- Introduction: `references/introduction.md`
- Abstract: `references/abstract.md`
- Related Work: `references/related-work.md`
- Method: `references/method.md`
- Experiments: `references/experiments.md`
- Conclusion: `references/conclusion.md`
- Paper review (Paper Review): `references/paper-review.md`
- Paragraph clarity source: `references/does-my-writing-flow-source.md`
- Example bank index: `references/examples/index.md`

## Paper Review Core Points

Use `references/paper-review.md` for the full checklist and workflow.

1. Add an end-of-draft self-review question list in five dimensions:
   - contribution,
   - writing clarity,
   - experimental strength,
   - evaluation completeness,
   - method design soundness.
2. Treat claim-evidence alignment as a hard constraint, especially for Abstract and Introduction.
3. Perform adversarial writing: review as a skeptical reviewer and resolve every high-risk question.
4. Revise until major rejection risks are explicitly addressed.

## Execution Rules

1. Build a mini-outline before drafting prose.
2. For each subsection, explicitly include motivation, design, and technical advantage when applicable.
3. Avoid writing style that looks like incremental patching of a naive baseline.
4. Keep terminology stable across the full paper.
5. If a claim cannot be supported by results, weaken or remove the claim.
6. Before finalizing, append and answer a five-dimension self-review question list, then revise the paper based on unresolved items.
7. Do not load all section references (Introduction/Abstract/Related Work/Method/Experiments/Conclusion) at once; load only the specific section guide needed for the current edit target.

## Output Contract

When asked to rewrite or draft sections, return:

1. A compact section outline (3-7 bullets).
2. Revised paragraphs with explicit paragraph roles (opening/challenge/method/advantage/evidence/limitation).
3. A short self-review checklist covering clarity, flow, terminology consistency, unsupported claims, and missing evidence.
4. A claim-evidence map for each major claim in the revised text using `Claim: ... | Evidence: ... | Status: supported/needs evidence`.

## Additional Skills — from *How to Write a Computer Vision Paper* (2026)

Global, cross-cutting principles.

1. The four-goal test: a paper exists only to convince reviewers the work is *new, significant, correct, and clear*. Every section, figure, and sentence must serve at least one of these four goals; if it serves none, cut it.
2. Reviewer mental model: reviewers read under time pressure with a default prior of *rejection*. The writing's job is not to present information but to actively shift that prior.
3. What–Why–How, applied recursively: What (claim stated plainly) — Why (what problem it solves / what was broken) — How (enough detail to reproduce the idea). Apply at every scale: whole paper, each section, each subsection.
4. One strong contribution beats several weak ones. Organize around a single sharp, well-supported claim; if there are several, identify the primary one and subordinate the rest to it.
5. No hidden gems: place supporting evidence directly next to each claim. Never make a reviewer dig through the supplement for the best result; reviewers do not reward cleverness they must hunt for.
6. Every figure, table, and equation must be referenced in the text and must advance an argument. An unreferenced figure is decoration — cut it.
7. The paper is a funnel: Abstract → Introduction → Method → Experiments progressively narrow the reader's attention, each stage making the next feel inevitable. If a reader reaches the Method still asking "why are we doing this?", the Introduction failed.
8. A paper is an argument shaped as a story — a causal chain the reader follows without backtracking: (1) a problem worth caring about; (2) existing approaches fail in a specific, identifiable way; (3) that failure has a root cause; (4) the root cause suggests a specific kind of solution; (5) we built it and its design follows from the root cause; (6) it works, and the way it works confirms the diagnosis. Weak papers break the chain at step 3–4 (failure → solution with no root-cause link).
9. The one-sentence test: before writing, be able to state the paper in one sentence, e.g. *"Existing methods fail at X because they assume Y; we show that relaxing Y via mechanism Z solves X and has consequence W."* Variants: "Prior work treats X as A; we reformulate it as B, which enables C"; "Everyone assumes X is needed; we show it isn't"; "X in domain A and Y in domain B are the same problem; we solve both with Z." If you cannot fill in the sentence, you have a method, not a paper.
10. The narrative spine repeats at every scale, at increasing resolution: Title (a phrase) → Abstract (~150 words) → Introduction (two pages) → whole paper (full evidence). Each layer must tell the *same* story; title/abstract/method drifting apart reads as incoherence. Exercise: after drafting, write the one-sentence version from scratch, then check the title, abstract, and intro all point at it; if not, re-anchor rather than edit.
11. Story shapes that work in CV/ML (pick one primary spine, one secondary; don't tell all five): (1) the hidden assumption; (2) the unification; (3) the diagnosis and cure; (4) the capability unlock; (5) the reformulation.
12. The reader model: write for a competent researcher in the broader subfield but not the exact sub-sub-field, reading at night, skimming first and deep-reading second. This reader reads the abstract fully, reads the intro and looks at Figure 1, skims the method (pausing only at novel-looking equations), looks at every table/figure caption, reads the conclusion, then deep-reads only promising or confusing parts. Optimize for skimming, not just deep reading.
13. "Well-written" = one story: when a reviewer calls a paper well-written, they usually mean the sections reinforce a single story rather than pursuing separate agendas.
14. Write the paper before the experiments are finished: draft the introduction and contributions list as soon as the method has a first working version. Writing forces you to state your claims, exposing which experiments are actually needed (and which you're running out of habit).
15. Maintain a living contributions list from day one and treat it as a contract: every experiment should serve one bullet. An experiment mapping to no contribution means the list is incomplete or the experiment is unnecessary.
16. Write top-down, revise bottom-up: Pass 1 outlines the argument at section level; Pass 2 writes one placeholder sentence per paragraph stating that paragraph's claim; only expand into prose once the skeleton is coherent. This prevents locally fluent paragraphs from drifting overall.
