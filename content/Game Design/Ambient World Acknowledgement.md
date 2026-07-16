---
tags:
  - boundarybend/design
  - boundarybend/narrative
  - boundarybend/world-facts
status: developing
---

# Ambient World Acknowledgement

The world can acknowledge an authored situation without converting that acknowledgement into instructions.

## Core pattern

When a scenario, person, or conspicuous event exists nearby, selected residents may mention it in ordinary dialogue. Their comment confirms that the world notices itself, but it does not provide an objective, compass marker, exact location, solution, or promise of reward.

Example: Fish Folk in the area mention a strange person seen in the woods. The comment supports the goblin in the bare yard without telling the player where to find the goblin.

## Why this is useful

- authored events feel socially situated;
- rumors can make plain or awkward placements feel intentional;
- information gathering remains play rather than UI cleanup;
- areas can contain many small situations without orbiting one savior quest; and
- a player who never follows the rumor has still received a meaningful piece of local life.

## System boundary

This should listen to coarse authored facts such as `ScenarioAvailable`, `AbsenceNoticed`, or `RegionGrowsWatchful`. It should not generate infinite gossip, summarize every completed action, or require every NPC to remember everything.

The smallest implementation is a local dialogue variant selected by one fact condition.
