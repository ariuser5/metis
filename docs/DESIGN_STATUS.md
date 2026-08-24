# Design Status

This is the live register of what is confirmed, hypothesized, merely possible, or still open. It prevents ideas from becoming accidental commitments.

## Status vocabulary

- **Confirmed constraint** — explicitly part of the project direction; changing it requires an explicit decision.
- **Hypothesis** — a belief that needs design analysis or PoC evidence.
- **Candidate** — a possible feature or system with no scope commitment.
- **Open decision** — a consequential choice that has not been made.

## Confirmed constraints

### Product

- The game is a persistent, multiplayer, server-authoritative, long-term strategy game.
- The setting is contemporary and based on geopolitical entities rather than science-fiction planets or solar systems.
- The game must develop its own identity and must not clone its inspirations.
- Planning quality should matter more than login frequency or constant clicking.
- A player with stronger strategy and roughly two check-ins per day should remain competitive with a player checking hourly.
- Players need enough predictability to forecast their own state and other players' state.
- Randomness must not dominate strategic decisions.
- Player-authored conditional or ordered planning is a core mechanic to explore.
- Automation must not remove meaningful decision-making or become abusive autopilot.
- The first playable scope must be a small PoC focused on testing whether the fundamental loop is fun.

### Process

- The current phase is game-design and architecture discovery.
- No implementation, technology-stack selection, or GitHub Project/GitHub issue creation is currently authorized.
- Design ideas should be challenged on gameplay, balance, complexity, scalability, and technical-debt grounds.
- The project owner must explicitly authorize the transition out of the discussion and design phase before the implementation workflow begins.
- After that transition, every implementation or material project modification must be tracked in GitHub Project and represented by a GitHub issue.
- Changes must be made on an issue-associated branch and delivered through a pull request; direct commits to the protected default branch are not permitted.
- Every pull request requires review and approval by a human with the necessary project permissions before merge.
- Issues and GitHub Project items are closed or marked complete only after the approved pull request has been merged.
- The project uses a read-only project-scoped `design_advisor` during the current design phase; it challenges ideas but does not make product decisions.
- The future implementation workflow uses project-scoped Codex agents with separate architect, implementor, reviewer, and QA responsibilities; this does not replace mandatory human PR review.

### Engineering values for future implementation

- Clear responsibilities and strong separation of concerns.
- Business rules that are explicit and readable.
- Infrastructure kept outside the domain model.
- Clean Architecture, appropriate DDD, SOLID, useful vertical slices, and a rich domain model.
- No God classes, service spaghetti, hidden business rules, magic behavior, or premature optimization.

## Hypotheses to validate

- Conditional planning can reduce the advantage of frequent logins without turning the game into an idle game.
- A sufficiently predictable competitive world creates deeper planning and counter-planning.
- A very small set of strategic levers can expose whether the intended experience is fun before MMO-scale systems are built.
- Long-term depth can come from interacting understandable systems rather than excessive feature count or randomness.
- A mature world of existing factions and institutions can give newcomers meaningful context without requiring them to found and grow an isolated settlement.
- Persistent player-authored doctrine can remain effective while a player is absent yet become counterable as opponents observe, learn, and adapt.
- Different hierarchy levels can offer distinct but equally meaningful struggles instead of making lower ranks a tutorial and higher ranks a solved end state.
- Reversible rank, increased exposure for prominent leaders, and recovery after defeat can create turnover without erasing long-term identity and achievement.
- Information-intensive precision and scale-oriented brute force can both remain viable in different situations.

These are not proven. The PoC and design work must define how to test them.

## Emerging owner direction — exploratory, not confirmed scope

The detailed discussion is preserved in [MMO Challenges and Emerging Direction](MMO_DESIGN_CHALLENGES_AND_EMERGING_DIRECTION.md). The following items are candidates with a strong owner preference, not approved mechanics or PoC scope:

### World and scarcity

- Players enter a mature world of established states, factions, territory, institutions, and economic relationships instead of founding a new polity from nothing.
- NPCs initially operate unfilled offices and institutions, particularly before enough players exist to occupy them.
- Important scarcity comes from limited extraction sites, extraction methods, access rights, and ownership rather than only from finite quantities of material.

### Roles, authority, and governance

