# 3.10.01 (26-OCT-2022)
 - changed - wearing location will no longer update while in combat
 - changed - quiver and ammo bag slots will no longer update while in combat (hunters may still have issues with ammo in normal bags)
 - fixed - alignment of the quest border texture
 - fixed - alignment of the new item glow texture
 - fixed - money display position in status window
 - fixed - backpack tokens should now align properly when the empty text or money frames are not enabled
 - fixed - wearing location should now update on trinket/ring changes
 - changed - the status bar will now increase/decrease in height to match the selected font size
 - changed - backpack tokens are now centered and will grow to fit the amount of available space - if there are too many tokens to fit within the space they will move to the next line down
 - fixed - bag type and slot count issues due to blizzard changing the API
 - fixed - removed xml OnTooltipAddMoney from ArkScanTooltipTemplate (appears to have been deprecated)
 - fixed - https://github.com/arkayenro/arkinventory/issues/1616 - bag types and some category names are missing/invalid.  swapped to Enum.xxxxx due to removal of all LE_ITEM_zzzzz globals, which are used to find bag types and category names, from the latest beta
 - fixed - https://github.com/arkayenro/arkinventory/issues/1615 - summon mount secure action button / keybind
 - added - config > settings > item > status icons / overlays > profession quality - options for displaying as a number, and setting colour
 - fixed - https://github.com/arkayenro/arkinventory/issues/1507 - profession based set requirement failures should no longer be seen as not being unable to wear the actual item
 - added - a one off (per enable) warning message if your profile is using a blueprint that no longer exists
 - fixed - cursor not getting reset when leaving an item
 - fixed - the normal action cursors should no longer show when in edit mode
 - fixed - (dragonflight) new item glow not getting reset when entering an item
 - added - if you use Peddler, junk items are now identified via it, and not via ArkInventory
 - fixed - (dragonflight) C_TradeSkillUI.OpenTradeSkill is now a protected function so onload scans can no longer be performed and will be skipped if enabled
 - fixed - other issues with tradeskill scanning
 - added - https://github.com/arkayenro/arkinventory/issues/1547 - config > settings > window > scroll bar
 - added - config > settings > item > status icons / overlays > junk > size
 - added - config > settings > item > status icons / overlays > upgrade > size
 - added - config > settings > item > status icons / overlays > corruption > size
 - added - config > settings > item > status icons / overlays > quest > anchor
 - added - config > settings > item > status icons / overlays > quest > size
 - fixed - issue with quest icon not always showing when it should
 - fixed - https://github.com/arkayenro/arkinventory/issues/1609 - issue with cross client tradeskill scanning
 - fixed - (dragonflight) the default ui bank frame should no longer open when you open the bank
 - fixed - (dragonflight) the default ui guild bank frame should no longer open when you open the guild bank
 - changed - money frame click has gone back to the single generic money popup, not the individual gold/silver/copper ones
 - fixed - issue with tradeskill scanning (nil key values)
 - changed - (retail) toc updated to 100002
 - fixed - https://github.com/arkayenro/arkinventory/issues/1604 - client detection issue that caused some categories to not show
 - changed - https://github.com/arkayenro/arkinventory/issues/1605 - outfit( ) rule function will now check using all supported outfit mods as well as the equipment manager, and not just the first one that is enabled.
 - changed - various cross client functions for dragonflight
 - fixed - some non battlepet items were incorrectly causing a battlepet tooltip to be generated
 - fixed - cooldown should now display in the wearing window
 - fixed - frame levels werent getting reset properly so the background would occasionally end up above the items and block mouse input
 - added - cosmetic item overlay - can be disabled via config > settings > item > status icons / overlays > cosmetic
 - added - conduit item overlay - can be disabled via config > settings > item > status icons / overlays > conduit
 - added - professional quality item overlay - can be disabled, the position or size changed, via config > settings > item > status icons / overlays > profession quality
 - added - profession quality as a new sort method key
 - changed - default sort methods updated to include profession quality
 - changed - reagent bank and reagent bags share the same slot type
 - added - (dragonflight) restack now supports the reagent bag
 - fixed - issues with multiple functions that reference the project id to hide data that shouldnt exist.  wrath getting a new project id sort of broke them so that check has been removed and you may see old character data appear in item counts, gold, search, and when switching to another character.  you can manually delete the old data from the switch character menus, or in the config.
 - fixed - https://github.com/arkayenro/arkinventory/issues/1602 - removed internal debug output
 - fixed - (wrath) https://github.com/arkayenro/arkinventory/issues/1593 - outfit( ) rule function when using the blizzard equipment manager
 - fixed - frame name mouseover tooltip (only applies to shortened names)
 - fixed - https://github.com/arkayenro/arkinventory/issues/1599 - renamed xml element for bar names
 - fixed - https://github.com/arkayenro/arkinventory/issues/1600 - tradeskill scanning
 - fixed - issue with several tradeskill based tooltips
 - fixed - https://github.com/arkayenro/arkinventory/issues/1597 - currency based tooltips
 - added - (dragonflight) item counts on recipe output item
 - added - (dragonflight) item counts on recipe reagent items
 - changed - client detection and checking code to support pre-patch
 - added - (dragonflight) category: class evoker
 - fixed - issue where the reagent bank wasnt being scanned when away from the bank (bank and bank bags cant be scanned away from the bank, so its partially helpful)
 - changed - restack action menu consolidated into a single layer
 - added - option to disable restack
 - fixed - (wrath) https://github.com/arkayenro/arkinventory/issues/1594 - category: class death knight unhidden
 - fixed - (wrath) https://github.com/arkayenro/arkinventory/issues/1595 - category: skill inscription unhidden
 - changed - client detection code to support pre-patch
 - changed - multiple categories have had their client states updated (if a category is missing or showing when it shouldnt, let me know via a ticket)
 - added - support for 10.0 PTR prepatch - there will be issues, please log a ticket for them
 - fixed - (dragonflight) money frame elements
 - added  - (dragonflight) reagent bag slot (not sure if it works properly as i cant find any reagent bags)
 - changed - right click bag slot menus to work with all game clients
 - fixed - (dragonflight) issue with bank and reagent bank tooltips

# 3.09.68 (08-SEP-2022)
 - fixed - issue with WOW_PROJECT_ID getting a new client value for wrath (WOW_PROJECT_WRATH_CLASSIC)
 - fixed - https://github.com/arkayenro/arkinventory/issues/1575 - issue with toybox filters not being restored to their original values after a scan
 - changed - (Retail) toc updated to 90207
 - updated - recategorised some items
 - added - wrath toc file

# 3.09.67 (05-JUN-2022)
 - updated - recategorised some items
 - fixed - parts of the LDB object wouldnt always update on first load (waiting for currencies and rep to become ready)
 - changed - (TBC) toc updated to 20504
 - changed - (Classic) toc updated to 11403
 - changed - (Retail) toc updated to 90205

# 3.09.66 (18-MAR-2022)
 - fixed - mythic keystone data never being ready causing constant resorting
 - updated - recategorised some items

# 3.09.65 (16-MAR-2022)
 - added - category 461 - Consumable > Abilities and Actions
 - added - item level 200 korthian equipment tokens
 - added - item level 226 zereth mortis equipment tokens
 - added - more code around getting item info
 - changed - itemframe onenter code for bags, bank, and keyring, to allow for tiptac mouse anchoring
 - updated - achievement to unlock flying in zereth mortis
 - updated - mount data to 9.2.0
 - updated - pet data to 9.2.0
 - updated - recategorised some items

# 3.09.64 (23-FEB-2022)
 - fixed - issue with LibDialog-1.0 (temporarily until the author fixes it)
 - fixed - (TBC) issue with splitting stacks in the guild bank
 - added - wago project id
 - changed - (TBC) toc updated to 20503
 - changed - (Classic) toc updated to 11402
 - changed - (Retail) toc updated to 90200
 - changed - renamed mainline toc files because curse cant handle them and rejects the upload
 - note - contains new folder structure - do NOT upgrade while the game is running

# 3.09.63 (30-NOV-2021)
 - added - client specific toc files
 - added - config option advanced > ldb > item tracking > show zero - disabling this option will hide the icon for any items you dont have (zero count), they will remain in the tooltip
 - note - contains new files - do NOT upgrade while the game is running
 
# 3.09.62 (28-NOV-2021)
 - no longer available
 
# 3.09.61 (19-NOV-2021)
 - fixed - (mostly) issue when right clicking on a completely identical item in your bags that you are also currently wearing not updating the locked status (remained faded) when they swap (if you keep swapping them multiple times it will eventually get out of sync until the next window update)
 - fixed - issue with the junk quality, and soulbound options, not clearing the item cache when you change them (so would need a reload to actually change)
 - fixed - (maybe) belowaverage rule function to stop an issue where it somehow collects more items than it should
 - fixed - inactive heart of azeroth items are no longer considered unusable (or junk because of that)
 - fixed - issue with unequipable status if you enter the game while in the arena, mythic plus, or torghast, or while in combat and open your bags while still in combat
 - added - config option for junk soulbound equipment to ignore item level requirement (ie a level 60 item when you are level 58 would no longer be considered junk) - enabled by default
 
# 3.09.60 (10-NOV-2021)
 - added - config option to disable object data not found warning message - disabled by default
 - added - config option for junk selling to continue while in combat - disabled by default
 - added - rule function `belowaverage( )`
 - fixed - issue with item count array being erased while in the middle of building
 - fixed - issue with sell junk items destroy code.  you can only destroy one item/stack per keypress
 - fixed - typo in the soulbound equip junk code that was causing it to never do the check
 - changed - toc updated to 90105
 - changed - updated workaround for the issue with bank bag slot id values to use the `GetFirstBagBankSlotIndex( )` function if available
 - changed - already known for junk purposes should now apply to all items
 - removed - no longer listen for action bar events

# 3.09.59 (xx-xxx-xxxx)
 - no longer available
 
# 3.09.58 (06-OCT-2021)
 - fixed - issue with some leftover pet test code
 - fixed - issue with ilevel value for some items
 - fixed - (classic) added a workaround to cater for an issue where the bank bag slot id values returned by blizzard are incorrect.  they are out by 4 as if the bank had 28 slots instead of 24
 - added - extra error catching code for a weird item count (i think) issue that i cant duplicate yet and only rarely happens
 
# 3.09.57 (16-SEP-2021)
 - fixed - conflict with skillet.  scan on load is now ignored if skillet is loaded and enabled.  you have to open the blizzard tradeskill window to trigger a scan, it will not scan the skillet window.
 - fixed - issue with extracting the stock value from tooltip for some languages
 - fixed - (classic) issue with `ITEM_COSMETIC` not existing
 - fixed - (bcc) guild bank should now be working properly.  thanks to the Variance guild on Myzrael for the invite so i could test.
 - fixed - issue with a variable that should have been local
 - changed - guild bank icon as its current one did not work in bcc
 - changed - window redraws when item data is eventually retrieved have been lowered to refresh to stop full rebuilds when you dont have sorting set to instant
 
# 3.09.56 (27-AUG-2021)
 - fixed - issue with languages that use a period (.), or nothing, for their thousands separator
 - fixed - issue with auto close not working when at the auction house (typo in code)
 - fixed - issue with void storage hyperlinks
 - fixed - issue with ldb object for tracked items when the item data wasnt ready (the squished up tooltip)
 - fixed - will ignore reagentrestocker issues until it has been updated
 - fixed - the unknown category assignment was getting cached so it would never recheck once the item data become available
 - fixed - issue with toggling the bonusid count/search config options
 - fixed - a restack started while dead (not ghost) would cause the client to lock up
 - fixed - issue converting string to number if there are thousand seperator characters in them
 - fixed - the window layout should build correctly when viewing other character data, and in general when item data isnt available yet.  it should also try up to five times to rebuild the window while item data is not available.
 - fixed - (classic ptr) issue with reagent, explosive, and devices categories not having default values after being removed in the ptr
 - fixed - issue with reputation tooltips when repuation level text is nil due to the data not being ready yet
 - fixed - issue with mailbox update timer config option
 - fixed - issue with `location( )` rule function for the mailbox
 - fixed - issue with bag rescan queue
 - fixed - issue with object caching for money (in mail)
 - fixed - restack code issue where the API can return a bag type of nil so it looks like a (non zero) profession bag
 - fixed - primary tradeskill assignment error with the vault after erasing its data
 - fixed - the window layout should build correctly when viewing other character data, and in general when item data isnt ready yet.  it will try up to five times (by default) to rebuild the window while item data is not ready.
 - fixed - issues with some of the legion rep tokens
 - fixed - issue with "unknown" reputation objects in the search window.  these were from other faction reputations and should now work properly.
 - fixed - the custom battlepet tooltip will now contain the "collected (x/y)" line even with item counts disabled
 - added - data correction code for GetItemInfo
 - added - categorisation for some fishing items
 - added - config option settings > design > items > item level > stock level (disabled by default) to display values for items that have "stock" values, eg ancient mana, anima, korthian relics.  bags will show the slot count.
 - added - category consumable > power systems (old)
 - removed - category system > artifact relic, and consumable > artifact power.  those items will now be assigned the power systems (old) category
 - added - bonus ids that change the item name (eg shadowlands legendaries) so that they show up in searches under their actual name and not the base item name
 - added - object data retrieval is now queued and threaded, it will not process while in combat so if you login while in combat you may end up with one big block of items until youre out of combat
 - added - a warning message will be generated if data cannot be retrieved after 5 attempts.  the warning will only be output once per item per session.  you can enable debug mode to see any further retry failures.
 - note - if you copied your savedvariables file, or imported a profile, from a higher expansion, please ensure you remove any higher expansion items from the LDB item tracking list.  they will cause warnings
 - added - config option advanced > threads > retrieving object data
 - removed - update timers have been temporarily removed
 - added - keybinding for manual junk sell.  if you are not at a merchant it will only destroy any non sellable items.  when at a merchant it will both sell and destroy.
 - note - when manually selling/destroying the threading has to be temporarily disabled which may cause some items to not sell (if you are at a merchant).
 - added - config option advanced > other > ui > retry - specify how many times it should rebuild the window while item data is not ready, before giving up
 - changed - rule function `outfit( )` requires an exact match on the set name
 - changed - decreased memory usage by caching and consolidating a bunch of data tables
 - changed - the config option settings > design > items > item level has been broken down into equip/bags/stock options
 - changed - bag scans will now yield after each slot has been scanned, not each bag.
 - changed - ldb object updates for item, currency, reputation, pet, and mount, will now wait until you are out of combat
 - changed - the New Item category is now using the C_NewItem API so moving an existing item to another slot will no longer see it as new
 - changed - if item data isnt ready when its scanned another scan is queued
 - changed - config option for junk > auto sell now only applies to auto selling when opening a merchant, and no longer disables the other options.  destroying non sellable items can only be done via the keybinding.
 - changed - using the API to work out which items are anima items
 - changed - scan code cleaned up
 - updated - config option layout for profile and item override to (hopefully) makes some things clearer
 
# 3.09.55 (13-AUG-2021)
 - no longer available

# 3.09.54 (13-AUG-2021)
 - no longer available
 
# 3.09.53 (12-AUG-2021)
 - no longer available

# 3.09.52 (10-JUL-2021)
 - fixed - (tbc) keyring: the item count is being retrieved as there are now stackable keys
 - changed - toc updated to 90100
 - changed - flying mounts should work once shadowlands flying is learnt
 - changed - collection scanning will now yield more often to reduce lag
 - changed - exportable internal data structures are now tagged with a unique guid to allow for updates when importing instead of creating an entirely new set of objects
 - added - categorisation for some of the korthia items
 - added - profile import/export
 - removed - design export/import
 
# 3.09.51 (21-JUN-2021)
 - fixed - level up issue with itemrack and `equip( )` rule function
 - fixed - (tbc) enabled category 513 trade goods > jewelcrafting
 - fixed - (tbc) enabled category 434 trade goods > gems
 - fixed - ANIMA global is now POWER_TYPE_ANIMA
 - fixed - issue with `itemstat( )` rule function and weapons
 - fixed - issue with the mailbox scan locking up the game when you have a massive amount of emails.  the number of visible emails was increased from 50 to 100 in shadowlands.
 - added - `outfit( )` rule function now supports the GearQuipper addon
 - added - config option advanced > update timers > reagent bank > cleanup delay - allows you to increase the delay if you are getting item is locked errors when running restack set to blizzard
 - updated - mount cross reference data to 9.0.5
 - updated - pet cross reference data to 9.0.5
 
# 3.09.50 (03-JUN-2021)
 - removed - config > custom categories
 - added - config > category sets > custom categories: to allow for management of the items in the custom categories (view, add, remove)
 - changed - junk auto sell no longer auto sells all grey items.  grey items must be in a category with autosell enabled for the junk process to auto sell them now.
 - fixed - issue with the number of availble bank bag slots in burning crusade
 - fixed (maybe) - (classic/tbc) issue with clicking items in the keyring
 - fixed (maybe) - (classic/tbc) quest item borders
 - updated - itemrack 3.66 support for `equip( )` rule function
 
# 3.09.49 (02-MAY-2021)
 - added - config > settings > designs > item > border > alpha - sets an alpha value for item borders
 - added - config > settings > designs > item > border > coloured borders - allows you to colour the border texture (disable if you use an already coloured texture)
 - added - config > settings > designs > item > border > colour - allows you to set the border colour for each slot type (typically for empty slots)
 - changed - toc updated to 90005
 - changed - config > settings > designs > item > empty slot > colour - these colour options now only apply to the empty slot background
 - changed - the default border colour is now the bag border colour - this colour is used when quality border colours are not enabled, and when the item quality is below the quality cutoff value
 - updated - client detection code (burning crusade beta)
 
# 3.09.48 (15-FEB-2020)
 - fixed - cosmetic issue with bfa still displaying in some menus and titles instead of shadowlands
 - fixed - issue with bar name alignment not updating until a uireload (or the bar name was changed)
 - fixed - issue with MailCommander and OpenAllBags
 - changed - category: system > anima and conduits split into their own separate categories
 - added - category: system > covenant for other covenant items (item categorisation is a work in progress)
 - added - config option to center bar name text
 - updated - pt categories for anima items so they are seen as currency
 - removed - bar and item move menu options - use drag and drop instead
 - removed - (as you are now dismounted by the game) if you click on the anima deposit button while mounted an error message will be displayed to remind you that it wont work while mounted
 
# 3.09.47 (07-DEC-2020)
 - fixed - toc issue - missing file
 - changed - category: consumable > anima renamed to anima & conduits, and now picks up conduit items as well

# 3.09.46 (30-NOV-2020)
 - changed - CallBackHandler library updated to 1.0.7
 - disabled - the delete option for junk selling has been disabled due to blizzard protecting the DeleteCursorItem function
 
# 3.09.45 (22-NOV-2020)
 - changed - toc updated to 90002
 - added - category: system > equipment (party loot) - only works in the bag, and when its online
 - added - category: system > equipment (refundable) - only works in the bag, and when its online
 - changed - new items category options moved underneath an override tab along with the new party loot and refundable category options

# 3.09.44 (31-OCT-2020)
 - fixed - issue with arkdewdrop library

# 3.09.43 (23-OCT-2020)
 - fixed - issue with junksell not triggering when you talk to a merchant and the bag window is also not open (eg with auto open disabled)
 - fixed - issue with GetCurrencyListInfo not returning the correct value for isTypeUnused
 - fixed - setbackdrop issue with LibDialog library
 - fixed - issue with gold in your mailbox causing the search to get stuck in an inifinite loop
 
# 3.09.42 (16-OCT-2020)
 - changed - toc file order, added/removed files - do NOT upgrade with the game running
 - fixed - issue with initial tradeskill scan leaving the window open
 - fixed - issue with initial tradeskill scan leaving the sound muted
 - fixed - issue with tinted unusable being active in offline mode when it shouldnt
 - fixed - junk (equipment and known) are now disabled when the location is offline
 - fixed - issue with tooltip item count where an item can be made by different tradeskills
 - fixed - issue with reversed name sorting
 - fixed - issue with backpack currency tokens not showing due to change in GetBackpackCurrencyInfo
 - added - config > settings > designs > bars > style > width - allows you to set default min and max bar width values
 
# 3.09.41 (08-OCT-2020)
 - note - all tradeskill data has been erased.  please login to each character to update its data
 - fixed - issue with tooltips for currencies that are actually reputations
 - fixed - issue with restack topup for the bank
 - fixed - issue with config menu when mounts are not being monitored
 - fixed - issue with backpack currency token display
 - fixed - (classic) backpack currency tokens were getting enabled
 - fixed - issue with LDB objects when their location isnt being monitored
 - fixed - issue with LDB pet object tooltip
 - fixed - issue with LDB pet object OnClick when only one pet was selected or owned
 - fixed - isuse with unusable tint on heirlooms
 - fixed - issue with tooltip item counts when enabling/disabling the monitor state of a location
 - fixed - issue with item links from void storage in chat
 - fixed - issue with dropdown menus closing when they shouldnt
 - fixed - issue with search window not updating
 - fixed - issue with search window query still running after window is closed
 - changed - entries in config > profiles > controls and toggle location are now sorted alphabetically (you can sort them numerically under config > advanced > other > ui if you prefer it the old way)
 - changed - config > general > professions options moved to config > profiles > controls > professions
 - changed - tradeskill monitor state defaulted to disabled
 - added - paragon reward alert message
 - added - tooltip item counts for professions
 - note - will only really work once the professions for that character have been scanned
 - note - an item that can be created by a profession will show the profession name next to the characters that can create it
 - note - a recipe link will show either "Learned" or "Unlearned" next to the characters that have the tradeskill
 - note - theres no recipe to enchant data at the moment, i have to go look all that up at some point
 - added - config > general > junk > soulbound > already known - to disable soulbound already known recipes being categorised as junk
 - added - config > general > junk > soulbound > equipment - to disable soulbound unusable equipment being categorised as junk

