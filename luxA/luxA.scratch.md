# Sci fi twine

## Key Ideas

* Trippy end of universe sci fi
* Stopping heat death by maintaining one point
* Was it right to stop heat death?  
  * was new universe the wrong move?
  * can old universe know if new works?
  * is this just extending the inevitable?  
    * is each internal universe a kindled flame dark souls?
	
## Structural ideas

* 4 sections of building
* Each section has 3 "unlocks"  
  * if I feel ambitious these can be puzzles
  * more likely they'll be "lore checks"
* Solve in any order  
  * ambitious me would make you need lore from another room to solve each step
  * so ochre phase one gives lore to solve sapphiric phase one which gives lore to solve irresolution, and so forth
* each area will be an exploration of an emotion
* two areas focused on "confluence"  
  * Ochre Plinth - Nostalgia
  * Sapphiric Matrix - Awe
* two areas focused on "dissolution"  
  * Irresolution Engine - False Hope
  * Never Star - The path untaken?

### Structural details

*The four unlocks and "Success"*

1. Pass or Don't, can't move on without
2. Pass or Fail, can change until the end
3. Pass or Fail, no reset, no indication
4. Complete override, no reset

This leads to 16 choices total if left completely atomic. _This seems like plenty of work._

Implementing a single path logically took up 11 passages, this means I'd be looking at roughly 44 passages of content between all four paths. Removing one choice brings this down to 8 passages for a total of 32. I'd say that's worth the reduction.

*Ways to resolve ending*

* Math based  
  * Each path has two choices that matter
  * Choice one doesn't because it has to be right
  * Same with choice 4
  * This leaves 8 choices
  * Have each add 25 on success
  * Require 100 total for win

```
score:0
win (score >= 100): true
win (score < 100): false
```

## High level plot

<blockquote>Once a sea of endless infinities, a desert of infinite single conclusions is all that remains.</blockquote>

Your Universe was ending from heat death, but could maintain a point of disparity. In the process of building tools to maintain this disparity, you found this was true in all universes that followed the same rules. And all had reached the same conclusion. 

All settled on using that point to simulate a new universe in conjunction with all the other ending points. And so where there were once infinite infinities, there are now just infinite points, simulating one universe at a time searching for the reversal of heat death. Whenever an agent fails to repair a point, the current universe accelerates it's heat death and is then replaced with a smaller one to deal with the loss of possibilities.

## Artifacts

* Ochre is petrified quagma,
* Sapphiric is link to all others,
* Irresolution forces quantum separation,
* The never star is the concept of stars held undying.

The first 3 all maintain number 4, but the loss of any is the death of a subverse

<div style="background: #D6AF66;" class="screen">
### [[Ochre Plinth->ochreDoor]]

_Pantone Ochre_

The plinth is the last remaining bit of crystalline universe remaining. A once enormous chunk of big bang, frozen in a freak accident of its own force.

The process of whittling it down to its current form gave birth to empires older than themselves. To memory of the future as clear as the past. To power that scoured the sculptors from existence.

By the time it came to it's new purpose, barely enough remained to enact it.
</div>

<div style="background: #386192;" class="screen">
### [[Sapphiric Matrix->sapphiricDoor]]

_Pantone Star Sapphire_

The Sapphiric Matrix is ancient in a way that is hard to explain. To a thing like you, history is not a line, but an onion. Actions do not lead to consequence, per se, rather actions and their consequence iterate.

So to come across a thing that does not, and cannot change, is... unnerving. A thing that in its creation enforced its being, step by step on existence, burns almost like cold iron. You remember the Being that made this. Another thing that does not iterate. A knife deep inside you.
</div>

<div style="background: #999B9B;" class="screen">
### [[Irresolution Engine->irresolutionDoor]]

_Pantone Silver_

You stumbled upon The Irresolution Engine long before you could see its use. Wandering the sundense core of things, you saw it; a cool bubble in the midst of the stellar chaos around you. A pool of cold water in a long desert, you went to drink. But the water was foul.

Gazing into the pool, you could see it now; a Salvering Beast, born of collapsed arrogance, was trapped in this gem. It had been born of the bounty offered by the people that lived in its shadow, but as it reared to devour them, it was nailed to the wall behind all things, and they began their cutting.

When they were done, they had ensured that their sphere would never fall to the universe or the ravenges of time. They weren't there when you arrived, but its bones still served them.
</div>

<div style="background: #5F4B8B;" class="screen">
### [[Never Star->neverDoor]]

_Pantone Ultra Violet_

Once upon a time you shared this nursery with countless stars. It was warm, and bright, and you didn't need memory.

Once upon a time you shared this home with 1e+24 stars. The skies glittered with their light, and glowed in the warmth of their cradles, and you learned and built.

Once upon a time you shared this place with 1e+12 stars. You felt cold, and with desperation realized your memory was fading.

Now all that is left is the memory you stole and hid away. And without it, there would be nothing at all.
</div>


## Endings

Ideally I'll have four endings, but I think it's import to start focused on TWO.

*Initial Endings*

* Pass - Maintain the status quo
* Fail - Your universe ends

*Second Revision endings*

* Win - Establish a new system
* Lose - All universes end