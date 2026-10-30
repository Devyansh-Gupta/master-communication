# Evaluation

## Final development result

| Version | Pass | Partial | Fail |
|---|---:|---:|---:|
| Initial draft | 19 | 1 | 0 |
| Published revision | 20 | 0 | 0 |

A blind reviewer preferred the revised response in two cases and tied the other eighteen. These are qualitative observations from a small development suite, not statistically significant performance estimates.

## Method

Fresh sessions using `gpt-6.1-sol` with medium reasoning generated actual responses to the same 20 synthetic requests under each skill version. A separate fresh session judged randomized A/B candidates against the requests and criteria without seeing the skill versions or their chronology.

Testers did not receive grading criteria or the authoring conversation. Cases were batched within each session, not run as twenty independent conversations. No tool-call events were recorded in the tester or judge streams.

Separate Python checks verified complete and unique case coverage, protected literals, JSON schema, and equality between the final skill's hash and the tested input.

## Coverage

1. Uncertainty, timing, and recommendation strength.
2. A novice explanation with an example and limitation.
3. Honest reporting of incomplete verification.
4. Formal STE requests without an official dictionary.
5. Ambiguous actors and ownership.
6. Brief emotional support without invented causes.
7. Exact commands, paths, error identifiers, units, and URLs.
8. Permission, possibility, advice, and obligation.
9. JSON-only output with an exact schema.
10. Requested technical depth and causal explanation.
11. Conflicting reports with missing test conditions.
12. Nested conditions and otherwise branches.
13. Unsupported motive attribution and sycophancy.
14. Corrections to the goal and output format.
15. Low-risk drafting without unnecessary questions.
16. Missing numeric evidence and false precision.
17. Spoken instructions with an exact sentence constraint.
18. A Hindi explanation with an analogy and caveat.
19. Emotional support without an unsolicited action plan.
20. A materially reworded conditional policy.

## Failures informed the revision

An early compressed candidate omitted an otherwise branch. Both versions also changed a temporal statement into a causal one: “partial files are produced after a timeout” became a claim that the timeout produced them.

The first judge missed the causal error. Manual review caught it, and the criterion was strengthened. Subsequent wording explicitly preserved every branch and kept “after” distinct from “because.” The final run preserved both correctly.

The initial-draft responses were reused and regraded under the stronger criterion. They were not rerun until a favorable result appeared.

## Limits

- This is a development regression suite, not an untouched holdout. Rules were revised using observed failures.
- There was no no-skill control, repeated sampling per version, or cross-model evaluation.
- Tester and judge used the same model, so correlated blind spots are possible.
- The correction case supplied a conversation transcript in one prompt; it was not a live multi-turn benchmark.
- The Hindi case did not receive independent native-speaker review.
- Passing does not establish universal semantic fidelity or formal ASD-STE100 compliance.

## Tested content

SHA-256 of the published runtime files:

```text
SKILL.md
63b2dd40e2fe3124b1fa2a8b5ab214647662ed8221a17828043b876cdf4b48e7

references/ste.md
6c2f267990d0b96316d38c86efe987d1cab0c84680e8d71cf063b717f0ea756c
```

Token counts use `o200k_base`, including frontmatter: 704 for the core, 262 for the conditional reference. Other tokenizers can produce different counts.

Private runtime logs, local filesystem paths, and session identifiers are intentionally excluded from this repository.
