# 3.10.03 Alpha 5 (03-NOV-2022)
 - fixed - tooltip text in edit mode for re-assignment to the default category
 - workaround - added a config > advanced > workarounds > player interaction option to disable overriding the PlayerInteractionFrameManager.  The down side is that the default Bank and Vault frames will also open, but there should be no taint any more.
 - changed - BAG_UPDATE timer reduced from 0.5 to 0.3 seconds
 
# 3.10.03 Alpha 4 (01-NOV-2022)
 - fixed - junk check code for peddler
 - fixed - rule functions `wearable( )` and `unwearble( )`
 
# 3.10.03 Alpha 3 (31-OCT-2022)
 - no longer available

# 3.10.03 Alpha 2 (30-OCT-2022)
 - added - rule function `wearable( )`
 - added - rule function `unwearable( )`
 
# 3.10.03 Alpha 1 (30-OCT-2022)
 - no longer available

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

