# 3.10.33 Alpha 30 (03-AUG-2024)
 - disabled - context fading when at the guild bank as there seems to be a bug in the blizzard code and everything gets faded
 - fixed - all bags have had their display status reset to true

# 3.10.33 Alpha 29 (02-AUG-2024)
 - changed - the bank window will now only show bank bags when first opened. click on the bag changer slots to show items from the reagent/account bank
 - fixed - item context fading for bag items when you have the account or reagent bank open
 - fixed - issue with some empty slot border colours not getting applied
 - fixed - guild bank edit mode
 
# 3.10.33 Alpha 28 (01-AUG-2024)
 - fixed - https://github.com/arkayenro/arkinventory/issues/1941 - issue with ensemble tooltips and a possible delay to the data being returned
 - added - right clicking on a bag slot in the changer window at the bank will have a new option to isolate (only show) the bags that belong to the current panel (bank/reagent bank/account bank)
 - note - if you only want to see a specific account bank tab you can use the existing isolate option off the same right click menu
 - fixed - https://github.com/arkayenro/arkinventory/issues/1946 - scroll bar anchor points adjusted to properly fit the container window
 - added - support for account wide currencies
 - note - all saved currency data has been erased. please login to each character to update its data
 - added - support for account wide reputation
 - note - all saved reputation data has been erased. please login to each character to update its data
 
# 3.10.33 Alpha 27 (28-JUL-2024)
 - fixed - https://github.com/arkayenro/arkinventory/issues/1939 - issue with trash( ) / junk( ) rule function
 - added - category: system > equipment (warbound until equipped)
 
# 3.10.33 Alpha 26 (27-JUL-2024)
 - fixed - issue with item counts not being properly reset when moving items in and out of the reagent bank and reagent bag
 - fixed - issue with ItemCacheClear code
 - fixed - issue with ItemCacheClear and GetObjectInfo code looping through each other

# 3.10.33 Alpha 25 (27-JUL-2024)
 - fixed - https://github.com/arkayenro/arkinventory/issues/1937 - issue with right clicking on the reagent bank or an account bank slot in the changer window
 - fixed - https://github.com/arkayenro/arkinventory/issues/1936 - issue with paint all code
 - fixed - https://github.com/arkayenro/arkinventory/issues/1936 - issue with edit mode bar dragging

# 3.10.33 Alpha 24 (26-JUL-2024)
 - fixed - issue with bag changer code
 - fixed - issue with data erase code
 - fixed - https://github.com/arkayenro/arkinventory/issues/1931 - C_Spell.IsCurrentSpell replaces IsCurrentSpell
 - fixed - https://github.com/arkayenro/arkinventory/issues/1935 - potential issue with bag highlight code
 - fixed - https://github.com/arkayenro/arkinventory/issues/1936 - issue with mapping and storage code impacting rules (and other things)
 - fixed - https://github.com/arkayenro/arkinventory/issues/1937 - bag and bank saved data is invalid after the fixes in alpha 22
 - note - all saved bag data has been erased. please login to each character to update its data
 - note - all saved bank data has been erased. please login to each character to update its data

# 3.10.33 Alpha 23 (26-JUL-2024)
 - no longer available

# 3.10.33 Alpha 22 (26-JUL-2024)
 - no longer available
 
# 3.10.33 Alpha 21 (25-JUL-2024)
 - fixed - https://github.com/arkayenro/arkinventory/issues/1925 - issue with mailbox scanning
 - fixed - issue with action code
 - fixed - error output code
 - fixed - https://github.com/arkayenro/arkinventory/issues/1927 - issue with some tooltip generation
 
# 3.10.33 Alpha 20 (24-JUL-2024)
 - fixed - API changed from GetMouseFocus to GetMouseFoci
 - fixed - caged battlepets and pet tooltips displaying while scanning
 - fixed - bank window not opening when interacting with warband bank convergence (bank and reagent bank slots are currently visible but not usable)
 - fixed - warbank being in use should now show the locked tooltip and not prompt you to buy the next slot
 
# 3.10.33 Alpha 19 (23-JUL-2024)
 - fixed - (maybe) https://github.com/arkayenro/arkinventory/issues/1920 - issue with codex generation

# 3.10.33 Alpha 18 (22-JUL-2024)
 - removed - leftover debug output
 - fixed - (maybe) https://github.com/arkayenro/arkinventory/issues/1920 - issue with codex generation

# 3.10.33 Alpha 17 (21-JUL-2024)
 - fixed - (maybe) https://github.com/arkayenro/arkinventory/issues/1920 - issue with codex generation

# 3.10.33 Alpha 16 (21-JUL-2024)
 - no longer available
 
# 3.10.33 Alpha 15 (20-JUL-2024)
 - fixed - https://github.com/arkayenro/arkinventory/issues/1917 - issue with displaying data from other characters

# 3.10.33 Alpha 14 (18-JUL-2024)
 - fixed - https://github.com/arkayenro/arkinventory/issues/1917 - issue with switch character menu
 - removed - leftover tooltip debug output
 
# 3.10.33 Alpha 13 (14-JUL-2024)
 - fixed - https://github.com/arkayenro/arkinventory/issues/1916 - issue with profile import

# 3.10.33 Alpha 12 (13-JUL-2024)
 - fixed - https://github.com/arkayenro/arkinventory/issues/1910 - issue with mailbox scanning
 - fixed - item counts for recipes will now show correctly, not the count for the item they create
 
# 3.10.33 Alpha 11 (12-JUL-2024)
 - removed - vault changer action button
 - changed - the actions from the vault changer action button have been moved to a right click menu off the vault changer bag icons to be consistent with the other locations
 - fixed - account bank and vault tab name and icon assignment
 
