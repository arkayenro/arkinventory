# 3.12.00 Alpha 2 (22-JUL-2025)
 - fixed - issue with 3rd level of the bar menu system not generating properly
 - fixed - issue with timerunning menu option displaying when it shouldnt
 - updated - unuseable and unwearable item tinting options moved to their own tab in the config. added ignore options for item level and already known
 - updated - some lolcalisations based off game constants

# 3.12.00 Alpha 1 (21-JUL-2025)
 - updated - (retail) toc updated to 11.2.0
 - removed - (11.2) locations - reagent bank (internal), void storage
 - removed - (11.2) events - PLAYERBANKBAGSLOTS_CHANGED, REAGENTBANK_PURCHASED, REAGENTBANK_UPDATE, PLAYERREAGENTBANKSLOTS_CHANGED
 - added - (11.2) option to split the bank tabs up into their own panels, the same way as the warbank can be split up if needed.  the isolate/display options will remain but only work when the bank is combined into a single panel
 - fixed - tab name, icon, and filter settings should now work properly
 - added - (classic) - workaround for the current invalid hyperlink format blizzard has set
 - note - (11.2) all saved bank data has been erased. please login to each character to update its data
 - note - (11.2) all saved keyring data has been erased. please login to each character to update its data
 - note - (11.2) all saved warbank data has been erased. please login to any character to update its data

# known issues 11.2
 - in non 11.2 game clients there are two xml errors, these can be ignored
   - ARKINV_BankPanelTabSettingsFrame: Has bad mixin: BankPanelTabSettingsMenuMixin
   - Couldn't find inherited node: BankPanelTabSettingsMenuTemplate
 - when swapping the bank from single tabs to combined the last selected tab will remain highlighted
 - without reagent or profession bags in the bank a restack wont transfer new stacks of reageants or profession items - potential workaround will be to look for tabs that have been assigned 'reagents' and treat those the same way the reagent bank was previously

# known issues
 - some default frames (vendor/merchant at minimum) that would normally open via the PlayerInteractionFrameManager no longer open if you are in combat, you just get an addon error.  there is currently no workaround.
 - (dragonflight) reagentbank slots are no longer readable unless the bank is open
 - Enum.ItemConsumableSubclass is missing the Flask entry and everything after has moved down a value which screws up the category names (have hardcoded a workaround for the moment)
 - items with an active cooldown dont allow comparison tooltips to generate
 - cooldowns no longer start automatically.  you can close/open the bag to get them to show (if you enable that option).  all of the cooldown events ACTIONBAR_UPDATE_COOLDOWN, BAG_UPDATE_COOLDOWN, PET_BAR_UPDATE_COOLDOWN, SPELL_UPDATE_COOLDOWN, appear to trigger off other players as well, but do not provide any indication whether the event was triggered by you or them, so cooldowns will trigger window refreshes fairly constantly when you are around large numbers of players.  even limiting it to one update per second generated too much lag, especially in massive groups.
 - chat link for a battlepet in the guild bank will not send
 - the first time you click on a hyperlink in chat it wont show the item counts


# to do
 - double check all categories show/hide for the right clients
 - restack disable - maybe change this to require a modifier key instead of a straight disable?  might be easier to shift/alt/ctrl click on it than turning it on/off and its not like youll accidentally do it (which is why the disable was added)
 - backpack tokens to scroll when max width reached on second line
 - extend the categoryset actions to individual items for additional granular control.
 - add action; move (bank to bag, bag to bank, bag to vault, vault to bag)
 - add actions to items
 - allow multiple actions on a category / item
 - secure action button for toybox (and keyring)
