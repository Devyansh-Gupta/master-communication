# Research and design notes

## Scope

The design review examined primary-source abstracts and publication metadata available on 30 October 2026, including 2026 revisions and ACL 2026 papers. This was a bounded survey, not an exhaustive review of every communication scenario or an independent audit of each study's methods.

The papers motivate the problem selection. They do not establish that these particular prompt instructions solve the underlying model limitations.

## Problems distilled into general rules

| Problem | Primary source | Design response |
|---|---|---|
| Agreement mistaken for helpfulness | [User Detection and Response Patterns of Sycophantic Behavior in Conversational AI](https://arxiv.org/abs/2601.10467v4), May 2026 revision | Acknowledge feelings without endorsing unsupported interpretations. Retain warmth rather than becoming reflexively contrary. |
| Confident guessing | [Why Language Models Hallucinate](https://arxiv.org/abs/2509.04664), September 2025 | Distinguish evidence, inference, and uncertainty. Avoid invented precision. |
| Early assumptions survive corrections | [LLMs Get Lost In Multi-Turn Conversation](https://arxiv.org/abs/2505.06120), May 2025; [One Battle After Another](https://aclanthology.org/2026.acl-long.433/), ACL 2026 | Track the latest goal and constraints. Update the answer when corrected. |
| Clarification becomes user labor | [Structured Uncertainty guided Clarification for LLM Agents](https://aclanthology.org/2026.findings-acl.2028/), ACL 2026 | Distinguish missing facts from missing intent. Ask result-changing questions instead of making the user specify every detail. |
| Verbosity hides useful information | [ConCISE](https://arxiv.org/abs/2511.16846v2), March 2026 revision | Remove non-essential content, not necessary depth. Optimize total user effort rather than word count alone. |
| A single style does not fit every reader | [Culturally-Aware Conversations](https://arxiv.org/abs/2510.11563), October 2025 | Respect stated language, tone, expertise, and context without stereotyping. |

## Foundations

- [Grice, *Logic and Conversation* (1975), excerpt of pages 45–47](https://www.sfu.ca/~jeffpell/Cogs300/GriceLogicConvers75.pdf): the four maxims provide a compact organizing structure.
- [ASD-STE100 official site](https://www.asd-ste100.org/): authoritative source for the standard and official-copy request. Formal compliance requires the applicable standard and dictionary.
- [danyuchn/asd-ste100-skill at revision `8da6b6340aa22faf46fd07db8efbdea010cd38d9`](https://github.com/danyuchn/asd-ste100-skill/tree/8da6b6340aa22faf46fd07db8efbdea010cd38d9): the main skill, rule summary, examples, README, and MIT license were studied. The strongest adopted principle is that semantic fidelity takes priority over mechanical shortening. This project uses independently authored instructions, not copied upstream implementation or the official ASD dictionary.

## Deliberate boundaries

The skill contains no domain-specific chapters, mandatory answer template, citation quota, or universal paragraph limit. Domain expertise and safety rules belong in their own guidance.

Technical writing targets do not govern every conversation. Creative voice and emotional support should not be flattened into maintenance-manual prose. Likewise, simple wording must not convert a recommendation into a requirement or a temporal sequence into a causal claim.
