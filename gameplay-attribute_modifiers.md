Hello! Thank you for taking a look.

I've always liked seeing how games combine different elements to create different gameplay.
I thought it'd be great to have some sort of "encyclopedia" of gameplay. So lets start with attribute_modifiers.


Here are some examples for modifiers and combinations:
* an enemy drops rotating lazer beams that the player has to dodge in a boss fight
* an enemy drops an ice bomb that explodes and freezes enemies
* A player has an ability that steals life from an enemy when cast
* A player has a weapon that steals life on hit.
* A player has a weapn that 'drains' life.

So what you end up seeing are combinations of a few things applied in different ways.
This is often leveraged in games that use proc-gen. Some games that come to mind here are:
* Diablo 3
* Dead Cells
* Hades


So, Let's break things down and see what we can come up with.


To have an 'effect' you need some 'target' that it is applied to. Not just an entity, but an attribute.
So, lets back up and say 'attribute'. The 'attribute' should have some affordance and impact gameplay in someway.
This is the begging of all modifiers. Being such, it is tied closely to what is 'in game'.
Hopefully by the end of this you can have enough to create a wide range of modifiers for your games.


Common Attributes:
- Armor - buff, steal, ignore
- Health - overheal, shield, damage
- MoveSpeed - rooted, hamstrung, slow
- Control - example a 'fear' ability that makes the character flee, or allows the character to take control.
- Mana - Drain, Steal, etc.
- Visibility - extra sneak


Sometimes status effects 'transfer'. Examples of items that 'transfer' or 'transfuse'.


Sometimes an effect doesn't directly impact what would classically be considered an entity. Take for example, a vortex grenade that pulls enemies toward it using force fields.
Another example could be an ability that makes it easier for a target to be targeted by it's enemy. It doesn't impact an attribute of the thing attached to.

Some effects take effect immediately. Example: bullet hit that removes health.
Some effects take effect over time. Example: a 'curse' ability that does damage over time.
All of the above deal with the 'time' variable. or the 'application'.

Sometimes different ability.

- time delay until ability triggers (like a bomb)
- raycast & instant, like a shot.
- area of effect


Another aspect of combination is the abilty, or how the status effect is applied.
Examples here are:
- turret drops that apply the status effect
- area of effect ability
- instant cast
- channeled cast
- projectile
- raycast
- Aoe from self or at target, example, a projectile you can detonate, or an explosive pulse from self.
- cleave
This boils down to some form of geometry, that can change each frame & is used to select what can be applied to.
So, the AOE is a sphere, in one case the origin is at the character in another it is elsewhere.
It grows from there and you can have a cleave, and even a cleave region that propogates forward thatt would be useful for casting something like a flame wall.
Real world examples of the cleave version are 'cone of cold' from world of warcraft.


So, we can see that we've added some sort of collision detection as there is a 'region' that triggers an 'effect'.


The next step to consider is that this only selects candidates that intersect and you need rules for deciding what the 'effect' can be applied to.
For example, if you were to cast an AOE that rooted entity in place, to root a streetsign would be strange.


You really can be extremely imaginative with ability. For example you could have the character charge forward, and when things contact with the character they get crowd cortroled and knocked down.



So this seems like alot of rambling, and to a degree it is. However, what are our takeaways?
This is a surprise to me but it seems to boil down to the five W's.
1) Who? - Entity selection, both source, and targets.
2) What? - What data, field, attribute, or object is modified or added?
3) Where? - What area can be impacted by the modifications?
4) When? - How does the modification interact with regard to time?
5) Why? - Worlds need to be consistent. Think it terms of an enemy cast it, or it was triggered somehow.



