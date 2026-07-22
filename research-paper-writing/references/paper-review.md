# Paper Review (Paper Rview)

## Goal

Use an adversarial, reviewer-style checklist to detect reject risks early and revise the paper before submission.

## Core Principle

Pursue perfectionism in paper quality: assume reviewers will probe every weak point and proactively fix them.

## Critical Rule (Do Not Violate)

Every major claim, especially in Abstract and Introduction, must be:

1. technically correct, and
2. explicitly supported by experimental evidence.

If a claim is not supported, either add evidence or weaken/remove the claim.

## What Usually Gets a Paper Accepted

1. Sufficient contribution (for example: novel task, novel pipeline, novel module, novel design choices, new experimental findings, or new insight).
2. Better empirical performance than prior methods under fair comparisons.
3. Sufficient comparison experiments and ablation studies.

## Common Rejection Dimensions

| Rejection Dimension          | Typical Failure Signals                                                                                                                                                                                                                                                                    |
| ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 1. Insufficient contribution | 1.1 Targeted failure cases are too common.<br /> 1.2 Proposed technique is already well explored; expected gains are predictable/well-known.                                                                                                                                               |
| 2. Unclear writing           | 2.1 Missing technical details; work is not reproducible.<br />2.2 A method module lacks clear motivation.                                                                                                                                                                                  |
| 3. Weak empirical effect     | 3.1 Improvement over prior methods is only marginal.<br /> 3.2 Even if better than previous methods, absolute performance is still not strong enough.                                                                                                                                      |
| 4. Incomplete evaluation     | 4.1 Missing ablation studies.<br />4.2 Missing important baselines or important evaluation metrics.<br /> 4.3 Datasets are too simple to prove the method truly works.                                                                                                                    |
| 5. Problematic method design | 5.1 Experimental setting is unrealistic.<br />5.2 Method has technical flaws and appears unreasonable.<br />5.3 Method is not robust and needs per-scenario hyperparameter tuning. <br /> 5.4 New design introduces stronger limitations than its benefits, leading to negative net value. |

## End-of-Paper Self-Review Question List

Add this checklist near the end of the draft while revising.
Use each question to trigger concrete edits before submission.

### 1. Contribution

1. What new knowledge does this paper give to readers?
2. Are we solving a truly meaningful failure case, not a trivial/common one?
3. Is the technical idea genuinely non-obvious beyond well-explored practice?
4. Is our gain surprising or insightful rather than a predictable improvement?
5. Is there at least one clear novelty type (task/pipeline/module/design finding/insight)?

### 2. Writing Clarity

1. Can a knowledgeable reader reproduce the method from the paper?
2. Did we provide enough technical detail for each key module?
3. Is the motivation of every module explicit and logically connected to a challenge?
4. Are terms and notation consistent across sections?
5. Does each paragraph carry one clear message with smooth transitions?

### 3. Experimental Strength

1. Are improvements over strong baselines meaningful, not just statistically tiny?
2. Is absolute performance competitive enough for the target venue?
3. Are gains consistent across multiple datasets/settings/metrics?
4. Do we report both strengths and failure cases honestly?

### 4. Evaluation Completeness

1. Do we include ablations for all key design choices?
2. Are all strong/recent baselines included under fair settings?
3. Are evaluation metrics standard and sufficient for this task?
4. Are datasets/scenarios challenging enough to validate real effectiveness?
5. Are comparison and ablation protocols clearly documented?

### 5. Method Design Soundness

1. Is the experimental setting realistic for practical use?
2. Does the method have hidden technical defects or unreasonable assumptions?
3. Is the method robust without heavy per-case hyperparameter retuning?
4. Do benefits outweigh added complexity and new limitations?
5. Could reviewers reasonably argue that the net benefit is negative?

## Adversarial Writing Workflow

1. Read the paper as a skeptical reviewer.
2. Answer every question above with explicit evidence from the paper.
3. Mark each item as `pass`, `needs revision`, or `needs new experiment`.
4. Revise claims, writing, experiments, or method scope accordingly.
5. Repeat until no major rejection risk remains.

## Additional Skills — from *How to Write a Computer Vision Paper* (2026)

### Novelty (establishing and ranking the contribution)

