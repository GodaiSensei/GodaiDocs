# 🗂 Key battle concepts

## Health points (HP)

Health points represent the vitality of a fighters. The goal of each battle is to bring the opponents HP as low as possible, as the fighter with the highest HP at the end of the battle wins. Fighters reduce the opponent's HP by dealing damage.

## Focus points (FP)

Focus points represent the concentration of the fighter and his ability to use skills. Every turn each fighter gains the base amount of FP and possibly additional FP stemming from energizing hits or skill effects. The gained FP is cumulatively added to the fighters skills until they become ready for use.

## Actions

Before entering a battle, the fighter must be assigned a **build**. The first part of the build consists of a sequence of actions that the fighter will follow in a given match. Each action corresponds to one of the elements. The relations between the corresponding elements determines the outcome of each battle turn.

## Skills

The second part of the fighter's build consists of skills. Each skills has it's own **focus cost** and **cooldown**, which determine how much FP is needed to activate the skill and how long will it take for the skill to become available again after successful activation. Each skill keeps track of the accumulated FP separately, so that if one skill is activated its FP resets to 0, while other skills remain charged with whatever FP they have accumulated. The skills that are on cooldown do not accumulate FP.

The skills are activated only when they are full charged (i.e. have accumulated sufficient FP) and the fighter lends a successful attack. If the fighter has multiple charged skills the first (i.e. left-most) skill is activated, while others remain unaffected.

The skills can have a variety of effects. Based on their duration, they are grouped in 3 categories:

* **Instants**: the effect is applied instantaneously
* **(De-)Buffs**: the effect lasts for a given number of turns (max. 3 buffs at the time, no limit for debuffs)
* **Stances**: the effect is triggered at some later point when the specific conditions are fulfilled (max. 1 stance at a time).

According to the effect type, the skills can be grouped in the following categories:

* **Physical damage:** basic damage dealt by the attacks
* **Elemental damage:** special damage corresponding to one of the elements
* **Physical defense:** defense against physical damage
* **Elemental defense:** defense against elemental damage
* **Heal:** restoration of fighter's HP
* **Reflection:** redirect physical damage back to the opponent
* **Lifesteal:** special damage that heals the fighter for an amount equal to the damage dealt
* **Focus:** provides additional FP
* **Focus loss:** reduces the FP gain
* **Remove stance:** removes a stance
* **Remove (de)buffs:** removes a given number of buffs or debuffs

## Counters

Counters are the temporary boosts that the fighters accumulate by performing actions. Each action generates one counter according to the **generating** relation between the elements (e.g. kick, belonging to the fire elements, generates an earth counter). The counters provide a boost in the damage (+50% physical damage per counter) and focus gain (+20% FP per counter) from successful attacks of the corresponding element. The counters last for three turns and are stackable.
