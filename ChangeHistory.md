# 3.10.11 (04-DEC-2022)
 - added - blueprint config option to main menu
 - fixed - removed some debug output
 - fixed - summon mount keybinding when travel form is enabled will now correctly summon a dragonriding mount when on the dragon isles
 - fixed - wrong item quality was being saved during scanning
 - changed - quality data is no longer saved and is retrieved when required instead
 - fixed - missing or changed blizzard events will no longer cause errors and will generate a warning instead
 - changed - right clicking on the LDB mount object now opens the mount config instead.  there were too many mounts for the menu system to be viable.
 - added - mount config option to main menu
 - added - dragonriding option in config and ldb object to swap the air/land mount selection when in the dragon isles.  disabled by default.  these are per character settings.
 - fixed - (wrath/classic) issue with tooltip unusable red text detection
 - fixed - issue with item cache clear code
 - fixed - dragonriding mounts in azure span
 - changed - the default has been changed to false for pre-loading the bag and bank data (it appears to be causing some weird issues)
 - updated - categorised some items
 
 
# known issues
 - (dragonflight) reagentbank slots are no longer readable unless the bank is open
 - recipes on vendors are showing item counts for the items they create, not the recipe
 - (dragonflight) currency tokens on the backback no longer have a fixed amount and will keep going until you run out of space, they can get messy
 - Enum.ItemConsumableSubclass is missing the Flask entry and everything after has moved down a value which screws up the category names (have hardcoded a workaround for the moment)
 - items with an active cooldown dont allow comparison tooltips to generate
 - cooldowns no longer start automatically.  you can close/open the bag to get them to show (if you enable that option).  all of the cooldown events ACTIONBAR_UPDATE_COOLDOWN, BAG_UPDATE_COOLDOWN, PET_BAR_UPDATE_COOLDOWN, SPELL_UPDATE_COOLDOWN, appear to trigger off other players as well, but do not provide any indication whether the event was triggered by you or them, so cooldowns will trigger window refreshes fairly constantly when you are around large numbers of players.  even limiting it to one update per second generated too much lag, especially in massive groups.
 - chat link for a battlepet in the guild bank will not send
 - the first time you click on a hyperlink in chat it wont show the item counts
 
# to do
 - double check all categories show/hide for the right clients
 - confirm things havent broken in classic, wrath, or shadowlands
 - restack disable - maybe change this to require a modifier key instead of a straight disable?  might be easier to shift/alt/ctrl click on it than turning it on/off and its not like youll accidentally do it (which is why the disable was added)
 - backpack tokens to scroll when max width reached on second line
 - extend the categoryset actions to individual items for additional granular control.
 - add action; move (bank to bag, bag to bank, bag to vault, vault to bag)
 - add actions to items
 - allow multiple actions on a category / item
 