1. Demonstrate novelty by showing no prior work addressed the same problem or proposed a conceptually similar approach. Avenues: (a) a new problem formulation, ideally paired with a dataset/benchmark; (b) a new approach to a well-known problem; (c) a creative combination of existing ideas yielding a non-obvious capability; (d) a non-trivial application to a new domain where the adaptation itself required insight; (e) removing a limitation of prior work through a principled fix — not a patch.
2. Novelty must be non-trivial intellectual effort. A new problem needs a dataset with genuine collection/annotation (manual labeling, expert verification, non-trivial scale) or a method not derivable by routine engineering. Applying an off-the-shelf method with minor tweaks, or swapping one backbone for another, does not qualify — regardless of performance.
3. The weekend self-test: if a competent researcher in the subfield, given your problem statement and a weekend, could produce something close to your method, it is probably engineering, not novelty. Reframe, deepen the analysis, or find the non-obvious insight.
4. Novelty ranking (strongest → weakest): (a) paradigm-shifting (rare, usually recognized only in retrospect); (b) new problem formulation with a principled solution; (c) new method for an established problem with conceptual novelty that generalizes beyond the paper's setup; (d) non-trivial combination/adaptation requiring new analysis; (e) removing a well-known limitation of a specific prior method; (f) incremental improvement (often rejected at top venues unless the engineering is exceptional or gains are very large).
5. Alternative "Levels of Novelty" frequency scale: new concept for the world (e.g. theory of relativity) — never; new concept for CV (level sets, MRFs, AlexNet) — extremely rare; important extension/algorithmic novelty (α-expansion, batchnorm, ResNet) — very rare; new clever engineering with known ingredients (SIFT, vocabulary tree, VGG) — rare; useful minor upgrade (loss tweaks, efficient real-time versions) — frequent; application to a new task (GANs for X) — frequent; consolidation and infrastructure (comparisons, benchmarks, revisiting forgotten knowledge) — moderately frequent.

### Significance (what makes work significant)

1. Criteria for significance: (a) a substantial, consistent accuracy improvement, ideally across multiple benchmarks/settings; (b) a meaningful reduction in time/memory/parameter complexity with the quality trade-off quantified; (c) a decrease in the required level of supervision (fewer labels, less paired data, weaker annotation); (d) a useful by-product (better interpretability, a reusable intermediate representation, an unlocked downstream capability); (e) a modern adaptation of classical theory (optimal transport, spectral methods, control theory with neural parameterization) proven on real data; (f) enabling something previously impossible — often the most defensible form of significance.

### Rebuttals

1. Be short, specific, and data-driven. Reviewers skim rebuttals harder than papers — start each response with the concern in one line and your answer in two.
2. Run the experiments they ask for. Even for an unfair review, the strongest rebuttal is "we ran the requested experiment; here is the result." Reviewers reward visible effort.
3. Address every concern, even ones you think are wrong. Silently skipping a complaint signals you can't answer it; address misguided concerns with grace ("We appreciate the concern — this is addressed by X in Section Y, which we'll clarify in the revision").
4. Never be defensive, dismissive, or condescending. Reviewers have egos; a rebuttal that makes them feel stupid loses votes regardless of technical merit.
5. Identify the one or two load-bearing objections and invest disproportionately in them (prioritize the decisive vote, politely).
6. Know when to concede. Acknowledge a legitimate weakness, state what you'll fix in the camera-ready, and move on — denying valid criticism damages credibility elsewhere.

### Reviewing (to become a better writer)

1. A PhD student becomes a better writer by reviewing, not by writing.
2. Review as you'd want to be reviewed: specific, constructive, not lazy.
3. Pay attention to what makes you, as a reviewer, tired, confused, or skeptical — those are exactly the reactions reviewers of your paper are having. Use reviewing to diagnose your own writing.
4. Notice your own biases. Reviewers reject on "vibes" more often than admitted; understanding this in yourself is the first step to writing papers that resist those biases.

### Venue choice

1. Match the paper to the venue's tastes. CVPR/ICCV/ECCV have different reviewer pools and cultural preferences; NeurIPS/ICML reward theoretical framing more than CVPR; SIGGRAPH rewards visual quality and system completeness. Read recent accepted papers from your target venue before finalizing framing.
2. Do not resubmit unchanged. Rebuttal-style improvements matter more than a venue change — a weak reject at CVPR is usually a weak reject at ICCV unless you genuinely address the reviews.
3. Do not aim too low defensively. Top-venue rejections teach more than mid-venue acceptances — except at end-of-PhD, where acceptance velocity matters and you should optimize pragmatically.

### Intellectual honesty

1. If your method doesn't work in some regime, say so — stated limitations read as maturity; hidden ones read as dishonesty, and the paper is stronger for admitting them.
2. Do not oversell. Calling a two-line loss modification a "novel framework" trips the reviewer's nonsense detector and makes everything else you claim look inflated.
