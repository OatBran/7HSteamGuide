# FF7 7thHeaven Steam Conversion
 
**A Detailed 7th Heaven 2.0+ Guide With Manual FFNx Update**
   - Written By: [OatBran](http://forums.qhimm.com/index.php?action=profile;u=27603) 
   - For 7H Version 2.2.1.485 & [FF7 Steam Build 115956](https://steamdb.info/depot/39143/manifests/)
     - Last Guide Update: July 3rd, 2020

# Pre-Requisets

**Be Absolutely Sure you have done the following before following this guide**
  - **[Purchase a LEGAL copy of Final Fantasy 7 on Steam](https://store.steampowered.com/app/39140/FINAL_FANTASY_VII/)**
    - 7th Heaven is ONLY compatible with the English, French, German, and Spanish versions of FF7
      - Or you can try the bundled GameConverter.exe that comes with 7th Heaven located in its resources folder.
  - **There is Absolutely [NO SUPPORT]() for manually updating or modifying your 7th Heaven client installation! assess the possible benefits and risks before you decide to try unsupported things!**
  - **There is Absolutely [NO SUPPORT](https://github.com/OatBran/7HSteamGuide#YARRRRRR) for Pirated copies of the game**
    - **This can include certain unofficial "Language Packs" - Be Cautious**
  - **Change your [Folder View Settings](https://kb.blackbaud.com/articles/Article/41890) to properly display files, to avoid renaming mistakes**
  - **Be aware of the version of Windows you are using. FFNx is only compatible with windows 7 or higher as of version 1.6.1**
  
  
# HEY USER READING THIS GUIDE!!!
**7th Heaven now uses FFNx natively with a default installation!, you dont have to manually alter the 7H installation anymore to solve common issues caused by the use of the legacy Aali driver. However, 7H gets updated fairly rarely, and is actually in beta right now. FFNx actually gets updated daily pretty much, so if you want to use a canary version of FFNx, or possibly a stable version upgrade that is released ahead of its incorporation into 7H itself you may want to still follow the contents of this section, but depending on factors at the time it may provide relatively little value to go through the effort. FFNx is only rapidly updated currently in the pursuit of major features and bug fixes at this stage in development. this will slow down at some point and become less and less relevant to even consider the already-questionable decision to try and mess with the default driver included with 7H**

**If you would rather just play with the stable version chosen for the release of 7H but you want to either:
learn how to acquire and use IRO mods in the first place, [skip here.](https://github.com/OatBran/7HSteamGuide#Acquiring-and-Installing-IROs)
or just convert/use all DDS texture mods for enhanced performance: [skip here.](https://github.com/OatBran/7HSteamGuide#PNG-To-DDS-Conversion)**

**You can also manually [change all the config options](https://github.com/OatBran/7HSteamGuide#Manual-Configuration-of-FFNx) that are not included in the UI of 7H.
as well as change the UI of 7H itself but i havent written that yet - if people even want to know how to do that or want me to just make a custom xml to be distributed here then [let me know!](http://forums.qhimm.com/index.php?topic=19932)**

**If you are Starting from scratch:**

1. Install FF7 via Steam Client and/or [Verify Integrity of Game Cache](https://support.steampowered.com/kb_article.php?ref=2037-QEUH-3335)

2. [Download 7th Heaven 2.2 BETA](http://7thheaven.rocks/releases/Setup-SeventhHeaven-BETA-v2.2.1.486.exe)

3. Open the 7H Installer and install 7th Heaven to default location `C:\7th Heaven\`

4. Open 7th Heaven and verify it found your installation of FF7 on Steam
   - If auto-detect fails, configure each field on the dialogue pop up to the correct location.

5. Click the `Play` button in the top left. 
   - Launching via 7th Heaven Client completes the following tasks **Automatically:** 
     - Copy needed files from your Steam installation, Create needed directory structure 
     - Patch `Steam-2013 FF7.exe-v1.09` Downgrading it to `1998-Eidos FF7.exe-v1.02`    
       - **Note that your Steam installation is not modified in any way. It will still function as normal.**
     - A Completed 7H Modded Install is created at `C:\Games\FF7\`     
     - Quit the game once you reach the title screen
       - **Be aware;** Launching the game via 7th Heaven disables ALL Steam features and integration

### Manual 7H Upgrading
**THERES NO SUPPORT FOR THIS AND YOU PROBABLY WONT BENEFIT FROM TRYING THIS SO SKIP TO THE NEXT SECTION**

6. Open the newly created 7H Modded Install directory `C:\Games\FF7\`
   - Locate the file `ffnx.dll` and RENAME this file to `ffnx.dll.BAK`
   - As you proceed from here on, Keep the following in mind.  
&nbsp;
&nbsp;  

   >**Manually Changing/Upgrading 7th Heaven is NOT SUPPORTED officially by the [7th Heaven Team](https://github.com/unab0mb/7h#authors).**
   
   >**Please DO NOT approach [7th Heaven Team](https://github.com/unab0mb/7h#authors) if something is not working properly.**
   
 
7. Download FFNx. Acquire **Only** the `FFNx-FF7_1998` archive for 7H Installs! ***NOT The FFNx-Steam Release!!*** EXTREMELY IMPORTANT!
   - The [Stable](https://github.com/julianxhokaxhiu/FFNx/releases/) Release has the most testing and is the most reliable on average.
   - The [Canary](https://github.com/julianxhokaxhiu/FFNx/releases/tag/canary) Release Is the bleeding edge build and changes constantly. Stability varies.
&nbsp;  
&nbsp;  

   >Note that Canary builds are further ahead in development, but using those comes with risks, be aware of those risks and expect more problems to occur! SAVE OFTEN
   
   >Note that Canary is also a rolling-beta branch, there is only ever 1 build available at any one time. Previous versions are not hosted. 
   
   >If you plan to update Canary builds frequently KEEP BACKUPS of previous builds in case of instability or other unforeseen issues!


8. Extract the downloaded `FFNx-FF7-1998` archive to BOTH of these locations:
   - your 7H Modded Install directory `C:\Games\FF7\`
   - the 7H resources folder `C:\7th Heaven\Resources\Game Driver` overwriting all the files. might want to backup the whole game driver folder first. 
   - Ignore the included `ffnx.reg` file, do not execute it.

9. Open 7th Heaven and click `Play` in the top left. 
   - Verify that the game launches, and reaches the title screen. Game will be in a very small window. **This is normal.**
     - If you do not reach the title screen, immediate crash, or only black screen. Double check you did step 6-8 correctly.
     - If you instead get Null Reference Exception, [read this](https://github.com/OatBran/7HSteamGuide#Common-Game-Launch-Problems)
   - Quit the game.

## Manual Configuration of FFNx

**After verifying FFNx is installed correctly, you may want to change its behavior.** 

10. Navigate to the 7H Modded Install `C:\Games\FF7\` \( [*Or another FFNx.dll Installation*](https://github.com/julianxhokaxhiu/FFNx#how-to-install) \)
   
   - Locate the file `ffnx.cfg` and OPEN this file with a text editor.
   - READ though this file, and locate settings you want to change. REMOVE leading \# Symbols to set values to be read at runtime.
     - Copy any of these to your clipboard and search in-file with `CTRL+F` if you cant locate them
   - DOUBLE CHECK for typos and removal of comment \# symbols for each change you make. 
     - THIS IS VITAL! DO NOT FORGET!!
     
     - `renderer_backend`
       - `Direct3D11` is commonly reported to perform well.
     - `fullscreen`  
       - Change to `yes` to allow fullscreen
     - `resolution settings`  \( are a collection of the following 2 values \)       
       - `window_size_x = 1920`  
       - `window_size_y  = 1080`
         - If your `fullscreen = yes` leave both set to 0 to use your desktop resolution. 
         - For `fullscreen = no` [Use This Chart to aid in determining your desired resolution](https://en.wikipedia.org/wiki/Display_resolution#/media/File:Vector_Video_Standards8.svg)
     - `resolution_scale` 
       - Experiencing high RAM usage and graphical errors using many PNG texture IRO's ? 
       - Change value to 2 for better performance, [or use DDS textures.](https://github.com/OatBran/7HSteamGuide#PNG-To-DDS-Conversion)
     - `preserve_aspect` 
       - Set to `no` if you want the black sidebars removed and render stretched to window size.
   - READ through the rest of the file and decide if you want to make other uncommon changes. 
     - Valid configuration options are listed in the .cfg file itself. 
     - Lines containing values to modify are preceeded by a line of `~~~~~~~`
   - *Debugging Options*
     - `show_stats`
       - Set to `yes` to show debug related stats on the title bar if windowed / top-left corner if fullscreen
     - `renderer_debug`
       - Set to `yes` to show extended debug info to the screen. Dont use unless you know what to do with the info.
     - `ff7_more_debug`
       - Set to `yes` to write many engine related things to a log file, use only if you are troubleshooting crashes    
    
   - SAVE the file and exit the editor.


  - Be aware that there is no configuration option for preferred display adapter. Your primary display will be used for fullscreen runtimes.
    - It has been reported (but not confirmed!) by @Barachiel that very high DPI settings in combination with >1440p HD resolution settings can cause graphical glitches with models displayed in the game. Try lowering your DPI to <200 if possible in the event of glitchy models being displayed.
    - If you want to play on your secondary / tertiary display, you need to use windowed mode. There is a fullscreen borderless window mod on the 7H catalog that you can use in this case.

  - **If you are planning on using the maximum amount of HD models/textures and/or in combination with the Cetra/ECHOS/CAMS mod, you may want to do the following**
    - [Apply the Large-Address-Aware patch](https://ntcore.com/files/4gb_patch.zip) to `C:\Games\FF7\ff7.exe` allowing the game to utilize 3.5GB of RAM, effecively doubling the capacity for mod data.

## Acquiring and Installing IROs

**Finally you are ready to start installing your mods**

11. Open 7th Heaven and browse/download catalog IRO's, or [manually download IRO mod packs](http://forums.qhimm.com/index.php) prioritize [DDS converted packs.](https://forums.qhimm.com/index.php?topic=19204.0)
   - For manual IRO Downloads, Click on `Import-Mod` Button in right sidebar to open IRO import tool. 
   - Select batch/single tab and select folder/file to import from. 
   - Activate any selected catalog mods, or manually imported mods with Toggle 
   - Configure one-by-one, clicking the settings `Cog Button` with mod selected and active. Assign category if necessary.
   - Click on `Auto-Sort` Button, 4th from the top on right side bar.

12. In 7th Heaven Window click top left `"Settings" -> "Game Launcher"` and identify / select your needed controller configuration and other personalized launch settings. Click save. 
    - `Steam KB+Swap AB/XO Gamepad` for XInput North American Button Layout Control Configuration
       - ***Help! My Playstation DS4 controller isnt working!***
          - [Use DS4Windows](http://ds4windows.com/) Select DS4W driver as preferred gamepad in devices and controllers windows control panel \(Xbox360 wireless controller\)

13. Click Play in top right and enjoy your modded FF7 Experience with 7th Heaven & Updated FFNx!
    - Consider [upgrading your PNG texture packs to DDS Format](https://github.com/OatBran/7HSteamGuide#PNG-To-DDS-Conversion) if using the catalog IRO's for better performance 


### Common Game Launch Problems

**A series of issues after installing / upgrading  7th Heaven with FFNx**

   - Covers _FAQ:_ **Help! I'm getting the `Value cannot be null. Parameter name: input` Error on launch**

* This error means you have a corrupt/incorrect `ffnx.dll` or a somehow faulty 7th Heaven Installation. use a compatible graphics driver, or Restart the entire process from scratch and try again. Make absolutely sure you did step 6 correctly if you manually updated FFnX. if you are upgrading from a 7H 2.0 install and you used a super old version of ffnx previously, then thats the problem you need to remove the ffnx.dll from the modded game install directory. `C:\Games\FF7\` and 7H will copy a newer one in there for you when you hit play, fixing the error.
   - Before you attempt to repair a broken installation, ensure a backup of your user data. \( if any relevant data exists \)

1. Backup your `*.iro` mods by copying `C:\Games\FF7\mods\` to a new location; Ex. `C:\7h-mods-backup\`
   - Use your backup location to import IRO files from, [during step 11 above.](https://github.com/OatBran/7HSteamGuide#FF7-7thHeaven-Steam-Conversion)

2. Backup your `*.ff7` save files by copying `C:\Games\FF7\save\` to a new location; Ex. `C:\FF7Saves\`
   - Copy from your backup location to `C:\Games\FF7\save\` [after step 6 and before step 13 above.](https://github.com/OatBran/7HSteamGuide#FF7-7thHeaven-Steam-Conversion)

3. Backup your 7th Heaven profile by copying `C:\7th Heaven\7thWorkshop\profiles\Default.xml` to a new location; Ex.`C:\7h-profile\`
   - After restoring your backup IRO files from [this sections step 1,](https://github.com/OatBran/7HSteamGuide#Common-Game-Launch-Problems) close 7th Heaven and copy this file back to its original location and overwrite it.
   - \( Step 3 is completely optional, and possibly not needed! Depending on changes to your IRO file set your old profile could be useless. Reconfiguration of individual IRO settings may be required regardless.  \)

4. DELETE both `C:\Games\FF7\` and `C:\7th Heaven\`

5. Uninstall FF7 through the steam client.
   - Delete `Final Fantasy VII` Folder from your `%Steam%\steamapps\common\` directory.

6. [Restart install process from beginning;](https://github.com/OatBran/7HSteamGuide#FF7-7thHeaven-Steam-Conversion)

### YARRRRRR!

**If you instead get the following `Error code: YARR! Unable to continue. Please report this error on the Qhimm forums.`**

 - Save yourself the embarassment of actually posting on the forums, because you more than likely are trying to use a pirated copy of the game. **This can happen with language "patches"** even with a valid purchased copy. If you believe that a legitimate copy has been a target of a false-positive, then please by all means contact @Unab0mb on the forums or discord and provide your proof. Do not waste our time trying to pass a pirated copy as legitimate. You will not succeed. There has only ever been 1 semi-false positive proven in the entire history of the community. Just spend the $5 and buy a legit copy.


# PNG To DDS Conversion

**How to Identify, Convert and Replace PNG-Based Texture Packs**
  
  - Covers _FAQ:_**Help! Running FFNx with many texture mods feels choppy or slow! Especially in battle!**
   
   - **IMMEDIATELY DISABLE the "60FPS Battles" Mod located in the "Animations" Catalog! This mod in combination with FFNx severely hinders in-battle performance and has no positive effect on the game whatsoever. DO NOT IGNORE THIS**

1. [Download the SYW Pack Builder](https://forums.qhimm.com/index.php?topic=19204.0)

2. Open 7th Heaven and identify the mods you are replacing. The pack builder can REPLACE the following iros in the 7th Heaven Catalog
   - `World Textures - Qhimm Catalog` <==> `Worldmap upscaled textures`
   - `Field Textures - Qhimm Catalog` <==> `Fields background upscaled textures`
   - `Battle Textures - Qhimm Catalog` <==> `Battle background upscaled textures`
   - `Spell Textures - Qhimm Catalog` <==> `Magic and combat Fx textures`
   - `Minigames - Qhimm Catalog` <==> `Minigames upscaled textures`
   - `User Interface` / `ESUI` <==> `Menu (SYW v4 HD gui)` **NOT a direct ESUI or Full "User Interface" Replacement!**

3. Open the pack builder, and configure it to your needs based on the information gained from step 2 
      - [Image on thread from step 1](https://forums.qhimm.com/index.php?topic=19204.0) is the recommended default settings
   - _FAQ:_ **Help! Pack Builder wont open! Says its a virus!** 
        - Disable your Antivirus / Windows Defender RealTime protection. Pack Builder is Safe.

4. Click on `"Make IRO from DDS Files"` Button. 
   - Recommended to use`"nothing"` compression level for best performance.
   - Be patient and wait for it to finish.

5. Open 7th Heaven, Toggle Each Active Mod being replaced to `Off`
   - *OR* outright REMOVE them by clicking the trashcan icon in right sidebar
   - *OR* Backup PNG IRO's being replaced Moving them out of `C:\Games\FF7\mods\7th Workshop`
   - Click refresh inside of 7th Heaven

6. In 7th Heaven click `"Import Mod"` Button 
   - Select `"Batch Import"` tab 
   - Select Output Folder from step 4, click OK.
      - *OR* COPY the produced IRO files from step 4 into the mods folder `C:\Games\FF7\mods\7th Workshop` 
   - Click Refresh in 7th Heaven

7. Activate and configure imported DDS IRO's

8. Click Play with mods in top left and enjoy the 40-70% increased performence over PNG!


## Manual PNG To DDS Conversion

**Optional but recommended - Mixing texture formats is not optimal for performance!** 

- Covers _FAQ:_ **I have other PNG mods that arent included in the pack builder!** 
    - Includes mods such as ESUI, Avatars, Gameplay mods with textures, etc.
- **During Manual DDS Conversion, ONLY graphical-related mods are required to be converted. (PNG textures+mipmaps only) However, the following tool allows conversion of any IRO it just extends the conversion time needlessly.**

9. [Download the PNG to DDS Converter tool by satsuki](http://forums.qhimm.com/index.php?topic=19701.0)
   - Extract archive to a working directory; Ex. `C:\PNG2DDS\`
   - Open `Satsuki.IroPng2Dds.exe` 
        - Again Possibly needing to disable AntiVirus RealTime Protection

10. Identify mods for conversion and disable them in 7th Heaven.
   - Open your 7th Heaven mods folder `C:\Games\FF7\mods\7th Workshop`
   - Select the mods identified previously and drag them all to the open Converter window
   - Select your conversion options.  match them to [image on the thread in step 9](http://forums.qhimm.com/index.php?topic=19701.0), 
       - Default options Illustrated are **highly** recommended!

11. Click `"convert iro to dds version"`    
   - ***Help! nothing happens or I get errors during conversion!***
   - Install the provided runtimes located in the `"runtimes"` folder of the extracted package. Run the converter as administrator in a file-writeable directory

12. Import and configure the converted IRO's via the same method [outlined in steps 5 & 6 above.](https://github.com/OatBran/7HSteamGuide#PNG-To-DDS-Conversion)

**Additional DDS Texture Mod Information**

- If you have a mod list that contains BOTH DDS and PNG mods active simultaneously, be aware that due to the way the windows API functions with FFNx, data is sent as it appears in the load order. However, PNG textures are considered FALLBACK/LEGACY by FFNx, and DDS format is prioritized. Meaning, If you want a PNG texture mod to be loaded instead of a DDS one and you have it set before (i.e ABOVE) the DDS version, it will make no difference. The DDS mod will take priority no matter what. This can cause issues between mods that share file structure. Part of a PNG mod can and WILL be overwritten by the DDS portion of another. Hopefully that explaination made sense. Try your best to only use one format or the other. At least pay extra attention to your active toggles and load order in the event you have a heavily mixed-format mod list in your 7th Heaven client. (7H PROFILES ARE YOUR FRIEND HERE)

## Thanks

**Thank you for reading.**

**Special Thanks to those who helped me gather the information needed to make this**
- *\[TrueOdin\]*
- *\[Unab0mb\]*
- *\[SithLord48\]*
- *\[LordUrQuan\]*

# End of Guide

**Go back to the [Forum Thread](http://forums.qhimm.com/index.php?topic=19932) and tell me what you think! Or post questions if you are having trouble!**

**Join the [Discord](https://discord.gg/N6M6pKS) and hit me up on there if you want too, if posting on forums isnt your thing**
