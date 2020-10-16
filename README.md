# RemoveCatalinaApps
How to remove protected apps, such as News, Stocks, and Home from a Catalina macOS installation

### Special thanks to [9define](https://github.com/9define) for suggesting this workaround! :) 

## About
Have you upgraded to Catalina on your mac and object to sponsored apps? Refuse to be pushed Apple's liberal News or to be shilled Apple's Home ecosystem of products? Hate the XNU kernel? Don't want to disable SIP just to nuke a few apps?

## Problem
![alt text](https://raw.githubusercontent.com/banzr/RemoveMojaveApps/master/screens/cant-delete.png)

## Reasons

* Stocks -- Streams CNBC echonomic news, which is a biased news outlet.
* News -- Multiple liberal sources. Biased. Little to no unfiltered conservative representation. Shills Apple products.
* Home -- Forces users to buy products that pay Apple for the priviledge of being compatible with macOS and iOS.

## Steps
1. Install/Upgrade to Mojave

2. Reboot into recovery mode. 
	* Shutdown your mac.
	* Hold `Command + R` and press power. Continue to hold the keyboard keys until the Apple logo and loading bar appears. 

3. Select Disk Utility from the list of options
![Recovery mode splash screen](https://raw.githubusercontent.com/banzr/RemoveMojaveApps/master/screens/recovery-mode-opts.jpg)

4. Select your MacOS Mojave installation disk on the left and click `Mount` on the top right.
![Disk utility select root drive](https://raw.githubusercontent.com/banzr/RemoveMojaveApps/master/screens/unmounted-root-drive.jpg)
![Disk utility mount root drive](https://raw.githubusercontent.com/banzr/RemoveMojaveApps/master/screens/mount-root-drive.jpg)

4a. If the internal disk is encrypted select startup disks and insert password, this will mount it and make it available

5. Close Disk Utility

6. Open Terminal by clicking `Utilities -> Terminal`

7. Catalina systems apps are in: /Volumes/macos/System/Applications you can cd into it

8. Make a copy of your apps if you want to go back of anything goes wrong (ie. future upgrades of MacOs)

`cp -r News.app "/Volumes/macos - Data/Users/pasquale/Desktop/News.app"
cp -r Podcasts.app "/Volumes/macos - Data/Users/pasquale/Desktop/Podcasts.app"
cp -r Books.app "/Volumes/macos - Data/Users/pasquale/Desktop/Books.app"
cp -r Chess.app "/Volumes/macos - Data/Users/pasquale/Desktop/Chess.app"
cp -r Home.app "/Volumes/macos - Data/Users/pasquale/Desktop/Home.app"
cp -r Music.app "/Volumes/macos - Data/Users/pasquale/Desktop/Music.app"
cp -r Photos.app "/Volumes/macos - Data/Users/pasquale/Desktop/Photos.app"
cp -r Reminders.app "/Volumes/macos - Data/Users/pasquale/Desktop/Reminders.app"
cp -r Stickies.app "/Volumes/macos - Data/Users/pasquale/Desktop/Stickies.app"
cp -r Stocks.app "/Volumes/macos - Data/Users/pasquale/Desktop/Stocks.app"`

9. Remove the apps you don't want:

`rm -rf News.app/ Podcasts.app/ Books.app/ Chess.app/ Home.app/ Music.app/ Photos.app/ Reminders.app/ Stickies.app/ Stocks.app/`

10. Reboot and Enjoy your new macOS without stock bloatware!

