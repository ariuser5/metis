# MMO Design Challenges and Emerging Direction

Recorded: 2026-08-24

Status: **Design exploration, not approved scope**

This note preserves two connected discussions:

1. the design advisor's map of common persistent-MMO failure modes;
2. the project owner's emerging concept for a mature hierarchical world, persistent delegated strategy, and meaningful play at every level of authority.

`DESIGN_STATUS.md` remains the canonical status register. Nothing in this note promotes a mechanic into confirmed scope. Titles, units, historical comparisons, and “points” are examples or placeholders unless explicitly stated otherwise.

## Status language used here

- **Confirmed** — already established in the canonical project direction.
- **Candidate (owner preference)** — an exploratory direction the owner currently favors.
- **Candidate** — an option worth considering without commitment.
- **Hypothesis** — a belief that needs design analysis or PoC evidence.
- **Open** — a consequential question not yet resolved.
- **Illustration only** — an analogy or example that is not proposed game content.
- **Recommended** — design-advisor guidance, not a product decision.

## The PoC boundary

The design advisor's central warning was:

> Solving every MMO problem before prototyping would bury the core experiment. Solve the questions that define the PoC now, and keep production-scale risks visible without building them into a miniature production MMO.

The owner agreed with this framing. The immediate objective remains to discover the smallest experiment that can demonstrate whether player-authored strategy, asynchronous execution, and opponent adaptation are genuinely fun.

## Five PoC-defining blockers and the owner's response

### 1. Core decision loop and meaning of success

**Advisor concern:** Persistent games can offer many activities without one satisfying repeated decision. The result may be a resource queue or optimization spreadsheet whose reward is merely larger numbers.

**Original question:** What decision should make the player feel clever during each twice-daily visit, and what visible outcome proves it was clever?

**Owner response:** **Open.** The owner does not yet have this answer and expects it to emerge after the world and player experience are described more fully. The hierarchical-world concept below establishes context for the loop, but it does not yet identify the repeated clever decision.

### 2. Activity advantage and real-world time pressure

**Advisor concern:** Even if construction is automated, faster reactions can compound through markets, scouting, combat, diplomacy, plan editing, and resource handling. A planner alone does not guarantee twice-daily competitiveness.

**Original question:** What may an hourly player do more frequently without receiving a compounding strategic advantage?

**Owner response:** **Candidate (owner preference).** Players should be able to configure a gameplay style or doctrine and let the game execute it successfully for days if the strategy is sound. Staying offline indefinitely should not be optimal: opponents may observe it, gain experience against it, refine a counter, and eventually defeat it.

**Hypothesis:** A good strategy can remain viable across several days while still requiring revision perhaps once, twice, or several times per week. The exact cadence is open.

**Unresolved tension:** If active opponents can inspect and edit counters continuously, the activity advantage may simply move from action execution to doctrine revision.

### 3. Planner as agency versus autopilot

**Advisor concern:** Too little planner expressiveness makes the feature cosmetic; too much turns the game into a programming contest or a collection of copied optimal scripts.

**Original question:** Which decisions must remain player judgments, and how frequently should new information make a plan worth revising?

**Owner response:** **Candidate (owner preference).** Players should author conditional doctrine for different situations instead of commanding every individual actor. Opponents must have enough levers to learn from previous encounters, alter their approach, and displace a formerly successful doctrine. There should be no perfect tactic that beats everything.

Potential rules might say:

- respond to an enemy relying on drones by emphasizing a particular weapon, using hit-and-run tactics, yielding ground, or retreating;
- react over a longer horizon to an opponent's tank-heavy force by seeking air superiority and attacking the tanks from the air;
- define responses not only for combat but also for governance crises, diplomacy, or other delegated responsibilities.

These are **illustrations only**, not selected units, commands, or systems.

**Candidate:** A player who authors no rules could inherit a usable default doctrine.

