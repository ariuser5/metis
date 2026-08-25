# Project Brief

This document is the canonical synthesis of the initial Metis project direction. It records established intent without pretending that unresolved design questions have already been answered.

## Product concept

Metis is a persistent online MMO strategy game inspired by games such as Old Light, Tribal Wars, and other long-term strategy games. It must develop its own mechanics and identity rather than clone an existing game.

The setting is contemporary, not science-fiction. Instead of competing over solar systems or planets, players compete over real-world-inspired geopolitical entities that may include:

- countries;
- states or provinces;
- regions;
- cities;
- towns;
- villages.

The exact world model and the meaning of control at each geographical level remain open.

## Intended experience

The game should be:

- persistent;
- multiplayer;
- server-authoritative;
- strategy-focused;
- long-term;
- playable for years;
- deep enough that players continually discover stronger strategies.

Its defining principle is that strategy and planning matter significantly more than activity frequency. Players should not feel compelled to log in every hour. A player who checks the game roughly twice per day but plans better should remain competitive against someone who checks hourly.

The game should reward:

- planning;
- forecasting;
- prioritization;
- logistics;
- diplomacy;
- long-term optimization.

It should not primarily reward:

- constant clicking;
- frequent activity for its own sake;
- being online all day.

## Player-authored planning and automation

One core mechanic to explore is delegating conditional and ordered decisions to the game. A player who cannot yet afford an action should be able to describe future intent rather than return at the exact resource threshold.

Example ordered plan:

> When resources become available, build Farm level 5, then upgrade Roads, then expand Industry; otherwise recruit soldiers.

Example state-based plans:

> If population exceeds X, prioritize housing.

> If morale drops below Y, spend resources on public services.

The design target is a **strategy planner**, not idle automation. The system must:

- retain strategic tradeoffs and meaningful player decisions;
- avoid turning optimal play into unattended autopilot;
- resist abuse;
- behave predictably and explainably;
- reduce the advantage of checking the game at the exact right moment.

Within a contest, manual overrides may be submitted at any time, but preconfigured automatic contingencies must execute materially faster. This rewards preparation over frequent reaction; the exact timing difference remains a pre-release balance question. To avoid a scripting contest, the eventual contingency language must be bounded, standardized, predictable, and explainable.

Automatic contingencies may only use information realistically available to their faction, never the simulation's hidden state. Each eventual trigger must identify its observable source and confidence, and its resolution log must show the evidence used. The exact visibility and confidence model remains open.

For the PoC, a faction sees its own force's strength, energy, and morale exactly, while enemy condition is an intelligence-based estimate. The release version may later introduce own-force uncertainty only through legible, actionable reporting limits: players must see what is confirmed, estimated, or stale, why confidence is limited, and which choices can improve it.

The PoC may show broad enemy force size and estimated current posture. The release version should not reliably expose enemy posture, but hidden posture must leave observable, intelligence-gated signals that allow players to form and revise hypotheses; it must not create decisive outcomes that a faction could not plausibly anticipate.

When an attack begins, the defender's standing strategy responds immediately. The defender receives a notification but no guaranteed pause for manual input; preparation is the owner's responsibility. Manual intervention remains available under the slower-override rule.

The planner's syntax, limits, conflict resolution, information requirements, execution timing, counterplay, and failure behavior are not yet decided.

## Predictability and randomness

Players should be able to reasonably predict the future state of both their own empire and other players' empires. Predictability is necessary for planning and counter-planning.

Random events may exist, but excessive randomness must not dominate strategic decisions. The acceptable roles, visibility, and impact of randomness remain open design questions.

## Candidate systems

The following are ideas, not approved scope:

- infrastructure;
- resource production;
- trade routes;
- logistics;
- supply chains;
- population growth;
- population morale;
- reputation;
- officer or subordinate reputation;
- diplomacy;
- alliances;
- global diplomacy in the spirit of the United Nations;
- a global market;
- regional influence;
- intelligence and espionage;
- economy;
- technology;
- military;
- civilian infrastructure.

Each system must eventually be classified as essential to the PoC, deferred until later, or removed. The only current classification is the narrow military-contest boundary described below; no broader system classification has been agreed.

## Proof of concept

The project should begin with a very small PoC that contains only the primary strategic levers needed to validate the fundamental gameplay loop.

Its purpose is to answer:

> **Is this actually fun?**

The PoC is not meant to demonstrate the breadth of the eventual MMO. Its first confirmed boundary is a self-contained military contest in which the player chooses where to visibly commit forces, how much strength to show versus retain, and one simple conditional tactic for that force. This is meant to test bluffing, force allocation, and limited conditional behavior without a complete tactics editor or automatic reinforcement calls from other districts. Its remaining systems, player count, duration, success criteria, and validation method remain open.

## Required design agreement before implementation

Before code is written, the project must reach sufficient agreement on:

- overall gameplay;
- the core gameplay loop;
- victory or success conditions;
- long-term player motivation;
- economy;
- progression;
- diplomacy;
- military;
- pacing;
- strategic depth;
- anti-frustration mechanics;
- interactions among systems;
- the smallest meaningful PoC;
- the boundary between core gameplay and future nice-to-have features.

## Software quality and architecture values

The project is intended to become an example of clean software architecture. Code should retain clear responsibilities, business logic should read almost like documentation, and infrastructure concerns should not pollute domain logic. Prefer explicitness over magic.

When implementation begins, favor:

- Clean Architecture;
- Domain-Driven Design where appropriate;
- SOLID principles;
- Vertical Slice Architecture where it makes sense;
- a rich domain model;
- strong separation of concerns;
- explicit business rules.

Avoid:

- God classes;
- service spaghetti;
- hidden business rules;
- infrastructure leaking into the domain;
- premature optimization.

The codebase should remain understandable years later. These are architectural values, not a selected technology stack.

## Expected design posture

Project collaborators should operate as senior game-systems designers and senior software architects. They should challenge assumptions rather than simply agree, especially when an idea may create technical debt, poor gameplay, balance issues, scaling problems, or unnecessary complexity. Criticism should include reasoning and, where possible, a better alternative.

## Current directive

At this stage:

- ask necessary questions;
- identify ambiguities;
- challenge assumptions;
- identify major design risks;
- suggest improvements;
- help define the smallest PoC capable of validating genuine fun;
- distinguish core gameplay from future nice-to-have features.

Do **not**:

- implement anything;
- create GitHub issues;
- propose or select a technology stack;
- rush past design disagreements.

Once sufficient agreement exists, the project will create GitHub issues and proceed incrementally under the documented development workflow.
