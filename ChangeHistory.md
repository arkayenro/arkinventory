# 3.10.00 Alpha 2 (xx-xxx-2022)
 - fixed - (classic) issue where the return data from setting the tooltip included a species value which made the item appear to be a battlepet
 - changed - client detection and checking code to support pre-patch
 - added - (dragonflight) category: class evoker
 - fixed - issue where the reagent bank wasnt being scanned when away from the bank (bank and bank bags cant be scanned away from the bank, so its partially helpful)
 - changed - restack action menu consolidated into a single layer
 - added - option to disable restack (someone asked for it)
 
# 3.10.00 Alpha 1 (22-SEP-2022)
 - fixed - (wrath) category: class death knight unhidden
 - fixed - (wrath) category: skill inscription unhidden
 - fixed - client detection code to support pre-patch
 - changed - multiple categories have had their client states updated (if a category is missing or showing when it shouldnt, let me know via a ticket)
 - added - support for 10.0 PTR prepatch - there will be issues, please log a ticket for them
 - fixed - (dragonflight) money frame elements
 - changed - money frame onclick has gone back to the single generic money popup, not the individual gold/silver/copper ones (when it works)
 - added  - (dragonflight) reagent bag slot (not sure if it works properly as i cant find any reagent bags)
 - changed - right click bag slot menus to work with all game clients
 - fixed - (dragonflight) issue with bank and reagent bank tooltips
 
# known issues
 - BankFrame no longer opens via the BANKFRAME_OPENED event so i cannot unregister it to stop it from opening and it will always open.  hiding the bank interface in any way closes the bank.  i havent found a way around this yet.
 - reagentbank slots are no longer readable in dragonflight unless the bank is open
 
# to do
 - check issue with outfit rule and equipment manager (in wrath? its always been weird)
 - fix tradeskill scanning in dragonflight
 - double check all categories show/hide for the right clients
 - confirm things havent broken in classic, wrath, or shadowlands
 - config wont load in prepatch (ace libraries not updated? yet)
 
 