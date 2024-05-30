# 3.10.30 Alpha 5 (30-MAY-2024)
 - removed - (cataclysm) keyring location

# 3.10.30 Alpha 4 (29-MAY-2024)
 - removed - config > actions > vendor > delete
 - added - config > actions > delete (only applies to junk items that have no sell price)
 - changed - delete no longer requires you to be at a vendor
 - fixed - https://github.com/arkayenro/arkinventory/issues/1894 - vendor/delete actions now exclude refundable items
 - updated - category for some items
 
# 3.10.30 Alpha 3 (22-MAY-2024)
 - changed - currency scans will now only be skipped if youre in an actual dragon race, not just mounted.
 - changed - all collection scanning will now be skipped during dragonriding races.  it will re-scan once the race is over (if needed).

# 3.10.30 Alpha 2 (20-MAY-2024)
 - fixed - (cataclysm) https://github.com/arkayenro/arkinventory/issues/1893 - issue getting the currency id from its link
 
# 3.10.30 Alpha 1 (20-MAY-2024)
 - added - category system > openable
 - added - category consumable > professions - knowledge (it used to fall back into power systems (old))
 - added - (timerunning) config > general > actions > use - will automatically use (open) any infinite treasure or bronze caches that you loot (disabled by default)
 - updated - (timerunning) mailbox auto send has been disabled


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
