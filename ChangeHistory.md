# 3.10.33 Alpha 5 (20-JUN-2024)
 - added - https://github.com/arkayenro/arkinventory/issues/1901 - handle multiple ids when manually adding items to a custom category
 - fixed - (regression) issue with mail action trying to add more than 12 items to a mail
 - fixed - (retail) API change from C_Item.GetItemIcon to C_Item.GetItemIconByID
 - fixed - issue with item data retrieval where if it couldnt find the item it would loop forever
 
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
 - added - (war within) basic compatibility (there will be issues)
 
# 3.10.33 Alpha 1 (07-JUN-2024)
 - fixed - https://github.com/arkayenro/arkinventory/issues/1899 - issue with junk icon not getting displayed when using the scrap addon


# known issues
 - some default frames (vendor/merchant at minimum) that would normally open via the PlayerInteractionFrameManager no longer open if you are in combat, you just get an addon error.  there is currently no workaround.
 - (dragonflight) reagentbank slots are no longer readable unless the bank is open
 - recipes on vendors are showing item counts for the items they create, not the recipe
 - Enum.ItemConsumableSubclass is missing the Flask entry and everything after has moved down a value which screws up the category names (have hardcoded a workaround for the moment)
 - items with an active cooldown dont allow comparison tooltips to generate
 - cooldowns no longer start automatically.  you can close/open the bag to get them to show (if you enable that option).  all of the cooldown events ACTIONBAR_UPDATE_COOLDOWN, BAG_UPDATE_COOLDOWN, PET_BAR_UPDATE_COOLDOWN, SPELL_UPDATE_COOLDOWN, appear to trigger off other players as well, but do not provide any indication whether the event was triggered by you or them, so cooldowns will trigger window refreshes fairly constantly when you are around large numbers of players.  even limiting it to one update per second generated too much lag, especially in massive groups.
 - chat link for a battlepet in the guild bank will not send
 - the first time you click on a hyperlink in chat it wont show the item counts

# to do
 - double check all categories show/hide for the right clients
 - confirm things havent broken in classic, wrath, or shadowlands
 - restack disable - maybe change this to require a modifier key instead of a straight disable?  might be easier to shift/alt/ctrl click on it than turning it on/off and its not like youll accidentally do it (which is why the disable was added)
 - backpack tokens to scroll when max width reached on second line
 - extend the categoryset actions to individual items for additional granular control.
 - add action; move (bank to bag, bag to bank, bag to vault, vault to bag)
 - add actions to items
 - allow multiple actions on a category / item
