# 3.10.13 (08-JAN-2023)
 - changed - profession rank icons: using the internal icons
 - changed - profession rank icons: size range adjusted
 - fixed - quest bucket timer should now update the icons once the value is reached, and not wait for the next window refresh
 - added - config > settings > designs > items > general > tint unwearble (default is disabled)
 - changed - debug output now goes to its own window (the output text is copyable)
 - moved - debug options are now under config > advanced > debug
 - changed - the enable debug option will now persist though reloads
 - added - keybinding for toggling the debug window.  you can also open it from the config.
 - changed - dragonriding zone restrictions changed to check for spell usage as there were too many instanced zones you could use them in.  so long as blizzard sets the usability of the spell correctly its more reliable.
 - added - "you are in the wrong zone" to acceptable red text to cater for shadowlands legendarys that are actually wearable/usable
 - fixed - issues with some of the object correction data.  cosmetic, would have shown the wrong type/subtype text in the debug menu
 - changed - the changer frame for the vault can no longer be hidden (as its the only way to change tabs) - it ignores the hide changer option from the profile
 - updated - CallBackHandler embedded library
 - fixed - item counts getting added to some tooltips
 - fixed - reputation standing text and values for the new factions
 - updated - categorised some items
 - changed - currency update bucket timer default increased from 1 to 3 seconds
 - fixed - mount summon in the dragon isles with druid travel form enabled
 - workaround - acknowledged the reagent bag tutorial so its popup wont open - if its already open then you'll need another reload for it to go away.
 - fixed - battle pet quality borders
 - fixed - (possibly) framelevel issue
 - fixed - issue with GetContainerNumFreeSlots
 
 
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
 