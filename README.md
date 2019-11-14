# FAQ
## Here you can find the most common questions and their respective answer. Simple as that. READ THEM.

**Q - How do I use WakeBlock?**

**A** - Once you have installed the app, just open it and click on "Install Core Mod". Choose your flash type off the list (Automatic = Flashed once the zip file is created, Manual = Manually reboot to recovery and flash the flash-me.zip in the WakeBlock folder, Magisk = Manually open the Magisk app and flash the wakeblock-magisk.zip inside the WakeBlock folder) and flash it!
**Side Note:** There is no difference in the patch itself between the different flashing method. The generic course of action is to use the Automatic or the Magisk flash. If those fails, try the Manual one.

**Q - How can I block wakelocks?**

**A** - From within the app, just switch to the "Wakelock" tab. Here every wakelock recorded since the first boot with the core mod installed, so give it at least 2/3 days of normal use before blocking anything. Click on the wakelock you want to block, press the "Block" button and then set for how long is the wakelock gonna be blocked!

**Q - Which wakelock should I block? For how long?**

**A** - We suggest to check out this guide on XDA (https://goo.gl/PFAPJ2) to fully understand what it means to block a wakelocks and how it affects your system. 

**Q - I'm lazy af and I don't want to read all of that, can't you give me a short list?**

**A** - Ok, but we don't take any responsibilities if the phone bricks or your ROM explodes. You are totally free to change the blocking time value to make it as you please but, again, we don't take any responsibilities. You can find the list here: https://github.com/MrLast98/WakeBlock/blob/master/wakelocks.md
**Remember:** if you don't find one of the wakelocks, just check in later. If you still don't find it, don't worry at all!
**Side Note:** the search button is _not_ case-sensitive.

**Q - Can I block the [wakelock name] wakelock?**

**A** - If it is part of the list linked above, you're good to go! If not, we can't assure a thing, but if you find any safe-to-block wakelock let us know!

**Q - Your app is great: How can I donate to you guys?**

**A** - First, thank you! Second, we have a Patreon set up! Here's the link! https://www.patreon.com/wakeblock

**Q - I installed the Magisk Module and everything exploded! How can I remove it?**

**A** - If you phone bootloops (it\'s HIGHLY UNLIKELY, but we stil love your device) simply create a file in your /system (or /system/system for A/B devices) called "disable.module" and the module will be automagically removed! After the removal, you MUST remove the disable.module file by yourself [Temporary]

**Q - When is the new version/fix/graphic coming?**

**A** - _Do not ask for an ETA._ We do this for free, without any ads in the app nor donation packages, we don't even put a price on our app. We all have jobs, university and a private life to manage, we don't have superpowers, so managing all of this takes time. Our free time is pretty short, but we usually put at least half of it on the developing of the app. Be patient and do not harass the team nor the Telegram group.

**Q - Your app killed [insert any feature here] in my phone!**

**A** - Everything is done by user input, the app by itself (even with the core mod installed) doesn't do anything but reading which wakelock the system is calling. Unless you blocked something we didn't suggest you do to this problem and our app are totally unrelated.

**Q - I want to build the service.odex for my phone manually, how do i do that?**

**A** - **GUIDE FOR ODEXED ROMS** Easy: Download the **whole sourcecode** of your ROM, then copy the files you find here https://goo.gl/vg23MU in _wakeblock/templates/java/services/core/java/com/_ and place them into the sourcecode. You will deal with _two_ files: *PowerManagerService.java* and *WakeBlockService.java*. For **WakeBlockService.java**, you just need to create the directory tree into your sourcecode **corresponding to the GitHub directory tree** (_services/core/java/com/giovannibozzano/wakeblock_) and place the file there, for **PowerManagerService.java**, you have to check inside the *PowerManagerService.java* file on GitHub for the piece of code **surrounded in "WAKEBLOCK" comments** and place that piece of code **in the same place inside your PowerManagerService.java** in ***the same place as you see in the file on GitHub***. Then, just run the command **make services** in your shell of choice and you will have in your output directory *all the files you need!* (**SIDE NOTE:** You only need **service.odex and service.vdex**, nothing else). Just copy the old .odex and .vdex somewhere as a backup and place the file you created in the *right directory* (**/system/framework/oat/arm** or **/system/framework/oat/arm64**, depending on your system). If it bootloops, **you might have fucked up!**

**Q - Your app is killing my battery life! WTF!**

**A** - By itself, the app doesn't do anything even with the core mod installed. Keep WakeBlock whitelisted in every hybernation app (like greenify) but the basic Android Optimization. If the battery drain has increased, double check what you blocked, that might be the reason!

**Q - How can I MANUALLY uninstall the app/coremod?**

**A** - First of all, *we are sad that you want to leave us.* If you **didn't install the Core Mod**, or it failed in any way, *you just need to delete the app* and everything is gone! If you **did install successfully the Core Mod**, check the WakeBlock backup folder ***(/sdcard/WakeBlock/Backups).*** Here, you will have one of **two cases:**

1. If you flashed the file using the **"Automatic"** or **"Manual"** option, you will find different folders with a backup inside them in /sdcard/WakeBlock/Bakups, *they are taken every time you patch and won't be deleted unless you manually delete it*, just **flash the zip file inside the folder with the most recent date and you're good to go**.

2. If you went for the **"Magisk Module"**, simply *create a file in your /system (or /system/system for A/B devices) called* ***"disable.module"*** and the module will be automagically **removed!** After the removal, you *MUST remove the disable.module file by yourself*.

**Q - YOUR APP DOESN'T WORK, WHY?**

**A** - It works. We tested it (and we keep testing it) many times before committing an update! Double check permissons and give it a reboot, usually fixes most of the "doesn't work" problems.

**Q - I found a bug! How can I report it?**

**A** - First of all, check on the telegram group (https://t.me/wakeblock) if anyone else had your problem, both by first searching and then asking directly. It will ask for a logcat, so make sure you make one while you encounter the problem. _DO NOT CONTACT ANYONE OF THE TEAM UNLESS EXPLICITLY ASKED TO._

**Q - How do I take a logcat?**

**A** - First of all, make sure that you have the needed _Platform Tools_ (https://goo.gl/2rgkLY). Due to the fact that the app reboots, it's better if you take it with a pc rathern than with an app. Plug the phone into your PC, you start the cmd.exe as administrator (or, if you use Linux, you need to open the terminal with root privileges) and run the command _"adb shell"_, now the console will show the internal console of the phone. From there, run _"su"_, a prompt will appear to your phone to ask for root permission. Approve it, then run "cd /sdcard/Download". Afterwards, run _"logcat >> log.txt"_ (Nothing will appear on screen because it's redirecting every output to the log file). Now start the patch. When it gives the error (or after it reboots), close the app, click _"Ctrl + C"_ to stop the logcat. Then, from the phone, send us the log.txt (you will find it in your Download folder).

## TO-DO LIST
- Alarms. Yeah.
- Flags for extensive debug messages vs a phase based message
- Kernel Wakelocks? Maybe?
- Various fixes and improvements
