# 3.10.02 (27-OCT-2022)
 - fixed - upgrade icon should now display if using pawn
 - changed - object data that cannot be retrieved after 10 attempts is marked as dead (should stop constant requests for unknown items)
 - fixed - constant attempts to scan the mailbox if you had a battlepet in there
 - fixed - (dragonflight) guild bank frame open/close now triggered off the player interaction function - blizzard removed the events)
 - changed - (dragonflight) bank frame open/close now triggered off the player interaction function instead of the events
 - changed - (dragonflight) mailbox frame open/close now triggered off the player interaction function instead of the events
 - changed - (dragonflight) auction frame open/close now triggered off the player interaction function instead of the events
 - changed - (dragonflight) void storage frame open/close now triggered off the player interaction function instead of the events
 - changed - (dragonflight) player trade frame open/close now triggered off the player interaction function instead of the events
 - changed - (dragonflight) transmog frame open/close now triggered off the player interaction function instead of the events
 - changed - (dragonflight) merchant/vendor frame open/close now triggered off the player interaction function instead of the events
 - updated - categorised some items
 
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
 