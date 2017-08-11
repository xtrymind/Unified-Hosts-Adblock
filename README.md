# Unified Hosts Adblock
Small adblock magisk module using unified host files from Steven Black [(Check out his github for more information)](https://github.com/StevenBlack/hosts)  
##Usage: 
#### First Enable Systemless Hosts in Magisk Manager
 - Open terminal then type:  
 `su`  
 `hosts`
 - Then follow the prompts to install host file of choice
OR
 - Open terminal and type:
 `su -c hosts arg1 arg2 arg3`
 - The script will apply your arguments all at once and close. Useful for automation purposes
 - For example: `su -c hosts m wr b`
 - Script will apply the master filter, then your regex whitelist, then your blacklist

#### Whitelist Instructions:
 - Create a text file on sdcard called "whitelist"
 - Either add exact lines you want remove to it -> Run hosts script and choose whitelist option
 - Or add regex for lines you want removed -> Run hosts script and choose whitelist regex option

#### Blacklist Instructions:
 - Create a text file on sdcard called "blacklist"
 - Add exact lines you want to remove it (do not include the 0.0.0.0 -> so for example: "facebook.com")
 - Run hosts script and choose blacklist option
 
#### To Remove Whitelist/Blacklist:
 - Just run hosts script and reinstall host file of choice

## [Support](https://forum.xda-developers.com/apps/magisk/magisk-unified-hosts-adblocker-t3559019)

## Changelog
v1.0
 - Initial release

v1.1 
 - Changed from using curl to wget and built in wget (not all roms have curl apparently)

v1.2
 - Made minor changes to Readme, removed support and donate links from module.prop, and removed changelog to meet standards of magisk manager 4.2 update

v1.3
 - Removed broken disable option and added directions for disabling hosts mod

v1.4
 - Added date hosts were last updated (so you can determine if yours need updated)
 - Added whitelist feature
 - Minor restructuring of hosts script header

v1.5
 - Updated to magisk 11.5 (template v2)
 
v1.6
 - Updated to magisk 11.6 (template v3)
 
v1.7
 - Added pixel support
 
v1.8
 - Added all possible letter combinations (order no longer matters)
 - Fixed up pixel support - still WIP (thanks to @ahrion at xda-developers)
 - Fixed Last Updated date change
 - Added update check notification at beginning of script

v1.9
 - Fixed last updated date change
 - Fixed whitelist option
 
v2.0
 - Moved included wget to out of system completely, hosts script is only file that will use it (prevents potential conflicts). Thanks to @rignfool and @veez21
 - Added wildcard support to whitelist
 
v2.1
 - Update for magisk 13.1 (NOTE: previous versions of magisk are no longer compatible)
 
v2.2
 - Added blacklist feature
 
v2.3
 - Bug fixes for pixels
 
v2.4
 - Added cache workaround (oddly absent from magisk module template v4). Thanks to @g40q90 at xda-developers for troubleshooting
 
v2.5
 - Added fixes for samsung stock kernel users. Thanks to @jenslody at xda-developers for the fix
 - Fixed versioncode for magisk manager (thanks to @Nomelas on github for pointing it out)
 - Script now won't throw error if user inputs 'm' with other options (for example, inputting 'mfp' instead of 'fp' won't thrown an error) (thanks to @Didgeridoohan at xda-developers for the idea)
 
v2.6
 - Added argument capability to the script for easy automation (thanks to @Didgeridoohan at xda-developers for the idea)
 - Moved all temporary files to /cache, added unique prefix to all to prevent errors due to already existing files/folders
 