# 3.12.16 Alpha 5 (27-SEP-2026)
 - added - (classic) toc file for 1.60.00
 - added - support for classic forever

# 3.12.16 Alpha 4 (26-SEP-2026)
 - changed - currency tracking - if a cap is reached the text will now be shown in red
 - fixed - (classic) season/hardcore/forever is now included in the version text
 - fixed - (classic) issue with forever using the retail api

# 3.12.16 Alpha 3 (22-AUG-2026)
 - workaround - (retail) issue with guild bank function using IsVisible instead of IsShown
 - updated - category for some items

# 3.12.16 Alpha 2 (17-AUG-2026)
 - workaround - guild bank not opening due to PlayerInteractionFrameManager being disabled/removed.  for the moment both the blizzard and arkinventory window will open/close together

# 3.12.16 Alpha 1 (14-AUG-2026)
 - fixed - (classic) issues due to PlayerInteractionFrameManager being disabled/removed

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
