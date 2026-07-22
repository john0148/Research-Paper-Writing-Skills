# Conclusion Writing Guide

## Goal

Close the paper with clear takeaways and credible limitations.

## Structure

1. Restate solved problem and core technical idea.
2. Summarize strongest evidence from experiments.
3. State practical impact or new insight.
4. Add limitation paragraph.
5. End with concrete future direction.

## Limitation Guidance

Prefer limitations tied to task goal/setting boundaries, for example:

1. Data regime limitation (e.g., only short sequences).
2. Assumption limitation (e.g., controlled viewpoints only).
3. Deployment scope limitation (e.g., specific sensor setup).

Avoid framing conclusion around fixable implementation flaws unless they critically define your method's scope.

## Distinguish Limitation Types

1. Technical defect: underperforms strong baselines on key metrics or causes unacceptable tradeoff.
2. Scope limitation: bounded by current task setting and still competitive vs. current SOTA.

## Template

1. This paper addresses [problem] by proposing [method].
2. The key idea is [core insight], which enables [main benefit].
3. Experiments show [main gains] across [datasets/settings].
4. A current limitation is [scope boundary], and extending to [future setting] is an important next step.

## Additional Skills — from *How to Write a Computer Vision Paper* (2026)

1. Weight the recap toward experimental results, not method description. Recap the contributions and — more importantly — the results that support them.
2. Close the loop on the introduction: return to the motivating problem and state, in plain language, what has now changed.
3. Expose limitations proactively. A limitations paragraph that a hostile reviewer could not have written more damningly is the mark of a mature paper — and it disarms the reviewer, who can no longer hold a named weakness against you as a secret flaw.
4. Make future work concrete and following from your contribution — not generic "we will explore more applications."
5. Avoid vague gestures toward "broader impact" or "many applications" unless you have specific examples; reviewers read these as padding.
6. Narrative job: the conclusion closes the loop by returning to the problem posed in the introduction and stating what has changed.
