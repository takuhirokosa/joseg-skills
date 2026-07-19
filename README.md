# joseg-skills

Reusable agent skills derived from workflows that have been tested in real work and generalized for broader use.

## Available skills

| Skill | Description |
| --- | --- |
| `dev-log-to-article` | Turn development logs and work records into a reusable, reader-focused explanatory article. |

## Repository structure

Each skill lives in its own folder under `skills/` and includes a required `SKILL.md` file.

```text
skills/
└── dev-log-to-article/
    ├── SKILL.md
    ├── agents/
    │   └── openai.yaml
    └── references/
        └── article-structure.md
```

Use a compatible Agent Skills installer to list or install an individual skill from this repository.

## License

This repository is licensed under the GNU General Public License v3.0 only (`GPL-3.0-only`). See [LICENSE](LICENSE).
