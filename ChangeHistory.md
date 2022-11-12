# 3.10.04 Alpha 15 (13-NOV-2022)
 - fixed - rule functions `wearable` and `unwearable` now have an option to ignore player level requirements
 - fixed - item cooldown number should now display properly
 - fixed - BAG_UPDATE_COOLDOWN no longer provides a bag id, and no other events are available to trigger cooldowns, so it may cause a refresh (not redraw) every second
 - added - mail send added as a category action. you can select from any character you already have in arkinventory, or you can manually enter anything else. there are currently no options and a lot of debug output for it at the moment just to make sure its doing what its meant to
 - changed - the junk sell keybinding has been renamed to manual action, and it runs all of the manual actions depending on where you are at the time.

# 3.10.04 Alpha 14 (xx-NOV-2022)
 - no longer available
 
# 3.10.04 Alpha 13 (11-NOV-2022)
 - fixed - various caged battlepet (and tooltip) issues in the vault, inbox, inventory (bank bag 0)
 - note - (ptr/beta) stack size for a lot of older items has increased to 1000, please restack/cleanup to gain more free slots
 
# 3.10.04 Alpha 12 (10-NOV-2022)
 - added - zone restrictions for mounts so they dont get called when in the wrong zone
 - fixed - (ptr/beta) caged battlepets, and battlepet tooltips showing when they shouldnt
 - updated - pets and mounts to 10.0.0
 
# 3.10.04 Alpha 11 (09-NOV-2022)
 - changed - categoryset internal data structure
 - added - one action can be assigned to each category/rule in a categoryset.  actions can be set to disabled, automatic, or manual
 - changed - auto sell (junk) renamed to vendor and made an action
 - changed - when at a vendor right clicking on a "no sell price" item that has a junk icon will now delete it.  the config > general > junk > delete option must be enabled for this to work.
 
# 3.10.04 Alpha 10 (07-NOV-2022)
 - fixed - the one off (per enable) warning message if your profile is using a blueprint that no longer exists should now only trigger on valid locations for your game client
 - updated - blueprint options in the config will now show if the currently selected option has been deleted instead of showing the default, so that you can see it and change it more easily
 
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
 - extend the categoryset actions to individual items for additional granular control.
 - add action; mail (send items in that category to a specified character)
 - add action; bank (move from bank to bag)
 - add action; bag (move from bag to bank)
 