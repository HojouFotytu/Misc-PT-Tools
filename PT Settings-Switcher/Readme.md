### NOTE:  
Profit Trailer no longer provides a collection of public configs for which this tutorial was originally created.  However an archive of these settings can be found here: https://github.com/PTdude/Profit-Trailer-Settings.


# Profit Trailer Settings-Switcher
This is a walk-through for using PTMagic to switch between Profit Trailer configs, based on changing market trends.  This can also be used as a more robust replacement of PT's Auto-Config switcher. However, PTMagic can only switch settings based on the average price trends YOU DEFINE across various time-frames.  It cannot use PTADXTREND, VWAPPERCENTAGE, MVWAPPERCENTAGE, or (X)MALINE.

## Requirements: 
 - Copies of the configs/settings you are using from Profit Trailer
 - PTMagic v2
---

### Profit Trailer Settings
Most Profit Trailer users already have a few config/settings they switch between depending on changing market conditions.  You will need to __download copies of the PAIRS, DCA, and INDICATORS files__ for all of the different configs/settings you use. 

To avoid complications, it's best if you __DO NOT use configs/settings that incorporate Positive DCA or Pending Orders__ as part of the trading strategy without exentsive testing. Quickly changing between settings that use those techniques and those that don't could lead to unforseen and unintended side-effects (this doesn't include **PTDefender**'s use of pending, since this isn't actually part of the trading strategy). Only use settings that are based on standard buy and sell techniques, so they can be quickly switched according to changing market conditions, without accidentally opening yourself up to unintended risks.

### PTMagic
PTMagic will be used to automatically change between your configs/settings. PTMagic is a free, open-source add-on for Profit Trailer, which is designed to __automatically modify Profit Trailer's settings based on changing market conditions__.  It's main purpose is to ensure more protection and versatility than a single strategy can provide -- by adjusting your bot's behavior in different market conditions automatically, 24 hours a day, seven days a week. You can read more about it here:  https://github.com/PTMagicians/PT-Magic/wiki   

__PTMagic does not interact with your exchange in any way__.  It only __makes adjustments to your Profit Trailer config settings__, based on it's analysis of current market conditions and the behavior of individual coins.

### Caution
After following the instructions below and getting everything set up, run your Profit Trailer bot in test mode so you can watch how things work, make any necessary adjustments, and make sure you didn't make any mistakes. Anytime you try new strategies or trading techniques, you should take your time and test your settings to ensure you aren't exposing yourself to too much risk.  Crypto markets are highly volatile -- sudden changes in market conditions can result in large losses if Profit Trailer or PTMagic are configured incorrectly.  

---
## Getting Started

### 1. Download and install the latest release of PTMagic  
Extract it to location where you plan to keep it, but do not launch it or doing anything else with it just yet.  Grab your drink of choice, and get to work!  First, follow the instructions here: https://github.com/PTMagicians/PTMagic/wiki/Setup-PT-Magic-on-Windows

### 2. Launch Profit Trailer
In your Profit Trailer webpage monitor, go to "Other Configs"

### 3. Decide which configs you want to use for the following market conditions:
It is ok to use the same settings for multiple market conditions. 

- Tanking (extreme downward moving market) 
- Bear
- Sideways (low volatility)
- Default (higher volatility, slight uptrend)
- Bull
- Moon (extreme upward moving market)
- (later you can add more if needed)

### 4. Download your config files
Select the Config dropdown at the top of your Profit Trailer screen, and select "Other Configs." If you haven't already, you will need to add the public configs you want to use.  Then select the title of the active config to select the config files you want, and click the "DOWNLOAD" button to the right -- __NOT "SAVE"__ -- and all three files (pairs, dca, and indicators) will be downloaded to your browsers default download folder.

### 5. Change the extensions of all downloaded files from ".txt" to ".properties"
You should now have three files for all six cases listed in #3, with the names of your settings.  e.g., ElGringoLoco-PAIRS.properties, ElGringoLoco-DCA.properties, ElGringoLoco-INDICATOR.properties.  

### 6. Create the folders listed in step #3
Once you have downloaded all the files you need, create six folders: Tanking, Bear, Sideways, Default, Bull, Moon.  Move the settings pairs/dca/indicators files into the appropriate folders.  If you choose to use slightly different names for your folders, that's fine -- but __at least one of your folders MUST BE NAMED DEFAULT__ or PTMagic will close with an error.  

If you decide to use the same settings for multiple market scenarios, for example if ElGringoLoco will perform well in both a Bear and Tanking market, simply make a duplicate of the files for the second folder.

### 7. Find your PTMagic installation, and open the "PTMagic" folder
Drop all six folders, each with the three settings files, into the folder named "_presets"

### 8. Configure PTMagic
Carefully follow the instructions found here:  https://github.com/PTMagicians/PT-Magic/wiki/Setup-Guide, but __SKIP STEPS 6, 6 and 8__ -- we will take care of those steps now.

### 9. Download the settings.analyzer.json
Download the latest release of the settings.analyzer.json from this repo: https://github.com/HojouFotytu/Misc-PT-Tools/tree/master/PT%20Settings-Switcher, and copy it to your PTMagic folder, replacing the default version.

### 10. Enter the names of your settings
Open the settings.analyzer.json with Notepad++ (https://notepad-plus-plus.org/).  Take your time, and carefully edit "File": so the name exactly matches each of your PAIRS, DCA, and INDICATOR files.  Do this for every global setting.   Also make sure the **"SettingName" exactly matches the names of the folders** in which the settings are contained.  Remember, at the very least you __must have a folder named DEFAULT__ with your default PT settings.   

### 11.  Adjust the GLOBAL SETTINGS according to your preferences
Look over the global settings, read the comments, and adjust the "keep_balance", "initial_cost", "max_trading_pairs" and other settings according to your trading style and risk-tolerance.  Do this __for every setting__  

Also notice for the tanking setting, you can remove the comment markers and enable sell_only_mode if that is your preference.

### 12. Adjust the COIN-SPECIFIC settings according to your preferences
It IS possible to get creative and insert almost any of Profit Trailer's coin-specific settings you choose here, but be careful!  These settings will be applied for coins that trigger these setting in addition to your global market settings -- if you are using different buy or sell strategies for different global settings, your coin-specific settings might not match very well, and lead to unintended side-effects.

### 13. Launch!
Make sure profit trailer is running, and make sure you have carefully followed the all the steps above.  Double-Click on __Start PTMagic.cmd__ from the PTMagic folder, then refill your drink.  

For the first run, PTMagic will have to download the last seven days of market data so it can calculate the trends of individual coins.  After it has finished and you see a summary of it's first "Raid" you can double-click __Start PTMagic Monitor__ and begin exploring the PTMagic GUI.  You do not need to run the PTMagic monitor for the analyzer and switching to function.  The web-monitor merely displays information about the bot, and offers a GUI interface with information and the ability to change various settings.

### 12. Ready to Trade!
When you feel comfortable that everything is working as intended, it's time to enable trading.  Open the settings.analyzer.json file and for every Global Setting, change "Default_trading_enabled" to "true".  There is no danger in editing this file while PTMatic is running. Any changes you make will take effect after you save the file and PTMagic loads it at the beginning of it's next raid. 

---

If you have any problems or questions, first search the related wikis!  For questions about specific settings, how they work, and allowed values, search the appropriate section of the Profit Trailer wiki.  For questions about PTMagic, search the wiki or visit the PTMagic Discord server:  https://discord.gg/KYmHMfk

Good luck! 