- A new player begins with a bounded subordinate responsibility inside an existing faction and may rise or fall through several layers of authority.
- Increasing rank expands the player's authority to plan, order, allocate, or govern; exact roles such as commander, politician, corporate executive, president, or emperor are illustrations only.
- Factions may distribute authority differently, ranging from concentrated leadership to power shared among several players and NPCs.
- A faction's form of governance may change during play, although the mechanism and protections are open.

### Delegated strategy and counterplay

- Players may express persistent military, political, economic, or governance doctrine through conditional rules rather than directing every atomic action.
- A usable inherited default doctrine may support new players who have not authored rules.
- Subordinate commanders or officials may differ in competence, interpretation, and improvisation, making delegation choices meaningful.
- No doctrine should be universally optimal; opponents should be able to learn from encounters and develop counters.
- Non-transitive and contextual strengths may help create counterplay, but the design must avoid collapsing into a rigid lookup table.
- Conflict and governance resolution should be computationally bounded rather than dependent on detailed simulation of every individual actor.

### Power, recovery, and recognition

- Rank and authority are reversible: a top leader may fall to middle or lower office and later recover through effective decisions.
- Prominence increases visibility and gives rivals more reason to challenge the player, while low-ranked players are generally less valuable targets.
- Effective tenure and contribution to world development may support long-term recognition; “points” is only a placeholder, not a selected scoring system.

### Information and accessibility

- Intelligence may be powerful but should not make information investment the only viable strategic style.
- Scale, volume, and brute force should remain viable in some contexts even against more precise approaches.
- Onboarding should remain approachable while long-term play continues to reveal deeper interactions, shortcuts, and counters.
- If hierarchy is retained, every layer should be enjoyable and retain meaningful vulnerability; advancement should change the struggle rather than eliminate it.

## Unclassified candidate systems

None of the following has been accepted into the PoC or final game scope:

- infrastructure and civilian infrastructure;
- resource production;
- trade routes;
- logistics and supply chains;
- population growth and morale;
- reputation, including officer or subordinate reputation;
- diplomacy and alliances;
- global diplomacy;
- a global market;
- regional influence;
- intelligence and espionage;
- economy;
- technology;
- military.

The design process must place each candidate into one of three groups: **PoC core**, **deferred**, or **removed**.

## Open decisions

### World and ownership

- What is the playable unit: country, province, region, city, town, village, or a deliberate hierarchy?
- Is the world fictional, procedurally generated, or recognizably based on real geography?
- What does ownership or influence mean at each geographical level?
- How does a persistent world handle finite territory, new players, defeated players, inactive players, and server age?
- Which parts of the mature world are fixed history, and which can players meaningfully transform?
- How do scarce extraction sites and rights remain accessible to newcomers and recovering players?

### Hierarchy, roles, and governance

- Is the player fundamentally a persistent person, an officeholder, a household, an organization, or a career spanning several offices?
- What authority, assets, knowledge, and relationships belong to the player, office, faction, or territory?
- How are appointment, promotion, demotion, dismissal, succession, and vacant offices decided?
- How do NPC-held offices yield to players without NPCs being either useless or unfairly superior?
- Can superiors override subordinate doctrine, and can subordinates resist harmful orders?
- How can governance change without arbitrary disenfranchisement or faction capture?
- What prevents high office from requiring more real-world availability than lower office?
- How does each hierarchy layer provide a complete game rather than a waiting room for promotion?

### Fundamental loop and objectives

- What decisions make up one repeatable gameplay cycle?
- What are the smallest primary strategic levers?
- Is there victory, seasonal success, persistent status, personal goals, collective goals, or a combination?
- What motivates play over days, months, and years without making early leads permanent?
- What duration and cadence should decisions, plans, conflicts, and recovery have?

### Planning system

- What can a player plan, and how expressive may conditions and priorities become?
- What limits prevent the planner from solving the game or rewarding external scripting?
- How are conflicting rules ordered and explained?
- When does the server evaluate and execute plans?
- What information can plans use without granting perfect intelligence?
- How can opponents anticipate or disrupt plans while outcomes remain understandable?
- What happens when assumptions change, prerequisites disappear, or a plan partially fails?
- What makes a stale doctrine counterable without rewarding hourly rule edits?
- What commitment, delay, or cost applies when doctrine changes?
- How are subordinate competence and improvisation previewed and explained after an outcome?
- Where is the abstraction boundary between strategic doctrine and tactical micromanagement?

