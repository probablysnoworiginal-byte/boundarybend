---
aliases:
  - Wave Ways
tags:
  - boundarybend/design
  - boundarybend/traversal
  - boundarybend/world-structure
status: proposal
---

# Wave-Ways

Wave-ways are a strong candidate for one surviving form of the [[World/Places/Traveler Legacy Hub/Protection and Fallen Routes|Original Travelers' fallen transit network]]. They are ancient, repairable routes built for fast, joyful, mostly guided movement around the circular world.

## Player experience

A working wave-way should feel closer to steering through a high-speed track than watching a fast-travel loading screen:

- momentum is exciting but bounded;
- the route is largely set, while the player still steers, reacts, or chooses between local opportunities;
- the speed is far above ordinary travel without becoming visually or mechanically incomprehensible; and
- riding the route teaches the shape of the world rather than skipping it.

## Repair changes more than the player

Restoring a wave-way establishes a fact such as `WaveWay_[Route]_Usable`. The route then becomes available to travelers, traders, local residents, enemies, or institutions whose authored behavior cares about that connection.

This is a recalibration, not a real-time economy simulation. The game only needs to present selected consequences worth authoring: new travelers at a stop, changed rumors, a reopened service, a new threat path, or a visibly used station.

## Circular-world fit

The circular world gives wave-ways a readable topology. A route can follow part of the circumference, cross a chord, change rings, or connect a local arc back to the Hub. Its map representation can remain stable at any scale because an event or stop can be stored by angular position and overlay lane rather than fixed screen pixels.

## Technical questions

- Can the movement system support high-speed constrained steering in co-op?
- How do players enter, exit, fail, regroup, or leave a route without desynchronizing the party?
- Are route repairs shared world facts, host-authoritative facts, or local session state?
- How much surrounding world must stream while the player moves at wave-way speed?
- Can one route support authored interruptions without becoming a disguised linear level?
