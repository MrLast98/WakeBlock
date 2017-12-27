# FAQ
## Here you can find the most common questions and their respective answer. Simple as that. READ THEM.

**Q - How do i use wakeblock?**

**A** - Once you have installed the app, just open it and click on "Install Core Mod", the app will create the Core Mod needed for your device (this might take a while) and then will reboot the phone to flash it. When the phone has rebooted, open the app: If the message says "Service Bound" you're all set!

**Q - How can i block wakelocks?**

**A** - From within the app, just switch to the "Wakelock" tab. Here every wakelock recorded since the first boot with the core mod installed, so give it at least 2/3 days of normal use before blocking anything. Click on the wakelock you want to block, press the "Block" button and then set for how long is the wakelock gonna be blocked!

**Q - Which wakelock should i block? For how long?**

**A** - We suggest to check out the Amplify guide on XDA (https://goo.gl/NUYbCj). Remember: if you don't find one of the wakelocks, just check in later. If you still don't find it, don't worry at all! Side note: the search button is not case-sensitive.

**Q - I'm lazy af and i don't want to read all of that, can't you give me a short list?**

**A** - Ok, but we don't take any responsibilities if the phone bricks or your ROM explodes. You are totally free to change the blocking time value to make it as you please but, again, we don't take any responsibilities. You can find the list here: https://goo.gl/xAE8ny

**Q - When is the new version/fix/graphic coming?**

**A** - _Do not ask for an ETA._ We do this for free, without any ads in the app nor donation packages, we don't even put a price on our app. We all have jobs, university and a private life to manage, we don't have superpowers, so managing all of this takes time. Our free time is pretty short, but we usually put at least half of it on the developing of the app. Be patient and do not harass the team nor the telegram group.

**Q - Can i block the [wakelock name] wakelock?**

**A** - If it is part of the list down here, you're good to go! If not, we can't assure a thing, but if you find any safe-to-block wakelock let us know!

**Q - Your app killed [insert any feature here] in my phone!**

**A** - Everything is done by user input, the app by itself (even with the core mod installed), so unless you blocked something we didn't i think the problem and the app are unrelated.

**Q - Your app is killing my battery life! WTF!**

**A** - By itself, the app doesn't do anything even with the core mod installed. Keep WakeBlock whitelisted in every hybernation app (like greenify) but the basic Android Optimization. If the battery drain has increased, double check what you blocked, that might be the reason!

**Q - I just updated and it doesn't see the Core Mod!**

**A** - It's a known bug. Check if the app kept all permission (Both _root privileges_ and _Storage permission_) and simply reboot your phone. It will magically start to see it again! **SIDE NOTE:** you don't need to reinstall the Core Mod every time you update the app!

**Q - How can i uninstall the app?**

**A** - First of all, we are sad that you want to leave us. If you didn't install the Core Mod, or it failed in any way, you just need to delete the app and everything is gone! If you did install successfully the Core Mod, replace the service.odex you find in the data folder (/sdcard/WakeBlock) with the one of your device (Depending on which ROM you use and which device you use, it can be in different positions) and then delete the app. Otherwise, we suggest a flash of the system.img of your ROM.

**Q - YOUR APP DOESN'T WORK, WHY?**

**A** - It works. We tested it (and we keep testing it) many times before committing an update! Double check permissons and give it a reboot, usually fixes most of the "doesn't work" problems.


**Q - I found a bug! How can i report it?**

**A** - First of all, check on the telegram group (https://t.me/wakeblock) if anyone else had your problem, both by first searching and then asking directly. If no one can help you on the spot, send a ticket on the @WakeBlockSupportBot. It will ask for a logcat, so make sure you make one while you encounter the problem. _DO NOT CONTACT ANYONE OF THE TEAM UNLESS EXPLICITLY ASKED TO._

**Q - How do i take a logcat?**

**A** - First of all, make sure that you have the needed _Platform Tools_(https://goo.gl/2rgkLY). Due to the fact that the app reboots, it's better if you take it with a pc rathern than with an app. Plug the phone into your PC, you start the cmd.exe as administrator (or, if you use Linux, you need to open the terminal with root privileges) and run the command _"adb shell"_, now the console will show the internal console of the phone. From there, run _"su"_, a prompt will appear to your phone to ask for root permission. Approve it, then run "cd /sdcard/Download". Afterwards, run _"logcat >> log.txt"_ (Nothing will appear on screen because it's redirecting every output to the log file). Now start the patch. When it gives the error (or after it reboots), close the app, click _"Ctrl + C"_ to stop the logcat. Then, from the phone, send us the log.txt (you will find it in your Download folder).

**Q - Wow! You guys are awesome!**

**A** - Thank you!

## TO-DO LIST | 
- Automatic Core Mod Removal
- Automatic Core Mod Detection (to avoid double install and eventual bootloops)
- Alarms. Yeah.
- Fixing problems related to some Samsung devices and Pixel devices
- Import/Export system for the blocked Wakelock
- Inserting the FAQ and the suggested wakelock-to-block list into the actual app
- Adding the feature to change the block time without unblocking the wakelock
- Various fixes and improvements
