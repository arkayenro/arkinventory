# 3.10.07 (19-NOV-2022)
 - fixed - issue with pressing ESCAPE to close windows (like the map) and getting blocked when in combat
 - added - category name as a new sort method key.  only applies to custom categories and rules.  system categories will sort by id as they have no name.
 - added - mail action options - config > general > actions > mail
 - fixed - keybindings are back in their own section and should not cause any taint.
 - fixed - empty reagent bank slots should be in the correct category again
 - fixed - should no longer generate a second frame open causing issues for other mods (like tsm) at the auction house
 - updated - config > settings > designs > items > cooldown > on window open.  cooldowns will no longer automatically show.  you will need to enable this option and then they will update when you close/open the window.  triggering off the cooldown events generated too much lag especially in large crowds
 - fixed - issue with mailbox scanning
 - fixed - battlepet tooltips showing during scanning
 - fixed - battlepets in the vault
 - fixed - issue with config not opening from 3.10.06
 
# known issues
 - (dragonflight) reagentbank slots are no longer readable unless the bank is open
 - recipes on vendors are showing item counts for the items they create, not the recipe
 - (dragonflight) currency tokens on the backback no longer have a fixed amount and will keep going until you run out of space, they can get messy
 - Enum.ItemConsumableSubclass is missing the Flask entry and everything after has moved down a value which screws up the category names (have hardcoded a workaround for the moment)
 - items with an active cooldown dont allow comparison tooltips to generate
 - cooldowns no longer start automatically.  you can close/open the bag to get them to show (if you enable that option).  all of the cooldown events ACTIONBAR_UPDATE_COOLDOWN, BAG_UPDATE_COOLDOWN, PET_BAR_UPDATE_COOLDOWN, SPELL_UPDATE_COOLDOWN, appear to trigger off other players as well, but do not provide any indication when the event was triggered by you or them, so cooldowns will trigger window refreshes fairly constantly when you are around large numbers of players.  even limiting it to one update per second generated too much lag, especially in massive groups.
 
# to do
 - double check all categories show/hide for the right clients
 - confirm things havent broken in classic, wrath, or shadowlands
 - restack disable - maybe change this to require a modifier key instead of a straight disable?  might be easier to shift/alt/ctrl click on it than turning it on/off and its not like youll accidentally do it (which is why the disable was added)
 - backpack tokens to scroll when max width reached on second line
 - extend the categoryset actions to individual items for additional granular control.
 - add action; bank (move from bank to bag)
 - add action; bag (move from bag to bank)
 