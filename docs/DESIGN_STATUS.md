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
- No implementation, technology-stack selection, or GitHub issue creation is currently authorized.
- Design ideas should be challenged on gameplay, balance, complexity, scalability, and technical-debt grounds.
- Once development begins, work follows the issue and pull-request workflow in `DEVELOPMENT_WORKFLOW.md`.

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

These are not proven. The PoC and design work must define how to test them.

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

### Competition and information

- How much of another player's current and future state is visible?
- What uncertainty creates useful deduction rather than arbitrary surprise?
- How are offline players protected without removing meaningful aggression?
- What catch-up, recovery, or anti-snowball mechanisms preserve long-term competition?

### PoC validation

- What minimal economy, conflict, geography, and planning model is sufficient?
- Does the PoC need real multiplayer, simulated opponents, or both?
- How long must a session or test world run to reveal the intended decisions?
- What observable evidence will distinguish strategic fun from novelty or simple optimization?
- Which results would invalidate or materially change the central design hypothesis?

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

## Decision log

No post-bootstrap game-design decisions have been recorded yet.

Add future entries in this form:

```text
### YYYY-MM-DD — Decision title

Status: Confirmed | Superseded

Decision:
Rationale:
Alternatives considered:
Consequences and follow-ups:
```
