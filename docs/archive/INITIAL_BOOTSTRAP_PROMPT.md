# Codex Project Bootstrap Prompt — Modern Persistent MMO Strategy Game

## Context

I want to build a persistent online MMO strategy game inspired by games like Old Light, Tribal Wars, and similar long-term strategy games.

This is **not** intended to be a clone. I want to design a modern strategy game with its own mechanics and identity.

The setting should be contemporary rather than science-fiction.

Instead of conquering solar systems and planets, players compete over real-world-inspired geopolitical entities:

- Countries
- States / Provinces
- Regions
- Cities
- Towns
- Villages

The exact world representation is still open for discussion.

---

# Important

Do **not** start implementing anything.

We are currently in the **game design and architecture phase**.

Your role is to act as both:

- Senior Software Architect
- Senior Game Systems Designer

Challenge ideas whenever appropriate.

If you believe something would create technical debt, poor gameplay, balance issues, scalability problems, or unnecessary complexity, explain why and propose alternatives.

Do not simply agree with every idea.

---

# High-Level Vision

The game should be:

- persistent
- multiplayer
- server authoritative
- strategy focused
- long-term
- playable for years
- deep enough that players continuously discover better strategies

The objective is to create a game where **strategy and planning matter significantly more than activity frequency**.

I do **not** want players to feel forced to log in every hour.

Instead, I want players who think ahead and create better long-term strategies to outperform others.

---

# Core Design Principle

The game should reward:

- planning
- forecasting
- prioritization
- logistics
- diplomacy
- long-term optimization

more than:

- constant clicking
- activity frequency
- being online all day

A player who logs in twice a day with a better strategy should still be competitive against someone checking the game every hour.

---

# Planned Automation

One of the core mechanics I want to explore is allowing players to delegate decisions to the game.

For example:

The player currently lacks enough resources to build something.

Instead of forcing them to return later, they should be able to create plans such as:

"When resources become available:

1. Build Farm level 5.
2. Then upgrade Roads.
3. Then expand Industry.
4. Otherwise recruit soldiers."

or

"If population exceeds X, prioritize housing."

or

"If morale drops below Y, spend resources on public services."

The game should execute these automatically once their conditions become true.

Think of it as a strategy planner rather than idle automation.

Help design this system so that it:

- remains strategic
- cannot be abused
- does not eliminate meaningful decisions

---

# Predictability

Another important design principle:

Players should be able to reasonably predict the future state of both:

- their own empire
- other players

This predictability enables planning.

The game should avoid excessive randomness.

Random events may exist, but should not dominate strategic decisions.

---

# Possible Systems

These are ideas, not final decisions.

Examples include:

- Infrastructure
- Resource production
- Trading routes
- Logistics
- Supply chains
- Population growth
- Population morale
- Reputation
- Officer / subordinate reputation
- Diplomacy
- Alliances
- Global diplomacy (similar in spirit to the United Nations)
- Global market
- Regional influence
- Intelligence / espionage
- Economy
- Technology
- Military
- Civilian infrastructure

Help determine:

- which systems belong in the PoC
- which should wait
- which should be removed entirely

---

# Development Philosophy

Code quality is extremely important.

I want this project to become an example of clean software architecture.

Everything should have clear responsibilities.

Business logic should read almost like documentation.

Infrastructure concerns should never pollute the domain logic.

I prefer explicitness over magic.

---

# Architectural Principles

Favor:

- Clean Architecture
- Domain Driven Design where appropriate
- SOLID
- Vertical Slice Architecture where it makes sense
- Rich domain model
- Strong separation of concerns
- Explicit business rules

Avoid:

- God classes
- Service spaghetti
- Hidden business rules
- Infrastructure leaking into the domain
- Premature optimization

The code should remain understandable years later.

---

# Development Workflow

The repository will use GitHub.

Before any implementation begins:

Every piece of work must have an issue.

Workflow:

1. Discuss feature.
2. Refine requirements.
3. Create GitHub Issue.
4. Move issue to "In Progress".
5. Implement.
6. Push branch.
7. Open Pull Request.
8. Wait for review.
9. Address feedback.
10. Merge only after approval.

No implementation should happen outside this workflow.

---

# Proof of Concept

We should start with a very small PoC.

The PoC should validate only the game's fundamental gameplay loop.

The objective is to answer:

"Is this actually fun?"

The PoC should contain only the primary strategic levers available to players.

Everything else can be postponed.

Your task will be to help identify what absolutely belongs in the first playable version.

---

# Project Initialization

Before writing any code, I want us to reach agreement on:

- overall gameplay
- core gameplay loop
- victory (or success) conditions
- long-term player motivation
- economy
- progression
- diplomacy
- military
- pacing
- strategic depth
- anti-frustration mechanics
- systems interactions

Do not rush into implementation.

We should iterate on the design until we are both confident the PoC validates the right ideas.

---

# Your First Tasks

Do not create issues.

Do not write code.

Do not propose a technology stack yet.

Instead:

1. Ask any questions you need.
2. Identify ambiguities.
3. Challenge assumptions.
4. Identify major design risks.
5. Suggest improvements.
6. Help define the smallest possible PoC capable of validating whether the game is genuinely fun.
7. Help distinguish between "core gameplay" and "future nice-to-have features."

Once we have sufficient agreement, we will begin creating GitHub issues and implementing the project incrementally.
