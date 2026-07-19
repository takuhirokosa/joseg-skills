# joseg-skills

[日本語](README.md)

Reusable agent skills derived from workflows that have been tested in real work and generalized for broader use.

## Available skills

| Skill | Description |
| --- | --- |
| `dev-log-to-article` | Turn development logs and work records into a reusable, reader-focused explanatory article. |
| `summarize-work-session` | Summarize long work into completed results, changed artifacts, unverified items, and ordered next actions. |

## Installation

Use a compatible Agent Skills installer to install an individual skill from this repository.

```bash
npx skills add takuhirokosa/joseg-skills --skill dev-log-to-article
```

```bash
npx skills add takuhirokosa/joseg-skills --skill summarize-work-session
```

## Repository structure

Each skill lives in its own folder under `skills/` and includes a required `SKILL.md` file.

```text
skills/
├── dev-log-to-article/
    ├── SKILL.md
    ├── agents/
    │   └── openai.yaml
    └── references/
        └── article-structure.md
└── summarize-work-session/
    ├── SKILL.md
    └── agents/
        └── openai.yaml
```

## Contributing

Issues and pull requests that provide meaningful value are welcome, including new skills, improvements, bug fixes, usage examples, and industry-specific knowledge.

## License

This repository is licensed under the GNU General Public License v3.0 only (`GPL-3.0-only`). See [LICENSE](LICENSE).
