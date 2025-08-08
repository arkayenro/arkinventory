# 3.12.01 Alpha 4 (08-AUG-2025)
 - fixed - (retail) issue with bank tabs opening as bags when AI does not override the bank
 - fixed - (retail) issue with right clicking an item to move it to the account bank.  it should no longer end up in the normal bank if the selected tab is full, it should get moved to one of the other tabs (if they have space)

# 3.12.01 Alpha 3 (07-AUG-2025)
 - fixed - potential issue with bonusid handling from malformed hyperlinks
 - fixed - (retail) issue with outfit rule function when using equipment manager

# 3.12.01 Alpha 2 (07-AUG-2025)
 - fixed - (retail) issue with warbank bag mapping - needs saved data to be removed
 - note - (retail) all saved keyring data has been erased. please login to each character to update its data
 - note - (retail) all saved bank data has been erased. please login to each character to update its data
 - note - (retail) all saved warbank data has been erased. please login to any character to update its data

# 3.12.01 Alpha 1 (06-AUG-2025)
 - fixed - tab name and icon should now update immediately after changing it
 - fixed - (non retail clients) issue with items in bank slots not being able to generate tooltips
 - fixed - (retail) issue with AccountBankPanel no longer existing

# known issues post 11.2
 - in non 11.2 game clients there are two xml errors, these can be ignored
   - ARKINV_BankPanelTabSettingsFrame: Has bad mixin: BankPanelTabSettingsMenuMixin
   - Couldn't find inherited node: BankPanelTabSettingsMenuTemplate
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
