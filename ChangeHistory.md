# 3.11.01 Alpha 2 (30-AUG-2024)
 - changed - https://github.com/arkayenro/arkinventory/issues/1918 - restack - profession bags will now search for both crafting and reagent items
 - added - flying mount config mode option to set which flight mode (all/steady/dynamic) a mount can be used with
 - changed - flying mount selection is now based on the steady/dynamic aura you have active (if you dont have an aura the default is dynamic)
 - fixed - (regression) https://github.com/arkayenro/arkinventory/issues/1996 - ieeuse with auction house scanning in classic
 
# 3.11.01 Alpha 1 (xx-xxx-xxxx)
 - never existed


# known issues
 - account bank tabs are currently excluded from restack
 - interacting with the account bank convergence leaves the normal bank and reagent bank slots visible but not usable
 
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