# 3.09.40 (xx-xxx-2020)
 - never existed, skipped to allow alpha point versioning

# 3.09.39 (24-SEP-2020)
 - fixed - issue with the mouseover tooltip of another players pet (i may have broken this with all the new code, having issues finding other players with pets out to confirm if its working ok)
 - fixed - tooltip auto reloads should be less intrusive and only apply to toolotips that require an item count to be generated
 - fixed - issue with LDB reputation object generating an error
 - fixed - issue with currency location keybinding
 - fixed - (classic) issue with keybindings for locations that dont exist in classic (you'll get a warning message)
 - fixed - issue with tint unusable
 - fixed - the config option text for monitor and save data have been corrected to no longer state they are per character.  i updated the matching translations but i may have botched them.  feel free to let me know the correct text
 - fixed - issue with battletpet hyperlink not displaying properly in the pet battle upgrade alert
 - fixed - issue with battlepet health value
 - fixed - issue with elite / legendary / trainer battlepet displayed data and on mouseover
 - fixed - issue with SetBuybackItem
 - fixed - issue with SetAuctionSellItem
 - fixed - cater for removal of ExpandCurrencyList
 - changed - toc file order, added/removed files - do NOT upgrade with the game running
 - changed - transmog icons made a bit more visible (i still think they could be better)
 - added - (retail) profession scanning (disabled by default, doesnt do much at the moment, just scans)
 - added - config options for profession scanning - if you enable it there is a fair amount of debug output at the moment
 - added - API funtions as a workaround for AllTheThings to hook them so it can handle the tooltip reloads
 - added - (shadowlands) if you click on the anima deposit button while mounted an error message will be displayed to remind you that it wont work while mounted (i keep forgetting)

# 3.09.38 (16-SEP-2020)
 - fixed (classic) issue with C_CVar
 
# 3.09.37 (16-SEP-2020)
 - fixed - issue with SetLootItem
 - fixed - issue with SetLootCurrency
 - fixed - issue with SetTradeTargetItem
 - fixed - issues with the battlepet custom tootip
 - fixed - issue with pet tooltips when not using the custom tooltip
 - fixed - conflict with battlepet tooltips and BattlePetBreedID for pets with custom names
 - fixed - issue with the colourblind setting not being recognised properly when changed
 - removed - battlepet mouseover tooltip options as they werent really viable (i cant add to the default battlepet tooltip)
 - removed - itemreftooltip onenter debug output
 
# 3.09.36 (15-SEP-2020)
 - fixed - issue with mailbox location keybinding
 - fixed - issue with level 1 menus going off screen
 - fixed - (classic) issue with repuation not updating when you close the repuation window
 - fixed - (classic) issue with client detection code
 - fixed - issue with tooltips (eg achievement, and others) closing at the first refresh
 - fixed - issue with not being able to find an item/spell on certain tooltips
 - fixed - tooltip reload code rebuilt to make it more reliable
 - fixed - issue with SetCurrencyByID
 - fixed - issue with SetBagItem
 - fixed - issue with SetInboxItem (mostly with battlepets)
 - fixed - any open menus are now close when edit mode is toggled
 - fixed - issue where azerite items were categorised as junk if you didnt have the heart equipped
 - fixed - saving/deleting an equipment set in itemrackoptions will now trigger an item cache clear to re-categorise the items
 - fixed - issue with item cache being cleared on some bag updates when it didnt need to be
 - fixed - issue with search window not showing any names when first opened
 - fixed - issue with an empty row at the top of the search list
 - fixed - issue where items were categorised as junk if they had low durability
 - fixed - removed Scrap_Merchant as an optional dependency (it wasnt needed)
 - fixed - issue with ItemRefTooltip not auto refreshing item counts
 - changed - you can now enable auto-sell on system categories (at your own risk)
 - changed - edit mode: item menu updated to allow access to its category options
 - changed - LDB menus (pet, mount, reputation) can now be accessed from their respective windows main menu in the event you dont have an LDB display mod installed
 - changed - the reputation format token *bp* generates an integer (no decimal places).  if you want 1 or 2 decimal places use *bp1* or *bp2
 - note - where an item is a hand-in for more than one reputation only the first match (its semi-random) is displayed.  i'll try to find a way to display all of them but that might mean a very large tooltip
 - changed - LDB currency module now uses a heirarchical menu
 - changed - LDB reputation module now uses a heirarchical menu
 - changed - clicking empty space anywhere inside the window will now close any menus that are open
 - changed - search window is now threaded (will take a bit longer to populate but wont lock up the game)
 - added - backwards support for Battle Pet BreedID mod (until they update)
 - added - backwards support for skinning addons that relied on the "ArkBorder" frame name (i think it will work)
 - added - edit mode: visual feedback when drag and dropping bars
 - added - edit mode: visual feedback when drag and dropping items
 - added - edit mode: with ALT down, dragging a bar and dropping it onto another bar will move all categories on the source bar to the destination bar
 - added - edit mode: with ALT down, dragging an item and dropping it onto another item will assign the (non rule) category of the destination item to the source item
 - updated - internal periodictable data
 
# 3.09.35 (30-AUG-2020)
 - fixed - (classic) issue with LDB module options in the config

# 3.09.34 (30-AUG-2020)
 - fixed - issue with border edge size not refreshing when changed
 - fixed - issue with borders not displaying properly due to incorrect framelevel
 - fixed - cater for more than the current three backpack currency elements (if added by other mods, or blizzard change it)
 - fixed - issue with auto sell not running when the Extended Vendor UI addon was loaded
 - fixed - issue with some of the LDB modules (eg currency) displaying in classic when they shouldnt
 - fixed - LDB module for reputation should now display in classic
 - added - category: consumable > anima
 - changed - equip location sorting has been changed from alphabetical to the slot order on the character pane
 - changed - if using another mod for scrap/junk selling the ai options will be disabled to make it more obvious that they arent being used
 - changed - cater for MAX_CONTAINER_ITEMS being removed as a global
 - changed - (shadowlands) removed achievement requirements for flight in legion and draenor
 - changed - internal code for handling the different client types (retail/classic, ptr/beta)
 - changed - reputation location icon changed to one that works in classic as well
 
# 3.09.33 (30-AUG-2020)* [broken in retail - deleted]

# 3.09.32 (29-AUG-2020)* [broken in classic - deleted]
 
# 3.09.31 (11-AUG-2020)
 - fixed - issue with itemstats rule function
 - fixed - display issues with the rules window
 - fixed - issue with cursor icon being cleared when comparing items
 - fixed - (shadowlands) issue due to changes in C_LossOfControl
 - fixed - (shadowlands) error with currency list tooltips
 - fixed - (shadowlands) issue with backpack watched currency showing nil instead of the icon and amount
 - added - config option to set the width of the rules window
 - added - config option to set the number of rows in the rules window
 - added - support for shadowlands
 - workaround - ignoring flying capability in Shadowlands until flying is actually available there
 
# 3.09.30 (05-AUG-2020)
 - fixed - issue with itemstring rule function
 - added - option to display bar names when in edit mode

# 3.09.29 (28-JUN-2020)
 - changed - the bar category will no longer override other categories/rules
 
# 3.09.28 (03-JUN-2020)
 - fixed - issue with `bonus( )` rule function
 - fixed - issue with dragging bars
 - fixed - issue with soulbound status for guild bank items
 - fixed - (classic) issue with non threaded keyring scanning
 - added - ability to disable the item counts in tooltips for specific items.  accessed via the item menu when in edit mode
 - workaround - possible issue with sortkeys being nil
 
# 3.09.27 (16-MAY-2020)
 - fixed - issue with tradeframe
 - added - option to hide/show connected realm data loaded message
 - added - option to hide/show rules enabled/disabled message
 
# 3.09.26 (14-MAY-2020)
 - changed - auto open/close options
 - fixed - issue with auto close options not mirroring what the default blizzard interface does (eg the bag should not have been closed if it was already opened when you opened the mailbox, then you close the mailbox).  an "always" option has been added if you want to bag to always close.
 - fixed - issues with null battlepet tooltips
 - fixed - issues with pet cages causing constant rescans
 - fixed - if a bag rescan is required then the item cache will be cleared. this should allow the rule and category assignments to update once the new data is available
 - fixed - issue with itemstring rule function
 - fixed - issue with rule tooltips
 
# 3.09.25 (02-MAY-2020)
 - fixed - removed debug output that was accidentally left in

# 3.09.24 (01-MAY-2020)
 - fixed - issue with null tooltips leading to inability to determine an items soulbound status

# 3.09.23 (29-APR-2020)
 - fixed - (classic) hide the deposit all reagents menu option
 - fixed - rule function: tooltip for items in guild bank and mailbox
 - added - in edit mode when you drag an item onto another item while holding down ALT it will assign the destination items category to the item being dragged
 - changed - rule function: transmog will now accept one parameter, if that argument is true then secondaries will also be checked even if you have disabled their display

# 3.09.22 (28-FEB-2020)
 - fixed - issue with search option for corruption only working when suffix was also enabled
 - fixed - issue with bonus id caching
 - added - config option to change the tooltip thread timeout value

# 3.09.21 (15-FEB-2020)
 - fixed - issue with corrupted status icon in classic
 
# 3.09.20 (15-FEB-2020)
 - fixed - issue with corrupted status icon remaining visible

# 3.09.19 (14-FEB-2020)
 - fixed - flagged event WORLD_QUEST_COMPLETED_BY_SPELL as retail only

# 3.09.18 (14-FEB-2020)
 - fixed - issue with rules code that was stopping some results from being cached
 - fixed - issue with quest bang/border display
 - changed - rule caching increased to the slot level (this will suck up more memory)
 - changed - `outfit( )` rule function for outfitter changed to use slot number where possible to cater for azerite traits, falling back to hyperlink
 - changed - the anchor point options for age, ilvl, count, junk, transmog, corruption, and upgrade, can now also select top, bottom, left, right, and center
 - added - azerite item overlay - can be disabled via config > settings > item > status icons / overlays > azerite
 - added - n'zoth corruption item overlay as a status icon - can be disabled/positioned via config > settings > item > status icons / overlays > n'zoth

# 3.09.17 (09-FEB-2020)
 - fixed - issue with item level for timewalking and some other scaling items
 
# 3.09.16 (04-FEB-2020)
 - fixed - issue with upgrade code
 
# 3.09.15 (04-FEB-2020)
 - fixed - issue with sort code
 - changed - config structure rearranged
 
# 3.09.14 (02-FEB-2020)
 - changed - sort order - the ascending/descending option that applied to the sort method as a whole has been removed and each of the sort options now has its own  ascending/descending option
 - changed - sort order - there was always a hidden item count + bag id + slot id sorting tacked onto the end of each sort method. this has been made visible and user configurable (in case you dont want it).  all your existing sort methods have been updated to include them but newly created sort methods will not include these options by default
 - changed - using CHAT_MSG_COMBAT_FACTION_CHANGE instead of UPDATE_FACTION to listen for reputation changes
 - added - black empire corruption text now included in search data
 - fixed - (retail) item counts are now back on auction item tooltips

# 3.09.13 (20-JAN-2020)
 - changed - toc updated to 80300
 - fixed - issue with menu library with dual/large resolution monitors
 - changed - config > settings > design and config > settings > profiles updated to make them a bit easier to use
 - added - truncated bar names will display the full bar name when you mouseover them

# 3.09.12 (16-JAN-2020)
 - fixed - issue with auto bag open from ItemInteractionFrame (corruption removal process from MOTHER)
 - fixed - issue with menu library

# 3.09.11 Alpha 1 (15-JAN-2020)
 - fixed - issues with item suffix handing code
 - changed - `equip( )` rule function will now accept the inventory type codes as well, eg INVTYPE_xxx
 - fixed - bags are no longer seen as equipable items for rules
 - changed - soulbound mounts that you already know are now classified as junk
 - changed - soulbound recipes that you already know are now classified as junk
 - fixed - tsm based rule functions will now also see battlepets and keystones, not just items
 - fixed - item counts on quest required items panel

# 3.09.10 (06-JAN-2020)
 - added - in edit mode you can drag an item onto another item to move its category to the bar that item is in
 - added - in edit mode you can drag a bar id onto an item to move it to that items bar (it will insert it there, not merge it)
 - fixed - removed the ability to drag a bag (in the bag changer window) while in edit mode
 - fixed - issue with config not updating the windows after copying a profile, design, category set, or sort method
 - added - config option for itemlevel text to be coloured the same as the item quality
 - changed - category: system > soulbound is now system > bound as it contains both soulbound and account bound items (that arent in any other category)
 - changed - category: system > equipable items is now system > equipment
 - changed - (classic) enabled the pet and mount categories

# 3.09.09 (25-DEC-2019)
 - added - conflict check for GW2 UI when it replaces the bank frame
 - added - config > miscellanous > item suffixes.  allows you to use item suffix variants in the search and counts, eg Item of the Monkey and Item of the Feverflare can now be seen as discrete items for search and count purposes
 - fixed - issue with bag changer icons not always getting vertically centered
 - fixed - issue with upgrade code
 - added - in edit mode you can drag an item onto a bar id to move its category to that bar

# 3.09.08 (15-DEC-2019)
 - fixed - (classic) issue with keyring scanning

# 3.09.07 (14-DEC-2019)
 - fixed - issue with TSM4 API (tsm rule function)

# 3.09.06 (13-DEC-2019)
 - added - (classic) Keyring
 - fixed - issue with elemental items being assigned to jewelcrafting
 - fixed - issue with TSM4 API (tsmgroup rule function)

# 3.09.05 (18-NOV-2019)
 - fixed - removed debug output for auction scan

# 3.09.04 (15-NOV-2019)
 - changed - junk icon now defaults to being shown
 - changed - if you use Scrap, SellJunk, or ReagentRestocker, junk items are now identified via those, and not via ArkInventory
 - changed - money and item count tooltip options have been separated
 - fixed - (classic) item counts on reagent tooltips from the tradeskill window
 - fixed - (classic) ranged item slot now included in wearing
 - fixed - issue with item counts being displayed even if you disabled them
 - fixed - issue with clicking the OK button on a design import
 - added - mount equipment
 - added - support for 80300 auction house api (you must open the auctions tab for it to scan at the moment)

# 3.09.03 (04-OCT-2019)
 - changed - toc updated to 80205
 - fixed - item categorisation - runecloth (as cloth, not reputation)
 - fixed - item categorisation - tradegoods > cooking
 - fixed - issue with C_Reputation.GetFactionParagonInfo returning nil values
 - changed - switch character menus for account only locations will no longer show the realm name
 - changed - data structure to cater for future multiple account data
 - added - config > accounts. for future use (you can also erase data from here)

# 3.09.02 (21-SEP-2019)
 - added - config > general > professions > priority.  option to ignore your professions for categorisation
 - fixed - error due to null skills table

# 3.09.01 (19-SEP-2019)
 - changed - item categorisation (using internal periodictable sets to move some items to their correct category and make it easier to update longer term)
 - added - config > general > professions > priority.  option to select which primary profession to prioritise the item categorisation for if you have two that overlap (eg if you have mining (first) and blacksmithing (second) and you want the ores/bars under mining you would prioritise mining, if you want them under blacksmithing then you would prioritse blacksmithing).  default is your first profession.
 - fixed - (classic) your professions should now scan properly and categorise items accordingly
 - changed - armor tokens should now categorise as account bound equipable items
 - fixed - (classic) class reagents should now be categorised properly, eg warlock soulshards
 - fixed - issue with bag rescan
 - fixed - issue with wearing data being erased on logout (you will need to login into each character to get it back)

# 3.09.00 (09-SEP-2019)
 - changed - classic and retail code streams merged so it works on both clients.  classic config will need to be setup again (or just copy the savedvaraibles file from the retail client)
 - changed - restack, change character, wearing location, icons to work in classic
 - changed - selecting or deselecting travel form as a mount option no longer requires a reload to become active
 - fixed - errors due to characters from other clients (if you copied the saved variable file)
 - fixed - restack bag ignore options
 - fixed - (classic) transmog issue
 - fixed - (classic) item debug menu
 - fixed - (classic) restack not filling up quivers/ammo bags from full stacks in normal bags (needs more testing)
 - fixed - (classic) issue with guns being INVTYPE_RANGEDRIGHT (which doesnt seem to exist) instead of INVTYPE_RANGED
 - fixed - (classic) cleanup options removed and it will revert to restack
 - fixed - (classic) restack code
 - fixed - (classic) soul bags should now be recognised
 - fixed - categories should all be localised
 - fixed - (classic) item default category assignments should be a bit better
 - fixed - (classic) empty category for quiver and soul bag slots
 - fixed - issue with itemrack
 - note - you will need to log into each character before you can see their offline data again (just login, you dont have to access the bank or other locations)

# 3.08.29 (10-AUG-2019)
 - fixed - issue with right clicking on an empty item slot in the bag location when at the bank and the reagent bank is active
 
# 3.08.28 (15-JUL-2019)
 - fixed - removed the warning when the heart forge [AzeriteEssenceUI] is opened

# 3.08.27 (04-JUL-2019)
 - changed - flying capability for Battle for Azeroth set to Pathfinder Part 2 achievement
 - removed - all water surface mount options
 - fixed - ldb pet/mount config menu option
 
# 3.08.26 (28-JUN-2019)
 - workaround - ignoring flying capability in Nazjatar until flying is actually available there
 - fixed - issue with menu library and 8.2 setpoint
 
# 3.08.25 (26-JUN-2019)
 - changed - toc updated to 80200
 
# 3.08.24 (17-APR-2019)
 - fixed - issue with mailbox scanning not always running when it should
 - fixed - issue with vault info/logs not updating the changer tabs/icons
 - added - right clicking on a crafting item in your bag while at the bank should now put it into the reagent bank (requires at least one free reagent bank slot, it will not work while in combat to avoid taint)
 - added - config options to scale the title, search, changer and status windows (relative to the main window scale)
 - added - config options to hide the currency tokens and the gold amount from the status window
 - updated - mount and battlepet data
 - fixed - issue with some of the previous battlepet data
 - fixed - issues with bar labels
 - added - config option for bar label alignment
 - workaround - added delays to blizzard cleanup code to allow for item locks to be cleared
 - changed - config options: current profile selection moved to general tab
 - changed - config options: merged profiles and settings tabs
 - fixed - initial positioning and visibility of icons in the bag changer window
 - fixed - issue with void storage not updating when items deposited
 - fixed - issue with OpenAllBags/ToggleAllBags hook function not opening the bag when it should if one of the bank or bag override was disabled
 - workaround - issue with bag slot ids 12 and 13 causing errors (they only exist as xml containerframes, not actual bag slots)
 
# 3.08.23 (21-MAR-2019)
 - fixed - issue where item scale might not get applied on first display of a slot
 - fixed - issue where bar frames sometimes dont hide when empty
 - fixed - issue with the jani trash piles when youve turned them into scrapping machines
 - fixed - issue with add to/remove from tracking list text
 - fixed - issue with restack when the reagent bank has not been unlocked
 - fixed - issue with item lock desaturation not always returning to normal when swapping bags/items, or when you open something and it ends up in the same slot
 - fixed - potential issue with the transmog status icon indicator code
 - fixed - issue with bank window shifting between offline to online and not being able to click on the items
 - fixed - issue with config option for window anchor point
 - added - restack (right click) option to prioritise filling up either the reagent bank (default) or profession bags
 - added - support for External Vendor addon (will not use AI Junk Sell when loaded)
 - fixed - issue with selljunk function not always running when it should
 - updated - to cater for the api changes in 8.1.5 (WorldMapTooltip, ItemButton)

# 3.08.22 (21-MAR-2019)
 - skipped - left threads disabled
 
# 3.08.21 (26-JAN-2019)
 - changed - borders for locked slots are now desaturated the same as the icons
 - changed - any system or non purchased bag changer slot (includes vault "tabs") will now have an artifact coloured border (if you have item borders enabled)
 - fixed - the borders for the bag changer slots will now disappear when the item border style is set to None
 - changed - the fade value for the vault changer tabs has been lowered to make it more obvious which tab is current
 - changed - config > controls options moved to profiles to make it more obvious that they are the profile settings
 - fixed - issue with changes made in config > custom categories not updating config > settings > category sets > custom categories
 - fixed - issue with changes made in config > rules not updating config > settings > category sets > rules
 - removed - cleaned/removed old ace profile entries from saved variables file
 - fixed - issue with changing profiles not resetting everything it should have
 - restored - a set amount of non tainted usable item slots for the backpack are pre-built to cater for entering the world when in combat
 - fixed - potential taint issue in the junksell code
 - changed - lowered the yield timer for junksell to speed it up
 - fixed - added extra logic to some of the item frame functions to ensure they dont run unless they are passed an arkinventory frame
 - added - extra api functions for other mods
 - other - CanIMogIt users will need to move or copy Addons\ArkInventory\Plugins\CanIMogIt\arkinventory.lua to Addons\CanIMogIt\Plugins\arkinventory.lua - at least until the CanIMogIt addon has been updated to match the new code

# 3.08.20 (27-DEC-2018)
 - added - caching for ObjectIDCount/ObjectStringDecode functions for better speed performance
 - fixed - issue with inconsistent returns from pet tooltip api
 - fixed - item counts on currency
 
# 3.08.19 (22-DEC-2018)
# 3.08.18 (22-DEC-2018)
 - fixed - issue with Junk Sell where GetContainerItemInfo returns no data

# 3.08.17 (18-DEC-2018)
 - added - option to hide/show quest bang (!) icon
 - added - option to hide/show quest border
 - fixed - issue with splitting stacks in the guild bank
 
# 3.08.16 (14-DEC-2018)
 - changed - toc updated to 80100
 
# 3.08.15 (04-OCT-2018)
 - fixed - issue with custom tooltips that dont have comparison tooltips configured
 - fixed - issue with collections not always updating their respective LDB objects

# 3.08.14 (23-SEP-2018)
 - fixed - issue with comparison tooltips disappearing
 - fixed - issue with collections not getting rescanned when leaving combat
 
# 3.08.13 (15-SEP-2018)
 - fixed - issue with create new custom category menu option in edit mode
 - fixed - issue with floating battlepet tooltip hooking
 - fixed - issue with copying a categoryset
 - fixed - issue with pet level in sort methods
 - fixed - issue with blizzard equipment manager set changes not being recognised

# 3.08.12 (28-AUG-2018)
 - fixed - issue with window randomly refreshing
 - fixed - restored the battlepet opponent details code that was accidentally removed
 - fixed - issue with guild bank modes
 - changed - updated the `tsm( )` and `tsmgroup( )` rule functions to support both TSM3 and TSM4
 - changed - config menus rearranged
 - changed - ability to enable/disable custom categories and rules added back into config
 - changed - auto sell junk is now threaded, should allow for less issues with all items not getting sold
 - changed - updating an outfit in the blizzard equipment amanager should no longer rebuild the window, it will just flag it for a rebuild
 - updated - mount and battlepet data
 - added - main window anchor point now has top, right, bottom, and left, options available
 - added - config options to auto open/close the backpack at the scrapper
 - added - config option to set the junk auto sell thread timer value (default is 100ms)
 - added - system category for crafting reagents
 - added - rule function `bound( )`

# 3.08.11 (13-AUG-2018)
 - fixed - issue with battlepets and the rule tooltip
 - fixed - issue with window layout when all the visible bars in a row have a minimum width set
 - fixed - issue with the upgrade code when there are no profiles at all
 - fixed - issue where tooltip functions were passed a nil and i passed that through instead of blocking it
 - fixed - issue with slot not updating when a different variant of the same item is swapped into it
 - fixed - junk auto sell should now work when TSM is installed
 - fixed - issue with empty counts in the bag changer not updating immediately
 - fixed - issue with guild bank not always updating on open
 - fixed - issue with the non active guild bank tabs being tinted instead of faded (tabs you have no access to remain tinted)
 - fixed - issue with reputation list tooltips not showing
 - fixed - disabled the ability to make changes to the [9999] system default categoryset
 - updated - localisation text
 - changed - restricted SetHyperlink based refreshes to just objects that item counts go on.  should minimise the impact to other mods that use GameTooltip:SetHyperlink for other things
 - changed - config first page is now tabbed to give more space to the options
 - removed - some config options from the custom category and rules tabs to minimize confusion (you can still get at them via the bar menu in edit mode, where they make more sense)
 - added - rule function `itemstat( )`
 
# 3.08.10 (07-AUG-2018)
 - fixed - added a [1000] default profile so that people dont use the [9999] system default profile (which gets cleared every reload)
 - fixed - removed the ability to select the [9999] profile for active use, anyone using [9999] will be changed to [1000].  you will need to re-apply the location control options to that profile

# 3.08.09 (07-AUG-2018)
 - changed - restack will now take items from the bank (including profession bags) to topup the reagent bank as well as moving stacks into any empty reagent bank slots (not configurable yet)
 - fixed - issue with the restack code
 - fixed - multiple issues with the tooltip code
 - fixed - issue with guild bank not updating when changing tabs

# 3.08.08 (05-AUG-2018)
 - changed - LDB reputation menu layout
 - changed - hooks and onupdate for item counts in tooltips
 - changed - window open loading (initial open after upgrade may shift location)
 - changed - item and bar anchoring to reduce tearing during rebuild
 - changed - mailbox and merchant hooks to remove potential conflicts with other mods
 - fixed - subframe anchoring and alignment
 - fixed - border offset default values (due to the subframe anchoring issue)
 - fixed - layout issues with list view
 - fixed - issue with scanning tooltips
 - fixed - issue with embedded tooltip tooltips (eg the worldmap quest ones). they cant be scaled as the border doesnt notice the scaling
 - fixed - issue with default data cleanup
 
# 3.08.07 (30-JUL-2018)
 - fixed - issue with default profile getting cleared
 
# 3.08.06 (29-JUL-2018)
 - changed - transmog options moved to global and added some extra options
 - fixed - issue with the defaults not getting cleared properly
 - fixed - issue with blueprint options displaying blank when set to a deleted categoryset/design (will show default now)
 - fixed - issue with bar layout when title frame was hidden
 - fixed - issue with leftover code for pre-loading item frames at load time
 - fixed - issue with constant for item frame size
 - changed - updated the `tsm( )` and `tsmgroup( )` rule functions to support TSM4
 - changed - during a refresh/rebuild the bars and items should completely hide, then re-appear as a whole.  no strobing, no jumping around

# 3.08.05 (25-JUL-2018)
 - note - all reputation data has been erased.  please login to each character to update its data
 - fixed - issue with itemlevel anchor point
 - fixed - issue with tooltip scanning not ignoring the embedded items in recipes
 - fixed - the bars and items should no longer "strobe" as much during a refresh/rebuild (into and out of edit mode is still messy)
 - fixed - issue with list view
 - fixed - issue with reputation scanning
 - fixed - mythic keystones should show up in searches again
 - fixed - issue when changing tooltip options causing the item counts to no longer display
 - fixed - issue with `location( )` rule function
 - changed - misc and consumable (other) pet items should get categorised a bit better
 - updated - reputation ldb object, you can now select which reputation to watch, which ones to see in the tooltip, and how to format the text
 - added - config options for the ldb reputation object
 - added - config options for the tooltip reputation text
 - added - reputation tooltips now show rep levels for other characters
 - added - cross ref links between legion rep items and their faction (so the item count tooltip for a rep token will show the rep levels attained for that faction)
 - added - rule function `transmog( )`

# 3.08.03 (20-JUL-2018)
 - fixed - issue with tsm rule function

# 3.08.02 (20-JUL-2018)
 - changed - junk auto sell should no longer try to sell to vendors that dont have a buyback slot and dont sell any items
 - fixed - item category code to better handle tooltips that arent ready
 - fixed - issue with reputation LDB object and header rep entries
 - fixed - corrected for new mythic keystone itemstring format (level should now be correct, instance and affix ids are unknown at this point)
 
# 3.08.01 (18-JUL-2018)
 - changed - status icons (junk, upgrade, transmog) moved to their own sub menu
 - changed - location rule to use internal numeric value
 - fixed - attempting to summon a mount while pacified should now generate a warning
 - fixed - border offset default values

# 3.08.00 r727-alpha (12-JUL-2018)
 - fixed - transmog status icons should work properly now
 - added - expansion id as a sort option

# 3.08.00 r726-alpha (08-JUL-2018)
 - fixed - issue with some of the system defaults not getting updated when i change them
 - fixed - issue with toybox scanning
 - changed - config > general menu is now more in line with the rest of the config
 - changed - config > settings > design menu is now more in line with the rest of the config
 - added - junk icon for items that are tagged as "junk" for autosell purposes
 - added - transmog icon for items you have not learnt the appearance of yet
 - added - config options for transmog icon
 - added - rule function `expansion( )`

# 3.08.00 r725-alpha (07-JUL-2018)
 - changed - default text for all LDB objects changed to "Loading..."
 - changed - config options for the item count and item level text
 - fixed - issue with LDB mount object
 - added - config options for the upgrade and junk icons
 - fixed - issue with quest event

# 3.08.00 r723-alpha (05-JUL-2018)
 - fixed - item counts should now get added to non updating tooltips
 - fixed - item counts should no longer show location counts when the item is only in one location
 - fixed - item counts should no longer remove and re-add when the count changes, it should just update

# 3.08.00 r722-alpha (28-JUN-2018)
 - fixed - issue with bar labels not aligning properly
 - fixed - pet scanning
 - changed - lowered thread timer minimum values to 25ms
 - updated - LibDialog to 1.8

# 3.08.00 r721-alpha (11-JUN-2018)
 - fixed - paragon levels were displaying one level higher than they really were
 - fixed - issue with added tooltip text when not class coloured
 - fixed - issue with search window
 - changed - searching in a window will now hide the items instead of fading them.  should make it easier to see the results
 - changed - searching in a list view will now compact the list
 - changed - window, bar, and item, padding limits changed to 0 and 50
 - fixed - issue with window layout calculation from padding values

# 3.08.00 r720-alpha (06-JUN-2018)
 - fixed - issue with coin icon missing for assigned categories set to auto-sell
 - fixed - issue with item level being incorrect for languages with a ' in the item level tooltip text and the item has bonus ids
 - fixed - toybox tooltips
 - changed - item counts on tooltips are now processed in the background to minimise lag (there will always be some but it shouldnt be as bad as it was)
 - added - list view (not finished)
 - added - repuation window
 - added - repitation object (not finished)
 - changed - collection scanning code rebuilt
 - changed - tooltip item count code rebuilt
 - changed - item count code rebuilt
 - removed - restriction for running on live servers
 
# 3.08.00 r719-alpha (22-MAY-2018)
 - fixed - issue with currency tooltips
 - fixed - issue with item counts not always updating on tooltips
 - changed - calculate item counts as the items are scanned to reduce mouseover lag (hopefully)
 - changed - general code cleanup

# 3.08.00 r718-alpha (18-MAY-2018)
 - fixed - issue with item count clear code
 - changed - inital lag spike on entering world transferred to first window open
 - fixed - issue with export code
 - workaround - issue with border texture getting mangled when the window is opened after the initial load (appears to be a blizzard issue)
 - changed - general code cleanup
 - note - there may be random debug output still active
 
# 3.08.00 r717-alpha (25-APR-2018)
 - changed - toc updated to 80000
 - fixed - minor issues for BFA
 - fixed - should error and disable if run on the live servers
 - changed - pet and mount LDB objects now have a static icon

# 3.07.43 (05-APR-2018)
 - fixed - mount summon logic
 - changed - window search frame - will now search against tooltip, equip location, item type, item subtype, and quality
 - changed - window search frame - single and double quotes are ignored (in both filter and search text)
 - changed - window search frame - plain text searching enabled - regex patterns will no longer work
 - added - support for tooltips from other mods that are linked via metatables to the gametooltip
 - changed - search window - should be quicker now due to caching (at the expense of memory usage)
 - changed - search window - plain text searching enabled - regex patterns will no longer work
 - changed - search window - can be replaced with custom search mods
 - changed - bag location name changed to backpack
 - fixed - merchant currencies should show item counts (again)
 - fixed - issue with clearing item glow on bag close
 
# 3.07.42 (07-MAR-2018)
 - fixed - issue with itemlinks getting added twice
 - fixed - issue where clicking on an item in the bag/bank did nothing until after the window was refreshed for the first time
 
# 3.07.41 (06-MAR-2018)
 - added - config > general > new item glow > clear - option to clear the new item glow from all items when the window is closed
 - fixed - issue with initial font height
 - fixed - issue with config option for search font height
 - fixed - issue with frames being called by other addons before they were created
 - added - more config options for stack limit.  note: the identification option is extremely CPU intensive on the first load
 - fixed - issue with pet scanning
 - fixed - toybox scanning code updated to include new expansion filter
 - fixed - issue with selected mounts not being deselected after you change their type
 - fixed - opposite faction mounts should no longer show in the selection menu
 - fixed - issue where unaligned pandaren were seeing the alliance only mounts when they shouldnt
 - fixed - mounts you couldnt actually use were being included in the list of usable mounts (both mount.usable and spell.usable are now being checked)
 - fixed - the use all for flying/surface mounts should now work properly and add your flying/surface mounts to your land mounts
 - changed - mount selection code no longer uses the map
 - changed - selecting use all (the old random) for mounts/pets will no longer clear your selections, its just overrides them when its enabled
 - changed - use all has been set as enabled, you'll need to disable it to revert to your specific selections
 - workaround - for flying issues with characters that never purchased the continent flying spells that were removed in 7.3.5 (affects kalimdor, eastern kingdoms, and northrend)
 - changed - pet/mount use all can be random or sequential.  its always sequential when there are three or less usable pets/mounts
 - added - config > companions > mounts > random - to allow for random/sequential selection
 - added - config > companions > pets > random - to allow for random/sequential selection

# 3.07.40 (28-JAN-2018)
 - changed - collection scanning code
 
# 3.07.39 (21-JAN-2018)
 - changed - removed checks for continent flight spells for azeroth, northrend and pandaria due to blizzard removing those requirements

# 3.07.38 (17-JAN-2018)
 - changed - pet journal will get scanned when locked by another user on the same account (should help with missing pet icons)

# 3.07.37 (29-NOV-2017)
 - fixed - issue with ilvl sorting (was only catering for 3 digits)
 
# 3.07.36 (30-OCT-2017)
 - changed - (druid) if "use travel form" is selected as a mount then cat form will now be used when indoors
 - changed - mount action will now dismount you if you are in combat, mounted, and not flying (you used to have to attack/heal something to dismount)
 - updated - companion item/critter data to 7.3.0
 - added - bar menu option to set a minimum width (this might be a bit flaky, and will ignore window width if you set it for all the bars in that row)
 - added - bar menu option to set a maximum width
 - fixed - restack code to handle potentially invalid returns from the blizzard api - `GetItemFamily( )`
 - fixed - issue with removing a bag from a slot
 - fixed - issue with emptying a bags contents (it no longer yields so may hit the script timer)
 - changed - window drawing should be better.  the initial window draw should be a lot better
 - fixed - toybox scanning
 - fixed - erasing account data (pets, toys, mounts, heirlooms) will now cause an immediate rescan like it does for other player locations
 
# 3.07.35 (30-AUG-2017)
 - changed - toc updated to 70300

# 3.07.34 (30-AUG-2017)
 - fixed - calls to `PlaySound( )`

# 3.07.33 (07-AUG-2017)
 - added - error prevention logic to mount, pet, and toy, collection scan code to handle potentially invalid returns from the blizzard api
 - fixed - issue with refreshing windows that arent visible

# 3.07.32 (01-AUG-2017)
 - fixed - queue for rescan message will no longer print out when set to disabled
 - fixed - removed a pet debug output that always displayed
 - added - error prevention logic to sort key generation code to handle potentially invalid returns from the blizzard api

# 3.07.31 (09-JUL-2017)
 - removed - config options for in-combat yielding
 - added - config options for thread timeout values (defaults to 100ms for in-combat and 100ms for out-of-combat)
 - changed - bag, pet, mount, toybox, heirloom, mailbox, auction, void storage, and vault scans are now threaded
 - changed - window drawing is now threaded all the time (not just in combat) - initial window draw can be a bit laggy
 - changed - restack should be a bit slower but leave the game more responsive (depends on what you set the out of combat thread timeout to)
 - fixed - issue where pet scanning might sometimes not run
 - fixed - bag rescans will now just rescan the bag having an issue, not all the bags in that location
 - fixed - issue with search filter initilisation causing a second window rebuild at the first open
 - fixed - issue with font size on initial window load

# 3.07.30 (25-JUN-2017)
 - fixed - issue with some tooltip text containing a UTF-8 non breaking space sequence (its not the same as a normal space character so doesnt match)
 - fixed - issue with artifact power items not being categorised properly for non-english languages
 - fixed - issue with ancient mana items not being categorised properly
 - fixed - issue with artifact power and ancient mana amounts not displaying for non-english languages (the amount should show up but still requires translation of some suffixes)
 - note - some languages (RU) do not have the text "Ancient Mana" in the toltip for Ancient Mana items so the values cannot be extracted at this time
 - note - some languages (KR, CN, TW) have different structures so the values cannot be extracted at this time
 
# 3.07.29 (22-JUN-2017)
 - added - artifact power and ancient mana items will now display their values in the ilvl field (if item level is displayed)
 - changed - disabled ldb update code after zoning, its not really needed and seems to be causing "script ran too long" errors while out of combat
 - added - maximum quality option for auto sell
 - fixed - bar and item category menus now use the same structure and colouring scheme
 - reverted - you can click on a category name to assign it to a bar again (if its already assigned it will remove it)
 - added - bar/item menu option to set auto sell flag for an individual category, option is per categoryset
 - added - config option for testing auto sell mode (this is enabled by default, if you currently have auto sell enabled it will display a warning and wont sell anything until you disable this)

# 3.07.28 (17-JUN-2017)
 - fixed - display issue with backpack currency icons in status section

# 3.07.27 (08-MAY-2017)
 - changed - cooldown event handling should use less cpu
 - changed - code that stores the item name (the search frame had too many items with no name)
 - fixed - item counts for some auction house items was not working (due to invalid item links in the tooltip)
 - changed - unuseable item tint changed to allow for cooldown issue

# 3.07.26 (18-APR-2017)
 - fixed - mythic keystones should now have an icon (had to temporarily hardcode it in)
 - changed - mythic keystone level value replaces the ilvl value
 - added - category for system > mythic keystone
 - changed - artifact relic +item levels value replaces the ilvl value
 - fixed - updated rules to use new C_EquipmentSet code for blizzard equipment manager
 - changed - LDB currency and item tracking counts now use thousands seperators
 - added - option to set the base item size (before scaling) under config > settings > styles / layouts > (id) > items > style > items
 
# 3.07.25 (29-MAR-2017)
 - changed - toc updated to 70200
 - added - keystone object class to stop error message (still needs work to integrate fully)
 
# 3.07.24 (24-MAR-2017)
 - fixed - issue with sell junk limit option being inverted (it still has issues selling large numbers of items)
 - added - option to disable showing the upgrade arrow under config > settings > styles / layouts > (id) > items > style > items (disabling shouldnt impact other mods, like pawn, that use it)
 - fixed - mount issue when reaching level 20 and not purchasing a riding skill locks out all mounts including the chauffered ones that youve been using up to level 20
 - fixed - illidari felstalker changed from flying to land mount
 - changed - extended rule id (exrid) results are now cached, this increases memory use but lowers cpu
 - added - edit mode menu options for custom bar border colours
 - changed - edit mode menu for category assignment to a bar changed so that assign is now a menu choice (to make it clear that you have to click on it to assign it, previously you had to click on the category name which wasnt as obvious)
 - fixed - (maybe) issue with `outfit( )` rule and blizzard equipment manager

# 3.07.23 (05-FEB-2017)
 - changed - internal rule id now includes all gem, enchant, suffix and bonusid data to be able to see the different variations (note: does not apply to categories)
 - fixed - issue with debug and displaying which PT sets an item is in
 - added - the green upgrade icon should display when blizzard think the item is an upgrade for you (note, the API is currently returning false for all items so its not actually going to show anything at this point but may later)
 - changed - the green upgrade icon has been moved to the bottom left so as to not overlap the item level text
 - fixed - issue with tooltip rule where it couldnt match against the green <Right click to ...> last line text
 
# 3.07.22 (18-JAN-2017)
 - added - option to disable rule 3rd party mod load messages
 - added - option to disable rule registration messages
 - fixed - (maybe) issue with `outfit( )` rule and blizzard equipment manager

# 3.07.21 (18-JAN-2017)
 - changed - soulbound toys that you already know are now classified as trash
 - fixed - issue with `outfit( )` rule and blizzard equipment manager with items in your bank

# 3.07.20 (03-JAN-2017)
 - added - rule function `tsm( )` allows for regex matching on tsm group names
 - fixed - issue with `outfit( )` rule and blizzard equipment manager after changing specs
 - updated - repointed all urls in .pkgmeta to new curseforge location
 
# 3.07.19 (11-NOV-2016)
 - changed - default itemtype/subtype returns changed from 0/0 to -2/0 so that they dont conflict with consumable/explosives (which is 0/0)
 - changed - items ending up with default itemtype/subtype values will be assigned to the2 system > unknown category (it should only be temporary until the game returns the correct information)
 - changed - items in the system > unknown category are no longer cached and should update to their correct category (and get cached) once the game returns the correct information
 - added - option to disable warning for unknown bag type rescans
 
# 3.07.18 (28-OCT-2016)
 - fixed - issue with default font size not applying for some objects (rule column headers, guild bank money and info logs)
 - fixed - issue with tackle container slots not being recognised properly
 
 3.07.17 (26-OCT-2016)
 - changed - toc updated to 70100
 - workaround - issue with increased item level due to GetItemInfo returning a slightly different hyperlink than the one passed in (only seems to impact artifacts).  presumably blizzard will fix it at some point

# 3.07.16 (21-OCT-2016)
 - fixed - issue with regex matching against some of the globalstrings that contain special regex characters
 - fixed - issue with sorting by id as id was not a zero padded in the string
 - fixed - issue where the window would recalculate whenever leaving combat

# 3.07.15 (02-OCT-2016)
 - fixed - rule function: itemstring
 
# 3.07.14 (01-OCT-2016)
 - fixed - issue with sell junk notification not always displaying
 - fixed - issue with sort category equip location
 - fixed - issue with artifact power items not getting categorised properly when colorblind mode is enabled
 - removed - rule function: `id( )`
 - added - rule function: `itemstring( )`
 - added - sorting: slot type
 - fixed - restack function should no longer be able to stall, should also not lock up the game while it does it

# 3.07.13 (26-SEP-2016)
 - fixed - removed debug output
 
# 3.07.12 (26-SEP-2016)
 - changed - co-routine code rewritten to remove the possibility of item updates in between a yield/resume being ignored (redraws may now take longer to complete under some circumstances)
 - changed - bag rescan timer for zero slot bug lowered from 10 to 2 seconds
 - fixed - objectstringdecode function to handle new itemstring format
 - fixed - issue with restack code and positioning of profession bags
 - changed - sell junk also displays number of items destroyed (if any)

# 3.07.11 (24-SEP-2016)
 - fixed - item counts restored for currency and spell (mount) objects
 - fixed - typo in objectstringdecode function for bonusids3
 - fixed (maybe) - issue with artifact power items in zhCN locale
 - updated - mount data

# 3.07.10 (23-SEP-2016)
 - fixed - issue with inconsistent hyperlinks causing an error

# 3.07.09 (23-SEP-2016)
 - fixed - issue with `type( )` rule function
 - workaround - issue with i being nil when getting an items assigned category. still need to work out the cause
 - fixed - item counts should only be added to tooltips for items

# 3.07.08 (22-SEP-2016)
 - note - all item data has been erased.  please login to each character to update its data
 - changed - items that end up assigned to the default category now have that assignment cached to speed up display.
 - changed - rules should use slightly less cpu.  should be more noticable if you have a lot of rules
 - changed - starlight rosedust should now have a default category of system > quest
 - fixed - creeping carpet set to ground mount
 - fixed - errors inside coroutines should now display (the ones where the bag window is usually just black, or partially built)
 - added - rule variables. rules can now access most of the item information directly via the i, osd and info variables (see wiki for details)
 - changed - sell junk function now only sells items assigned to the system > junk category.  if you have a grey item you dont want sold just assign it to another category.  if you have non grey items you want auto sold then assign them to the system > junk category.  deletion of non sellable greens (or higher) will still prompt for confirmation
 - fixed - issue with item counts not getting added to some types of links (mostly the tradeskill ones)

# 3.07.07 (11-SEP-2016)
 - added - artifact relics should now show their item level (if enabled)
 - added - category for consumable > artifact power (to be able split up relics and power)
 - changed - artifact power items should now have a default category of consumable > artifact power
 - changed - ancient mana items should now have a default category of system > currency
 - fixed - items being incorrectly assigned to the equipable items category (the equip location value for some items is nil and not an empty string which it has been up until now)
 - fixed - toybox items were getting incorrectly flagged as being unusable (if you had that enabled)
 - fixed - toybox item cooldowns should now display
 - fixed - issue with changing search options in config when the search module is not loaded
 - changed - ldb tooltip for currencies now includes the total and weekly maximums

# 3.07.06 (03-SEP-2016)
 - changed - translations for mining and herbalism will try to get data from spells instead of items (to hopefully get them to work more reliably)
 - fixed - issue with recipes/patterns being flagged as soulbound when they arent due to the item they create being soulbound
 - changed - artifact power and artifact relic items should now be categorised under system > artifact relic
 - fixed - issue with bar names that were too long getting wrapped instead of shortened (and ending up underneath the item)
 - fixed - equipping a new bag in an empty bag slot will now update the window correctly
 - fixed - issue with toybox source filter

# 3.07.05 (20-AUG-2016)
 - fixed - issue with item age being reset on login due to tooltip data not being ready
 - fixed - issue with item age being nil causing the bank to fail

# 3.07.04 (15-AUG-2016)
 - fixed - issue with ToggleAllBags and OpenAllBags code (when not overriding the bank and bags)
 - fixed - issue with re-hooking when ai is disabled and then enabled within the same game session
 - fixed - issue with re-hooking the bank when changing the override option
 - changed - new item glow changed to cover the entire item and is user configurable via config > general > new item glow
 - fixed - issue with 30230 upgrade code
 
# 3.07.03 (13-AUG-2016)
 - fixed - issue with error message about "you should never have got here" displaying incorrectly
 - fixed - upgrade code
 - fixed - issue with chatlinked items doubling up (in bag and bank)
 - fixed - issue with moving items around in the guild bank
 - fixed (maybe) - issue with mailbox/vendor not opening
 - added - categories and rules can be enabled/disabled in the config window

# 3.07.02 (10-AUG-2016)
 - fixed - issue with 30260 upgrade code
 - fixed - issue with copying category sets
 
# 3.07.01 (10-AUG-2016)
# 3.07.00 (08-AUG-2016) BETA 8
 - fixed - issue with 30271 upgrade code
 - fixed - issue with config (profiles)
 - fixed - issue with chatlinked items doubling up
 - fixed - issue with void storage not getting scanned
 - removed - debug output of favourite toy ids

# 3.07.00 (07-AUG-2016) BETA 7
 - fixed - issue with 30230 upgrade code
 - added - heirlooms window (view only)
 - fixed - issue with tooltips in account location windows

# 3.07.00 (03-AUG-2016) BETA 6
 - changed - removed redundant refresh actions in the vault update code
 - fixed - removed toybox debug output

# 3.07.00 (01-AUG-2016) BETA 5
 - fixed - issue with online tooltip for the mailbox not showing
 - fixed - issue with offline tooltip for gold amounts in mailbox
 - workaround - issue with mailbox being slow due to having to rescan the whole thing every time, default update timer is now 2 seconds (changeable in config)
 - fixed - issue with config > rules being blank
 - fixed - issue with upgrade code introduced in beta 4

# 3.07.00 (31-JUL-2016) BETA 4
 - fixed - issue with profiles not applying when opening a non player window (guild bank/account)
 - fixed - upgrade code missed bag to bar assignments which ended up causing a black window on open
 - fixed - codex issue causing the default profile to be used in some cases
 - fixed - issue copying a layout/style/catset and the current window not updating
 - fixed - issue where items would sometimes be picked up when in edit mode (mostly at the bank/vault)
 - fixed - issue where vault was refreshing on each change
 - fixed - issue with toybox scanning

# 3.07.00 (28-JUL-2016) BETA 3
 - added - when the title frame is hidden a smaller set of action icons is displayed in the container frame
 - fixed - issue with style/layout/category set not getting applied immediately when you change it in a profile
 - fixed - issue with vault window sometimes opening with the players data (ERR and empty) instead of guild data
 - fixed - issue with an internal item id format causing item counts to be wonky
 
# 3.07.00 (27-JUL-2016) BETA 2
 - fixed - issue with gold amounts displayed in tooltips when in colourblind mode

# 3.07.00 (26-JUL-2016) BETA 1
 - added - profiles
 - recover - where possible previous profile data will be recovered, if it cant be done you just need to set the controls for the profile

# 3.06.17 (24-JUL-2016)
 - fixed - issue with pet filters

# 3.06.16 (23-JUL-2016)
 - fixed - issue with deleted rules still showing in the list
 - fixed - issue with copying category sets
 - changed - Settings > Design changed to Settings > Styles / Layouts to make it more obvious where they are

# 3.06.15 (22-JUL-2016)
 - added - default [1000] editable profile for all locations (this should let you use it from scratch without the need to create anything first)
 - fixed - issue with tooltip positioning whe using CVAR:alwaysCompareItems
 - added - right click menu option from refresh icon to reset the cached category data (needs to be used after TSM users update their groups)

# 3.06.14 (21-JUL-2016)
 - fixed - issue with items manually assigned to a system category not getting placed in the correct bar

# 3.06.13 (21-JUL-2016)
 - fixed - issue with data conversion due to the last change, if you have a backup from 30512 and your new setup is wrong please restore it and login again
 - fixed - issue with ldb bag count text
 - fixed - issue with deleted categories still being assigned to a bar
 - fixed - issue with upgrade code for older versions
 - changed - BreakUpLargeNumbers replaced with FormatLargeNumber
 - fixed - issue with item categorisation

# 3.06.12 (21-JUL-2016)
 - changed - edit mode should expand the window more sideways and less downwards
 - fixed - issue with data conversion, if you have a backup from 30512 please restore it and login again
 
# 3.06.11 (20-JUL-2016)
 - fixed - issue with custom category item assignments not getting converted properly
 
# 3.06.10 (20-JUL-2016)
 - fixed - cleared translation errors in DE/FR/RU/TW

# 3.06.09 (20-JUL-2016)
 - fixed - issue with windows not always updating when blueprint settings changed
 - fixed - serializer issue

# 3.06.08 (20-JUL-2016)
 - fixed - issue with servers without any cross realm servers

# 3.06.07 (20-JUL-2016)
 - fixed - issue with servers without any cross realm servers
 - fixed - issue with warning about duplicate realm data
 - fixed - issue with window not sorting on open (or instantly)
 - fixed - issue with outfitter failure causing rules to not enable
 - fixed - issue with accessing config menu from blizzard interface
 
# 3.06.06 (19-JUL-2016)
 - fixed - issue with serializer library on beta clients
 - fixed - issue with blizzard bank frame still opening when overridden
 
# 3.06.05 (18-JUL-2016) BETA
 - changed - rule function tsmgroup moved back to main rules addon
 - fixed - issues with dependencies on internal blizzard addons
 
# 3.06.04 (16-JUL-2016) BETA
 - WARNING - you need to copy over your arkinventory savedvariables file from the live game client again to the ptr client as some of the data cannot be upgraded.  if you cannot do this then some settings will be reset back to default
 - added - config > settings > designs > export
 - added - config > settings > designs > import
 - note - import/export is currently limited to just design options (layout and style).  any non system sort methods or categories or rules used by the design are not exported at this time
 - added - rule function `bonus( )` - checks for any/specific bonus ids an item has
 - added - debug item data displays source and bonus ids
 - added - option to disable monitoring of updates for pets, mounts and toys
 - added - right clicking on an item in the mailbox window while at the mailbox will retrieve that item
 - added - gold amount in mails now show up as an item (and are lootable)
 - fixed - issue with renaming designs
 - fixed - issue with rule functions vendorpriceover and vendorpriceunder
 - fixed - new items time display will now display for all locations, not just the bag
 - fixed - issue with battlepet item counts caused by previous change of internal item id
 - fixed - issue with the offline vault handling shift clicks (stack split menu opened when it shouldnt)
 - added - deleted category sets can be restored/purged
 - added - category sets can be copied
 - changed - rule data moved from profile to category sets
 - changed - rules are enabled/disabled when in edit mode from the bar menu
 - changed - custom category data moved from profile to category sets
 - added - custom categories are enabled/disabled when in edit mode from the bar menu
 - added - in edit mode you can drag a bar id to another bar id to move it there (it will insert it there, not merge it)
 - added - bar menu action for setting a custom name colour (specific to each bar)
 - added - bar menu action for setting a custom background colour (specific to each bar)
 - added - bar menu action for setting a custom border colour (specific to each bar)
 - changed - bar name height option replaced with bar name font size option
 - changed - edit mode no longer turns everything red (so you can see your custom colours when setting them)
 - changed - item counts now use thousands seperators
 - fixed - issue with moving a bar upwards, would not move the underlying bar options with it
 - changed - viewing another characters data will now use their settings
 - changed - font has been moved to global, unable to transfer setting, please set it again
 - changed - outfit rule function always returns false when used in an offline location
 - added - font size of title frame text can be set (title frame adjusts height to fit)
 - changed - title bar action buttons set to a single row
 - added - font size of search frame text can be set (search frame adjusts height to fit)
 - added - font size of status frame text can be set (status frame adjusts height to fit)
 - added - if you rename your character its previous data will transfer over to the new name (must have logged in at least once using 3.04.06 or higher with the old name before it will work)
 - added - category: "system > artifact relic" and "consumable > vantus rune"
 - changed - category: "tradegoods > devices" and "tradegoods > explosives" merged to "consumable > explosives and devices"
 - changed - category: "consumable > item enhancement" moved to "system > item enhancement"
 - changed - category: "tradegoods > enchantment" merged to "system > item enhancement"
 - removed - category: "consumable > scroll"
 - changed - connected realms should always work for the current realm as the information is pulled from the game now.  it might be out of date for other realms
 - changed - rule function `type( )` now also takes the numeric itemclass values
 - changed - rule function `subtype( )` now also takes the numeric itemsubclass values
 - added - ability to set the font size of the dropdown menus
 - added - ability to set the font size and colour of the item level text
 - added - ability to set the font size and colour of the item count text
 - added - ability to set the font size and colour of the item age text
 
# 3.06.03 (30-JUN-2016) BETA
 - added - config > general > junk items - options for auto selling junk quality items when you visit a merchant (will not run if you have Scrap or SellJunk mods loaded)
 - fixed - an inconsistency with the restack menu and config choices
 - fixed - issue with opening custom category config from item in edit mode
 - fixed - issue with opening sort methods config from bars in edit mode
 
# 3.06.02 (27-JUN-2016) BETA
 - changed - tooltip counts: when all items are from a single location only the name is listed (not the duplicate item count)
 - removed - config > controls > location > reposition on load
 - removed - config > controls > location > reposition now
 - added - config > display > reposition on show (defaults to enabled) - any windows partially off screen are repositioned back on screen when opened, if its still too big to fit it will remain partially off screen (set the window height to enable the scrollbar to make it fit)
 - removed - config > show hidden items - right click on refresh button instead
 - removed - main icon > right click > show hidden - right click on refresh button instead
 - removed - config > settings > window > sorting > on window open
 - removed - config > settings > window > sorting > instant
 - added - config > display > refresh sorting (defaults to manual) - this is now global and replaces/combines the two above options
 - added - deleted sort methods can be restored/purged
 - added - sort methods can be copied
 - added - deleted custom categories can be restored/purged
 - changed - most profile based settings have been moved to global based "design".  designs are made up of style and layout options that be assigned seperately to a window to determine how its built
 - added - deleted designs can be restored/purged
 - added - designs can be copied
 - moved - config > settings has been moved to config > settings > designs
 - moved - config > auto open/close has been moved to config > settings > auto open/close
 - moved - config > sorting has been moved to config > settings > sort methods
 - moved - config > categories has been moved to config > settings > custom categories
 - fixed - issue with tooltips not adding item counts when hovering over currencies at merchants
 
# 3.06.01 (18-JUN-2016) BETA
 - fixed - arkdewdrop lib on curse

# 3.06.00 (17-JUN-2016) BETA
 - fixed - issue with restack code and unpurchased bag slots
 - fixed - gold amount in tooltip formatted with thousands seperator
 - fixed - issue with item counts sometimes not updating
 - added - rule function: itemfamily | family
 - added - item family value to debug menu for bag slots
 - added - option to use druid travel forms instead of mounts (warning, the dismount in flight option is not useable with travel form, you will always cancel travel form by pressing the summon mount keybind, if youre in flight form just press it again before you hit the ground and you'll be fine.)
 - changed - search window moved to its own load on demand module
 - changed - toc updated to 70000 (legion compatible)

# 3.05.12 (23-NOV-2015)
 - fixed - issue with aborting a restack when leaving bank/vault
 - fixed - issue with item counts on merchant cost itemstring
 - added - workaround/fix for issue with item counts on tradeskill results and reagents due to invalid hyperlink returned by blizzard
 
# 3.05.11 (21-JUL-2015)
 - updated - draenor flying capability

# 3.05.10 (13-JUL-2015)
 - fixed - issue with tint unusable overlay
 - fixed - issue with battlepet tooltips at the auction house
 
# 3.05.09 (09-JUL-2015)
 - fixed - issue with /ai track
 - removed - references to LibItemUpgradeInfo-1.0

# 3.05.08 (08-JUL-2015)
 - fixed - issue with inserting bars

# 3.05.07 (05-JUL-2015)
 - fixed - empty item slot background issue
 - added - option to set empty item slot (solid colour) background alpha level

# 3.05.06 (04-JUL-2015)
 - note - all item data has been erased (to cater for the new itemstring format).  please login to each character to update its data
 - fixed - bar background colour should now apply correctly
 - fixed - window background should now update properly when changing between a texture and a solid colour

# 3.05.05 (02-JUL-2015)
 - changed - code adjusted for new itemstring format (specialisation id), no actual impact
 - changed - replaced LibItemUpgradeInfo-1.0 with internal code
 - fixed - timewarped items should now show their correct item levels
 - fixed - issue with clearing bars
 
# 3.05.04 (30-JUN-2015)
 - fixed - issue with adding/removing/moving bars

# 3.05.03 (27-JUN-2015)
 - changed - restack menu options
 - fixed - restack code (shouldnt move profession items, like the swiss army knife, into the bank any more, just crafting reagents that can go into that profession bag)
 - fixed - embeds for no-lib download
 
# 3.05.02 (25-JUN-2015)
 - toc updated to 60200
 
# 3.05.01 (xx-JUN-2015) Beta 4
 - fixed - restack code
 - changed - category assignment menus are now in internal id order
 - changed - rule assignment menus are now in priority order
 
# 3.05.01 (14-JUN-2015) Beta 3
 - fixed - restack code
 
# 3.05.01 (13-JUN-2015) Beta 2
 - changed - restack action no longer initiates mutliple location restacks, its now per window/location so you have more control over it
 - changed - restack menu: choice of blizzards cleanup or my restack code
 - changed - restack menu: auto deposit is now set here
 - info: cleanup code will compact then if enabled and at the bank will do a deposit all reagents
 - info: restack code will compact then consolidate
 - info: compact will condense all items into as few stacks as possible
 - info: consolidate will move profession items in normal bags and the reagent bank to profession bags, then move crafting items in normal bags to the reagent bank, then move crafting items in your bag to the bank.
 - info: when auto deposit is enabled and at the bank restack will move items in your bags to the bank (and reagent bank) as part of both the compact and consolidate processes
 - info: both code variants will abide by the ignore cleanup value assigned to a bag (if items in a bag are not touched by the code then check this setting)
 
# 3.05.01 (06-JUN-2015) Beta 1
 - removed - player level restictions for mount menus (allows you to pick the chauffered mounts when under level 20)
 - changed - rule formulas are no longer compressed into a single line.  you can add extra spaces and newlines and they will stay intact now
 - added - Chauffeured Chopper mount data
 - fixed - issue with new item flash/animation and search overlay causing new items to not hide when they didnt match the filter

# 3.05.00 (25-FEB-2015)
 - added - config > settings > location > window > frames > title > online (sets the colour of the character name in the title bar when online)
 - added - config > settings > location > window > frames > title > offline (sets the colour of the character name in the title bar when offline)
 - added - config > settings > location > window > frames > search > label (sets the colour of the label in the search bar)
 - added - config > settings > location > window > frames > search > text (sets the colour of the text in the search bar)
 - changed - toc set to 60100
 
# 3.04.22 (06-JAN-2015)
 - added - right click menu off refresh icon to toggle display of hidden categories/stacks
 - added - config > settings > location > items > limit stacks (range from 0 to 5, 0 will show all stacks, 1-5 will only show that many stacks of an item and hide the rest, toggle show hidden to temporarily see all hidden stacks) - note: displayed stack count does not increase to cater for the hidden stacks
 - added - rule function: mounttype | mtype ( "L" = land, "A" = flying, "S" = water surface, "U" = underwater, "X" = ignored/unknown)
 - added - config > settings > location > items > empty slots > sort position (Enabled: Empty slots are sorted first alphabetically | Disabled: empty slots are sorted last alphabetically)

# 3.04.21 (22-JAN-2015)
 - fixed - issue with first bank bag slot not being draggable
 - fixed - issue with pet breed text when Battle Pet BreedID addon is not installed
 - fixed - issue with new item glow showing in offline locations
 - fixed - issue with offline items still fading when the option was disabled
 
# 3.04.20 (14-JAN-2015)
 - added - new items category
 - added - config > settings > location > items > new items
 - added - right click menu off refresh icon for new item reset
 - added - pet breed information is now displayed on the custom tooltips when the Battle Pet BreedID addon is installed
 - updated - pet tooltips and code
 - changed - cosmetic issue with pet and mount totals in the status bar, they will now always show the total count (the option to swap between used/empty is ignored)
 - changed - translations (mostly around pet text)
 - fixed - issue with LibDataBroker not having a TOC file so cant be loaded as standalone.  moved it back to being an included library

# 3.04.19 (04-JAN-2015)
 - changed - minor adjustment to the cleanup/restack code
 - fixed - item age now defaults to topleft.  if itemlevel is displayed, then itemage it is positioned to center instead
 - fixed - issue with vault data for characters on different connected realms when in the same guild - you will have to manually erase any existing duplicated vault data
 - fixed - issue with pet item counts sometimes not updating
 - fixed - issue with pet scanning code sometimes not re-scanning when it should have

# 3.04.18 (21-DEC-2014)
 - fixed - item counts should now display on the tooltips for work order reagents and quest log items
 - fixed - item age should display if enabled
 - fixed - LDB actions menu

# 3.04.17 (25-NOV-2014)
 - added - libperiodictable libraries: ClassSpell, CurrencyItems, Gear, GearSet, InstanceLoot, InstanceLootHeroic, InstanceLootLFR, TradeskillLevels, TransmogSet
 - updated - external libraries
 - added - right click menu to cleanup icon to deposit all reagents
 - changed - ldb item tracking counts now include items from the bank
 
# 3.04.16 (11-NOV-2014)
 - fixed - frame level issue causing items from the window underneath to be clickable/mouseoverable
 - removed - old frame level workaround code (new code should stop it from happening anyway)
 - removed - workaround code for savedvariables having weird decimal places
 - changed - moved keybindings from Other to AddOns category in KeyBindings interface
 - updated - locale zhCN

# 3.04.15 (30-OCT-2014)
 - changed - library layout changed (LibDialog, LibDataBroker, LibStub and CallbackHandler are now externals so if you use the nolib version please ensure you have those already installed)
 - changed - pet scanning code
 - deleted - selected/ignored pets choices wiped (will revert to random) due to issue with list index value changing. using the global identifier value instead
 - fixed - issue with ldb and status frame showing an ERR or not updating the slot count

# 3.04.14 (26-OCT-2014)
 - fixed - window can be moved again by dragging within the container frame
 - fixed - issue with sometimes not removing data from previous scans causing the window to not be able to be drawn
 - removed - soul shard tracking code (item will still be listed in the tracking until removed)
 - fixed - issue with icons in menus
 
# 3.04.13 (25-OCT-2014)
 - fixed - dropping an item on the reagent bank "bag" will now move it to the reagent bank
 - added - to bag menu; assign to bag options (from blizzard bag options)
 - added - connected realms; Argent Dawn / The Scryers
 - added - connected realms; Malfurion / Trollbane
 - added - connected realms; Shattered Hand to Coilfang / Dark Iron / Dalvengyr / Demon Soul

# 3.04.12 (23-OCT-2014)
 - fixed - issue where it wasnt resetting the items back to the top when exiting edit mode after scrolling
 - fixed - guild bank tab icons
 - added - to bag menu; cleanup options; reverse cleanup and loot to leftmost (from blizzard interface options)
 
# 3.04.11 (22-OCT-2014)
 - changed - maximum container frame height increased to 2000
 - changed - default container height set to 2000
 
# 3.04.10 (22-OCT-2014)
 - changed - all locations now have a maximum height for the container frame, it will scroll the items if there are too many to fit and shrink to fit if less
 - added - config > settings > window > height (default 400) sets the maximum height of the container frame before it scrolls
 - changed - toybox scanning (should remove the taint)
 - changed - mount scanning
 - changed - if a bag type returns unknown during scanning it will be queued to be rescanned until its type is known (warnings are generated when this happens, they cannot be disabled)
 - fixed - issue with ignore cleanup option for bank and backpack not being remembered
 
# 3.04.09 (20-OCT-2014)
 - fixed - item counts on battlepet tooltips
 - fixed - mount favourite code
 - fixed - mount macro
 - fixed - issue with bank data going missing
 - changed - config option for first empty is now a range from 0 to 5, 0 will show all empty slots, 1-5 will show that many empty slots (of each type)

# 3.04.08 (17-OCT-2014)
 - fixed - issue with vault restack code
 - changed - restack will now combine into the lowest numbered slot (not the highest)
 - added - config > display > cleanup option, disable to use old restack function (it will do the same sort of action as the blizzard cleanup just slower and doesnt move items into empty slots)
 - removed - warnings about no usable mounts
 
# 3.04.07 (16-OCT-2014)
 - erased - pet data
 - fixed - issue with battlepet tooltips
 - fixed - cage, release and rename battlepet menu options
 - fixed - mount warning issue
 - changed - yielding while in combat re-enabled (forgot to turn in back on)
 - added - empty reagent bank category
 
# 3.04.06 (15-OCT-2014)
 - fixed - issue with ldb mount code
 - fixed - typo in ldb pet tooltip code
 - fixed - issue with sent mail tracking code
 - fixed - issue with pet dismiss code
 - fixed - issue with toybox scanning code not resetting the filters properly
 
# 3.04.05 (15-OCT-2014)
 - added - config > settings > location > items > empty slots > first only (hides all empty slots except the first of each type)
 - fixed - battlepet tooltip issue with new creature guid format
 - fixed - issue with pet/mount menus
 - fixed - issue with LDB pet/mount code
 - note - crafting using bank items has NOT been tested, item counts may not update.  Reagent Bank item counts will update.

# 3.04.04 (11-OCT-2014) BETA WARLORDS
 - changed - maximum bars per row increased from 16 to 40
 - added - ability to assign the contents of a bag to a specific bar - this overrides the items category/rule assignments
 - updated - battlepet data
 - changed - battlepet menu. added another level in an attempt to shrink the height

# 3.04.03 (05-SEP-2014) BETA WARLORDS
 - added - mail sent/returned to another character is now tracked (recipient must be on the same account and must have logged in at least once with the mod loaded for it to track - timeout returns/deletions not yet coded)
 - added - cleanup options to bag right click menu.  ignore (wont touch the bag contents) and deposit all reagents (enabling this automatically deposits reagents as part of the cleanup)

# 3.04.02 (24-AUG-2014) BETA WARLORDS
 - changed - required blizzard addons set to required in toc due to optional not fully loading them (specifically the pet/mount journal)
 - fixed - (maybe) item quality for boosted items (the green that occasionally gets bumped to a blue)
 - fixed - issue with ldb code loading before the mount journal so it wasnt seeing any mounts and removed all selected mounts due to them being non-existant
 - changed - realm connections: added Shadowmoon to Blackwing Lair / Dethecus / Detheroc / Haomarush / Lethon
 - changed - realm connections: added Burning Legion to Agamaggan / Archimonde / Jaedenar / The Underbog
 
# 3.04.01 (06-AUG-2014) BETA WARLORDS
 - fixed - mount code should work a lot better now
 - fixed - mount menu options
 - changed - option for using flying mounts as land mounts moved to the flying mounts menu
 - added - manually coded mount types - if anything ends up on the custom tab then let me know the number, name and type of mount and i'll update it
 - added - workaround for savedvariables issue
 
# 3.04.00 (31-JUL-2014) BETA WARLORDS
 - note - all item data has been erased.  please login to each character to update its data
 - changed - toc set to 60000
 - added - reagent bank - displayed as the last bank bag.  to purchase right click on the empty slot icon and select purchase (the cost is shown in the tooltip)
 - added - you can now purchase a bank bag slot via the right click menu (the cost is shown in the tooltip)
 - fixed - cosmetic issue when buying bank bag slots and the "buy" text staying there
 - changed - the restack function now uses the internal bag cleanup function for the bank and bags (its much faster and has options which i havent included yet)
 - added - second void storage tab is now scanned
 - added - toybox location and category (you cannot click on the items but you can drag them onto an action bar)
 - aded - new item glow
 - added - realm connections: new Elune and Gilneas
 - changed - realm connections: added Deathwing to Executus / Kalecgos / Shattered Halls
 - note - pets and mounts are a bit weird at the moment, make sure the translations have completed before trying to do anything with them
 - note - i cant tell what type of mount it is at the moment so youll need to set that up or you wont see any mounts - its in the config under LDB (yes i know i'll fix that later)
 - note - there will be issues, its beta, be patient

# 3.03.36 (20-JUN-2014)
 - added - ability to select flying mounts as land mounts (mostly for those without the flying skill), disabled by default, accessed via the ldb menu or mount locations main menu
 - added - cross realm support for item counts and money amounts
 - changed - money tooltips now use the item tooltip options to determine which othr characters data is displayed
 - fixed - cosmetic issue when buying bank bag slots and the "buy" text staying there (it now goes away after a refresh)
 - fixed - issue where tooltip option for self only was based on character name and the change to displaying multiple realms meant characters with the same name would all display, its now based on character id
 - fixed - issue where item counts were not being sorted alphabetically
 
# 3.03.35 (13-JUN-2014)
 - removed beta status

# 3.03.34 (07-JUN-2014) BETA 06-07-11-30
 - fixed - issue with money tooltip generating an error

# 3.03.34 (05-JUN-2014) BETA 06-05-21-00
 - note - all item data has been erased.  please login to each character to update its data
 - fixed - added example rule module back in (was removed when directory was renamed)
 - fixed - issue with clearing item counts when changing options
 - added - config > display > tooltips > item counts > self highlight - prepends this text to the currently displayed characters name so its more obvious in the list (defaults to blank text, not added when self only is enabled)
 - added - config > display > tooltips > item counts > realm only - limit item count results to the currently displayed realm
 - changed - data storage layout
 - changed - switch character option can switch to characters on other realms
 - changed - maximum items per row increased from 40 to 60
 - changed - config options moved to its own load on demand module
 - changed - guild bank info now stored only when the vault is accessed (should help stop the vault money amount from coming back all the time)
 - changed - money tooltip data based off the current locations realm (ldb tooltip is still based off the current players realm)
 - changed - item count tooltip text is being cached. this means more memory usage but significantly less impact on framerate
 - changed - item count tooltip data based off the current locations realm (tooltips from links are based off the current players realm)
 
# 3.03.33 (19-MAR-2014)
 - fixed - mount availability code when zoning
 - added - locales for itIT and ptBR
 
# 3.03.32 (19-NOV-2013)
 - fixed - some techniques were showing as unuseable because their tooltips were formatted differently to patterns and recipes
 - changed - tooltip item counts should use less cpu (less impact on framerate)
 - fixed - removed the blue glow from the bar numbers in edit mode
 - changed - (via keybinding only) druid bear/cat/travel/moonkin forms are now cancelled before attempting to mount (aquatic and flight forms are never cancelled as they are usually faster or same speed)
 - changed - (via keybinding only) shaman and warlock non humanoid forms are now cancelled before attempting to mount
 - fixed - timeless items (the "unopened" versions) are now be under the same category as the "opened" versions - equipable items (bind to account)

# 3.03.31 (11-AUG-2013)
 - changed - toc set to 50400
 - fixed - at load time hide the new item texture (blue glow) blizzard added to items in this patch (will sort out if this can be used properly later)
 
# 3.03.30 (26-AUG-2013)
 - changed - in combat threading
 - added - config > display > bug fixes > incombat yielding - to allow for user customisation of the deliberate delays to building a bag when opening for the first time in combat
 - fixed - displayed item level values should now include any item upgrade levels
 - fixed - location frame will be displayed above all others when opened
 - changed - restack will no longer start if you are in combat
 - fixed - initial frame level for items to ensure they are on top of the bars

# 3.03.29 (10-AUG-2013)
 - changed - pet scanning functions

# 3.03.28 (22-MAY-2013)
 - changed - toc set to 50300
 - changed - pet sorting (item type) now uses the type name and not the number
 - changed - rule function `pettype( )` now also accepts the (client localised) type name
 - fixed - issue with debug info for non wild battle pets
 - updated - companion item/critter data
 - changed - LibDialog from curse download is now souced from pkgmeta file
 - fixed - issue with outfit rules and change to EquipmentManager_UnpackLocation api function

# 3.03.27 (07-MAR-2013)
 - fixed - re-enabled threading in combat

# 3.03.26 (06-MAR-2013)
 - changed - toc updated
 - fixed - void storage item tooltips now include item counts
 - fixed - issue with toc file for rules (addonloader)
 - fixed - issue with toc file for example rule (addonloader)
 - fixed - issue with empty bag tooltip text
 - fixed - issue with mouseover tooltips not working for some of the newer battlepets (guid code needed an extra digit processed)
 - fixed - issue with "can use" code not working correctly for some patterns/recipes (will now scan downwards until the first blank line then scan upwards until the first blank line)
 - changed - battlepet scanning code
 - updated - notification code for better battlepets (checks level 25 approximate health, power and speed now, not just quality)
 - changed - battlepet cage, release and rename static popups now use LibDialog so should not taint blizzards secure code
 - changed - non wild battlepets now use their actual quality colour for their border, tooltips and links remain the default colour (yellow)
 - added - options to not display the restack messages

# 3.03.25 (21-DEC-2012)
 - added - config > controls > location > special (default = true) - treat the location window as special or not.  special windows are closed when the ESCAPE key is pressed
 - fixed - nil issue with stock count
 
# 3.03.24 (16-DEC-2012)
 - fixed - issue with disabling arkinventory and mouseover tooltips
 - fixed - issue with scanning pets (for max pet level)
 - changed - the equipable items category now only picks up items that have an actual equip location set
 - added - display item levels on equippable items (disabled by default) via config > settings > location > items > item level
 - added - tint unuseable will apply to battlepets in your bag when their level is above your maximum current pet level
 - fixed - issue with ldb random mount code not checking users custom changes

# 3.03.23 (30-NOV-2012)
 - added - cooking slot / container support
 - fixed - issue with normaltexture showing default item border

# 3.03.22 (29-NOV-2012)
 - fixed - updated for pet api changes (petid is now a guid string, not a number)
 - fixed - issue where pets and mounts submenus were showing up under the action menu

# 3.03.21 (28-NOV-2012)
 - changed - toc updated to 50100
 - fixed - issue with item tracking object not updating
 - fixed - issue with battlepet opponent detail output not linking all your pets
 - fixed - issue with normaltexture going green
 - added - new sort key - internal id (class:itemid:soulbound)
 
# 3.03.20 (16-NOV-2012)
 - fixed - tooltip code error
 
# 3.03.19 (15-NOV-2012)
 - changed - the equipment category name is now sourced from blizzard text
 - added - category: system > equippable items (account bound)
 - added - rule function: accountbound | ab
 - note - accountbound items are also considered soulbound so rule order will be important
 - added - option to disable adding information to mouseover tooltips
 - added - options to add source and description text to mouseover tooltips
 - changed - battlepet mouseover tooltips should now work with unit frames
 - changed - battlepet mouseover display format to show more detailed information about your matching uncaged battlepets
 - changed - battlepet opponent text will now link your existing pets if the opponent quality is equal or higher
 - added - rule function: pettype | ptype
 - added - rule function: petiswild
 - added - rule function: petcanbattle
 - potentially fixed - locked journal issue when multiple accounts on a battle.net account are logged in at the same time
 
# 3.03.18 (08-NOV-2012)
 - changed - guild money amounts will only update when at the guild now (should stop them from zero'ing)
 - fixed - issue with void storage scanning
 
# 3.03.17 (06-NOV-2012)
 - fixed - bug in item count code
 - fixed - the virtual account will no longer appear in the ldb money object
 - fixed - translation issue of german global constant being a different format to all other languages
 
# 3.03.16 (05-NOV-2012)
 - changed - pets are now stored under a virtual account user (so only one copy of pet data per realm is saved)
 - changed - mounts are now stored under a virtual account user (so only one copy of mount data per realm is saved)
 - note - rules do not currently work with battlepets or mounts
 - added - for sorting purposes, itemlevel is pet level
 - added - for sorting purposes, itemtype is pet family
 - fixed - issue with caged battlepets in vaults, although the blizzard interface has the same bug as well which didnt help
 - fixed - pet renames, level ups and favourite tags are now picked within 5 seconds
 - fixed - issue with pet item counts not updating properly
 - fixed - issue with random pet and mount summoning code (caused by translation delay)
 - fixed - drag and drop of pets will now work onto action bars as well as battle pet slots
 - added - item counts to mouseover tooltip for capturable and other players battlepets
 - added - config option to disable the custom battlepet tooltip used to display itemcounts
 - added - upon entering a pet battle the opponents pet details (hyperlinks) will be displayed to the chat window - can be disabled via config > mesages > battlepet > opponent
 - fixed - when summoning a ground mount in a non flying area and you have none it will attempt to use a flying mount if you have one of those
 - fixed - issue with zone restricted mounts
 - fixed - issue with dismounting while in combat
 - changed - mount capabilities are now retrieved from internal blizzard data, zone restrictions are still hand coded
 - changed - ldb mount menus are now disabled if your skill isnt high enough
 - note - the ability to ride a sea turtle when you have no riding skill and/or are less than level 20 is a blizzard bug (then again its no faster than walking so i doubt they care too much)
 - fixed - issue with cursor not updating properly when an item is updated underneath it
 - removed - shapeshift mount forms, i cant cast them from unsecure code anyway
 - changed - vault actions moved from the tab icons to a new menu button in the changer window
 
# 3.03.15 (28-SEP-2012)
 - added - config > settings > [location] > items > scale
 - fixed - optional dependency link for libpetjournal
 - fixed - x-embed dependency link for libpetjournal

 # 3.03.14 (27-SEP-2012)
 - fixed - idiot programmers really stupid mistake
 - note - all item data has been erased.  please login to each character to update its data
 
# 3.03.13 (27-SEP-2012)
 - fixed - issue with guild data not erasing gold value when erased
 - fixed - possible issue with erase data function (might not be fixed as i couldnt duplicate the issue)
 - changed - a guild bank now only has an option to erase all data

# 3.03.12 (26-SEP-2012)
 - fixed - issue with cursor not showing sell icon
 - changed - tooltip item counts, by default they now show only your own faction
  
# 3.03.11 (26-SEP-2012)
 - fixed - issue with clicking on gold amount in bag window
 - fixed - issue with rule caching
 - fixed - currency tokens now using blizzard linktype
 - fixed - currency tooltips now include item counts
 - fixed - the chatlink and dressup functions work for items in wearing, token, mail and void storage locations
 - fixed - pet window, summon/dismiss via left click, right click menu as per pet journal
 - fixed - ldb pet object, left click to summon next pet, shift left click to dismiss active pet, right click for setup
 - added - pets now break down into four categories, pet (bound), pet (tradeable), battle pet (bound) and battle pet (tradeable)
 - added - for sorting purposes item (stat) level = pet level, and item type and subtype = pet type
 - added - for rule purposes `ilvl( )` matches pet level, and `type( )` matches pet type
 - added - summoned/active pet has a pulsing glow
 - added - custom tooltip for battle pets, should override blizzard tooltip
 - added - option to not display source and description text from battlepet tooltip
 - note - pet, mount and currency tracking data for ldb has been erased, please login to each character to setup ldb
 
# 3.03.10 (17-SEP-2012)
 - fixed - outfitter support code should now work properly
 - changed - outfit rule will now check against each supported addon and then lastly check the equipment manager
 
# 3.03.09 (16-SEP-2012)
 - fixed - issue with empty bag slot custom colour reverting to grey when displayed offline
 - fixed - issue with soulbound status, item quality and default category assignment during scan
 - note - all saved data has been erased, please login to each character to update its data

# 3.03.08 (15-SEP-2012)
 - fixed - window drawing when in combat will draw slower but it will complete

# 3.03.07 (14-SEP-2012)
 - fixed - debug info for battlepets
 - fixed - parts and materials categorised by your primary skills, then under trade goods
 - fixed - keystones categorised under skill > archeology

# 3.03.06 (14-SEP-2012)
 - changed - default category; all trade goods reverted to trade goods category

# 3.03.05 (14-SEP-2012)
 - added - forge master and transmogrify npcs are now treated as merchants in regards to your auto open/close options
 - fixed - issue with item quality not updating in bags
 - fixed - issue where jewelcrafting didnt appear under the skill menu

# 3.03.04 (13-SEP-2012)
 - fixed - error with profession scanning code
 - changed - default category assignment code

# 3.03.03 (12-SEP-2012)
 - fixed - issue with profession scanning code
 - fixed - issue where internal sort keys were always recalculated every bag opening
 - fixed - issue when outfitter initialised after ai
 - changed - some translations reverted to blizzard internal values
 - changed - edit mode now ignores the tint unusable option
 - changed - bag highlight now uses the searchoverlay layer, custom layer removed

# 3.03.02 (01-SEP-2012)
 - fixed - issue with herbalism skill translation
 - fixed - issue with fishing skill translation
 
# 3.03.01 (29-AUG-2012)
 - changed - toc set to 50001
 - added - battle pet category
 - added - battle pet item and tooltip support
 - removed - ability to summon pets (via window and ldb, will return in a later version)

# 3.03.00 (21-AUG-2012) BETA 08-21-11-00
 - changed - toc set to 50001
 - changed - will not load on live servers
 - fixed - caged battlepet items and offline tooltips
 - removed (temporarily) - pets (theyre now account wide so i need to decide what to do with them)
 - removed (temporarily) - mounts

# 3.02.95 (09-AUG-2012)
 - fixed - removed ranged slot for mop beta
 - added - more checking of saved variables
 
# 3.02.94 (06-JUL-2012)
 - added - monk class
 
# 3.02.93 (04-JUL-2012)
 - fixed - issue when hooking other mods and clearing the item cache
 
# 3.02.92 (24-JUN-2012)
 - updated - item relocation will now clear the cached rule/category assignment for that item.  allows for custom rules to work better.

# 3.02.91 (02-MAY-2012)
 - updated - pets and mounts
 - fixed - issue with rules window font application

# 3.02.90 (22-APR-2012)
 - fixed - tainted frames caused by opening AI for the first time, while in combat.  the first 50 slots of each bag are pre-loaded before entering the game world to ensure they are secure. this will use up more memory but guarantee that all slots are usable while in combat
 - fixed - soulbound issue introduced in 3.02.89

# 3.02.89 (06-APR-2012)
 - fixed - another global variable taint issue
 - fixed - you can no longer move bags around in the changer frame while in combat (caused an interface error and locked the bag in place)
 - workaround - tainted frames caused by opening AI for the first time, while in combat.  tainted frames are tinted purple and unusable until you leave combat, at which point they are replaced with untainted frames
 - restored - `bag( )` rule function

# 3.02.88 (11-FEB-2012)
 - updated - pets and mounts

# 3.02.87 (24-DEC-2011)
 - fixed - code issue where i left out a local and potentially tainted a secure global variable

# 3.02.86 (17-DEC-2011)
 - fixed - menu library issue where menus were always expanding in size until they went off the screen
 
# 3.02.85 (17-DEC-2011)
 - fixed - issue when selecting vault/void sort method outside of those two locations
 - fixed - menu library issue where menus were always expanding in size until they went off the screen
 
# 3.02.84 (30-NOV-2011)
 - changed - TOC updated to 4.3
 - changed - void storage icon
 - fixed - void storage online/offline status
 - added - slash command `/ai summon pet`
 - added - slash command `/ai summon mount`
 
# 3.02.83 BETA (11-NOV-2011)
 - added - support for void storage
 - removed - rule function - `bag( )`

# 3.02.82 (08-AUG-2011)
 - added - cash flow contribution amount is now listed at the bottom of the money log list

# 3.02.81 (03-AUG-2011)
 - added - more pets and mounts
 - added - holding the dressup (control) button while summoning a mount will attempt to use a zone specific mount, if no zone specific mount is found it will revert to a non zone specific mount
 - added - holding the chatlink (shift) button while summoning a mount will attempt to use an alternative mode mount, ie if you can fly then a ground mount will be summoned, if you are swimming then a flying mount will be summoned
 - changed - clicking on the summon pet button with a pet out will now dismiss that pet, not summon a different pet
 - fixed - issue with clicking on hyperlinks in guildbank item logs
 - fixed - cosmetic issue with item menu text colouring
 - fixed - tint unusable item should work better for patterns/recipies you can learn but makes an item you cannot use

# 3.02.80 (29-JUN-2011)
 - fixed - bug in erase code
 - changed - TOC updated to 4.2
 - added - bound to battle.net account now treated as soulbound
 - removed - keyring

# 3.02.79 (29-JUN-2011)
 - incorrect upload
 
# 3.02.78 (28-APR-2011)
 - workaround - Open All Bags keybinding calls ToggleAllBags, ToggleAllBags is now hooked and calls OpenAllBags instead
 - changed - TOC updated to 4.1
 - changed - OpenAllBags now works properly

# 3.02.77 (26-FEB-2011)
 - changed - the map will no longer change to the current zone if opened and you change (sub)zones.  it will if you summon a mount.  when the map is open the ldb mount icon will no longer update as you change (sub)zones
 - workaround - frame overlap lag spike issue should no longer happen
 
# 3.02.76 (10-FEB-2011)
 - fixed - unknown zone ( -1 / 5 ) error message
 
# 3.02.75 (10-FEB-2011)
 - fixed - mount code using the wintergrasp timer that i missed
 
# 3.02.74 (09-FEB-2011)
 - fixed - mount code changed to cater for removal of a wintergrasp timer api function
 - fixed - code updated for auction house category changes (used for translations)
 
# 3.02.73 (26-JAN-2011)
 - workaround - fixed issue with bug where item hyperlinks are sometimes returned malformed so looks like the item has changed, when it hasnt
 - fixed - issue with updated ace locale library
 - added - tackle box
 
# 3.02.72 (04-DEC-2010)
 - fixed - issue with item age display showing when past the cutoff
 - fixed - issue with tracking shards for warlocks

# 3.02.71 (03-DEC-2010)
 - fixed - pet and mount selection menus
 - fixed - scanning issue where some locations were being unnecessarily scanned multiple times
 - fixed - issue with internal locations for spellbook and tradeskills
 - changed - default value for item age cutoff to 0
 - changed - item age display cutoff is now set in minutes instead of hours
 - changed - graphical space for search label increased so it fits other languages in

# 3.02.70 (28-NOV-2010)
 - updated - zhTW locale
 - changed - companion selection now allows you to ignore a companion so that it is never summoned via random

# 3.02.69 (22-NOV-2010)
 - fixed - issue with item count cache not being cleared after erasing data
 - fixed - issue with pet cleanup code erasing all selected pets and returning it to full random
 - fixed - potential issue with internal isflyable code when you have no flying only mount (ie only combination land and flying mounts)
 - fixed - issue with companions being scanned too frequently due to event being triggered too often in populated places
 - fixed - issue with scrap support in `trash( )` rule function
 
# 3.02.68 (12-NOV-2010)
 - note - auction house data purged to clean up invalid data left over from expiry code
 
# 3.02.67 (11-NOV-2010) ALPHA
 - fixed - issue with auction expiry code
 - fixed - issue with itemref tooltip

# 3.02.66 (10-NOV-2010)
 - fixed - auction scanning
 - removed - library libbabble-zone
 
# 3.02.65 (08-NOV-2010) BETA
 - fixed - mount and pet menus off the main menu for those windows (equivalent to the LDB menus)
 - added - auction house (may or may not work with more than 50 active auctions), thanks to Gromurg of Sinstralis (FR) for some code and ideas
 
# 3.02.64 (04-NOV-2010)
 - fixed - cooldowns should now display properly when "on global cooldown" is enabled
 - fixed - mount keybinding when used with a modifer should properly force an alterntive mount-type to be summoned, eg flying but you want ground.  swimming (at the surface) but you want flying
 - changed - framelevel workaround warnings set to disabled by default, and the warnings will now print (they never appeared regardless of setting)
 - reverted - crash code removed, it'll just crash now instead of trying to purge the corrupt data

# 3.02.63 (28-OCT-2010)
 - changed - any frames that are partially out of the game window will be brought fully back into the game window on first viewing (use the slash command to manually fix this issue after the first viewing, can be disabled in the config)
 - added - options to disable the translation status messages you get during load
 - added - slash command to reposition all frames back into the game window, `/ai reposition`
 - added - config option to disable reposition on first view (for those that want their bags left partially off screen)
 
# 3.02.62 (27-OCT-2010)
 - fixed - cleaned up references to libraries (ace2, dewdrop) that were no longer being used
 - fixed - embeds.xml will be commented out of the toc file for curse no-lib downloads so it doesnt try to load embedded libraries (which arent there for no-lib)
 - fixed - anchor issue
 
# 3.02.61 (26-OCT-2010)
 - fixed - issue with ArkObject not existing on tooltips
 - fixed - issue with the dragable frame background not being the correct height when the search frame was visible
 - fixed - anchors should now stay in the same place when scaling the window.  (some anchors may have ended up being reset to top right and you may have to use config > controls > reposition to bring the window back onto the screen)
  
# 3.02.60 (25-OCT-2010)
 - fixed - issue with crash workaround code triggering incorrectly
 
# 3.02.59 (25-OCT-2010)
 - fixed - mount data correction code issue with unknown mounts
 - fixed - Icebound Frostbrood Vanquisher mount had wrong spell id
 - fixed - tooltip comparison issue
 
# 3.02.58 (22-OCT-2010)
 - fixed - soul shards should reappear as an item tracking choice if you remove it and log on with a warlock
 - fixed - inscription skill no longer uses the auction house category and uses the spell instead (to fix a german translation issue)
 - changed - the new guild bank bag/slot sortmethod is now a separate system sort method and will need to be applied manually to the vault if required, the old bag/slot style has been reverted to its original style when used on the vault
 
# 3.02.57 (19-OCT-2010)
 - changed - mount code to work around a blizzard bug with `IsFlyableArea( )`
 - changed - default window width set to 14
 - changed - vault sorting order changed to make it look identical to blizzard interface.  best results with width set to 14, sort order set to bag / slot, bar and item anchors set to bottom right, and everything assigned to a single bar
 - changed - armor and weapon enchantment categories replaced with item enchantment category
 - fixed - config menu keybinding will now toggle the config window
 - fixed - erase data should finally erase all data, including gold
 - added - achievement link comparison (click on an achievement link, hover over the tooltip, press shift to bring up yours for comparison)
 - added - mount window main menu now includes the ldb mount menu so you can select which mounts you want summoned when you dont have an ldb display mod installed
 - removed - ldb ammo object and related code
 - removed - soulshard, projectile, bullet, arrow categories, bagtypes and empty slots
 - note - all item data has been erased, please login to each character to update its data

# 3.02.56 (14-OCT-2010)
 - fixed - vault purchase frame is now hidden once you have 6 tabs. tabs 7 & 8 are unlocked via guild achievements and not actually purchased (at least as far as i know)
 - changed - added failsafe code for when the translation code fails to stop (unable to test accurately as i cant get mine to break)
 - changed - all translation attempts now use an internal tooltip as the gametooltip may have been altered by other mods

# 3.02.55 (13-OCT-2010)
 - fixed - outiftter outfit items should now recategorise properly when changed
 - updated - toc to 40000
 
# 3.02.54 (12-OCT-2010) BETA 17-00-Cataclysm
 - fixed - item counts on tooltips for tokens
 - fixed - backpack token display (cataclysm)
 - fixed - editing rules
 - updated - mount and battlepet data
 - added - vendor price sorting as a system sort method

# 3.02.53 (01-OCT-2010) BETA 22-30-Cataclysm
 - fixed - issue with vault logs not scrolling via mousewheel
 - fixed - issue with selecting token in ldb currency tracking object
 - added - empty bag option to bag right click menu.  only available on replaceable bags
 - removed - library libbabble-inventory

# 3.02.52 (27-SEP-2010) BETA 23-30-Cataclysm
 - fixed - issue with auto dismount option not appearing unless you had random selected
 - fixed - rule function `id( )` should now work properly for pets and mounts
 - fixed - rule function `tooltip( )` should now work properly for pets and mounts
 - fixed - ldb pet object wouldnt summon pets
 - fixed - issue with tooltip item counts being erased and not recalculated when you moved items around in the guild bank
 - fixed - icon issue with tokens
 - changed - in edit mode you will now have an entire row added to make bar moves easier
 - changed - windows can now be moved off screen if required
 - changed - in edit mode the bar menu will now appear on any click (and not just a left click)
 - added - pet: mini thor
 - added - config > controls > reposition button to pull window back onto the screen (will end up in one of the screen corners depending on anchor)
 - restored - the rest of the ldb ammo object functionality for wrath users
 - note - the latest cataclysm beta has recategorised projectiles (ammo), quivers and soul bags - its going to cause some warnings and visual issues with category names

# 3.02.51 (21-SEP-2010) BETA 21-30-Cataclysm
 - fixed - issue with colorblind setting not being picked up properly
 - fixed - issue with money text displaying zero silver when you only have copper
 - fixed - issue with money text displaying "no sell value" when you have no money at all
 - fixed - leftover debug code where profiles were constantly being upgraded to 4.xxxx
 - added - config option to set the frameStrata level for all ArkInventory windows, default is set to MEDIUM

# 3.02.50 (18-SEP-2010) BETA 19-30-Cataclysm
 - changed - number of vault tabs expanded to 8
 - changed - frameStrata set to HIGH to get above the default actionbars
 - changed - ldb item tracking object will now count soul shards for cataclysm warlocks
 - changed - ldb pet and mount objects rewritten.  existing choices have been erased.  you can now select multiple pets/mounts that you want summoned (randomly), not just one or all.  if using the keybinding then holding any modifier will force the use of a ground mount (for cataclysm users that want to use one in flyable locations)
 - changed - category for Skill > Riding moved to System > Mount
 - changed - category for System > Projectile (Bullet) and System > Projectile (Arrow) merged with System > Projectile
 - changed - item text translations (for categorisation and menus) are now gathered from within the game, there are 10 attempts, 1 every 10 seconds, after which it will fail and you may have issues with items not being categorised and menus using place-holder text
 - added - category for Consumable > Item Enhancement

# 3.02.49 (10-SEP-2010) BETA 23-30-Cataclysm
 - note - (cataclysm) LDB mount object icon wont update in real time unless you have one of each type of mount on an action bar (anywhere), summoning will work properly regardless.
 - changed - dewdrop (menu) library customised to ace3/libstub and cataclysm (this/self issues)
 - changed - you can now move categories the same way that you move bars (sort of like cut-n-paste)
 - changed - ldb ammo object restored (for wrath only)
 - changed - summon mount logic
 - added - babble-zone and babble-inventory libraries (to simplify localisations)
 - fixed - issue with token scanning code
 - fixed - guild bank withdrawal amount wasnt updating correctly
 - fixed - when you can repair from guild funds but not withdraw, the repair funds will now show with the withdraw button disabled
 - fixed - money frames and tooltips now adhere to your colorblind setting
 - fixed - ammo and bullet slots
 - removed ace2 and acelibrary dependencies and libraries

# 3.02.48 (05-SEP-2010) BETA 18-20-Cataclysm
 - note - all item data will be cleared, you will need to log in to each toon to update its data
 - note - due to changes in the way tokens are being handled by blizzard you can no longer get item counts in tooltips for them off the character pane
 - note - ldb water mounts will not be summoned in vashj'ir when youre on the sea floor (youre not swimming), you must jump off to begin swimming for them to work properly.
 - changed - toc updated to 40000 (you will need to enable out of date mods on live servers for AI to load)
 - changed - remaining references to this replaced with self
 - changed - internal rule variable name ArkInventoryRules.Item changed to ArkInventoryRules.Object (all custom rules will need to make the same change)
 - changed - currency tracking ldb object name changed
 - changed - pet and mount ldb objects now allows you to direclty select a pet or mount that requires a reagent to summon (you obviously still need the reagent to actually summon it)
 - fixed - dk flying mount no longer set as a ground capable mount
 - fixed - issue with location change and character switch buttons
 - fxied - issue with item count not updating under certain circumstances (vault still has issues with inter-tab transfers, but that should be it)
 - fixed - controls should no longer reset ( save / monitor )
 - fixed - disabling the save option for guild bank will now wipe the data on leaving the vault
 - fixed - icon heights for the tracking LDB objects (they will still shrink the more you have)
 - fixed - item count code will now cache entries where you have none of that item (stops stuttering/lag when displaying tooltips)
 - fixed - tooltips in search window will now update, eg comparison tooltips will appear
 - added - item tracking ldb object (for tracking non currency items)
 - added - slash command `/ai track [ itemlink | item name | item id ]`, an invalid input will return a warning.  if using the item name you must have the item in your bags.
 - added - keybindings for refresh and reload actions
 - added - user config for tracking LDB object icon height workaround for wrath (not required and ignored for cataclysm)

# 3.02.47 (08-JUL-2010) BETA 23-15
 - changed - ldb currency object will now allow you to monitor an unlimited number of currencies (not linked to the 3 blizzard choices)
 - changed - internal mount data to handle water mounts and better handle combination mounts
 - changed - rules broken out into seperate addon (you can disable this addon to save some memory if you do not use rules at all) so custom rule fucntions can be created if required
 - added - X-53 Touring Rocket (flying mount)
 - added - slash commands `/ai edit | rules | search` - toggles their respective states/windows
 - fixed - flying mounts being selected via LDB in wintergrasp when a battle has started (non english clients)
 - fixed - border style offset values will now save properly
 - fixed - several locale updates

# 3.02.46 (22-MAY-2010)
 - added - config option for bar name anchor points - automatic (default) | top | bottom
 - fixed - mount: frosty flying carpet (was set as a land mount)

# 3.02.45 (18-APR-2010)
 - updated - zhTW locale
 - fixed - config window

# 3.02.44 (17-APR-2010)
 - fixed - slash commands would fail unless the config window had been previously opened
 - updated - mount and battlepet data
 - added - vault info mode.  when switching tabs any unsaved info text changes are discarded
 - added - right clicking on the search icon will toggle the inline search frame

# 3.02.43 (14-APR-2010)
 - fixed - zhTW locale; riding
 - fixed - issue with quest item glow not working for banked items
 - fixed - issue with adding categories via the item menu
 - fixed - issue with hooking 3rd party trash mods

# 3.02.42 (09-APR-2010) - fixed - config menu errors when accessed via main icon, slash command and ldb menu - added - quest item glows

# 3.02.41 (08-APR-2010)
 - fixed - potential nil issue in location scan code

# 3.02.40 (08-APR-2010)
 - fixed - missing border from rule formula field and it will now be the full width of the window
 - fixed - potential issue with first time use after an upgrade and creating a new rule/category/sort method
 - fixed - issue with cooldown option using actual location and not the settings option for that location
 - changed - some of the bag hooking code was causing issues for other mods
 - added - trash rule now supports ReagentRestocker auto sell list
 - added - normal and thin options for the title frame
 - added - option to stop global cooldowns refreshing the window

# 3.02.39 (14-MAR-2010)
 - fixed - issue with cooldowns casued by fix for previous issue
 - added - "show" buttons to open the appropriate windows in the rules and search config options
 - added - cooldown options under settings > items to allow for totally hiding cooldowns, and disabling new cooldowns while in combat (used to stop refreshes when the bag is open during combat. the GCDs from some spells/actions would end up causing too many refreshes and lagging)

# 3.02.38 (11-MAR-2010)
 - fixed - issue with bank window not refreshing properly when you enter or leave the bank (caused by fix for another bank issue)
 - fixed - cooldowns will now display instantly when instant sorting is not enabled
 - added - support for the following trash vendoring mods: SellJunk, Scrap
 - added - rule function - `trash( )`, uses supported mods if installed, otherwise will return all poor quality items

# 3.02.37 (09-MAR-2010) - fixed - issue with bank window showing red (unknown bag type) item borders for some slots - fixed - frFR translation for glyph - added - bypass code with warnings (forced on) during bag scans for a potential bag size issue/bug - you can disable the warnings via the config options - added - missing pets (curious wolvar pup, fortune coin, gryphon hatchling, wind rider cub)

# 3.02.36 (06-MAR-2010)
 - fixed - issue with outfit rule function when using closetgnome and itemrack

# 3.02.35 (05-MAR-2010)
 - fixed - invalid code in options table for rules > border > offset
 - fixed - dragging an item while the cursor is in target mode (blue glowing hand) would cause a blocked action warning.  dragging is now disabled while in target mode.
 - changed - default order for rules changed from 0 to 100
 - changed - rule function arguments are now specified differently, this will cause some of your rules to break and some to not work exactly how you intended.  string arguments now need to be quoted, eg name( "eternal", "shard" )

# 3.02.34 (09-FEB-2010) BETA 23-37
 - fixed - openallbags (shift+b) should now work more like the blizzard version when you're only overriding one of the bag or bank (it's not exactly the same but it is more logical)
 - fixed - `EraseSavedData( )` function was leaving some data intact, specifically guild bank gold
 - changed - consolidated the addon options table some more

# 3.02.33 (02-FEB-2010) BETA 21-42
 - added - fix corrupted categories caused by earlier betas

# 3.02.32 (02-FEB-2010) BETA 20-55
 - fixed - issue with conversion of custom categories

# 3.02.31 (30-JAN-2010) BETA 10-46
 - fixed - status bar not unhiding
 - fixed - rule conversion issues

# 3.02.30 (29-JAN-2010) BETA 18-57
 - changed - bar names are no longer displayed by default
 - changed - bar names are now on the inside of the bar and will swap between top and bottom depending on item anchor point
 - changed - sorting is now done through sort methods, all sorting has been reverted to bag/slot.  you will need to create a sort method and then assign that as a windows default sorting method.  you can also assign a different sort method to a bar so it sorts differently from the rest of the window
 - changed - bar movement menu options moved to bar menu (for less clicking)
 - changed - bar movement - reduced to 2 options, "move" and "move > complete"
 - changed - item counts now recognize learnt pets and mounts being the same as the item they are learnt from (note this is a manually maintained table, see companion.xls, so may not be 100% complete or accurate)
 - changed - LDB mount object - will only allow choices from a list of mounts it knows about so some of your mounts may not be available. if your mount isnt listed you can raise a ticket with its name/spell id and i'll add it
 - changed - LDB mount object - can now select a ground and a flying mount
 - changed - LDB mount object - random option now selects a mount based on whether the area you are in is flyable or not, and will fall back to a random ground mount in flyable areas if you dont have any valid flying mounts
 - changed - LDB mount object - random option will never select mounts with requirements, such as the standard AQ mounts, even if you meet those requirements
 - changed - LDB pet object - will only allow choices from a list of pets it knows about so some of your pets may not be available. if your pet isnt listed you can raise a ticket with its name/spell id and i'll add it
 - changed - LDB pet object - random option will never summon pets that need reagents, like snowballs, even if you have the required reagent
 - changed - borders now use sharedmedia - all borders have been reset to blizzard tooltip
 - changed - backgrounds now use sharedmedia
 - changed - all damaged rules are flagged as undamaged on login and rechecked, you will get warned about any invalid rules and they will be marked as damaged for that session
 - added - config option for how much space/padding to allocate for bar names, default is 12
 - added - LDB mount object - option for minimum mount speed when random is selected
 - added - keybindings for pet and mount summons
 - added - support for tracked currencies, set via the standard blizzard interface
 - fixed - issue where deleting an entire stack or learning a pattern/recipe wasnt updating its item count
 - fixed - honor points should now use the proper faction icon
 - fixed - arena points should now use the proper icon
 - removed - conversion of old data structures prior to v3 is no longer possible.  if you have a version that old then you will need to delete your arkinventory saved variables file

# 3.02.29 (09-JAN-2010)
 - fixed - added more logic checks around the gold information on money tooltips to remove potential errors
 - added - config option to change internal 'bucket' timers - how often the window updates when there are changes, default is 0.5 seconds

# 3.02.28 (12-DEC-2009)
 - changed - equipped bags are now included in item counts
 - changed - esES translation for leatherworking bags
 - changed - toc to 3.3

# 3.02.27 (28-NOV-2009)
 - fixed - items should now reassign properly when you modify an outfit (if the outfit mod is using the blizzard equipment manager as its back end)
 - fixed - corrected the ruRU translation for mining bags
 - fixed - taint issue when using class colours
 - changed - data now stored at realm level so you can see what you have on the other faction - all data has been erased, please login to each character to update its data
 - changed - function `ArkInventory.ObjectCountGet( search_id, just_me, ignore_vaults, ignore_other_faction )` - added 4th parameter to ignore the opposite faction when requesting item counts
 - changed - tooltip options rearranged

# 3.02.26 (04-NOV-2009)
 - fixed - border style issue due to renamed textures
 - fixed - tooltips are now scaled back to normal (100%) when you disable tooltip scaling
 - changed - settings config option changed to tab style to make the choices more obvious
 - added - background colour options for the search and rules windows

# 3.02.25 (03-NOV-2009)
 - added - 6 solid border styles, Tooltip 1/2/3 and Square 1/2/3 for better visibility
 - added - AddonLoader support, defaulting to `always:delayed`
 - fixed - potential issue when using a font that was loaded after this mod was loaded
 - fixed - removed extra blank line on tooltip item counts when item is only in a guild bank
 - changed - ace-oo library removed
 - changed - config options table changed to reduce memory footprint
 - changed - function ArkInventory.ObjectCountGet( search_id, just_me, ignore_vaults ) - added 3rd parameter to ignore guild banks when requesting item counts

# 3.02.24 (28-SEP-2009)
 - fixed - some partially erased data could cause issues, its now erased completely on startup if found
 - fixed - zhTW franslation for gem bags
 - changed - all references of `getfenv( )` changed to `_G`
 - changed - bag right click menus moved to above the bag so they dont overlap with the tootip under the bag
 - changed - consolidated redundant translations
 - added - tooltip item counts option for guild banks to show which tabs the item is in, default is enabled
 - added - option to disable purge notifications when not saving location data
 - added - system > glyph category
 - added - item border option to allow for selecting a cutoff quality for quality coloured borders (ie only colour epic items and above)

# 3.02.23 (15-AUG-2009)
 - fixed - option for tooltip scaling can now be entirely disabled

# 3.02.21 (13-AUG-2009)
 - fixed - item counts will now be added to reference comparison tooltips (eg, clicking on an item link opens the reference tooltip, holding down the shift key while over that tooltip will open the comparison tooltips)
 - fixed - tooltip not hiding properly for ldb money object
 - fixed - saved data was not being erased on logout even when the save option was disabled
 - fixed - guild bank gold amount is now displayed on money tooltip
 - fixed - money tooltip will now use class colours if enabled
 - fixed - options for auto-opening the bag at the mailbox and merchant have been re-enabled and work correctly now
 - fixed - koKR translation for soulshard bags
 - added - option to scale tooltips - scale will be game wide

# 3.02.20 (09-AUG-2009)
 - fixed - included withdrawal allowance on current vault tab tooltip
 - fixed - several issues caused by splitting up the pet and mount windows

# 3.02.19 (08-AUG-2009)
 - fixed - `EraseSavedData( )` function was leaving some data intact causing issues when attempting to view another characters data
 - note - all item data has been erased, you will need to login to each character at least once to update it

# 3.02.18 (08-AUG-2009)
 - changed - pets and mounts now have seperate windows and keybindings
 - note - pet, mount and token data has been erased, you will need to login to each character at least once to update it
 - added - libdatabroker objects for pets and mounts
 - added - options to alter the display of empty slot status (under settings > empty slots)
 - fixed - comparison tooltip conflict

# 3.02.17 (05-AUG-2009)
 - changed - auto open options for mail and vendor disabled due to blizzard auto opening them anyway
 - changed - libdatabroker object for bag was renamed
 - changed - search text is now cleared after closing and re-opening the same window
 - changed - vault restacking is also now significantly slower but shouldnt generate any errors
 - changed - `GetSellValue( )` support changed to blizzard api
 - fixed - issue with guild bank and patch 3.2
 - possibly fixed - restacking issue where it occasionally got stuck in an infinite loop
 - updated - all locales to version 3
 - updated - ruRU, zhCN locales, copied translations from esES to esMX to use as a starting point
 - added - libdatabroker objects for ammo, money and currency
 - removed - tooltip option for ilvl (now a blizzard option)
 - removed - tooltip option for vendor price (now a blizzard option)

# 3.02.16 (24-JUN-2009)
 - updated - ES locale for enchanting bags
 - fixed - potential issue for characters with no skills
 - changed - framelevel bugfix option is now enabled by default, notification set to silent
 - added - esMX locale (although it's empty and needs a translator)

# 3.02.15 (28-MAY-2009)
 - fixed - issue with incorrect custom tooltip data being added to comparison tooltips (eg, the same data for the main tooltip was being added to the comparison ones)
 - changed - `outfit( )` rule function now supports blizzard equipment manager, outfitter and itemrack addons have priority (if installed) - poor quality items are ignored as the trash category has a higher priority

# 3.02.14 (13-MAY-2009)
 - fixed - potential issue for characters with no skills as well as issues where a players skills werent being scanned on load

# 3.02.13 (06-MAY-2009)
 - updated - TW locale for soulshard bags
 - fixed - issue with restacking when you had the same type of profession bag in your inventory as well as already equipped in a bag slot
 - fixed - issue with tooltips for tokens not adding item counts (you will need to log into each character to update them)
 - fixed - issue with tooltips not adding item counts when hovering over currencies at merchants (honor and arena points still wont work)

# 3.02.12 (28-APR-2009)
 - fixed - (potentially) issue with font sizing caused by "not a number" and exceedingly small values < 1
 - updated - ES locale for inscription
 - added - support for `CUSTOM_CLASS_COLORS` (its not used to a great extent in AI though)

# 3.02.11 (18-APR-2009)
 - info - all cached item data has been cleared - you will need to login to each character for AI to rebuild their data
 - fixed - issue with internal player id's causing options and saved data to not work correctly, along with lots of other stuff
 - added - mouseover a gold will now popup a list all gold for all characters (guild banks not included)

# 3.02.10 (16-APR-2009)
 - fixed - issue with bags having a "no entry" image across them (caused by blizzard equipmentmanager changes)
 - updated - deDE locale
 - updated - toc to 30100
 - changed - player data is now stored per faction/realm instead of globally (ie you will only be able to see data for alts from the same realm and faction)
 - changed - tradeskill scanning method

# 3.02.09 (20-FEB-2009)
 - fixed - issue with search window not displaying item name when the wow item cache is reset (eg after a game patch)
 - fixed - empty inscription slot type added to menu
 - fixed - empty unknown slot type code

# 3.02.08 (xx-NOV-2008)
 - fixed - issue when enabled if the blizzard windows were already open, they will now be closed when AI is enabled
 - fixed - issue with debug info causing an error for key slots
 - fixed - locale zhTW

# 3.02.07 (23-NOV-2008)
 - fixed - lag related issue with unuseable tint being applied incorrectly after disenchanting an item
 - fixed - frFR locale
 - fixed - lag and memory issues on search window, scrolling should be significantly faster
 - added - item age (replaces new indicator) - may have issues with the age resetting

# 3.02.06 (16-NOV-2008)
 - fixed - issue with guild bank not always updating on first open
 - fixed - issue with guild bank not marking a newly purchased tab as active
 - updated - ruRU locale

# 3.02.05 (12-NOV-2008)
 - fixed - issue with framelevel workaround not kicking in when you change the value
 - fixed - click menu for ldb object now opens above or below object
 - fixed - issue with comparison tooltips if built via other mods
 - updated - frFR and koKR locales

# 3.02.04 (10-NOV-2008) BETA
 - fixed - issue with setting options showing what a location was using, not the actual setting
 - fixed - issue with upgrading category assignments prior to 3.02.01
 - fixed - issue with token icons not displaying
 - fixed - issue with restacking the bank
 - changed - all references (in xml files) to `this` changed to `self`
 - changed - reverted frame strata setting
 - changed - all external libs moved from the libs\ to the externals\ directory
 - added - libdatabroker object

# 3.02.03 (06-NOV-2008) BETA
 - fixed - issue with clearing search text when hiding the search frame
 - fixed - issue with the config option for hiding the title frame
 - fixed - issue with guild bank not always updating on first open
 - fixed - issue with guild bank not updating when trying to access tabs your alts are not authorised to access
 - fixed - issue with `/ai db reset confirm`
 - changed - frameStrata on all main frames set to HIGH
 - changed - rule function `bag( )` parameter is now numeric only, which bag number an item is in
 - updated - frFR, zhCN locales
 - added - rule function `location( )`, alias `loc( )`
 - removed - `loc( )` alias for rule function `bag( )`

# 3.02.02 (04-NOV-2008) BETA
 - fixed - added validation to all range values in config menu
 - fixed - item counts on other tooltips
 - added - search frame

# 3.02.01 (03-NOV-2008) BETA
 - fixed - issue with tooltip update not passing self reference
 - fixed - itemrack outfit issue (needs testing)
 - fixed - issue with empty slots staying white (when assigned a colour)
 - fixed - issue with mail items not having a quality border
 - fixed - issue with item categories not changing when profile is changed
 - fixed - issue with item anchor in config menu
 - fixed - issue with window not updating if "sort on window open" option was disabled
 - fixed - restored the sorting options for reversed names and ascending/descending sort
 - fixed - issue with override option in config menu not hooking/unhooking on change
 - fixed - issue with bank staying offline
 - fixed - empty slots not being categorised properly issue
 - updated - ruRU, deDE, zhTW locales
 - added - pet/mount location
 - added - token location
 - added - option to use class colours in tooltip item counts
 - added - custom category management to config menu

# 3.01.09 (17-OCT-2008)
 - fixed - ruRU locale issue
 - fixed - issue with settings for empty slot colours showing internal bag types
 - fixed - issue with settings for hiding the bag changer frame for windows that dont have a changer frame
 - fixed - profile issues
 - fixed - issue with switch character menu
 - changed - switch character menu reduced to two levels to make it easier to use

# 3.01.08 (15-OCT-2008)
 - fixed - issue with dropping BoE bags onto changer slots, should now prompt to confirm binding
 - fixed - issue with empty slots not changing categories when changing the clumping setting
 - changed - TOC set to 30000

# 3.01.07 (14-OCT-2008) BETA
 - fixed - issue with option menu
 - fixed - issue with rules and search window scrolling
 - added - category: consumable > food & drink (for combined health/mana foods & drinks)

# 3.01.06 (28-SEP-2008) BETA
 - fixed - issue with status window not updating consistently
 - fixed - issue wth `stacks( )` rule function
 - changed - repuation items are now checked for after most other categories
 - changed - deafult category assignment has been removed from the saved variables and uses an internal cache instead

# 3.01.05 (26-SEP-2008) BETA
 - fixed - issue with mailbox item counts

# 3.01.04 (25-SEP-2008) BETA
 - fixed - issue with empty slot colours in options menu
 - fixed - issue with offline items being tinted red
 - fixed - issue with the default character for the guild bank window
 - fixed - empty tooltip line option was adding two lines
 - fixed - RU locale file (engineering skill)
 - fixed - issue with guild bank showing as offline when it wasnt
 - fixed - issue with guild bank restack permission check (you only need view and deposit to restack)
 - changed - `quality( )` rule funtion to allow for level 7 / heirloom (bound to account) items
 - added - rule function `stacks( )`
 - added - rule function `count( )`

# 3.01.03 (26-AUG-2008) BETA
 - fixed - removed duplicate entries in some locale files
 - fixed - usable rule function
 - fixed - item tinting works again
 - fixed - inscription empty slot colour
 - fixed - tooltip issue for empty slots when adding an empty line was enabled
 - added - categories for battle and guardian elixirs

# 3.01.02 (24-AUG-2008) BETA
 - changed - cleaned up categories and locales
 - changed - search, rules, location and switch character icons on menu
 - fixed - localisation issue on bar and item menus
 - fixed - guild bank when in edit mode now only displays items from the current tab

# 3.01.01 (21-AUG-2008) BETA
 - fixed - issue with guild bank when you dont have any tabs purchased
 - fixed - instant sorting now works again
 - fixed - issue with vendor amount not displaying properly for some values
 - added - tooltip option to display item count just for the current character

# 3.01.00 (20-AUG-2008) BETA
 - fixed - issue with gold amount not displaying properly if you had gold coins but the silver coins were zero
 - fixed - issue with guild bank display not updating correctly when changing between modes
 - changed - TOC lowered to 20400 and code changed to work with the live servers

# 3.00.06 (19-AUG-2008) BETA WotLK
 - fixed - `outfit( )` function for itemrack compatibility
 - fixed - upgrade code error
 - fixed - issue with bar labels not being deleted when you delete a bar
 - changed - `/restack` is now `/ai restack` (until i can figure out how to put it back)
 - changed - menu system (nearly complete)

# 3.00.05 (18-AUG-2008) BETA WotLK
 - changed - menu system

# 3.00.04 (17-AUG-2008) BETA WotLK
 - added - skill > inscription category
 - fixed - bar functions > remove, clear
 - changed - default category assignment code altered slightly (most soulbound items should now categorise under their normal category)
 - changed - MOUNT category converted to SKILL > RIDING
 - changed - most libraries are now ace3
 - removed - FrameLevel bug fix code made user configurable, disabled by default

# 3.00.03 (13-AUG-2008) BETA WotLK
 - info - locale files are back in but the text is not completed
 - fixed - `MoneyFrame` self parameters
 - fixed - display issue at bank when purchasing a new bag slot
 - fixed - self parameter in `UIDropDownMenu` for config panel
 - fixed - issue with upgrade code

# 3.00.02 (12-AUG-2008) BETA WotLK
 - fixed - search window, scrolling frame
 - fixed - rules window, scrolling frame
 - fixed - rules window, rule formula entry

# 3.00.01 (12-AUG-2008) BETA WotLK
 - info - all cached item data has been cleared - you will need to login to each character for AI to rebuild their data
 - info - locale files disabled until text is completed
 - fixed - ES locale file
 - fixed - DE locale file
 - fixed - issue getting a "you are not in a guild" error message (usually on logout)
 - fixed - issue with vault item tooltips
 - fixed - issue with socketing window
 - fixed - display issue when empty slots were manually assigned to another category
 - fixed - items can be dropped onto the bank "bag" icon
 - added - custom categories
 - added - new rule function: `usable( )` - if an item can be used/worn by the user
 - added - un-usable items can now be tinted red if desired via menu > items > tint unusable
 - added - restack will now function against the current tab for the guild bank (it's slow though)
 - added - RU locale file
 - added - options menu via blizzard addon interface (work in progress)
 - added - `/ai config`
 - added - `/restack`
 - changed - database structure
 - changed - reduced memory usage during scanning
 - changed - empty slots only have a default category, they can no longer be assigned to a system or custom category or a rule
 - changed - restack will sequentially process all locations (instead of having a seperate button for each location)
 - removed - rule function: `empty( )`

# 2.27.09 (17-AUG-2008)
 - fixed - RU locale issue causing bag slots to be red (unknown)

# 2.27.08 (14-AUG-2008)
 - fixed - category issue for non soulbould items that require the riding skill

# 2.27.07 (13-AUG-2008)
 - added - RU locale

# 2.27.06 (15-MAY-2008)
 - fixed - issue when moving hidden categories to another bar
 - fixed - issue with saved window positions when scaled
 - fixed - issue with empty slots not being re-categorised when changing "clumping" mode

# 2.27.05 (06-MAY-2008)
 - fixed - locale files

# 2.27.04 (05-MAY-2008)
 - added - guild bank item and money logs (via right click menu on tab icons)
 - added - remaining daily withdrawals shown on guild bank tab tooltip
 - added - monitor option to completely disable monitoring changes at a location
 - fixed - issue with offline data cleanup routine
 - fixed - data is now purged when you leave the mailbox, bank and vault if you dont have them set for offline
 - fixed - issue when using standalone libraries
 - changed - status menu replaces/combines the monitor (new), offline, and hide blizzard menus
 - changed - monitor, offline and hide blizzard options are set per character
 - changed - menu now includes the switch character and location options if the title frame is hidden
 - changed - bucket timer increased to 0.5 seconds (item changes/moves wont update for that long)

# 2.27.03 (10-APR-2008)
 - info - all cached item data has been cleared - you will need to login to each character for AI to rebuild their data
 - added - emblem font
 - added - wearing window
 - added - mailbox window
 - added - keybindings for mailbox and wearing
 - fixed - warning message from guild bank when you dont have view access to the current tab but another alt does (and it tried to scan it)
 - fixed - tooltips for items on unviewable tabs
 - fixed - dressup and compare abilities on guild bank items
 - fixed - issue with wearing data
 - fixed - issue with debug info
 - fixed - issue with generic scanning code
 - fixed - bag tooltips now go under the icons so they don't overlap any item icons above them
 - changed - libsharedmedia (font/texture library) from version 2 to 3
 - changed - guild bank data retrieval from server
 - changed - search window will now search as each character is entered
 - changed - search window width increased slightly
 - changed - rule window will now search as each character is entered
 - changed - title window layout
 - changed - window width, minimum from 8 to 6, maximum from 32 to 40

# 2.27.01 (27-MAR-2008)
 - fixed - error in line 2701: attempt to compare nil with number
 - fixed - font style for new item indicators
 - fixed - issue with bar labels being placed incorrectly
 - fixed - search frame, focus is now set to filter field
 - changed - toc updated to 20400
 - changed - (restack and) compress uses the new blizzard api to figure out if an item can go in a profession bag
 - added - rule function bag( bag_number )
 - added - rule function vpo( copper ) - vendor price over ( copper ) a specific copper amount (per current stack size)
 - added - rule function vpu( copper ) - vendor price under ( copper ) a specific copper amount (per current stack size)
 - added - unknown category (for when you dont have item data cached), moving an item to another slot or clicking on menu > actions > reload should update the data from the server

# 2.26d (04-FEB-2008)
 - fixed - cleaned up fonts in xml
 - fixed - nil bag errors
 - fixed - zero padded the rule numbers so they sort "numerically" in the menus
 - fixed - issue with 2.08 upgrade code, nil category
 - fixed - layout issue where everything collapsed into a single bar (still happens occasionally in guild bank)
 - fixed - search menu text in keybindings menu wasnt set
 - fixed - openallbags will now toggle properly
 - changed - outfit code for itemrack 2.1 (previous versions will no longer work)
 - changed - guild bank will now only show a single tab
 - changed - layout of title bar icons and added search
 - added - empty bag slot counts to bag icons via menu > empty > show count
 - added - font colour options for empty bag slot counts
 - added - font option for all text
 - added - font, scale and border options to rules window
 - added - font, scale and border options to search window

# 2.26b (09-JAN-2008)
 - fixed - TOC issue

# 2.26a (09-JAN-2008)
 - fixed - moneyFrame issue for tooltip
 - removed - waterfall menu (keeping two menus systems in sync was a pain, i'll fix it properly when/if a new menu system comes out)
 - added - option to select ascending or descending sort order
 - added - window borders, options to hide/show, change texture and scale
 - added - bar borders, options to hide/show, change texture and scale

# 2.25b (08-JAN-2008)
 - fixed - nil realm issue
 - fixed - nil bag issue
 - fixed - issue with clearing the item cache

# 2.25a (06-JAN-2008)
 - added - item borders, option to hide/show, change texture and scale

# 2.24g (04-JAN-2008)
 - added - item (stat) level to sorting options

# 2.24f (01-JAN-2008)
 - fixed - vendor price tooltip issue
 - fixed - rule changes were not being applied until an item was moved and the window refreshed, they're now instant
 - added - vendor and item count info added to tooltip for clicked links

# 2.24e (25-DEC-2007)
 - fixed - display issue with backback not showing number of slots when first starting wow
 - fixed - clicking on a blizzard bag icon wouldn't open or toggle the window
 - changed - all references of `getglobal( )` to `getfenv( )[]` to remove some taint issues
 - changed - tooltip now shows the vendor price for the (partial) stack, not the single item vendor price
 - changed - tooltip item counts, guild banks are now shown first then characters
 - changed - tooltip item counts no longer include guild bank items in totals
 - added - keybinding for rules window
 - added - keybinding for search window
 - added - support for `GetSellValue( )` function - should use any other mod that stores vendor pricing (eg sellfish, informant)

# 2.24d (21-DEC-2007)
 - fixed - issue with wow global variable `ITEM_MIN_SKILL` having a different parameter layout for german client

# 2.24c (21-DEC-2007)
 - incorrect version uploaded

# 2.24b (20-DEC-2007)
 - fixed - error in DE translation file
 - fixed - included waterfall library
 - added - search function (requires tooltip count to be enabled) (not fully complete)

# 2.24a (20-DEC-2007)
 - fixed - error: attempt to index local 'b' (a nil value)
 - fixed - issue with skills when you opened the skill window and collapsed a heading, AI would not be able to see any of your skills under that heading which could then place items in the wrong category
 - fixed - display issue where right clicking an item to wear it would leave the old item (now in your bag) appearing as if it were locked (greyed out)
 - fixed - guild bank can split items (and accept deposited money that way as well)
 - fixed - bar edit icon locations adjusted to allow for item anchor setting
 - fixed - issue with other mods automatically opening bags
 - fixed - various "weird" issues due to non local variables
 - changed - "new item indicator" no longer global, now per settings option under "menu > items > new"
 - changed - "remember offline data" no longer global, now per character (enabled by default) "menu > offline > ...."
 - changed - "fade offline" no longer global, now per settings option under "menu > items > fade"
 - changed - window anchor points are now per window per profile (all anchor and position data has been reset to default)
 - changed - cached data layout
 - changed - bag scans are now instant when a change happens
 - changed - item sorting/categorisation, should be faster
 - changed - guild bank data is now stored under the guild name - if you have more than one character in the same guild then the data will be from the last one to access the vault
 - changed - switch character menu is now class colour coded
 - changed - switch character menu only shows characters that have data for the current window
 - changed - switch character menu now includes guild banks
 - changed - ammo slots now have a different empty slot icon to make them more obvious
 - changed - status window now shows the currently displayed characters gold (guild bank status always shows total guild bank gold)
 - changed - sortkey (internal data) no longer saved into saved variables file
 - added - "menu > window > anchor > lock position", you can now stop each window from being moved
 - added - waterfall menu (can be assigned a keybinding), not complete
 - added - "menu > tooltip > enabled", enable/disable tooltips - enabled by default
 - added - "menu > tooltip > show item count", show item counts and where they are located - enabled by default
 - added - "menu > tooltip > colour", change the colour of the item count text added to the tooltip - orange by default
 - added - edit mode: "menu > bar > move this bar up", swaps categories on this bar with the one above
 - added - edit mode: "menu > bar > move this bar down", swaps categories on this bar with the one below
 - added - bags slot count to bag icon in changer window
 - added - ability to hide or show the contents of a bag via right click menu on the bag in the bag changer window.  hidden bags are tinted red. this is a per character setting.
 - upgraded - periodictable library to 3.1 (copied the item search code from 3.0 so it can display what sets an item is in - may not work as well)
 - info - all offline data has been erased - you will need to login to each character for AI to pick it up again
 - info - you may need to logout/login or do a `/RL` after a profile is upgraded (if it errors when opening a window)

# 2.12d (22-NOV-2007)
 - changed - header, bag changer and status frame hiding is no longer global, it is now a per settings option under "menu > window > hide frames"
 - changed - "menu > hidden frames" changed to "menu > hide blizzard"
 - fixed - error when changing gear, should ignore those item locks now
 - added - "menu > items > anchor"

# 2.12c (19-NOV-2007)
 - added - `/ai misc alert { disable | short | long }` - defaults to long
 - added - `[class:level]` text to switch character menu.  will only update on login of each character
 - fixed - issue with sorting options not showing up

# 2.12b (17-NOV-2007)
 - fixed - issue with upgrade, was hiding all the ai windows
 - changed - some localisations and their menu options
 - changed - guild bank is now disabled default, you will need to enable it to use ai for the guild bank

# 2.12a (17-NOV-2007)
 - fixed - frame anchor bug
 - fixed - frame anchor point will now stay in place when the windows are rescaled
 - fixed - window will now stay in place when the anchor point is changed
 - fixed - guild bank, if you have view but not deposit access items will now fade and you won't be able to click on them (deposit access allows you to move items around on the tab but not remove them)
 - changed - you can now hide each blizzard frame seperately - old hidden frame values have been erased so you will need to change them if required
 - changed - handling of blizzard api hooks, most of the open functions are now toggle functions
 - added - partial gm functionality for guild banks - vault tab right click options are now available to change the icon and name, change only appear on the next item update (should be instant, still trying to figure out why)
 - added - total guild gold, available guild gold, deposit and withdrawl buttons (in the guild bank changer frame)
 - added - workaround/fix for "everything going black" - will recalculate all frame levels for all elements when the window is greater than 126.  may cause a 1-5 second lag spike when it does the fix (which will only occur when you open the window)

# 2.11a (15-NOV-2007)
 - fixed - display issue where everything would stop updating after zoning

# 2.11 (15-NOV-2007)
 - updated - TOC to 2.3
 - fixed - display issue where window width was ignored
 - fixed - display issue where a single item in the first bar of a row would have extra space
 - changed - window settings management
 - removed - hardcoded xml elements - will use less up front memory but be slower to load the first time
 - added - guild bank (it's slow and just has basic item functionality)
 - added - window anchor point

# 2.10g (03-NOV-2007)
 - added - more debug code
 - added - more localisation text
 - changed - hard coded font name changed to internal game font reference
 - changed - uses embeds.xml for embedded libraries

# 2.10f (13-OCT-2007)
 - fixed - error when changing gear or bags, will generate an error when an invalid bag id is passed in

# 2.10e (11-OCT-2007)
 - fixed - display issue when bags are opened for the first time (and the window is scaled)
 - added - debug output to trace an issue where bags are not updating

# 2.10d (08-OCT-2007)
 - changed - minimum window width set to 400 (reduced from 500) - purchase button will overlap the last two slots
 - fixed - possible error during conversion of data from pre 1.3 versions
 - fixed - error when changing gear or bags

# 2.10c (05-OCT-2007)
 - added - chat links now work for the bags in the bag changer window
 - fixed - korean locale issue

# 2.10b (28-SEP-2007)
 - fixed - added logic checking around a possible error
 - reverted - hardcoded xml elements are back in, blizzard didnt fix the background issue

# 2.10a (not released)
 - never actually existed, made a typo on one of the upload sites

# 2.10 (26-SEP-2007)
 - changed - various code and xml changes for 2.2

# 2.09a (23-AUG-2007)
 - fixed - cosmetic issue with the cursor when a merchant window is open and the AI window is in edit mode
 - fixed - issue with outfitter being called before it's initialised

# 2.09 (22-AUG-2007)
 - added - bag changer now can be used offline to see what bags your alts have
 - fixed - potential issue when changing profiles, previous characters items could be left displayed
 - fixed - issue when clearing the cache and then opening the bank window
 - changed - offline cache is now cleared via `PLAYER_LEAVING_WORLD` and not `PLAYER_LOGOUT` - potential fix for an issue where the cache was being incorrectly cleared on logout

# 2.08c (08-AUG-2007) - fixed - game tooltip issues (compare tooltip and compare/inspect icons)

# 2.08b (07-AUG-2007) - fixed - potential rule issue - fixed - localisation problem with sorting menu text

# 2.08a (06-AUG-2007) - fixed - instant sorting - fixed - edit mode key binding - fixed - rules, no longer need to be enabled/disabled to work

# 2.08 (05-AUG-2007) - changed - instant sort is no longer forced on when the bag changer frame is open - but it's still slow to do anything while this frame open (due to lack of events for bag changes) - changed - sped up the majority of the colour/display options - changed - sorting options are now coloured to make it more obvious which options have been included and which ones haven't.  the tooltip text has also been updated as well. - changed - rules view increased to display 15 rows - changed - soulbound checking should work better for all languages - fixed - player bag changer functionality works a bit better, you can drop things onto the backpack icon and the item will be placed into the backpack (if there's space) - fixed - bank bag changer functionality works a bit better, you can drop things onto the "bank" icon and the item will be placed into the bank (one of the 28 bank slots) (if there's space) - fixed - scanning tooltip should now build a complete tooltip when processing rules - added - clicking on a bag (in the blizzard bag frame) will now toggle AI (when the blizzard frames are set to hidden) - restored - you can assign items to system categories - takes precedence over rules - info - keybindings may need to be redone

# 2.07a (23-JUL-2007) - fixed - macs should no longer crash when opening the rules window (thanks go to 'ShinyToaster' for finding the error in the xml)

# 2.07 (19-JUL-2007) - changed - recoded tab and shift+tab to work in all fields when editing a rule - changed - sort order is now totally user customisable - fixed - spanish translation for the herbalism skill - fixed - items will now categorise properly after changing profiles

# 2.06 (12-JUL-2007) - info - all cached item data has been cleared - you will need to login to each character for AI to rebuild their data - fixed - an issue with item id's not being built properly during bag scans - fixed - an issue with the upgrade code - fixed - new item text, centered text, should be able to swap same id items without them being tagged as new

# 2.05 (11-JUL-2007) - added - "clear this bar" - an edit mode option to remove all categories from a bar - fixed - menu option to clear cached data for a character wasn't showing up - changed - xml elements on rule frame - hopefully will stop opening the rules window from crashing macs - added - new item status text - changed - number of rows in rules window increased from ten to twelve - added - rule menu option to hide disabled rules - fixed - error in sort code

# 2.04 (08-JUL-2007) - fixed - `RULE_PATTERN_ITEMNUMBER` issue with upgrade code - added - chinese translation (thanks candykiss)

# 2.03 (05-JUL-2007) - updated - closetgnome `outfit( )` code - added - rule function `ilvl( )` - added - rule function `ireq( )` - added - rule function `sb( )` alias for `soulbound( )` - added - rule function `tt( )` alias for `tooltip( )`

# 2.02 (02-JUL-2007) - fixed - disabling a rule via shift+clicking will now update the window - changed - include category in sort will now sort by rule order then rule number - fixed - closetgnome `outfit( )` code

# 2.01 (02-JUL-2007) - fixed - conversion of negative items

# 2.00 (02-JUL-2007) - fixed - itemrack outfit code (note you need to use the v2.0 beta of item rack) - added - shift clicking on a rule toggles enabled/disabled

# 2.00 (30-JUN-2007) (beta-2007-JUN-30-12-00) - warning - beta users will lose any rules they had, you can restore your 1.45 file and it will convert to the new format (if you know what you're doing you can edit the savedvariable file and move the rule data to the account location - make a backup) - fixed - rules are now global and can be enabled/disabled per profile, default is disabled - fixed - options to remember bank and alt data are now global and have been reset to default - fixed - options to auto open/close are now global and have been reset to default - fixed - options to hide the frames are now global and have been reset to default - fixed - fade offline option moved from item to offline menu, now global and has been reset to default - fixed - changing profiles will now work properly

# 2.00 (28-JUN-2007) (beta-2007-JUN-28-21-45) - fixed - bank items not updating their icons when moved out - added - items can be added to existing (enabled, undamaged) rules when in edit mode by clicking on the item and choosing "add to rule" - note that it's currently possible to have that rule open in edit mode so if save it then your edit mode item changes will not be there any longer - added - bag highlighting, when you mouse over a bag the slots in that bag are highlighted - added - menu option (under window) to change the bag highlighting colour - info - removed the exclamation marks from all the text

# 2.00 (25-JUN-2007) (beta-2007-JUN-25-22-00) - info - a lot of text has exclamation marks at the start - they're just temporary so i know which ones have been set up for translation - fixed - empty slot background icon - added - empty slot border colouring - changed - empty slot background colouring - changed - empty slot menu moved to main menu - fixed - items in hidden categories now show up in edit mode - fixed - bank and keyring items were picking up backpack items - fixed - compress and restack, would start but then stop after the first item merge

# 2.00 (24-JUN-2007) (beta-2007-JUN-24-02-00) - fixed - equip location sorting (will only effect equipable items now) - changed - hard coded in xml - bags, bars and items as a workaround for the grey problem. items above the hard coded limits will still be auto-created in code but these *will* be susceptible to the issue until blizzard can fix it - changed - slightly increased the thickness of the item borders

# 2.00 (21-JUN-2007) (beta-2007-JUN-21-20-30) - fixed - error in upgrade code for item id's - fixed - closetgnome outfit code - fixed - error in all non english locales

# 2.00 (20-JUN-2007) (beta-2007-JUN-20-22-45) - fixed - error in upgrade code (only impacted new or cleaned installs) - fixed - rule function `name( )` - added - rules are now validated before being saved - changed - `item( )` is now `id( )` - existing rules will just get damaged and stop working until you edit and change them to use the new function name - changed - `itemtype( )` is now `type( )` - existing rules will just get damaged and stop working until you edit and change them to use the new function name - changed - `itemsub( )` is now `subtype( )` - existing rules will just get damaged and stop working until you edit and change them to use the new function name - changed - rule description length increased from 20 to 80 characters

# 2.00 (18-JUN-2007) (beta-2007-JUN-18-21-15) - fixed - closetgnome outfit code - fixed - tooltip code (causing default categories to not work) - fixed - default categories - class (translators may need to update `WOW_TOOLTIP_CLASS`) - fixed - default categories - skill (translators may need to update `WOW_TOOLTIP_REQUIRES`) - changed - switched to blizzards strtrim function

# 2.00 (18-JUN-2007) (beta-2007-JUN-18-18-45) - fixed - issue where disabled rules would become enabled after a reload - fixed - default categories were wrong because of the new tooltip code - fixed - rule function `soulbound( )` - fixed - rule function `tooltip( )` - added - closetgnome linked to `outfit( )`

# 2.00 (17-JUN-2007) (beta-2007-JUN-17-20-45) - removed - `bagnum( )`, `slotnum( )` and `container( )` rule functions - until i can sort out a way to make them usable (they slow everything down too much) - fixed - rule function `tooltip( )` - fixed - rule function `equip( )` - added - rule function `quality( )` - added - rule function `outfit( )` - added - outfitter linked to `outfit( )` - added - option to enable/disable a rule - added - a rule will be flagged as damaged and no longer used if there is an error with it - changed - rule dialog box layout updated - removed - gratuity library

# 2.00 (17-JUN-2007) (beta-2007-JUN-17-??-??) - changed - debug menu, formatted the information the way it's required by the rules - fixed - rule function `item( )`

# 2.00 (16-JUN-2007) (beta-2007-JUN-16-12-30) - fixed - `container( )` should now work properly in rules - fixed - german translation file

# 2.00 (16-JUN-2007) (beta-2007-JUN-16-00-30) - info - all cached item data is erased - you will need to login to each character for AI to pick it up again - added - rules for category management - fixed - skinning and leatherworking spanish translations

# 1.45 (08-JUN-2007) - fixed - bar frames/borders will display in edit mode when hidden - fixed - PT set information on the debug window, will no longer generate an error when an item is not in any PT sets

# 1.44 (07-JUN-2007) - added - option on debug menu to see which PT sets an item is in

# 1.43 (07-JUN-2007) - fixed - player skills were only being read from the first character to login which effected default categorisation, they are now read every time a skill or profession changed (including at login) - added - option to hide the bar frames (to help get around the issue where DHUD appears to be pushing their frame levels too far up and my bar frames are ending up above the item frames)

```
  an alternate fix you can try - but will probably come back up if you have DHUD still loaded

  load up your character and open your bags, bank and keyring (doesn't matter if they're offline) and then enter the following into the chat window (one line at a time - copy and paste it)

  /script ARKINV_MainFrame1:SetFrameLevel( 3 )
  /script ARKINV_MainFrame2:SetFrameLevel( 3 )
  /script ARKINV_MainFrame3:SetFrameLevel( 3 )

  logout, log back in
```

# 1.42 (06-JUN-2007) - fixed - sorting (offline bug) - fixed - tooltips for empty offline items were showing values

# 1.41 (05-JUN-2007) - fixed - custom PT categories - fixed - soul shard categorisation - changed - categorisation, custom categories are checked first then PT categories second - fixed - potential problem with restack code - added - restack now puts items into empty special slots, eg bullets in a normal slot will get moved into an empty ammo slot (if one is available) - removed - soulbound equipment subcategories - use the sort>include location option to sort them properly

# 1.40 (04-JUN-2007) - added - icon to restack on main window - added - ability to include equipment location/type in sort (default is true) - added - ability to use reversed names in sort (default is false) - changed - default value for quality sort is now true - changed - default value for instant sort is now false - added - ability to use PT categories as "custom" categories.  Custom PT categories have first priority when items are being categorised. - added - keybinding for restacking bags - changed - edit mode, bar tags are larger - changed - various xml layout changes - added - korean translation (thanks fenlis)

# 1.39 (01-JUN-2007) - added - item restacking

# 1.38 (31-MAY-2007) - added - shift click to link in chat for offline items - added - control click to dress up with offline items

# 1.37 (30-MAY-2007) - removed - shift click to link in chat for offline items - brought back original security issues

# 1.36 (29-MAY-2007) - added - shift click to link in chat now works for offline items

# 1.35 (27-MAY-2007) - updated - using PeriodicTable 3.0 (hopefully it's embedded properly) - fixed - offline, bank and keyring tooltips are back (cooldown timer based tooltips may not update while open) - fixed - TW locale (removed PT translations - they shouldn't be in there)

# 1.34 (21-MAY-2007) - updated - TOC to 2.1 - added - traditional chinese translation (thanks mcc/chuanhsing)

# 1.33 - updated - french translation (thanks Dutorien)

# 1.32 (13-FEB-2007) - added - spanish translations (thanks shiftos) - fixed - riding skill name in french translation - added - compact mode for bars - ensures a fixed number of bars per row by compacting empty bars out

# 1.31 (12-FEB-2007) - added - option for internal bar padding - added - option for window padding - fixed - cooldown timers are back - added - toggle icons for edit, refresh, bag change on main window - added - tooltip text to icons so you can tell what they do - changed - if the blizzard frames are not hidden then AI will not appear at all. use keybindings to bring up AI when blizzard frames are active.  auto-open options are ignored but auto-close options are still used.  will probably have to move this to the parent menu so it's more obvious now. - added - option to set bar anchor corner - added - default category caching - should speed things up hopefully (thanks Miles) - updated - DE translations (thanks Maischter) - added - FR translations - fixed - bars that had a category assigned but no items would not always appear in edit mode

# 1.30 (not released - betas only) - fixed - clicking on a bag (in the blizzard bag frame) will now toggle AI - it was being ignored previously - unfixed - clicking on a bag is back to being ignored, it was annoying when you clicked on a bag in the AI changer frame it would close AI, not fun - changed - the way item buttons are created, stops various stack split and drag-n-drop issues from happening - added - windows won't stay off screen if you move them there (it will if you are on an edge and go into edit mode - no idea why, the frame just wont move for some reason) - added - most options are now set per window, with an option to use common settings (enabled by default) - fixed - a menu issue when moving a category via the item menu, would snap back to it's original bar after you moved it and used the menu again - changed - minimum bars reduced to 1

# 1.29 (07-JAN-2007) - fixed - issue when closing the bank, you cant reopen it until you get out of range and then come back - added - instant sort option so if you don't want things automatically being moved around while the window is open you can turn it off - changed - frame title layout - removed - option menu icon - added - option menu to main icon - added - bag change frame (note, if this frame is visible, instant sort is forcibly enabled so as to cater for issues that can arise when swapping bags and not updating the window, hide the frame when you don't need it so that instant sort can be disabled) - fixed - issue with keybinding for edit mode when at the bank

# 1.28 (04-JAN-07) - fixed - misspelt first aid category - added - more default item categories - added - you can hide the header frame as well now - added - bank frame hides now - added - window widths are now unique, you can have the bank at 18 wide and the bag at 10

# 1.27 (01-JAN-2007) - fixed - incorrect bars and items could end up displayed if you were looking at a window and erased the cache, or when you switched to an alt with no data - added - displays faction in title and alt dropdown (requires you to login to each character for it to update) - added - the alt dropdown list is now sorted - fixed - issue with no data showing for alts, you will have to log back into those alts for their data to get cached again then it should be ok - fixed - internal item id wasn't picking up the item suffix - fixed - empty slots in offline mode could sometimes show a tooltip for the active users bags/slot instead - added - can "restore" deleted custom categories (they come back as just the number so you'll need to rename them afterwards) - added - more default categories - via periodic table - i still don't like it though :) - fixed - choosing categories in other languages should now work - added - options to display the main window borders and change their colours as well - added - option to hide original blizzard bag frames

# 1.26 (29 DEC 2006) - item format has changed, added suffix and soulbound, it should convert items for you, soulbound items will need to be re-categorised - item format has changed, added enchant, it should convert items for you, enchanted items will need to be re-categorised - cache layout has changed - please use `/arkinv cache erase confirm` to erase all cached data - it wont erase your options - added - ability to hide categories - added - ability to globally override hidden categories so they get displayed - added - option to stop keeping offline data, sanity this is not, nor is it trying to be - added - status display now shows different slot types not just empty/total - updated - changed toc to allow for working without the embedded libraries - added - separate windows for each container (bag, keyring, bank - that can be active at the same time) - added - keybindings to toggle bag, key, bank windows - warning, opening the windows for the first time in a session will spike memory usage in a big way - lots of bug fixes but lots of code changes as well - fixed - ammo categorisation into bullets/arrows, didn't realise they were treated differently - added - some more default categorisations (need to find a way to get a players professions to make it better) - added - adding / renaming / deleting custom categories - removed the default 9 custom categories

# 1.24 (25 DEC 2006) - modified the bar edit menus so when choosing which categories you want to assign it colours those already assigned to other bars (and displays the bar it's currently assigned to) - added window background colour choice, including opacity - added opacity back as a user configurable option for bar backgrounds - added options to auto open/close at bank, auction house, trade, merchant, mailbox - added quality coloured borders and the backdrop icon, enabled the menu for it - fixed a bug in empty item clumping, also moved the menu from window to item - fixed a bug with opacity resetting when you go to change it - fixed a bug with moving bags from bag slots directly to the bank and vice versa

# 1.23 (24 DEC 2006) - added window scaling in options menu - added choice of slot backgrounds, icon or coloured - fixed a problem with categories and soulbound items in edit mode - still affects items in offline mode but not much i can do as you don't have any access to the actual item to see if it's soulbound - fixed a problem with items in bank slots losing tooltips when online - added a SOULBOUND EQUIPMENT category to differentiate between equipment picked up and stuff bound to you. items wont go into this category until you are online with the character - added an item option to desaturate offline items (they fade to grey) - on by default - added keybinding to toggling open/close

# 1.21 (22 DEC 2006) - bag | key | bank display added - location changes done via clicking on the small bag | key | bank icons next to the main icon - "offline" viewing of alt bag | bank | key added - change alts via the dropdown at the start of the name - `/arkinv cache erase confirm` - added to erase all cached data (not your options, just the item data for all characters)

# 1.20 (20 DEC 2006) - bug fixed for when at the bank - it would screw up all the bags - definitely fixed it this time

# 1.19 (20 DEC 2006) - bug fixed for when at the bank - it would screw up all the bags - bug fixed when resetting an items category back to it's default - bug fixed with default item categories - added more item default categories

# 1.18 (19 DEC 2006) - updated toc file - no other changes from 1.17

# 1.17 (19 DEC 2006) - edit mode working - menus for options, edit, bar, item menus added - category to bar assignment - item to category assignment - some default categorisation of items (needs to be worked on) - `/arkinv db reset confirm` (chat command to reset all options back to defaults - erases all item and bar customisation you have done) - autofit code changed to work a lot better

# 1.13 (14 DEC 2006) - Ace2 is now embedded - some options are now configurable via the command line - use `/ARKINV` or `/AI` - coloured empty slots are done - but not configurable yet (herb/green, ammo/orange, soul/purple and enchant/blue) - window defaults to 3 bars per row, 12 columns wide - default bars - ammo and empty ammo slots are grouped in bar6, all other empty slots are grouped in bar4, quest items in bar3 and everything else in bar1

# 1.10 (Initial Release) - Requires Ace2 (i didn't embed it) - does not hook the bag hook - it was made to work side by side with the bodgy conversion i did on enginventory to get that to work under BtS - you will need to create a macro with /arkinv gui and put that on an action to call this one - there are no user configurable options as yet - items are sorted by empty slots first then by item name in order of stack size - unlimited number of bars (there are practical limits though before your screen becomes full)
