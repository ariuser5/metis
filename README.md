# Metis

Metis is a persistent, server-authoritative MMO strategy game in which planning, forecasting, logistics, diplomacy, and long-term optimization should matter more than login frequency or constant clicking.

> **Current phase: game-design and architecture discovery.** The repository contains documentation only. Do not implement game code, choose a technology stack, or create GitHub Project items or GitHub issues yet.

## Vision

Metis takes inspiration from long-running strategy games such as Old Light and Tribal Wars, but it is not intended to be a clone. Its identity should emerge from a contemporary geopolitical setting, deliberately predictable systems, and player-authored strategic plans that the game can execute when their conditions become true.

The intended experience is:

- persistent, multiplayer, server-authoritative, strategy-focused, and playable for years;
- deep enough for players to keep discovering stronger strategies;
- friendly to players who log in only a few times per day;
- driven more by planning, forecasting, prioritization, logistics, diplomacy, and long-term optimization than by activity frequency;
- predictable enough for players to reason about the future state of their own holdings and those of other players;
- low in outcome-dominating randomness.

The setting is contemporary rather than science-fiction. The world may be represented through real-world-inspired countries, states or provinces, regions, cities, towns, and villages, but the exact representation is not decided.

## Central design hypothesis

Players should be able to express intent in advance instead of returning at the exact moment an action becomes affordable. A player might define an ordered plan such as:

1. Build Farm level 5 when resources become available.
2. Upgrade Roads.
3. Expand Industry.
4. Otherwise recruit soldiers.

Plans may also react to state, for example by prioritizing housing above a population threshold or public services below a morale threshold. This must remain a strategy planner, not an idle-game autopilot: automation must preserve meaningful decisions, expose understandable behavior, and resist abuse.

This mechanic and the fundamental gameplay loop must be validated in a deliberately small proof of concept. The PoC exists to answer one question: **Is this actually fun?** Its contents have not yet been selected.

## Current work

Before implementation, the project must reach sufficient agreement on:

- the core gameplay loop and primary strategic levers;
- victory or success conditions and long-term player motivation;
- economy, progression, diplomacy, military, and pacing;
- strategic depth and predictability;
- anti-frustration mechanics;
- interactions among the retained systems;
- the smallest PoC that can validate the core experience;
- which candidate systems are core, deferred, or unnecessary.

Until that agreement exists, contributors should clarify ambiguities, challenge assumptions, identify design and architecture risks, and compare alternatives. No candidate system is a committed feature merely because it appears in the documentation.

## Engineering direction

When implementation is authorized, the codebase should favor Clean Architecture, appropriate Domain-Driven Design, SOLID principles, Vertical Slice Architecture where it helps, a rich domain model, strong separation of concerns, and explicit business rules. Domain logic should read almost like documentation, infrastructure concerns must not leak into it, and explicitness is preferred over magic.

Avoid God classes, service spaghetti, hidden business rules, infrastructure leakage, and premature optimization. No technology stack has been selected.

## Documentation map

- [Project brief](docs/PROJECT_BRIEF.md) — canonical synthesis of the product vision, design principles, architectural values, and current mandate.
- [Design status](docs/DESIGN_STATUS.md) — confirmed constraints, uncommitted candidates, open decisions, and risks to investigate.
- [Development workflow](docs/DEVELOPMENT_WORKFLOW.md) — the gated GitHub workflow that applies once implementation begins.
- [Initial bootstrap prompt](docs/archive/INITIAL_BOOTSTRAP_PROMPT.md) — verbatim historical source, retained so no original context is lost.
- [Agent instructions](AGENTS.md) — repository-specific continuity rules for coding agents and future sessions.

When documents appear to conflict, use the original prompt to recover intent, then update the canonical project brief and design status together. A newer explicit decision from the project owner supersedes these documents and should be recorded promptly.

## Contribution gate

Do not start implementation based on this README. The next project activity is collaborative game-design refinement. Only after the project owner explicitly authorizes the transition to implementation will the project use the GitHub Project workflow: every material change must have a tracked project item and issue, implementation must happen on an issue-associated branch, and delivery must happen through a pull request with mandatory human review before merge into the protected default branch. The issue and project item are completed after the approved merge. See [the development workflow](docs/DEVELOPMENT_WORKFLOW.md) for the complete policy.
