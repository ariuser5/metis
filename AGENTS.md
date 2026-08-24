# Repository Instructions for Agents

These instructions apply to the entire repository.

## Start here

Before doing project work, read:

1. `README.md`
2. `docs/PROJECT_BRIEF.md`
3. `docs/DESIGN_STATUS.md`
4. `docs/DEVELOPMENT_WORKFLOW.md`

Consult `docs/archive/INITIAL_BOOTSTRAP_PROMPT.md` when checking the fidelity or intent of the canonical documentation. It is a historical source, not a place to record new decisions.

## Current phase gate

The project is in game-design and architecture discovery.

- Do not write game or infrastructure code.
- Do not select or propose a technology stack unless the project owner explicitly reopens that topic.
- Do not create GitHub issues yet.
- Do not treat a listed candidate system as approved scope.
- Do not silently resolve an open design question.

The current task is to refine the experience, expose assumptions, challenge weak ideas, identify risks and tradeoffs, and find the smallest PoC that can determine whether the fundamental gameplay loop is fun.

## Design collaboration

Act as both a senior game-systems designer and a senior software architect. Do not agree reflexively. Explain when an idea is likely to cause poor gameplay, balance problems, technical debt, scaling risk, or avoidable complexity, and propose a simpler alternative.

Protect these product principles unless the project owner explicitly changes them:

- strategy and planning should matter more than activity frequency;
- a thoughtful player logging in roughly twice per day should remain competitive with a player checking hourly;
- automation should express player strategy rather than replace meaningful decisions;
- important outcomes should be predictable enough to support forecasting;
- randomness may add texture but should not dominate strategic decisions;
- the game is persistent, multiplayer, server-authoritative, contemporary, and designed for long-term play.

Use precise status language:

- **Confirmed** means explicitly established by the project owner.
- **Hypothesis** means an idea the PoC should validate.
- **Candidate** means possible scope, not a commitment.
- **Open** means a consequential decision has not been made.

Never promote a hypothesis or candidate to confirmed without an explicit decision.

## Documentation continuity

Record new design decisions in `docs/DESIGN_STATUS.md` and reconcile affected wording in `README.md` or `docs/PROJECT_BRIEF.md` in the same change. Prefer links over duplicating detailed rules across files.

Keep `docs/archive/INITIAL_BOOTSTRAP_PROMPT.md` verbatim. Only change it to correct a proven transcription error, and explain that correction in the change summary.

When recording a decision, include its rationale, meaningful rejected alternatives, and unresolved consequences when known. When a decision is reversed, preserve enough history to explain why.

## Future implementation rules

Implementation remains locked until the project owner explicitly authorizes it after design agreement. Once unlocked:

1. Ensure the work has a refined GitHub issue.
2. Move the issue to **In Progress**.
3. Implement on a branch associated with that issue.
4. Push the branch and open a pull request.
5. Wait for review and address feedback.
6. Merge only after approval.

Favor Clean Architecture, appropriate DDD, SOLID, useful vertical slices, a rich domain model, strong separation of concerns, and explicit business rules. Keep infrastructure out of domain logic. Avoid God classes, service spaghetti, hidden rules, magic behavior, and premature optimization.

Preserve unrelated user changes, validate every change proportionately, and report checks that were not run.
