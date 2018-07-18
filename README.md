# PanicSystem
ModTek mod that adds a basic panic system for MechWarriors, both playable and non-playable into the game.  Forked from RealityMachina's fork (https://github.com/RealityMachina/Basic-Panic-System) of mpstark's PunchinOut mod (https://github.com/Mpstark/PunchinOut).

## Installation

Install like any ModTek mod.

## General Details

There are four states for a pilot to be in: Confident, Unsettled, Stressed, and Panicked.

Every time a pilot has their mech take an attack, they roll for panic. This roll is increased in strength by how powerful the attack was, where it hit, how damaged the pilot's mech is in terms of armour and structure, is the rest of their lance dead or gone, etc. It is decreased by a pilot's tactics and guts scores, and their team's morale.

If this roll succeeds, they are then knocked down to the next lower state. Once they hit Panicked, they then start rolling for ejection chances. This is affected by the same things as mentioned above.

By default, pilots can only get worse in panic states once per turn, to prevent runaway panic attacks from multiple mech attacks. 

For panic recovery, as long as a pilot avoids failing another roll while they're under a panic state, they recover one state up (ie Panicked -> Stressed, or Unsettled -> Normal) (currently bugged)

A typical chain of events under this system is thus something like Normal at start -> Turn 1 during enemy action: takes hit, downgrades to Unsettled -> Turn 2: manages to avoid failing a panic roll -> Turn 3 on pilot's movement: hits Normal again

## Panic Effects  -- stil subject to tweaks for RT

Unsettled pilots by default, experience -5 to their hit chances.

Stressed Pilots by default, experience -10 to their hit chances, and are 5% more likely to be hit due to improper piloting.

Panicked Pilots by default, experience -15 to their hit chances, and are 5% more likely to be hit due to improper piloting. They roll for ejection every time they're hit while in this state.

## Special Cases
Pilots with one point of HP left, have no weapons remaining, or are the last survivor in their lance will always roll for ejection when they receive an attack.

Certain classes of mechs may have their pilots roll for a lower capped chance to eject at an earlier panic state. By default, this applies to enemy light mechs only, when they hit the Unsettled panic state.