# 3.10.33 Alpha 10 (11-JUL-2024)
 - fixed - issue with GetItemQualityColor being deprecated
 - changed - the status bar will only display gold amounts in the the bag, vault, and bank windows, all other windows will no longer display a gold amount.
 - added - warbank deposit and withdraw access is via the action button in the status bar
 - changed - guild bank deposit and withdraw access is via the action button in the status bar

# 3.10.33 Alpha 9 (09-JUL-2024)
 - fixed - (regression) issue with restack
 - fixed - (regression) issue with action code

# 3.10.33 Alpha 8 (09-JUL-2024)
 - fixed - (regression) issue with empty slot background
 - changed - empty slot icon/background config option
 - changed - (war within) the dragonriding/normal mount preference config option has been removed and is now determined by the skyriding/steady flight aura you have enabled at the time
 - fixed - (cata) on the very first login after game launch there is keyring bag update even though it no longer exists.  this is now ignored instead of generating an error.
 - fixed - (i think) https://github.com/arkayenro/arkinventory/issues/1910 - issue with API functions

# 3.10.33 Alpha 7 (07-JUL-2024)
 - fixed - (regression) guild bank scanning
 - fixed - (regression) account bank bags showing in dragonflight
 - fixed - transmog events had the wrong expansion assigned to them so were trying to load in earlier clients
 - note - all saved data for currency has been erased
 - note - (war within) currency and reputation are not currently supported
 
# 3.10.33 Alpha 6 (06-JUL-2024)
 - fixed - issue with switch character menu showing other realm menu when you only have characters on a single realm
 - added - timerunner identifier icon next to character names (will need to login to each timerunning character to update its status)
 - changed - (war within) C_Spell.IsSpellUsable( ) replaces IsUsableSpell( )
 - added - (war within) account bank access - account bank gold is not supported yet
 - changed - (retail) toc updated to 110002
 - changed - bag changer slots will now only show the first purchasable slot instead of all of them.  no config option to disable this yet.
 - note - all saved data for the bag, bank, and reputation, has been erased.  please login to each character to update its data
 
# 3.10.33 Alpha 5 (20-JUN-2024)
 - added - https://github.com/arkayenro/arkinventory/issues/1901 - handle multiple ids when manually adding items to a custom category
 - fixed - (regression) issue with mail action trying to add more than 12 items to a mail
 - fixed - (retail) API change from C_Item.GetItemIcon to C_Item.GetItemIconByID
 - fixed - issue with item data retrieval where under specific circumstances if it couldnt find the item it would loop forever instead of tagging it as dead
 
# 3.10.33 Alpha 4 (18-JUN-2024)
 - fixed - issue with right click delete action ignoring all action config options
 - fixed - issue with scrap action (it was seeing other players spell casts and trying to update too soon)
 - changed - when not at a merchant deleting an item will now require a shift+right click for safety purposes
 - changed - items used for pet/mount parts will now revert to their original category once you have learnt that pet/mount
 - added - (timerunning) config > general > tooltips > transmog - adds state information for sets/items to the tooltip
 - fixed - issue with mount cross reference data not getting loaded
 - updated - cross reference data for mount and pet updated to 10.2.7
 - added - (timerunning) LDB object for bronze tracking (uses the item count config options)
 
# 3.10.33 Alpha 3 (08-JUN-2024)
 - fixed - issues with some of the action code
 - fixed - (war within) mount icons

# 3.10.33 Alpha 2 (07-JUN-2024)
 - added - (war within) basic compatibility (there may be issues, lodge a ticket if you run into one)
 
# 3.10.33 Alpha 1 (07-JUN-2024)
 - fixed - https://github.com/arkayenro/arkinventory/issues/1899 - issue with junk icon not getting displayed when using the scrap addon


# known issues
 - restack has some issues, some of it works, some doesnt
 
 - some default frames (vendor/merchant at minimum) that would normally open via the PlayerInteractionFrameManager no longer open if you are in combat, you just get an addon error.  there is currently no workaround.
 - (dragonflight) reagentbank slots are no longer readable unless the bank is open
 - Enum.ItemConsumableSubclass is missing the Flask entry and everything after has moved down a value which screws up the category names (have hardcoded a workaround for the moment)
 - items with an active cooldown dont allow comparison tooltips to generate
 - cooldowns no longer start automatically.  you can close/open the bag to get them to show (if you enable that option).  all of the cooldown events ACTIONBAR_UPDATE_COOLDOWN, BAG_UPDATE_COOLDOWN, PET_BAR_UPDATE_COOLDOWN, SPELL_UPDATE_COOLDOWN, appear to trigger off other players as well, but do not provide any indication whether the event was triggered by you or them, so cooldowns will trigger window refreshes fairly constantly when you are around large numbers of players.  even limiting it to one update per second generated too much lag, especially in massive groups.
 - chat link for a battlepet in the guild bank will not send
 - the first time you click on a hyperlink in chat it wont show the item counts
 
 
 

# to do
 - double check all categories show/hide for the right clients
 - restack disable - maybe change this to require a modifier key instead of a straight disable?  might be easier to shift/alt/ctrl click on it than turning it on/off and its not like youll accidentally do it (which is why the disable was added)
 - backpack tokens to scroll when max width reached on second line
 - extend the categoryset actions to individual items for additional granular control.
 - add action; move (bank to bag, bag to bank, bag to vault, vault to bag)
 - add actions to items
 - allow multiple actions on a category / item
 
 - secure action button for toybox (and keyring)
 - only show bank bags for the specific tabs (bank/reagent bank/account tabs)
