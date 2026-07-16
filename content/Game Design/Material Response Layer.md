---
tags:
  - boundarybend/design
  - boundarybend/combat
  - boundarybend/world
status: current
updated: 2026-07-16
---

# Material Response Layer

The Material Response Layer answers:

> What does world matter do when force acts on it?

This is not a full destruction system and not freeform digging terrain.

The invariant is:

> The world should feel like matter under force.

That means many surfaces can react, some authored objects can detach, and rare arenas or special places can reshape in controlled ways. It does not mean every meter of terrain is editable.

## Rule

World reaction should be common.

World reshaping should be rare.

## Preferred tiers

1. Cheap universal reaction
   - dust
   - sparks
   - cracks
   - scorch marks
   - sound
   - camera impulse
   - tiny debris

2. Selective interactable matter
   - rooted stone chunks
   - loose rocks
   - beams
   - shields
   - bones
   - roots
   - masonry

3. Authored break seams
   - cracked walls
   - weak bridges
   - blocked cave mouths
   - boss arena floor sections

4. Rare arena deformation
   - boss slam opens a crater
   - floor ring collapses
   - stone nodes become weapons
   - cover is created or destroyed

5. Avoid for now
   - arbitrary digging
   - persistent voxel terrain
   - fully editable landscape
   - every surface becoming simulation matter

## System stack

Kinetics asks: what force happened?

Material Response asks: what did the world material do?

Combat asks: did the resulting matter hit a body or change capability?

Resolution asks: did the material change matter to world state?

Example:

1. Player hits a marked stone node.
2. Material Response sees enough force.
3. The anchored stone detaches.
4. A scar remains in the ground.
5. A physics rock chunk appears.
6. If that rock hits an enemy hard enough, it applies normal combat impact.
7. If the node mattered to a quest, a world fact can change.

## Deliberate non-affordance

The layer also needs vocabulary for when useful matter is conspicuously absent. A close-range encounter may deliberately remove cover, long-range safety, loose projectiles, or easy elevation so the ground and surroundings make distance difficult to maintain.

Because Boundary Bend normally places enemies in spaces with useful interactions, this absence should read as authored pressure. It must not become an excuse for empty arena design.

## Playable proof

A rooted stone node provides the smallest useful demonstration. It reacts to force, stores enough impact to detach, leaves a visible scar, and becomes a throwable chunk that can affect combat through the same physical rules as any other heavy object.

A compact habitat can show three reusable matter states together:

1. anchored matter that defines the room;
2. loose bodies that move under ordinary force; and
3. authored nodes that can cross from anchored matter into loose matter.

The point is shared behavior, not one bespoke trick per prop. This is the economical version of “rip a rock out of the ground,” and the layer should stay selective until broader terrain changes clearly earn their cost.

## Multiplayer constraints

Later, the authority must decide:

- whether a node detached
- which detached body spawned
- where it spawned
- what velocity it received
- whether a collision impact counted
- whether a world fact changed

Clients can show dust and scars, but interactable detached matter should not be local-only.

## Scope guardrails

Do not build arbitrary terrain digging.

Do not build persistent craters.

Do not build full fracture simulation.

Do not make every ground polygon a material node.

Do not make NPC navigation depend on unbounded terrain edits.

The first goal is impact readability, not terrain freedom.
