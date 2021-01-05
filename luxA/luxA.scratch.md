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
* two areas focused on "confluence"
* two areas focused on "dissolution"

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

## Endings

Ideally I'll have four endings, but I think it's import to start focused on TWO.

*Initial Endings*

* Pass - Maintain the status quo
* Fail - Your universe ends

*Second Revision endings*

* Win - Establish a new system
* Lose - All universes end