**Candidate (owner preference):** Delegated commanders or officials could differ in competence and improvisation. Some would interpret intent well; others could perform poorly or undermine a tactic, making personnel selection part of strategy.

**Open:** Rule vocabulary, number of rules, priority and conflict resolution, commitment costs, change cadence, default behavior, explainability, and the boundary between doctrine and tactical micromanagement.

### 4. Persistent lifecycle, snowballing, defeat, and new entrants

**Advisor concern:** Persistent accumulation can turn an early advantage into permanent economic, territorial, military, informational, and social dominance. Conversely, frequent resets can make persistence feel false.

**Original question:** What remains permanent—identity, history, prestige, territory, or power—and what can defeated or late-arriving players recover?

**Owner response:** **Candidate (owner preference).** Metis should begin in a mature or “already resolved” world rather than asking every player to start at zero, gather unclaimed resources, and expand indefinitely. Here “resolved” means pre-established, not politically static or strategically solved.

A player could hold the highest office today, fall to a middle or low rank later, and eventually recover through effort and good decisions. Rank and current power would therefore be reversible.

**Candidate (owner preference):** Greater prominence should create greater visibility and stronger incentives for rivals to challenge the player. Lower-ranked players should usually be less valuable targets and receive relative protection through lack of strategic importance rather than complete immunity.

**Candidate:** Effective time in high office and contribution to developing the world might create long-term recognition. The word “points” is explicitly a placeholder; no scoring system has been selected.

**Open:** What persists across office changes, defeat, inactivity, or faction changes, and what makes recovery credible without making achievements meaningless.

### 5. Predictability versus uncertainty and counterplay

**Advisor concern:** Full information and determinism can make the game solvable. Hidden information, opaque complexity, or swingy randomness can make forecasting untrustworthy.

**Original question:** What may opponents know, infer, and never know, and when must hostile intent become visible?

**Owner response:** **Open and considered especially difficult.** Information may naturally become the most valuable resource because greater knowledge allows better counter-strategy. The owner does not necessarily want intelligence investment to become mandatory.

**Candidate (owner preference):** Players who favor large numbers, volume, or brute force should retain viable paths. In some situations, a sufficiently large or robust force should defeat a more sophisticated precision action.

**Open:** The desired balance among intelligence, concealment, precision, scale, commitment, and cost.

## Additional MMO challenge register

These challenges should remain visible, but most do not belong in the initial PoC as full systems.

1. **Economy and progression stability** — compounding production, faucets, sinks, stockpiles, and trade can produce inflation, veteran invulnerability, or one dominant growth path.
2. **Offline conflict and loss** — persistent aggression crosses sleep, work, and time zones, producing alarm-clock attacks or, if overcorrected, meaningless conflict.
3. **Defeat, recovery, and late entry** — total destruction drives players away, while consequence-free defeat and effortless catch-up make competition hollow.
4. **Alliance dominance and social power** — mega-alliances, leaders, and out-of-game coordination may dominate individual strategic quality.
5. **Collusion, alternate accounts, and adversarial play** — players may exploit alts, account sharing, information laundering, win-trading, scripting, and harassment.
6. **Onboarding and cognitive accessibility** — persistent consequences, layered roles, and rule authoring can punish early misunderstanding for a long time.
7. **Population density and world aging** — worlds may empty, overcrowd, ossify around inactive holdings, or become inaccessible to late arrivals.
8. **Metagame stagnation and live balancing** — understandable systems are solved and shared, while balance changes can invalidate months of investment and political commitments.
9. **Retention without chores** — dailies, collection windows, and repetitive maintenance can improve activity metrics while violating the strategy-over-activity promise.
10. **Monetization and competitive legitimacy** — selling speed, automation, intelligence, protection, or strategic power can invalidate fair competition.
11. **Contemporary geopolitical framing** — recognizable geography and institutions introduce representation, propaganda, territorial, and moderation risks.
12. **Moderation and community governance** — diplomacy-heavy play can create harassment, coercion, scams, exclusion, and power structures extending outside the game.
13. **Testing the wrong thing** — a broad or technically impressive PoC may fail to reveal whether the planning and counter-planning loop is fun.

