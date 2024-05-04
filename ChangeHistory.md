# 3.10.28 Alpha 4 (04-MAY-2024)
 - fixed - issue with packager not handling cataclysm toc files/values

# 3.10.28 Alpha 3 (03-MAY-2024)
 - added - cataclysm toc files 40400
 
# 3.10.28 Alpha 2 (02-MAY-2024)
 - added - ability to disable the text for each bag type in the status bar - config > design > window > style > status > empty slot
 - added - ability to disable the text for each bag type in the ldb object text - right click > ldb > display

# 3.10.28 Alpha 1 (01-MAY-2024)
 - fixed - issue with pawn based item upgrade icon displaying on non equipable items
 - fixed - https://github.com/arkayenro/arkinventory/issues/1880 - issue with CONTAINER_SLOTS in most non english languages using a conditional format, as well as being reversed, which breaks the matching and the value capture

# known issues
 - some default frames (vendor/merchant at minimum) that would normally open via the PlayerInteractionFrameManager no longer open if you are in combat, you just get an addon error.  there is currently no workaround.
 - (dragonflight) reagentbank slots are no longer readable unless the bank is open
 - recipes on vendors are showing item counts for the items they create, not the recipe
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
