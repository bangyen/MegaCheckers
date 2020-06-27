MegaCheckers:

A game where you take turns moving pieces to kill all of your enemy's pieces.  To do this, your pieces jump onto the enemy piece to crush them.  In order to aid you with this goal, every few turns a random number of mystery items will appear on empty spaces.  You pick up an item and on any subsequent turn,  you can use the item (depending on what the item is) to destroy enemy pieces, to set up traps, to alter the playing field (raise/lower, destroy, magnetize, make one way, push pieces, etc), to power up your piece, and so on.  Eventually networking will be enabled.  


v 0.6:
	Can keep track of empty spaces now. Orbs exist now. You can pick up items now.  The only item implemented is the "suicide row", but it's confirmed working.  The avatar attribute is now in effect.  Your piece's avatar changes color when it's holding an item.  (Haven't tested whether it disappears when it's used up since the only working item right now kills you anyway).  Corrected in error in keeping track of the location of pieces (forgot to change i,j to rows-i-1,j for the initialization procedure).  Added an item button that greys out when not valid.  Changed the visual size of the field to help fit on smaller monitors.  To do: add the option to view the stats of an orb (maybe via a context menu?), add more items (shield most likely).  Test to make sure pieces revert to normal when they don't have an item held anymore.

v 0.5.1:
	Spawn orbs now.  Spawns in legal locations.

v 0.5:
	Major logic changes.  No longer use a "player" class, as it seems pointless, at least at the moment.  Instead, the gameBoard list now contains two elements per location - a tile object slot to keep track of the tile (its conditions), and a piece object to keep track of the pieces (their items, location, and ownership).  This should result in easier coding going forward.  Beginning work on tracking empty spaces for item orb spawns.  

v 0.4:
	Put in even more information frames, including number of pieces left.  Messages show up more neatly now.  Considering a log output somewhere on the side or bottom. 

v 0.3:
	Put in a information frame on bottom, game properly calculates whether you can move to a location (diagonals have NOT been implemented yet - that will be added when that item is added to the game; same with "around the world" items that let you move pacman style from the right edge of the field to the left, for example).  Popups have been removed since all info appears on the bottom now. Still need todo the item generation.

v 0.2:
	Gameboard properly updates between turns.  Pieces can move around anywhere (teleporting). Pieces can kill.  Turns are properly tracked and a player can't move his piece twice (opposing players can't control their opponent's pieces).  To do: generate items and allow them to be picked up.  Note: this requires changing the board logic to go from "0" for a blank area to having a 1 for denoting that items exist.  Alternatively, may need to have a new class to represent spaces as eventually I'll want the floor to be raised and damaged and whatnot. 

v 0.1:
	Starting right out with a GUI.  Currently shows the field and properly generates the starting pieces and has a logical gameboard that gets displayed for debug purposes in the console.  The next commit should feature the ability to move the pieces around, followed by a commit for properly killing a piece, followed by generating items, then picking up items, then using items (with just a print message for now). 