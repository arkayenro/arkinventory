# 3.10.33 (07-JUN-2024)
 - fixed - (cataclysm) issue with warning output
 - fixed - issue with secure hook code
 - fixed - https://github.com/arkayenro/arkinventory/issues/1894 - vendor/delete actions now exclude refundable items
 - fixed - (cataclysm) https://github.com/arkayenro/arkinventory/issues/1893 - issue getting the currency id from its link
 - added - timerunning categories for gems and scrolls (threads and caches are under system > openable)
 - changed - added some more safety checks around the action code
 - added - config > actions > scrap (requires the scrap action to be applied to category).  will only fill up the slots until you run out of items to scrap, you have to click on the scrap button as that is protected
 - note - see https://github.com/arkayenro/arkinventory/wiki/Actions for information on actions
 - removed - (cataclysm) keyring location
 - removed - config > actions > vendor > delete
 - added - config > actions > delete (only applies to junk items that have no sell price - requires the vendor or delete action to be applied to category)
 - changed - delete no longer requires you to be at a vendor
 - changed - currency scans will now only be skipped if youre in an actual dragon race, not just mounted.
 - changed - all collection scanning will now be skipped during dragonriding races.  it will re-scan once the race is over (if needed).
 - added - category system > openable
 - added - category consumable > professions - knowledge (it used to fall back into power systems (old))
 - added - (timerunning) config > general > actions > use - will automatically use (open) any infinite treasure or bronze caches that you loot (disabled by default)
 - updated - (timerunning) mailbox auto send has been disabled
 - updated - category for some items


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
