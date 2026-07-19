# joseg-skills

[日本語](README.md)

Reusable agent skills derived from workflows that have been tested in real work and generalized for broader use.

## Available skills

### 022 | `dev-log-to-article` — Turn development logs into an explanatory article

Reads development logs, chat history, work notes, and Git changes, then restructures them into an explanatory article that other readers can learn from instead of a simple chronological record.

1. Separates directly observed facts from assumptions and unverified claims.
2. Organizes the material into context, problem, attempts, solution, result, and lessons learned.
3. Removes secrets, personal information, environment-specific paths, and other details that should not be published.
4. Produces a Markdown article with a title, introduction, headings, procedures, and cautions.

Useful for development retrospectives, technical blogs, internal knowledge bases, and troubleshooting article drafts.

### 009 | `summarize-work-session` — Create a handoff from a long work session

Turns a long conversation or multi-step work session into a handoff that another person or agent can use to resume the work immediately.

1. Identifies the objective and the latest approved scope.
2. Clearly separates completed and verified work, executed but unverified work, and work that was not started.
3. Records changed files, URLs, branches, commits, and decisions needed to resume the task.
4. Organizes open issues and next actions in a safe, executable order.

Useful at the end of a long session, during a change of ownership, when handing work to another AI, or before resuming work on a later day.

## Installation

Use a compatible Agent Skills installer to install an individual skill from this repository.

### 022 | Turn development logs into an explanatory article

```bash
npx skills add takuhirokosa/joseg-skills --skill dev-log-to-article
```

### 009 | Create a handoff from a long work session

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
