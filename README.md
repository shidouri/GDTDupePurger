# GDTDupePurger
A one-file script that takes duplicate asset errors from Black Ops 3 Mod Tools' linker output and attempt to resolve them.

# This version of GDTDupePurger is legacy and will no longer be updated. Instead, you should use GDTDupePurgerPy found here: 
## https://github.com/shidouri/GDTDupePurgerPy


How to use:

Do "Compile" in BO3 MT. If you have duplicates, they will show in the linker output, such as:

    J:\Steam\steamapps\common\Call of Duty Black Ops III\/gdtdb/gdtdb.exe /update

    gdtDB: updating

    errors found while updating database!

    ERROR: Duplicate 'beam' asset 'flamethrower_beam_dragon_gauntlet' found in j:\steam\steamapps\common\call of duty black ops iii\source_data       \wpn_t7_zmb_dlc3_gauntlet_dragon.gdt:2296
    ERROR: Duplicate 'beam' asset 'flamethrower_beam_dragon_gauntlet' found in j:\steam\steamapps\common\call of duty black ops iii\source_data\wpn_t7_zmb_dlc3_gauntlet_dragon_1.gdt:2296
    gdtDB: processed (2 GDTs) (584 assets) in 0.222 sec


Copy that entire output (all of the text). Open **dupe_error.txt** in a text editor such as notepad, paste the text, then save it and close.

Run ***dupe_fixer.exe***. The console window will show you any issues, or its progress through the GDT purging.

Try compiling in Mod Tools again. Your duplicates should be fixed!

Backups of GDTs will be placed in ***<dupe_fixer_folder>/backup***.



**FLAGS**
You can make shortcuts to the exe or run it from the command line with the following flags:

**debug** or **show_flags** - Shows the settings for these flags defined below on start EXE.

**no_preserve_stock** or **nps** - Doesn't take into account stock GDT's and will replace them if they appear first (alpha style purge)

**no_log** or **quiet** or **shh** - Doesn't print the progress it's making, just tells you when it's done.

**developer_no_backup_use_wisely** - Doesn't backup the GDT that gets edited. I DO NOT RECOMMEND USING THIS, EVER.




**NOTE**

v.1.0b only deletes a single duplicate for each asset.
If you have multiple duplicates of one asset, you will need to try compiling in MT after running **dupe_fixer.exe** to get the updated error list, and repeat as many times as necessary.
This will be fixed on full release.




