# 3.10.03 (29-OCT-2022)
 - fixed - ArkInventory.API.BlizzardBagIdToInternalId
 - fixed - (wrath/classic) the first bank bag was being treated like a reagent bag
 - fixed - some of the restack ignore bag options were being ignored due to a code issue
 - updated - xml for ArkScanTooltipTemplate, OnTooltipAddMoney (deprecated in beta) and OnTooltipCleared removed and are now cleared in OnLoad if they exist.  this should fix the lag issues.
 - fixed - https://github.com/arkayenro/arkinventory/issues/1634 (dragonflight) usable rule function and tinting.  tooltips are using a new red color
 
# known issues
 - (dragonflight) reagentbank slots are no longer readable unless the bank is open
 - (dragonflight) theres a weird issue where you randomly get an addon blocked due to resume( )
 - recipes on vendors are showing item counts for the items they create, not the recipe
 - (dragonflight) currency tokens on the backback no longer have a fixed amount and will keep going until you run out of space, they can get messy
 - Enum.ItemConsumableSubclass is missing the Flask entry and everything after has moved down a value which screws up the category names (have hardcoded a workaround in for the moment)
 - items with an active cooldown dont allow comparison tooltips to generate
 
# to do
 - double check all categories show/hide for the right clients
 - confirm things havent broken in classic, wrath, or shadowlands
 - restack disable - maybe change this to require a modifier key instead of a straight disable?  might be easier to shift/alt/ctrl click on it than turning it on/off and its not like youll accidentally do it (which is why the disable was added)
 - backpack tokens to scroll when max width reached on second line
 