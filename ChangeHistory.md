# 3.10.05 (16-NOV-2022)
 - changed - (retail) toc updated to 100002
 - fixed - map ids for some old zone mounts
 - fixed - issue with bucket events that get renamed
 - fixed - item cooldown numbers should display properly (if you have it enabled at the blizzard level)
 - added - config option to show numbers on the cooldown (it just lets you toggle the blizzard global cvar which is stored by the game, not by this mod)
 - updated - profile import and export to handle the new categoryset structure.  old exports will not work for the moment
 - changed - action data is removed from both profile exports and imports to ensure that people dont end up vendoring or mailing things off to players without them knowing
 - fixed - BAG_UPDATE_COOLDOWN no longer provides a bag id, and no other events (that arent as prolific) are available to trigger cooldowns, so it may cause a refresh (not redraw) every second
 - added - mail send added as a category action. you can select from any character you already have in arkinventory, or you can manually enter anything else. there are currently no options and a lot of debug output for it at the moment just to make sure its doing what its meant to
 - changed - the junk sell keybinding has been renamed to manual action, and it runs all of the manual actions depending on where you are at the time.
 - added - zone restrictions for mounts so they dont get called when in the wrong zone
 - updated - pets and mounts to 10.0.0
 - changed - categoryset internal data structure
 - added - one action can be assigned to each category/rule in a categoryset.  actions can be set to disabled, automatic, or manual
 - changed - auto sell (junk) renamed to vendor and made an action
 - changed - when at a vendor right clicking on a "no sell price" item that has a junk icon will now delete it.  the config > general > junk > delete option must be enabled for this to work.
 - fixed - the one off (per enable) warning message if your profile is using a blueprint that no longer exists should now only trigger on valid locations for your game client
 - updated - blueprint options in the config will now show if the currently selected option has been deleted instead of showing the default, so that you can see it and change it more easily
 - fixed - issues with uploads to wago
 - fixed - quest border and bang should now display (if enabled) for items that start a quest
 - fixed - issue with external junk addons
 - added - (workaround) a cooldown object has been directly included in the item template as it appears to not get added to the first few item objects that are created from it.
 - removed - workaround for taint from interactionframe.  was actually taint from the keybindings
 - fixed - (mostly) various caged battlepet (and tooltip) issues in the vault, inbox, inventory (bank bag 0).  battlepets in the vault will show a pet cage for the time being until i can work out a way to get at that data.
 - note - the stack size for a lot of older items has increased to 1000, please restack/cleanup to gain more free slots
 
# known issues
 - (dragonflight) reagentbank slots are no longer readable unless the bank is open
 - recipes on vendors are showing item counts for the items they create, not the recipe
 - (dragonflight) currency tokens on the backback no longer have a fixed amount and will keep going until you run out of space, they can get messy
 - Enum.ItemConsumableSubclass is missing the Flask entry and everything after has moved down a value which screws up the category names (have hardcoded a workaround in for the moment)
 - items with an active cooldown dont allow comparison tooltips to generate
 - all of the cooldown events ACTIONBAR_UPDATE_COOLDOWN, BAG_UPDATE_COOLDOWN, PET_BAR_UPDATE_COOLDOWN, SPELL_UPDATE_COOLDOWN, appear to trigger off other players as well, but do not provide any indication when the event was triggered by you or them, so cooldowns will trigger window refreshes fairly constantly when you are around large numbers of players (it has been limited to one per second for this reason)
 
# to do
 - double check all categories show/hide for the right clients
 - confirm things havent broken in classic, wrath, or shadowlands
 - restack disable - maybe change this to require a modifier key instead of a straight disable?  might be easier to shift/alt/ctrl click on it than turning it on/off and its not like youll accidentally do it (which is why the disable was added)
 - backpack tokens to scroll when max width reached on second line
 - extend the categoryset actions to individual items for additional granular control.
 - add action; bank (move from bank to bag)
 - add action; bag (move from bag to bank)
 