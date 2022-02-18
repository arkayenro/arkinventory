# ArkInventory (for Retail, Classic, and Burning Crusade)

ArkInventory's display windows are built from "virtual bars", you assign categories to bars so that items in that category are displayed on the specific bars you want. There is no limit to the number of bars you can have inside a window but obviously you only have so much screen real estate before it becomes "too many".

ArkInventory uses several methods to assign a default category to an item such as what professions you have, tooltip scanning, basic type/subtype and PeriodicTable. You then assign those categories to a virtual bar.

You can also over-ride the default category by creating a rule that matches either a single or multiple items.

<br>

**Overview:**
- user configurable window width and height
- separate keybindings for each location for easy viewing
- assign items to a category of your choice (overrides the default assignment)
- assign categories to the bar of your choice
- unlimited number of bars (there are practical limits though before your screen becomes full)
- sort each bar differently if required
- user configurable bars per row

<br>

**Key Bindings:**
- Press ESCAPE to bring up the blizzard menu
- click on Key Bindings
- scroll down to ArkInventory
- bind the keys you want to use

<br>

:bulb: **Wiki:** https://github.com/arkayenro/arkinventory/wiki

:bulb: **FAQ:** https://github.com/arkayenro/arkinventory/wiki/FAQ

:bulb: **Sorting:** https://github.com/arkayenro/arkinventory/wiki/UserGuide_HowTo_Sorting

:bulb: **Rules:** https://github.com/arkayenro/arkinventory/wiki/Rules

<br>

:memo: **If you are having an issue then the first step is to disable all other mods and just test ArkInventory by itself**

:memo: **If the issue is still there then please [check for an existing issue](https://github.com/arkayenro/arkinventory/issues) and lodge a new ticket if required.**

:memo: **If the issue is gone then re-enable your other mods one by one until the issue comes back, then report that to me as well as the other mods author**

<br>

See ChangeHistory.md and VersionHistory.txt for further details

<br>

### :boom: The NoLib variant

it seems quite a few people are somehow getting the NoLib variant from their download client when they didn't specifically ask for it instead of the full variant and its causing issues as they don't have the required libraries installed separately.  Please ensure you are downloading the full variant.  if you see nolib in the filename then its the wrong variant, unless you are actually installing all of the required libraries separately as well.  If you have to you can manually download the full variant from here.

### :boom: Junk Sell getting blocked

While auto-destroy remains blocked, From 30960 onwards you can setup a Key Binding to manually sell and destroy your items.  Note that blizzard require one keypress per deletion, so if you have multiple items that need to be deleted you will need to press the Key Binding multiple times.  A message will be output if you have remaining items that can still be deleted.

### :warning: Alpha / Beta Versions: Ensure you make a backup copy of your saved variables file

Sometimes you cannot revert back to a previous version without a backup so before installing any alpha/beta version please make sure you have made a backup of your saved variable file

Your saved variable file is normally located in `...\World of Warcraft\_client_\WTF\Account\yourwowaccountname\SavedVariables\ArkInventory.lua`

If you have your download client set to automatically download alpha/beta versions then it is your responsibility to ensure you have adequate backups of your saved variables file - do not complain if you lose your configuration or it gets screwed up because of an alpha/beta version, it is always a possibility so you need to be prepared.

A simple way to back it up is to just do a copy and paste then rename the new file (using the version number of ArkInventory or the date is a good idea), eg ArkInventory-30900.lua, or ArkInventory-20191228.lua