### Competition and information

- How much of another player's current and future state is visible?
- What uncertainty creates useful deduction rather than arbitrary surprise?
- How are offline players protected without removing meaningful aggression?
- What catch-up, recovery, or anti-snowball mechanisms preserve long-term competition?
- When should brute force overcome a refined counter, and what price should it pay?
- How is leadership pressure bounded so prominence remains desirable rather than becoming automatic dogpiling?

### Progression, recovery, and recognition

- What persists through promotion, demotion, defeat, faction change, or long absence?
- What does a defeated player need in order to become relevant again?
- What counts as developing the world or contributing to a faction?
- How can recognition avoid rewarding incumbency, low-value activity, or collusive metric farming?
- What replaces survival pressure at higher ranks without turning progression into constant crisis management?

### PoC validation

- What minimal economy, conflict, geography, and planning model is sufficient?
- Does the PoC need real multiplayer, simulated opponents, or both?
- How long must a session or test world run to reveal the intended decisions?
- What observable evidence will distinguish strategic fun from novelty or simple optimization?
- Which results would invalidate or materially change the central design hypothesis?
- What is the smallest test of hierarchical delegated play that does not require simulating the entire MMO?
- What meaningful decision does a new subordinate make during each expected check-in?

### Systems and interactions

- Which candidate systems are required to make the central tradeoffs legible?
- Which systems duplicate one another or add complexity without new decisions?
- How should economy, progression, diplomacy, military, pacing, morale, logistics, and anti-frustration mechanics interact?
- Which systems should be intentionally absent from the PoC?

## Initial risk register

These are risks to investigate, not conclusions or accepted solutions.

| Risk | Why it matters | Design question |
| --- | --- | --- |
| Automation becomes autopilot | The headline mechanic could eliminate play instead of enabling strategy. | Which decisions must remain manual, costly, constrained, or revisable? |
| Activity advantage reappears indirectly | Markets, combat timing, scouting, or rule edits may still reward constant presence. | What mechanisms make plans competitive with reactive hourly play? |
| Predictability becomes solvability | Fully deterministic systems may converge on one dominant script. | Where should hidden information, opponent choice, or bounded uncertainty create branches? |
| Randomness breaks planning | Large opaque swings would undermine forecasting and trust. | What random effects are telegraphed, bounded, and strategically manageable? |
| Persistent snowballing | Early winners may become permanently untouchable. | How do recovery, coalition play, costs of scale, or world structure preserve agency? |
| Offline punishment | Persistent conflict can turn sleep and work into strategic mistakes. | What attack timing, warnings, delegation, or defensive planning respects real lives? |
| Geography creates premature scope | A realistic hierarchy can multiply content, balance, data, and political-sensitivity costs. | What is the smallest abstract world that validates the loop? |
| Too many coupled systems | Broad simulation may hide whether the core loop itself is enjoyable. | Which few levers create the highest-value strategic interactions? |
| PoC tests the wrong thing | A technically impressive prototype may not answer whether planning is fun. | What explicit hypotheses and failure criteria govern the PoC? |
| Low-rank play becomes a waiting room | Scarce high offices mean most players may spend substantial time below the top. | What makes each authority layer a satisfying game in its own right? |
| High office requires constant availability | Leadership naturally produces more interruptions, negotiations, and emergencies. | How can authority increase without making frequent presence the real promotion requirement? |
| Finite offices become socially captured | Alliances, favoritism, alternate accounts, or activity may control appointment and promotion. | Which promotion and succession mechanisms preserve legitimate access to authority? |
| NPC governance undermines agency | Strong NPCs may be irrational to replace, while weak NPCs create arbitrary inherited failures. | What is the NPC's purpose, competence, and handoff rule? |
| Rule authoring becomes a scripting contest | Highly expressive doctrine may favor programmers and copied meta-rules over strategic judgment. | Which bounded rule vocabulary remains deep, readable, and accessible? |
| Commander behavior obscures causality | Hidden competence or improvisation can make a sound plan fail opaquely. | How are delegate behavior and responsibility made forecastable and explainable? |
| Counter systems become lookup tables | Hard counters can replace planning with scouting followed by an automatic response. | Which costs, commitments, mixed forces, and contextual factors keep counters non-trivial? |
| Anti-leader incentives become dogpiling | Universal rewards for attacking the visible leader can make promotion feel punitive. | How is pressure strong enough to prevent permanence but bounded enough to preserve leadership agency? |
| Contribution scoring rewards incumbency or farming | Tenure and world-development metrics can favor existing leaders or be manipulated. | What evidence of value cannot be cheaply manufactured or collusively repeated? |
| Mutable governance disenfranchises players | Institutional change may remove authority or invalidate a player's chosen role. | What consent, transition, opposition, and recovery mechanisms protect agency? |
| Constant struggle becomes constant stress | Uninterrupted vulnerability may turn long-term tension into exhaustion. | How can the nature of problems evolve while allowing periods of stability and achievement? |

