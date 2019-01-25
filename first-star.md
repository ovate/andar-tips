---
layout: default
---

## The first star - or "Why does my party walk on walls?"

#### By [Andar](https://forums.rpgmakerweb.com/index.php?members/andar.11882/), 3 Aug 2015

The forum has a lot of topics where someone complains "My Actors can walk on walls on a new map" or "My actors can't move on the new map".

In all cases one of the tips is to set the first tile of the B tab to Star Passability, and that usually solves the problem (unless the game froze due to an autorun, but that's not for this topic).

But why?
What makes that specific tile of the B-Sheet so special that the entire passability of a tileset is broken if it is not set to star passability?

Basically, all tiles are numbers on the layers. The first tile of B gets the number zero because that's where indices start. And the following tiles simply count up.

Now the map has "number storages" on every layer - similiar to variables. Because all those places have to have a number defined, an entire empty map has each tile on the upper layer automatically filled with zero - which is the index number for the first B tile.

To prevent grafical mistakes, the programmers placed one override that always turns the zero-tile (the first B tile) transparent, no matter what is on the tilesheet - otherwise the map would be filled with whatever grafic is on that tile.
Because of that, you should make sure that the tilesheet you use in the B-Slot has nothing important on that first position. Some tilesets even have a sheet that has a star at that position as a reminder to set it to star - the star in the tile itself will never be visible.

Unfortunately the programmers forgot to place a similiar override for the other data of the zero-tile, which means the entire map is automatically filled with the passability setting for the first B-tile on the upper layer.

If that setting is impassible, the player cannot move
If that setting is passable, the player walks on walls

But Star-Passability means "I have no passability on the upper layer, look at the lower layer tile for passability" - that is why the first B tile always has to be set to star, or the passability on that tileset is broken.

There is one other function of the Star in the passability settings, but this is general for all tiles and has nothing to do with the specific B-sheet.
If you go into the help file for Passage, it reads:

Passage
A star also means a passable tile, but the character will be hidden behind a structure (can only be set for tiles in tabs other than **A**).

This basically means that the pictures for Tiles with Star-setting are displayed above the player sprite. It is intended for structures that the player can go behind or under - may it be a bridge, the arc of a doorway or a hidden wall (use the same grafic as a regular wall and place the wall tile with the star where the player can move through the wall).
This is of course the reason why it forces the engine to look for the passability of the bottom layer as the tile on the upper layer is out of the way above the player.
And this is also why only tiles on B to E sheets can have the Star passability, the A-sheets are all on the bottom layer.

[back](./)
