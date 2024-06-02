# Arcane Assembly Resources
This is a repository full of resources for the excellent game "Arcane Assembly" by Isaac Lee.  It contains resources of all kinds, including spells, maps, and tutorials.

## Maps
For now, there is only a game map comprising screen shots from the in-game map with overlays for landmarks and items.  There are no plans at this time to compose maps based on screen shots.

## Tutorials
There is only one tutorial for now, a basic walkthrough.  This walkthrough involves importing spells from this repository.

In the future, I might add a tutorial about using CheatEngine to expand your gameplay a little.

## Spells
The spells are provided as import / export texts.  To use them:
- Open the spell in a text editor such as Notepad.
- Press CTRL-A or Command-A to select all text.
- Press CTRL-C or Command-C to copy the text to the clipboard.
- In Arcane Assembly, click your spellbook, click the [+] New Spell box
- In the Template selection box,  click _Import From Clipboard_.
- In the spell editor, edit the spell name to remove the "(Copy)" suffix.

### Enchanta Prima
Requirements:
- None

This is the first spell you create per the instructions in the in-game tutorial.  Nothing special here - it creates a single orb, enchants it and tosses it at the mouse cursor.  It is included just for those who might be having a hard time with the tutorial.

### Early Stream
Requirements: 
- None

This should be your first spell and you should import it immediately.  This sends a small number of fast, consecutive enchanted orbs toward the mouse cursor.  This is just like clicking the mouse button repeatedly to cast your first enchanted orb, but it's faster and is easier on your mouse button.  The _Early_ Stream is much like the normal _Stream_ spell, but it can be used before obtaining the _Repeat_ scroll.

Adjust the number of orbs it throws as you see fit.

### Cyclomatic Aspect
Requirements: 
- Repeat

This is not actually a spell.  It is a template for creating spells.  Spells which are created from this template can easily cycle through a set of aspects.  This way, you can shoot 9 orbs and they will be imbued with different aspects in order - Enchanted, Sharp, Ignite, Enchanted, Sharp, Ignite, Enchanted, Sharp, Ignite.  Most of the spells in this repository are derived from this.  

#### Note!  
This template only supports the *Enchanted* aspect.  You can import it early on in the game because it doesn't require aspects which you haven't acquired yet.  As you acquire the second and third aspects, you will need to go back to any spells which were born of this template and add the new aspect to the aspect list.  Just duplicate the previous one that added _Enchant_ to the aspects list, then change the aspect on the new line.

#### How it works...
The aspect list will contain one entry for each of the available aspects.  The list is created as a variable at the top of th espell instructions.  Then immediatley after this, the aspects are added.  Lastly, there is a _Repeat_ loop which will contain some spell code.  The first two lines of the _Repeat_ loop will contain a line which removes the first element from the list (the current aspect) and assign it to the _currentAspect_ variable for use in this _Repeat_ loop.  Then the second line immediately re-adds the aspect to the aspectList, which puts it at the end.  This action if pulling thye aspect from the top of the aspectList and putting it at the bottom causes the aspectList to cycle.  If we use the first element (at index 0) for our aspect at any given time, it will change every time we repeat the loop.

### Stream
Requirements: 
- Repeat

Like the Early Stream, this spell will simply shoot a number of orbs in the direction of the mouse pointer.  This version is derived from Cyclomatic Aspect, so it uses a _Repeat_ loop and is simplier than _Early Stream_.  It also cycles through aspects.  Be sure to add the new aspects as you acquire them if you want to cycle through them.  Feel free to modify the number of orbs thrown as well, if desired.

### Wide Cannon
Requirments:
- Repeat

Three parallel streams fire at once to cut a wide swathe through your enemies.

### Pry
Requirments:
- Repeat

Two streams fire and begin to separate, producing a wedge to attack in an ever-widening footprint.

### Scissor
Requirments:
- Repeat

The inverse of Pry, these two streams will be spread out at first and close in on each other as the spell progresses, closing in around your enemies.

### Barrage
Requirments:
- Repeat
- Sharp
- Ignite

This spell is very much like _Pry_, but it fires more orbs and it cycles through all 3 aspect types.  

#### Note!
The reason I include both Barrage and Pry is because there seems to be a bug we can exploit.  You cannot import a spell which uses a command or control you have not yet acquired.  However, it seems that you can import spells which use an _aspect_ you have not yet acquired!  You can import and cast this spell before you even reach the town.  I could have set up all the early spells to do this but I didn't want to spoil all the fun.  You will find the Barrage.txt file in the _cheats_ folder, not in the _spells_ folder.

