# Master Communication

A compact agent skill for clear, truthful, useful communication—guided by **Grice's Cooperative Principle** and **ASD-STE100-inspired technical writing**.

> Optimize total user effort: reading, deciding, acting, and correcting mistakes—not word count alone.

## What it changes

- Answer the current question and adapt when the user corrects it.
- Give enough detail without repeated summaries, filler, or unnecessary clarification.
- Separate evidence, inference, and uncertainty. Report work as verified only when it was verified.
- Be supportive without endorsing unsupported conclusions or using automatic praise.
- Preserve meaning, conditions, uncertainty, and obligation strength when editing.
- Adapt to technical explanations, creative writing, emotional support, voice, multilingual replies, and machine-readable output.

The skill is guidance, not a substitute for domain expertise, permissions, or safety requirements.

## Install

### Hermes Agent

```sh
hermes skills install https://raw.githubusercontent.com/Devyansh-Gupta/master-communication/main/SKILL.md
```

Hermes supports installing a skill from its `SKILL.md` URL and fetching explicitly linked supporting files. Installation is subject to its normal security scan. This command is provided for users; publication did not install the skill into the author's active profile.

Then ask Hermes to use `master-communication` for a response, rewrite, or review.

### Other skill-capable agents

Place `SKILL.md` and the `references/` directory together in a `master-communication` folder within your agent's skill directory. Follow that agent's discovery and invocation instructions.

## Use

Example requests:

- “Use master-communication to explain this without losing the technical details.”
- “Rewrite this status update. Preserve uncertainty and distinguish completed work from unverified work.”
- “Review this reply for unnecessary detail, unsupported agreement, and ambiguity.”

Ordinary use needs only [SKILL.md](SKILL.md). The [strict STE review reference](references/ste.md) is needed only for formal compliance or rule-audit requests.

## Context budget

Measured with `tiktoken` using `o200k_base`, including frontmatter:

| Content | Tokens |
|---|---:|
| Core skill | 704 |
| Conditional STE reference | 262 |
| Both files | 966 |

The core is one-third smaller than the initial draft. Actual token counts depend on the model's tokenizer. This README and the research/evaluation documents are not runtime skill instructions.

## Evaluation

The final draft passed all **20 scenarios** in a bounded development regression suite. A separate model session judged randomized A/B responses without seeing which version was newer. Mechanical checks covered literals, JSON format, case coverage, and the tested file hash.

This is not an untouched benchmark, a cross-model study, or a guarantee. The suite exposed failures during development, and the skill was revised using those failures. See [evaluation details and limitations](docs/EVALUATION.md).

## Foundations and attribution

- **H. Paul Grice:** quantity, quality, relation, and manner from *Logic and Conversation* (1975).
- **ASD-STE100:** technical clarity principles. This is an unofficial aid, not ASD/STEMG endorsement or a compliance certification. The official dictionary is not reproduced.
- **Dustin Yuchen Teng's [asd-ste100-skill](https://github.com/danyuchn/asd-ste100-skill):** studied as a design reference, especially its emphasis on preserving meaning over mechanical shortening. The wording here is independently authored; no upstream script is bundled.

See [research and source notes](docs/RESEARCH.md) for the studied revision and recent research that informed the design.

## License

[MIT](LICENSE).

<!-- BACKUP-SETUP -->
## Local setup / restore

This repository is a **backup copy** made before a machine reformat.

| | |
|---|---|
| Original location on disk | `C:\Users\Admin\Projects\master-communication` |
| Original remote | `https://github.com/Devyansh-Gupta/master-communication.git` |
| Backup remote (this repo) | `https://github.com/Devyansh-Gupta/master-communication` |

### Prerequisites

- Git

### Setup
No dependency manifest was detected in this folder. The files are archived as-is - open them directly, or see the notes below.

### What is *not* in this backup

These are regenerable and were deliberately excluded (see `.gitignore`):

`node_modules/`  `.venv/`  `dist/`  `build/`  `target/`  `.next/`  `__pycache__/`  `.tools/`  `.pytest_cache/`

Run the setup steps above to recreate them.
