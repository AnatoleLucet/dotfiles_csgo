# Documentation

[Go back to menu](https://github.com/AnatoleLucet/dotfiles-csgo)

**I just want to pressise that documentation is made for beginner so if something looks useless for you just skip it or go at the part you are interested in by the summary**

## Summary

[Firstly](#firstly) (must be read)

[All available functions and commands](#all-available-functions-and-commands)

[Configuring your graphic settings](#configuring-your-graphic-settings)

[CFG Configuration](#cfg-configuration)

## Firstly

Ok so i recommend you to install a complex code editor like the portable version of "[**Sublime Text 3**](https://download.sublimetext.com/Sublime%20Text%20Build%203143%20x64.zip)".

You can also use another editor like "**Atom**", "**Visual Studio Code**", BUT **don't use the windows notepad** or you will wast a lot of time. Let me explain why : github (the actual site you are on) is compressing every files by removing all line break, so you will have to use a real code editor if you don't want to press enter +600 times for aving all our line break again... Anyway.

---

### All available functions and commands

#### Easly join a community server in the console

What it does | Console command
--- | ---
Join a surf server | play_surf
Join a bhop server | play_bhop
Join a kz server | play_kz
Join an arena server | play_arena
Join an hns server | play_hns
Join a deathmatch server | play_dm
Join a duel server | play_duel

**Configuration :**

1. Open autoexec.cfg with you text editor
2. Press <kbd>ctrl</kbd>+<kbd>f</kbd> to open the search tool
3. Search "Easy Connect"

Now you should see somes line like this one : `alias "play_hns" "connect 185.114.224.63:27169"`

If you want to change the command you will type in your console you just have to modify the alias name. In our case we can change `"play_hns"` per `"join_my_favorite_server"` **BUT DON'T REMOVE "alias" OR IT WILL NO LONGER WORK (same for connect, you will see bellow)** .

If you want to change the server you will connet to, simply connect to the server > type `status` in the console and you should see the server IP (somewhere). Copy this IP and replace the one you want to change in the alias **BUT (again) DON'T REMOVE THE "connect" OR IT WILL NO LONGER WORK**.

If you want to create a new alias just duplicate one line and change the alias name and the ip. **And remember : two alias can't have to same name !**

#### Training commands
What it does | Console command
--- | ---
Join dust2 in solo and execute a dm commands layout | dm_dust2
Join mirage in solo and execute a dm commands layout | dm_mirage
Join inferno in solo and execute a dm commands layout | dm_inferno
Join cache in solo and execute a dm commands layout | dm_cache
Join dust2 in solo and execute a dm in hs mod commands layout | dm_dust2_hs
Join mirage in solo and execute a dm in hs mod commands layout | dm_mirage_hs
Join inferno in solo and execute a dm in hs mod commands layout | dm_inferno_hs
Join cache in solo and execute a dm in hs mod commands layout | dm_cache_hs
Join dust2 in solo and execute a training commands layout | training_dust2
Join mirage in solo and execute a training commands layout | training_mirage
Join inferno in solo and execute a training commands layout | training_inferno
Join cache in solo and execute a training commands layout | training_cache

**Configuration :**

Don't configure this if you don't know what you do or you may broke it.

1. Open autoexec.cfg with you text editor
2. Press <kbd>ctrl</kbd>+<kbd>f</kbd> to open the search tool
3. Search "Training / Deathmatch"

And now you can modify the "training_layout" or the alias name.

If you broke something just go on github and copy past the default "Training / Deathmatch" part.

---

## Configuring your graphic settings

**Open** the `video.txt` file with your new fabulous text editor

You will probably see something like this :

    "VideoConfig"
    {
        "setting.cpu_level"                      "0"
        "setting.gpu_level"                      "0"
        "setting.mat_antialias"                  "0"
        "setting.mat_aaquality"                  "0"
        "setting.mat_forceaniso"                 "0"
        "setting.mat_vsync"                      "0"
        "setting.mat_triplebuffered"             "0"
        "setting.mat_grain_scale_override"       "1"
        "setting.csm_quality_level"              "0"
        "setting.mat_software_aa_strength"       "0"
        "setting.mat_motion_blur_enabled"        "0"
        "setting.fullscreen"                     "1"
        "setting.defaultres"                  "1920"
        "setting.defaultresheight"            "1080"
        "setting.aspectratiomode"                "0"
        "setting.nowindowborder"                 "0"
    }

_I don't will explain you all of those lines but you will learn the basics._

So that is your graphic settings in csgo

### Let's set this up

1. **Start** csgo
2. Take a **screenshot** of your graphic settings
3. **Close** csgo

[My reference screenshot](https://prosettings.net/wp-content/uploads/2016/11/csgo-settings.jpg)

This table will help your to translate your graphic settings in to your video.txt (if the settings is not in you video.txt file just add the a new line with the parameter)

name (on screenshot) | set (on screenshot) | videos.txt |info
--- | --- | --- | ---
Brightness | 1.6 | "setting.mat_monitorgamma" "1.6" | can go to 1.6 at 2
Resolution (width) | 1920 x | "setting.defaultres" "1920" | change this value if you want to change your width in-game resolution
Resolution (height) | x 1080 | "setting.defaultresheight" "1080" | change this value if you want to change your height in-game resolution
Aspect Ratio | 16:9 | "setting.aspectratiomode" "1" | 0 = 4:3, 1 = 16:9, 2 = 16:10
Display Mode | Fullscreen | "setting.fullscreen" "1" | 0 = windowed, 1 = fullscreen
Display Mode (Windowed Fullscreen) | Not on screenshot | "setting.nowindowborder" "1" | 0 = disabled, 1 = enabled
Global Shadow Quality | Very Low | "setting.csm_quality_level" "0" | 0 = very low, 1 = low, 2 = medium, 3 = high
Model / Texture details | Low | "setting.gpu_mem_level" "0" | 0 = low, 1 = medium, 2 = high
Effect Detail | Low | "setting.cpu_level" "0" | 0 = low, 1 = medium, 2 = high
Multicore Rendering | Enabled | "setting.mat_queue_mode" "-1" | -1 = system default (recommended), 0 = synchronous single thread, 1 = queued single thread, 2 = multithreading
Multisampling Anti-Aliasing | None | "setting.mat_antialias" "0" | 0 = none, 2 = 2x MSAA, 4 = 4x MSAA, 8 = 8x MSAA
FXAA Anti-Aliasing | Disabled | "setting.mat_software_aa_strength" "0" | 0 = disabled, 1 = x1, 2 = x2, 4 = x4, 8 = x8, 16 = x16
Vertical Sync | Disabled | "setting.mat_vsync" "0" | 0 = disabled, 1 = enabled
Motion Blur | Disabled | "setting.mat_motion_blur_enabled" "0" | 0 = disabled, 1 = enabled

---

## CFG Configuration

**If you find a command and you want to know what it does : you can type the command on [this site](https://tools.dathost.net/csgo-commands).**

[Go back to menu](https://github.com/AnatoleLucet/dotfiles-csgo)