_**This spell lets you get past certain key barriers which enforce the game's timeline.  Use this spell only if you want to cheat!**_

### Early Orb Shield
Requirments:
- Repeat
- Orbit

This produces a growing spiral of orbs around you to smash any enemies who try to approach you.  It will follow you as you move.  This early version is a little weak.  It only has an _Enchant_ aspect and the spiral will fizzle out before it gets very big.  You can cast it multiple times to keep it going.

### Orb Shield
Requirments:
- Repeat
- Orbit
- Multiply Speed

This produces a larger spiral of orbs around you to smash any enemies who try to approach you.  It will follow you as you move.  Using Multiply Speed in the Orb Shield will cause the orbs to arrive at a larger orbit faster so they don't fizzle out while the spiral is still small.  

### Orb Decoy
Requirments:
- Repeat
- Orbit
- Multiply Speed

This produces a large spiral of orbs that spin in place where you cast it, waiting for your pursuing foes to be consumed by its furious edges.  Drop these behind you when running from persistent chasers, like bats and ghosts.

### Ward Burst
Requirments:
- Repeat
- Multiply Speed
- Ward

A very expensive spell which tosses out a pile of wards in all directions.

### Semi Burst
Requirments:
- Repeat
- Multiply Speed
- Ward

A less expensive version of the Semi burst which tosses out fewer wards.  This requires much less mana.

### Ward Halo
Requirments:
- Repeat
- Multiply Speed
- Ward

A very expensive spell that tosses out a pile of wards in all directions, then freezes them in place around you (more specifically, around the spot where you were when you cast it).

### Semi Halo
Requirments:
- Repeat
- Multiply Speed
- Ward

A less expensive version of the Ward Halo.  It tosses out fewer wards and freezes them much closer to you.  This spell is fast enough that it can protect you pretty well if you cast it while standing still.

### Ward Wall
Requirments:
- Repeat
- Multiply Speed
- Ward
- Spawn With Offset

This is a proper ward spell.  Now that we have Spawn With Offset, the orbs can be spawned about where we want them without all the rigamarole of timing, speed, order, freezing etc.  They just spawn, then they ward and then they're done.  However, you can't cast it until late in the game.

### Homing Missiles
Requirments:
- Repeat
- Enemy Angle
- Repeat
- Multiply Speed

Fires a set of orbs which target the nearest enemy.  They reassess their target several times during flight to adjust their trajectory.  This means they can hit moving targets.  

By their nature, they still fire if there are no enemies but then they don't know where to go.  Since the Enemy Angle returns 0 in this case, they will fire straight to the right of the player.  This seems strange but it also conveniently functions as an indicator that there are no enemies on the screen.


### Cluster Bomb
Requirements
- Explode / Collide
- Multipley Speed

Tosses an orb that shatters into several pieces on impact with anything.  These shattered pieces then immediately explode, blowing everything to bits.  Best used on stationary targets or enemies near a wall which you can aim for, this spell does an incredible amount of damage.

### Shock Wave
Requirements
- Repeat
- Connect

Casts expanding boxes around you in each of the aspects.  As the box grows, it encounters and damages your enemies.

### Death Wave
Requirements
- Repeat
- Connect

Projects a series of ever-growing lines in the direction of the mouse.  You can adjust the width of the wave.  The wider it is, the less you have to aim.  The narrower it is, the further the wave will travel.  This spell derives from Cyclomatic Aspect, so the lines in this wave will cycle through available aspects.  

### Turbine
Requirements
- Repeat
- Orbit
- Connect

Produces a series of lines which whip around you like the spokes of a wagon wheel.  This spell derives from Cyclomatic Aspect, so the lines in this wave will cycle through available aspects.  

### Booby Trap

Requirements
- Repeat
- Connect
- Spawn With Offset

This drops a series of conjoined lines like the spokes of a wagon wheel at the location of the player.  The lines stay in place waiting for any enemies to chase you and get tangled up in them.

### Grinder
Requirements
- Repeat
- Orbit
- Connect

Fires a long line toward the mouse cursor with a series of shorter "legs" attached to it which swing around looking for prey.  Prohibitively expensive.  This is modeled after a spell I saw on the Steam Store page for this game.  Those previews were produced while the game was still undergoing changes and there is no guarantee we even have the tools to make it work the same way, but this is at least similar.

### Binary Lightning
Requirements
- Repeat
- Connect
- Spawn With Offset

Constructs a binary tree of enchanted lines, representing the web of a lightning strike.  For fun, you can modify this to make "self" the first orb added to the list.  It will make the lighting spawn a little closer to you so that enemies don't escape the net.
