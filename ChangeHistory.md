# 3.10.09 (24-NOV-2022)
 - fixed - issue with rule functions wearble/unwearble and cloaks
 - restored - config > actions (was accidentally hidden)
 - fixed - issue with config transmog secondary option hiding the wrong sub options
 - restored - xml for ArkScanTooltipTemplate, OnTooltipAddMoney and OnTooltipCleared re-added both as several hundred individual MoneyFrames were being added to the scan tooltip just on entering the world.  this was the probable cause for the lag and ui crashes.
 - removed - PLAYER_AVG_ITEM_LEVEL_UPDATE event
 - removed - rescans should no longger trigger a full window refresh (they already update the items)
 - added - preloading item info from the bag and bank to make their initial opens are faster.  will not happen if you enter while in combat.  opening the window before this has completed will abort the preload.
 - added - preloading the bag and bank windows so their initial opens are faster.  will not happen if you enter while in combat.  opening the window before this has completed will abort the preload.
 - changed - the rules module no longer triggers full window rebuilds on enable (mucks up the preload)
 - removed - PLAYER_INTERACTION_MANAGER_FRAME_SHOW and PLAYER_INTERACTION_MANAGER_FRAME_HIDE events
 - removed - event UNIT_INVENTORY_CHANGED
 - changed - added yielding to every scan to alleviate any potential sources of lag
 - changed - added extra yielding to the window draw functions
 - changed - enforced a 25ms yield timer
 - fixed - edit mode item menu for empty slots should now show the type of slot, not "retrieving item data"
 - added - icons on the bag, combined bag, bank, and guild bank, frames to swap to ArkInventory control
 - added - location sub menu to switch window back to blizzard control.
 - fixed - issue with the conduit overlay when it had no quality set
 
 
# known issues
 - (dragonflight) reagentbank slots are no longer readable unless the bank is open
 - recipes on vendors are showing item counts for the items they create, not the recipe
 - (dragonflight) currency tokens on the backback no longer have a fixed amount and will keep going until you run out of space, they can get messy
 - Enum.ItemConsumableSubclass is missing the Flask entry and everything after has moved down a value which screws up the category names (have hardcoded a workaround for the moment)
 - items with an active cooldown dont allow comparison tooltips to generate
 - cooldowns no longer start automatically.  you can close/open the bag to get them to show (if you enable that option).  all of the cooldown events ACTIONBAR_UPDATE_COOLDOWN, BAG_UPDATE_COOLDOWN, PET_BAR_UPDATE_COOLDOWN, SPELL_UPDATE_COOLDOWN, appear to trigger off other players as well, but do not provide any indication whether the event was triggered by you or them, so cooldowns will trigger window refreshes fairly constantly when you are around large numbers of players.  even limiting it to one update per second generated too much lag, especially in massive groups.
 
# to do
 - double check all categories show/hide for the right clients
 - confirm things havent broken in classic, wrath, or shadowlands
 - restack disable - maybe change this to require a modifier key instead of a straight disable?  might be easier to shift/alt/ctrl click on it than turning it on/off and its not like youll accidentally do it (which is why the disable was added)
 - backpack tokens to scroll when max width reached on second line
 - extend the categoryset actions to individual items for additional granular control.
 - add action; bank (move from bank to bag)
 - add action; bag (move from bag to bank)
 