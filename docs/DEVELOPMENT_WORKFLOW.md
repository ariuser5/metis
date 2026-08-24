# Development Workflow

## Current gate

Implementation has not started. Do not create issues, choose a stack, or write code until the project owner confirms that the game design is sufficiently defined and authorizes the transition into implementation.

Current design and documentation work exists to reach that gate. Candidate features are not an implementation backlog.

## Required workflow once implementation is authorized

Every piece of development work must be represented by a GitHub issue. The intended flow is:

1. Discuss the feature.
2. Refine its requirements.
3. Create a GitHub issue.
4. Move the issue to **In Progress**.
5. Implement the agreed scope on a branch associated with the issue.
6. Push the branch.
7. Open a pull request.
8. Wait for review.
9. Address review feedback.
10. Merge only after approval.

No implementation should occur outside this workflow.

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
- wait for approval before merge.

Technology choices will be evaluated only after the design gate is opened. Architectural principles in the project brief constrain how choices are assessed but do not predetermine a stack.
