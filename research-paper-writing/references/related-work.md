# Related Work Writing Guide

## Goal

Position your work against the most relevant lines of research, and make your novelty easy to verify.

## Workflow

1. List directly competing and recent baseline papers first.
2. Group literature by technical topic (not by publication year alone).
3. For each topic: summarize common paradigm, then key limitation relevant to your challenge.
4. End each topic by clarifying your distinction.

## Topic Design

Use 2-4 focused topics, for example:

1. Task-specific mainstream methods.
2. Methods closest to your core idea.
3. Auxiliary techniques your method builds on.

## Paragraph Template

1. Topic sentence: define scope of this topic.
2. Representative methods: one compact summary.
3. Limitation tied to your target technical challenge.
4. Transition sentence that leads to your method.

## Do and Don't

1. Do compare mechanisms, assumptions, and failure modes.
2. Do emphasize the exact gap your method fills.
3. Do not make Related Work a citation dump.
4. Do not hide strongest baselines.

## Checklist

1. Are all strongest/recent competitors covered?
2. Is each topic connected to your problem setting?
3. Is your difference explained in technical terms, not marketing terms?
4. Is citation coverage complete for all core claims?

## Additional Skills — from *How to Write a Computer Vision Paper* (2026)

1. Goal restated: not to prove you read the literature, but to establish that *no existing work does what your paper does*, and to preempt "why didn't you compare against X?"
2. Applicability statements are mandatory. For any method that could reasonably apply to your setting, state one of two things: (a) we compare against it in Section X, or (b) it does not apply because [specific reason]. This preempts missing-baseline objections.
3. Every prior-work paragraph must end in a contrast, not a description. Describing what a paper does is necessary but insufficient.
4. Frame Related Work offensively, not defensively: use it to narrow the reader's field of view toward the gap you fill. By the end, the reader should feel your specific problem + approach combination is genuinely uninhabited territory.
5. Do not dismiss prior work. Reviewers are often the authors of papers you dismiss — contrast respectfully and factually.
6. Properly credit prior work, especially concurrent work. The field is small, and uncredited authors often become your reviewers.
7. Narrative job: Related Work places the story in a landscape — "here is the territory, here is where nobody has been, and that is where we went."
