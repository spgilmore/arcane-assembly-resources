# Arcane Assembly Cheats
## Barrage Spell
You can import the Barrage spell from the Barrage.txt file nearly at the very beginning of the game.  It will let you destroy barrier walls made of spider webs or flammable blocks.  You can then traverse areas of the map (such as the Yellow Area) earlier than you are allowed to.  This does not mean there won't be other barriers to your traversal, however!  Aside from that, it's a useful and competent spell on its own if you choose to use it.

## CheatEngine
You can download and compile the CheatEngine-i386 source and use it to acquire everything you need to be a diety in this game.  

### Obtain Oscene Amounts of Gold
To augment your gold amount: 

- Download the official source for CheatEngine-i386 from GitHub (`https://github.com/cheat-engine/cheat-engine`) and build it yourself using FreePascal.  NEVER use a build of this program that you downloaded from the internet.
- Start Arcane Assembly and start a game.  Kill a few petit enemies to acquire some amount of gold, preferably an amount which is greater than 10 and not a power of two.  Wait for the acquisition of the gold to be "counted" in the upper-right corner.  It only takes a moment for it to stabilize but it's important.
- Open CheatEngine-i386.exe.
- On the menu, click File -> Open Process.  In the Process List modal popup, under the _Applications_ tab, select The one that says `CodingMagicGame`.  It will have the ArcaneAssembly icon next to it.  Click the _Open_ button.
In the main CheatEngine window, you will see an empty panel on the upper left quadrant, an empty panel on the bottom half and a form on the upper-right quadrant.  In the form, set the Scan Type to `Exact Value` and the Value Type to `4 Bytes`.  In the Value field, type the number of gold pieces you have in the game.  Click the `First Scan` button.  It will populate the top-left panel with memory addresses and values.
For a few seconds, periodically click the `Next Scan` button.  As data is always changing in memory, any addresses which have changed will drop out of the list and narrow down the one we want just a little.
Go back to Arcane Assembly and acquire a little more gold.  Come back to CheatEngine and put the new gold amount into the Value field and click `Next Scan` again.  Once you have narrowed it down properly, you will _probably_ see 3 values remaining.  The one we want is _probably_ the last one.  To be sure, double-click on the row in the upper-left panel and it will appear on the bottom panel.  Double-click the value in the _value_ column and you can edit it.  Set it to 1 more than the previous value and see if you gained 1 gold inside the game.  If so, this is the one you want.  If not, change the value back to its previous value and remove it from the bottom panel with the red button.
If you edit the value and it affected your gold in the game then you have found the one we want.  Double-click on the value again and set it to 9999999 (that's seven digits of nine).  You can set it much higher without a problem, but it won't show the correct number.  Now that the game memory has been modified, you have a ton of gold.  
Some game events or actions can cause your modified data values to be wiped out and reset back to their "proper" values.  To prevent this, you want to immediately save your game on a bench.  Once this is done, your gold is set in stone.

### Obtain Red Gems, Blue Gems, Magic Shards.
While you have CheatEngine-i386 running and have the address for the gold amount in the bottom panel, click on the line and press CTRL-B on the keyboard.  A memory viewer window will appear.  In the bottom half, the data grid will show that the upper-left-most address is the address of the gold amount.  The next row contains all zeroes for the first 4 columns of 2-digit values.  Change the first two columns of the second row to be FF FF.  This will give you about 65535 red gems.  Do the same thing on the third line.  This will give you 65535 blue gems.  Do the same thing on the fourth line.  This will give you 65535 magic shards.  

Again, go sit on a bench to lock in these values.

### How much is enough?
These cheats are definitely enough.

With this amount of gold, you can very easily buy enough potions to upgrade to 1000 hit points and 1000 magic points along with 100 Essentia potions.  With this setup you can pretty much cast any spell you come up with, will very seldom run out of mana and can recharge all mana in about half a second if you need to.  It's fast enough that it pretty much takes care of itself.  If you want to go crazy, you can easily upgrade many times this much and still have plenty of gold.

With 65k of gems, you can easily upgrade your aspects 20 times.  The game doesn't tell you how much punch these upgrades give you, so I don't know how many constitutes "enough".  I have upgraded 10 times and it seems to me like it probably doubled the offensive power of the aspects but it's just a wild guess.

I like to upgrade my flask to have Flask Number of 10 and Flask Value that will refill 1000 health points so a single flask will refill all of my hit points at once.