## Decision log

### 2026-08-24 — Formal project-management workflow after the design gate

Status: Confirmed

Decision: The GitHub Project and its corresponding GitHub issues will govern all implementation-phase work. Every implementation or material repository modification must be justified by a tracked item, implemented on an associated branch, and delivered through a pull request. The protected default branch may only receive changes through an approved pull request. Each pull request requires review and approval by a human with the necessary project permissions. The issue and project item are completed only after the approved pull request is merged.

Rationale: This creates an auditable, reviewable workflow suitable for production software development and keeps project scope, implementation, review, and completion connected. It also ensures that automated agents cannot independently place changes into the protected default branch.

Alternatives considered: Direct commits to the default branch; pull requests without mandatory human approval; using GitHub issues without a GitHub Project. These alternatives provide weaker traceability, review control, or project-level progress tracking.

Consequences and follow-ups: The workflow is dormant during the current discussion and design phase. Before implementation starts, the GitHub Project workflow states, issue templates, branch naming convention, pull-request template, and repository branch protection/rulesets must be configured. The current default branch is `main`; if it is renamed to `master`, the same protections apply.

### 2026-08-24 — Project-scoped Codex agent team

Status: Confirmed

Decision: The future implementation workflow will use four narrow project-scoped Codex agents: `architect`, `implementor`, `reviewer`, and `qa`. The main Codex task orchestrates their handoffs. Architect, reviewer, and QA are read-only by default; only the implementor may modify source files. Agent output supplements but never replaces the required human PR review.

Rationale: Separate contexts and permissions make responsibilities clearer, reduce context pollution, and create an independent review and validation stage without allowing multiple agents to edit the same branch.

Alternatives considered: One general-purpose agent performing every stage; multiple write-capable agents editing the same branch; treating an automated reviewer as sufficient approval. These alternatives weaken separation of concerns, increase merge conflicts, or violate the human-review requirement.

Consequences and follow-ups: The definitions live in `.codex/agents/` and the concurrency limit in `.codex/config.toml`. Before implementation starts, the team should validate the prompts on a real issue and decide whether QA commands require a controlled writable sandbox for temporary test artifacts.

### 2026-08-24 — Design-advisor role during design discovery

Status: Confirmed

Decision: Metis will use a read-only project-scoped `design_advisor` as a discussion partner during the current game-design phase. It will challenge ideas, identify meaningful player decisions, surface risks and alternatives, distinguish core gameplay from deferred features or polish, and recommend PoC tests. It must not modify project files, create tickets, or silently resolve product decisions. The human project owner remains the decision-maker.

Rationale: The project is still determining its core gameplay, PoC scope, and the boundary between essential systems and attractive extras. A dedicated design role keeps those discussions focused and prevents the implementation-oriented Architect or general-purpose agent from prematurely treating ideas as requirements.

Alternatives considered: No dedicated design role; using the Architect for all design discussions; allowing a general-purpose agent to make implicit product decisions. These alternatives provide weaker separation between product exploration, technical architecture, and final ownership.

Consequences and follow-ups: The role is available now but does not open the implementation gate. Confirmed decisions must still be recorded by the human-approved documentation workflow in `DESIGN_STATUS.md`.

Add future entries in this form:

```text
### YYYY-MM-DD — Decision title

Status: Confirmed | Superseded

Decision:
Rationale:
Alternatives considered:
Consequences and follow-ups:
```