## Emerging world concept

### A mature world instead of isolated settlement founding

**Candidate (owner preference):** Players enter a world whose states, map, empires, institutions, holdings, and political relationships already exist. They do not begin by founding another interchangeable settlement and gathering unclaimed surroundings until they become large.

Early in the world's life, NPCs may operate factions and offices that players have not yet occupied. The competence, purpose, legitimacy, replacement, and handoff behavior of those NPCs remain open.

### Scarcity through place, access, and control

**Candidate (owner preference):** Resources are limited primarily by the number and location of extraction sites, available extraction methods, access rights, and ownership. The intended scarcity is therefore political and strategic, not necessarily permanent material exhaustion.

Open questions include whether extraction has throughput limits, degradation, substitutability, transport constraints, technological requirements, or replenishment, and how entrenched control remains contestable.

### Nested roles and authority

**Candidate (owner preference):** Each faction contains several layers of authority. A new player joins in a small, bounded role and manages what is immediately within that role's control. Strong performance may produce promotion, broader authority, and greater rights to plan or order how the faction operates.

Possible starting identities such as commander, politician, military official, or corporate executive are **illustrations only**. Likewise, emperor and president are example titles rather than selected government forms.

**Candidate (owner preference):** Different factions may distribute authority differently. One may concentrate power in a head of state; another may divide it among several players and NPCs. Governance form may change over time.

Open questions include appointment and promotion, superior and subordinate rights, override and resistance, succession, vacant offices, dismissal, legitimacy, constitutional change, and protection against social capture.

## Emerging strategy concept

### Persistent delegated doctrine

**Candidate (owner preference):** A player defines a style or doctrine that continues to operate while the player is absent. The game resolves situations according to conditional priorities and delegated judgment rather than repeatedly waiting for live input.

The resolution model should remain computationally bounded and avoid simulating every individual soldier or actor in detail. At the same time, it should contain enough meaningful variables and opponent choices that exact outcomes are difficult to predict without making outcomes arbitrary or inexplicable.

### Learning and counter-learning

**Hypothesis:** A strong doctrine can dominate for a time, but repeated observation gives opponents evidence from which they can develop a counter. The historical phalanx and later adaptations against it are an **illustration only** of an initially successful technique whose weaknesses take time to expose.

The cavalry, swordsmen, spearmen, and archers comparison is also **illustration only**. It represents a desired non-transitive structure in which strengths are contextual rather than universally ordered. Actual Metis units, facilities, and industries remain contemporary, with the exact extent of near-future content open.

The design must avoid turning contextual counterplay into a shallow rock-paper-scissors lookup table where scouting automatically determines the answer.

### Delegates and improvisation

**Candidate (owner preference):** A subordinate's competence affects how doctrine is interpreted and how well the subordinate responds to unanticipated conditions. Selecting whom to entrust with a conflict, crisis, or governing responsibility could therefore be strategically meaningful.

This introduces a major predictability requirement: the game must make it possible to distinguish a poor plan, a poor delegate, an opponent's superior response, and bounded uncertainty. Hidden “smart” or “dumb” behavior would otherwise make learning impossible.

## Progression and experience goals

### Approachable entry with long-term mastery

**Candidate (owner preference):** Onboarding should be as simple as possible. Continued play should nevertheless reveal quirks, shortcuts, counters, and stronger approaches so that the game does not become fully mastered immediately.

A default inherited doctrine is one candidate bridge: a new player could begin with functional behavior, understand a bounded role, and progressively replace defaults with deliberate choices. This is not yet an approved onboarding system.

### Meaningful play at every hierarchy layer

