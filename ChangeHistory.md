# 3.10.04 Alpha 9 (06-NOV-2022)
 - fixed - issues with uploads to wago
 - fixed - quest border and bang should now display (if enabled) for items that start a quest
 - workaround - taint from keybindings (blizzard changed or broke it)

# 3.10.04 Alpha 2-8 (xx-NOV-2022)
 - no longer available (testing the same upload to wago)
 
# 3.10.04 Alpha 1 (04-NOV-2022)
 - fixed - issue with external junk addons
 
# known issues
 - (dragonflight) reagentbank slots are no longer readable unless the bank is open
 - recipes on vendors are showing item counts for the items they create, not the recipe
 - (dragonflight) currency tokens on the backback no longer have a fixed amount and will keep going until you run out of space, they can get messy
 - Enum.ItemConsumableSubclass is missing the Flask entry and everything after has moved down a value which screws up the category names (have hardcoded a workaround in for the moment)
 - items with an active cooldown dont allow comparison tooltips to generate
 
# to do
 - double check all categories show/hide for the right clients
 - confirm things havent broken in classic, wrath, or shadowlands
 - restack disable - maybe change this to require a modifier key instead of a straight disable?  might be easier to shift/alt/ctrl click on it than turning it on/off and its not like youll accidentally do it (which is why the disable was added)
 - backpack tokens to scroll when max width reached on second line
