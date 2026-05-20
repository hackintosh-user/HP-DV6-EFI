## General
Welcome to this Github Repo! This repo has the EFI Folder for the HP Pavilion DV6-7070ex Ivy bridge notebook from 2012,
the EFI has an OpenCore Config to boot macOS Sequoia, Sonoma, and Ventura on this Ivy bridge laptop. But Some notes below

## NOTES
* This is a pre built EFI, i made it, So if you encounter any issues and go report to the Hackintosh Subreddit, or the Hackintosh
Discord, they will tell you to rebuild it yourself!! IF you have Any issues Please reffer to the Issues tab in this github repo.
* You will Need OpenCore Legacy patcher for Running macOS monterey 12 and later Due to Apple Dropping the Intel HD 4000.
* if your DV6-7070ex has a broadcom BCM Card, it is most likely unsupported in Modern MacOS! Switch it out with a: Intel Card Or
a Supported BCM Card with OCLP.
* OCLP Still Does not Support macOS Tahoe As of May 2026. If you Plan on Running macOS, Choose macOS Sequoia or macOS Sonoma as
they Still get Security updates.
* * In the Platform Tab in the config.plist i will leave it empty as you are required to Use GenSMBIOS to make a MacBookPro SMBIOS. [Use This Link to Get GenSMBIOS](https://github.com/corpnewt/gensmbios)


## Known Issues
* the "HP TrueVision" Webcame is turned off in the UTBMap.kext.
* Same Goes for the Intel Bluetooth Controller. It is Disabled.
* for macOS Sequoia+ You will need itlwm+heliport Or use OCLP to patch your WIFI.
* If Your Laptop's Screen is 1366x768 it will look like Shit! (forgive me but true).
* When Booting macOS Ventura+ Your System needs [Cryptexfixup.kext](https://github.com/acidanthera/CryptexFixup)
* When Booting macOS Ventura + Your system will Fail to boot with the boot arg
  ```zsh
  Debug=0x100
  ```
  remove it from the Congfig.plist in the NVRAM Section of said plist.


  ## Specs

  your System must have the following to make sure this EFI is a Perfect Fit here they are Below

  * CPU: intel Core i7-3610QM
  * RAM: either the  Stock 8GB or maxxed out 16GB Will be Fine But 8+ i recommend for Sequoia and Soon later.
  * SATA Mode: Must be AHCI for better compatabillity. RAID Is Stock.
  * WIFI: intel Card is prefered as Most BCM cards from 2012 are not Supported in macOS ( well atleast modern macOS)
  * Some Form of OS to make the Installer ( could be Windows Or Linux But Must have Python3. or A Mac).
  * GPU(s):
          * Intel HD Graphics 4000
          * Nvidia Geforce GT 630M ( will be Disabled in the BIOS/openCore)
 
