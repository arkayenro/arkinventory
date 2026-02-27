# 3.12.09 Alpha 3 (27-FEB-2026)
 - fixed - issue with paragon standing text
 - updated - category for some items

# 3.12.09 Alpha 2 (24-FEB-2026)
 - fixed - issue generating repuatation standing text
 - fixed - issue with backpack (bag 0) data getting incorrectly erased when the bag location is not set to saved and you hearth/portal

# 3.12.09 Alpha 1 (23-FEB-2026)
 - fixed - issue accessing the bank in offline mode after using the warbank distance inhibitor where it would not display the character bank, only the account bank
 - fixed - issue with some factions showing as paragon instead of renown
 - fixed - issue with ldb reputation tracking menu tooltip displaying the encoded hyperlink instead of the faction info
 - changed - when a location is locked its bags will no longer be scanned to preserve the saved data.  if you backup the savedvariables file, before its unlocked and you access that location again, you should have a list of all items that were in there before in the event blizard loses them.

# known issues post 11.2
 - without reagent or profession bags in the bank a restack wont transfer new stacks of reageants or profession items - potential workaround will be to look for tabs that have been assigned 'reagents' and treat those the same way the reagent bank was previously

# known issues
 - some default frames (vendor/merchant at minimum) that would normally open via the PlayerInteractionFrameManager no longer open if you are in combat, you just get an addon error.  there is currently no workaround.
 - items with an active cooldown dont allow comparison tooltips to generate
 - cooldowns no longer start automatically.  you can close/open the bag to get them to show (if you enable that option).  all of the cooldown events ACTIONBAR_UPDATE_COOLDOWN, BAG_UPDATE_COOLDOWN, PET_BAR_UPDATE_COOLDOWN, SPELL_UPDATE_COOLDOWN, appear to trigger off other players as well, but do not provide any indication whether the event was triggered by you or them, so cooldowns will trigger window refreshes fairly constantly when you are around large numbers of players.  even limiting it to one update per second generated too much lag, especially in massive groups.
 - caged pets in the guild bank show up as caged pets, not the pet itself
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
