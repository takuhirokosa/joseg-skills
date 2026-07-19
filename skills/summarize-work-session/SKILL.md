---
name: summarize-work-session
description: Summarize a long work session into an evidence-based handoff that separates completed work, changed artifacts, unverified items, and ordered next actions. Use when the user asks what was accomplished, requests a session summary or handoff, needs to resume later or in another agent, or wants the current state captured before context is lost.
---

# Summarize Work Session

Produce a self-contained handoff that lets another person or agent continue without rereading the full conversation. Separate observed results from intentions and unfinished work.

## Workflow

1. Identify the session objective and the latest user-approved scope.
2. Review available evidence before summarizing.
   - Use tool results, test output, inspected files, Git status, commits, screenshots, or external-system responses when available.
   - Treat a requested action, proposed plan, generated command, or success message without an observed result as unverified.
3. Build a concise state ledger.
   - Record what was executed.
   - Record what was verified from the resulting artifact or state.
   - Record what changed and why.
   - Record failures, open questions, and checks not yet performed.
4. Remove noise.
   - Omit repeated discussion, abandoned ideas, routine tool chatter, and intermediate attempts unless they explain the current state.
   - Preserve decisions and constraints that affect future work.
5. Redact secrets, credentials, private customer data, and unnecessary personal identifiers.
6. Write the handoff in the user's language using the output structure below.
7. Run the quality gate before returning it.

## Evidence Rules

- Use **Completed and verified** only when an observable result supports the claim.
- Use **Executed but unverified** when an action ran but its resulting quality or external state was not inspected.
- Use **Not started** when the session discussed an action without executing it.
- Do not equate a clean command exit, generated file, or commit with product-quality verification.
- Include exact file paths, branch names, commit identifiers, URLs, counts, dates, or error messages only when known and useful for resuming.
- If evidence conflicts, state the conflict and prefer the newest directly observed state.
- Never invent missing state to make the handoff look complete.

## Output Structure

Use only sections that contain useful information:

```markdown
# Work session handoff

## Objective
<The concrete outcome being pursued>

## Completed and verified
1. <Result and the evidence that confirms it>

## Changed artifacts
1. `<path or resource>` — <what changed and why>

## Executed but unverified
1. <Action and the missing verification>

## Decisions and constraints
1. <Decision future work must preserve>

## Open issues
1. <Failure, uncertainty, or blocker>

## Next actions
1. <First safe action, including its completion check>
```

Keep **Next actions** ordered and executable. Do not include optional ideas unless the user asks for recommendations.

## Quality Gate

Confirm all of the following:

1. A new reader can identify the objective and current state without the original conversation.
2. Every completion claim has supporting evidence.
3. Executed, verified, unverified, and not-started work are not mixed together.
4. Changed artifacts include enough identity to locate them again.
5. The next action starts from the actual current state rather than repeating completed work.
6. Sensitive information is removed.
7. The handoff is concise enough to scan quickly.

Revise the handoff if any item fails.

## Safety

Summarize only. Do not continue implementation, edit files, publish, send messages, or modify external systems unless the user separately requests those actions.
