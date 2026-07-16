---
tags:
  - boundarybend/design
  - boundarybend/combat
  - boundarybend/resolution
status: current
updated: 2026-07-16
---

# Resolution Layer

The Resolution Layer answers one question:

> Has this conflict changed the world enough that the world should now treat it as resolved?

It does not decide the emotional, moral, or narrative meaning by itself. It records broad outcomes and world facts so quests, NPCs, zones, and authored story can react without knowing the exact button press, weapon, spell, or animation that caused the change.

## Core rule

Combat ends when the encounter is resolved, not necessarily when a participant dies.

BoundaryBend should support conflicts ending through:

- death
- surrender
- collapse
- retreat
- capture
- incapacitation
- negotiation
- displacement
- delay
- scripted or special outcomes

The combat system reports changed states. The world decides what those states mean.

## System stack

Kinetics asks: what physically happened?

Condition asks: can this entity continue participating normally?

Behavior asks: how does this entity respond to its state?

Resolution asks: does the world consider this encounter, threat, or quest beat solved?

Quests should listen to world facts, not specific player actions.

Bad:

- If player killed goblin chief, complete quest.

Better:

- If `GoblinRaidThreatActive == false`, complete quest.

That fact might become false because the chief died, surrendered, was captured, negotiated, fled, lost supplies, accepted relocation, or because the food shortage driving the raids was solved.

## Outcome categories

The writing should not explode. The system should track meaningful categories, not every individual action.

Important categories:

- what changed
- who or what was affected
- how permanent it was
- how violent it was
- whether the outcome was lethal, nonlethal, capture, negotiation, displacement, surrender, or incapacity

This is not a pacifist/genocide ledger, karma meter, or universal soul stat.

This does not forbid the game from having three broad, authored tonal world conditions. Those conditions are a late interpretation of selected concrete facts at deliberate milestones, not a meter incremented after every action. A particular pattern of outcomes may therefore make the whole world feel substantially sadder while the underlying Resolution Layer remains factual and locally meaningful.

## Difference from a morality system

The Resolution Layer does not judge the player. It makes state explicit.

The world may later contain people who care about a fact. A village may care that the raid threat ended. A goblin survivor may care that the ending was violent. A healer may care that captured enemies still need aid. Those reactions should come from authored values, relationships, and local context, not from a hidden universal moral score.

One especially small response pattern is [[Ambient World Acknowledgement]]: local dialogue can notice that a situation exists or changed without becoming an objective marker, solution, or exhaustive history system.

## Playable proof

The smallest useful demonstration is a raid that can end through several outcomes while the world understands only the resolved fact.

1. Participants receive outcomes from shared combat and conversation rules.
2. Broad outcomes—incapacitated, surrendered, captured, fled, killed, negotiated, displaced, or condition-broken—are reported.
3. The encounter watches those outcomes.
4. Once its authored condition is satisfied, the raid threat becomes inactive.
5. The world can then remove a barricade, open a route, change a camp, or let a quest conclude.

The gate cares about one fact condition, not how that fact became true. That is the smallest proof that world state can drive presentation and collision without turning every action into a bespoke story branch.

## Authoring contract

The layer should expose simple facts and outcomes before it exposes complexity. Authored content can react to a changed fact, a reported outcome, or a resolved encounter without owning the combat state machine that produced it.

## Multiplayer constraints

Prototype code may run locally for now, but the architecture should not hide truth in a client-only quest script.

Later networking rules:

- world facts need one authority
- resolution outcomes must be explicit events
- clients can request outcomes, but authority decides accepted state
- debug HUDs can be local, but resolved facts cannot be local-only
- random client-side-only resolution logic should be avoided

## Scope guardrails

Do not build a giant quest framework yet.

Do not build a morality ledger.

Do not make every NPC remember every exact player action.

Do not track souls on every enemy.

Do not encode every goblin-specific story branch into combat scripts.

Build the smallest laws first. Let authored content care only about the facts that matter.
