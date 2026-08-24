# Development Workflow

## Current gate

Implementation has not started. The project is currently in the discussion and design phase. Do not create GitHub Project work items or GitHub issues, choose a stack, or write code until the project owner confirms that the game design is sufficiently defined and explicitly authorizes the transition into implementation.

Current design and documentation work exists to reach that gate. Candidate features are not an implementation backlog.

## Codex agent team

The repository contains project-scoped Codex agents under `.codex/agents/`.
They provide role separation for the future implementation workflow; their
presence does not authorize implementation during the current design phase.

The main Codex task acts as the orchestrator. The roles are:

- `design_advisor` — read-only game-design feedback on fun, scope, tradeoffs, and PoC value;
- `architect` — read-only requirements, architecture, risk, and acceptance-criteria analysis;
- `implementor` — implementation of one approved issue on its associated branch;
- `reviewer` — independent, read-only review of the branch against the issue and default branch;
- `qa` — read-only tests and validation against the issue acceptance criteria.

During the current design phase, the normal design handoff is:

```text
Idea or design question → design_advisor → human owner decision → DESIGN_STATUS.md
```

After the design gate is opened, the normal implementation handoff is:

```text
GitHub issue → architect → human plan approval → implementor → reviewer + QA → human PR review → merge
```

Only the implementor may modify source files during implementation. Reviewer
and QA report findings and do not repair the branch they review. They may run
in parallel after implementation because their default work is read-heavy and
independent. The orchestrator must not treat an agent review as the required
human approval, and no agent may approve, merge, or close the work.

Use explicit delegation prompts that identify the issue, branch, acceptance
criteria, required handoff, and whether the orchestrator should wait for all
roles before continuing. Avoid running multiple write-capable agents against
the same branch.

The design advisor is not the product owner and does not make final product
decisions. Its output should identify which statements are Confirmed,
Hypothesis, Candidate, Open, Recommended, or Rejected, and it must leave
consequential choices for the human owner to decide explicitly.

## Required project workflow after the design gate

After the project owner opens the implementation phase, the GitHub Project becomes the work-tracking source of truth. Every implementation and every material project modification must be justified by a GitHub Project item and represented by a corresponding GitHub issue. This applies to code, documentation, configuration, tests, assets, and other repository changes.

The required flow is:

1. Discuss the proposed change and confirm that it belongs in the authorized implementation phase.
2. Create or update the GitHub Project item and its corresponding GitHub issue.
3. Refine the issue until its scope and acceptance criteria are clear.
4. Move the issue to **In Progress** before starting work.
5. Create a branch associated with the issue and implement only the agreed scope.
6. Commit and push the work to that branch.
7. Open a pull request that links the issue and describes the change and validation.
8. Obtain review from a human with the necessary project permissions.
9. Address review feedback and required checks.
10. Merge the pull request into the protected default branch only after the required human approval and repository checks have passed.
11. Close the issue and move the GitHub Project item to its completed state after the merge.

No implementation or material repository change should occur outside this workflow once the implementation phase is authorized.

## Pull-request and merge rules

Every pull request must:

- link to the relevant GitHub issue or issues;
- be opened from a non-default branch;
- describe the change, scope, validation, and any remaining risks;
- receive approval from at least one human reviewer with the necessary repository permissions;
- pass the repository's required checks before merge.

The author or an automated agent must not self-approve or merge the pull request. A pull request must not be merged through a bypass path. The protected default branch is currently `main`; if the repository is renamed to `master`, the same protections and workflow apply to `master`.

The repository settings must enforce these rules with branch protection or repository rulesets. At minimum, direct pushes to the protected default branch must be disabled, pull requests must be required, the required human approval count must be configured, and required checks must pass before merge. Documentation describes the policy; GitHub settings provide the technical enforcement.

## Refinement expectations

Before an issue is ready for implementation, it should make clear:

- the player or project outcome being pursued;
- the applicable confirmed design decisions;
- scope and explicit non-goals;
- acceptance criteria;
- important domain rules and edge cases;
- dependencies and meaningful risks;
- how the result will be validated.

Requirements must not silently settle unresolved product questions. Return consequential ambiguity to design discussion and update `DESIGN_STATUS.md` when the owner makes a decision.

## Pull-request expectations

Implementation should be incremental and reviewable. A pull request should:

- link its issue;
- explain the behavior and design decision it implements;
- keep domain rules explicit and infrastructure concerns separated;
- avoid unrelated changes;
- include proportionate tests or other validation;
- disclose skipped or failed checks and remaining risks;
- wait for approval from an authorized human reviewer before merge.

Technology choices will be evaluated only after the design gate is opened. Architectural principles in the project brief constrain how choices are assessed but do not predetermine a stack.
