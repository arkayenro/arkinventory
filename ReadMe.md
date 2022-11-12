# ArkInventory (for Retail, Classic, and Wrath)

**Dragonflight Warning**

The next set of Alpha builds are being updated for Dragonflight/PrePatch and as such may cause issues in Classic, Wrath, and Shadowlands.  If you notice anything wrong please [check for an existing issue](https://github.com/arkayenro/arkinventory/issues) and create a new issue if required so i can fix it.

---

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
- sell junk items automatically or manually (delete available via a keybinding or right clicking when at a vendor)
- random pet and mount summons.  can also assign a group of them to select from

<br>

**Key Bindings:**
- Press ESCAPE to bring up the blizzard menu
- click on Key Bindings
- scroll down to AddOns > ArkInventory
- bind the keys you want to use

---

**Need Help?**

:memo: [Wiki](https://github.com/arkayenro/arkinventory/wiki)

:memo: [Frequently Asked Questions](https://github.com/arkayenro/arkinventory/wiki/FAQ)

:memo: [Sorting](https://github.com/arkayenro/arkinventory/wiki/UserGuide_HowTo_Sorting)

:memo: [Rules](https://github.com/arkayenro/arkinventory/wiki/Rules)

<br>

:memo: If you are having an issue the first step is to disable all other mods and test with only ArkInventory loaded

:memo: If the issue is still there, please [check for an existing issue](https://github.com/arkayenro/arkinventory/issues) and create a new issue if required.

:memo: If the issue is gone, re-enable your other mods one by one until the issue comes back, then note the last mod you enabled in your issue as well as notifying the author of the other mod

<br>

See [ChangeHistory.md](https://github.com/arkayenro/arkinventory/blob/master/ChangeHistory.md) for changes to the latest version.
See [VersionHistory.md](https://github.com/arkayenro/arkinventory/blob/master/VersionHistory.md) for all previous changes.

---

### :boom: The NoLib variant

it seems quite a few people are somehow getting the NoLib variant from their download client when they didn't specifically ask for it, instead of the full variant, and its causing issues as they don't have the required libraries installed separately.  Please ensure you are downloading the full.  if you see nolib in the filename then its the wrong variant, unless you are actually installing all of the required libraries separately as well.  If you have to you can manually download the full variant from [CurseForge](https://www.curseforge.com/wow/addons/ark-inventory), [WoWInterface](https://www.wowinterface.com/downloads/info6488-ArkInventory.html), or [Wago](https://addons.wago.io/addons/arkinventory).

### :boom: Junk Sell getting blocked

While auto-destroy remains blocked, From 30960 onwards you can setup a Key Binding to manually sell and destroy your items.  Note that blizzard require one keypress per item deletion, so if you have multiple items that need to be deleted you will need to press the Key Binding multiple times.  A message will be output if you have remaining items that can still be deleted.

### :warning: Ensure you have backup copies of your saved variables file

Sometimes you cannot revert back to a previous version without a backup, especially alpha or beta versions, so before upgrading please make sure you have made a backup of your saved variables file

Your saved variables file is normally located at `...\World of Warcraft\_client_\WTF\Account\yourwowaccountname\SavedVariables\ArkInventory.lua`

It is your responsibility to ensure you have adequate backups of your saved variables file.  You dont have to do them frequently, just after you've made major changes to your config is probably fine for most people, but you should get into the habit of making backups because when it does corrupt you wont have to reconfigure everything from scratch.

If you have your download client set to automatically download alpha/beta versions you should definitely have backups.

A simple way to back up the saved variables file is to just do a copy and paste then rename the new file (using the version number of ArkInventory or the date is a good idea), eg ArkInventory-30900.lua, or ArkInventory-20191228.lua