**Candidate (owner preference, conditional on retaining hierarchy):** Every level should be fun to play. Lower roles must not be mere waiting rooms, and top roles must not represent the point where struggle disappears.

The owner's Minecraft comparison is **illustration only**: early survival pressure can be compelling, but progression may eliminate that pressure and shift entirely toward creation. Metis should instead change the nature and scale of the player's problems as authority grows while preserving vulnerability, tension, and meaningful choices.

This does not imply nonstop emergency. “Constant struggle” must be reconciled with sustainable long-term play so that promotion increases agency rather than real-world workload and stress.

## Cross-cutting tensions to preserve

| Tension | Failure mode to avoid |
| --- | --- |
| Mature world versus newcomer agency | New players become irrelevant functionaries in somebody else's established story. |
| Scarce rights versus late entry | Entrenched ownership excludes newcomers and recovering players from meaningful economic positions. |
| Hierarchy versus scalable fun | Most players wait below a tiny number of worthwhile top offices. |
| Promotion versus social capture | Alliances, favoritism, alts, or activity determine advancement more than good decisions. |
| Authority versus twice-daily play | Leadership requires constant availability, making activity the real promotion criterion. |
| NPC bootstrapping versus legitimacy | NPCs are either irrationally strong incumbents or sources of arbitrary inherited failure. |
| Persistent autonomy versus activity advantage | Offline doctrine works, but hourly opponents gain by continuously switching counters. |
| Doctrine versus autopilot | Strategy becomes copied scripts rather than ongoing judgment. |
| Easy editing versus strategic commitment | Instant counter-swapping rewards constant reaction; slow changes punish understandable mistakes for days. |
| Delegate competence versus predictability | Outcomes feel random because players cannot attribute success or failure. |
| Counters versus lookup tables | Scouting reveals one automatic response instead of creating a strategic choice. |
| Intelligence versus brute force | Either information becomes mandatory or raw scale makes planning irrelevant. |
| Leader pressure versus viable leadership | Promotion triggers an unavoidable dogpile and becomes a punishment. |
| Reversible rank versus achievement | Turnover feels arbitrary, or retained power recreates permanent snowballing. |
| Tenure and contribution versus metric gaming | Incumbents or colluding factions manufacture recognition without meaningful value. |
| Mutable governance versus player agency | Institutional change removes roles or rights without meaningful participation or recovery. |
| Simple onboarding versus emergent complexity | The player faces several different games and rule languages before understanding one meaningful decision. |
| Constant struggle versus sustainable play | Persistent tension becomes persistent anxiety and obligation. |

## Candidate PoC implications, not approved scope

The emerging concept suggests—but does not yet approve—a bounded experiment containing:

- one pre-existing faction or institution;
- one meaningful subordinate office with inherited assets and authority;
- a usable default doctrine;
- a small number of player-editable conditional priorities;
- one scarce objective or resource-access right;
- limited but legible opponent information;
- an opponent capable of delayed adaptation;
- one short promotion, demotion, or authority-change signal;
- forecasts and execution explanations sufficient to learn why outcomes occurred.

Full constitutional change, realistic world geography, global markets, large alliances, the complete hierarchy, detailed individual combat, and production-scale live systems should remain outside this candidate test unless later analysis shows that one is necessary to answer the core hypothesis.

## Recommended next discussion order

1. Identify the persistent player identity: person, officeholder, household, organization, or career.
2. Define one low-level role and the complete gameplay loop available inside it.
3. Define what authority, assets, information, and responsibilities attach to that role.
4. Define one doctrine decision that can continue operating between visits.
5. Define how an opponent learns enough to counter it without hourly reaction becoming dominant.
6. Define how success, promotion, demotion, or recovery is demonstrated in the test.
7. Decide what remains permanently attached to the player when the office changes.

The first unresolved question remains:

> What decision should make a player feel clever during each expected visit, and what visible outcome proves that it was clever?
