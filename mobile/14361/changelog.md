### Start and Action Center
- When you dismiss multiple notifications at once, the background will no longer fade to black between them

### Cortana and search
- Cortana should now listen more reliably after tapping the mic button

### User Interface
- A number of icons, like the network icon have been updated

### Microsoft Edge
- Edge has been updated from version 38.14352 to version 38.14361 with the following updates
 - Download notificaions in Edge now include filenames, download status and site domain on separate lines
- The following flags have been added
 - TCP Fast Open is disabled by default but can be enabled
 - A flag has been added to enable Standard Fullscreen API

### Settings
- New panels, settings and options
 - Active hours can now be set to a range of up to 12 hours instead of 10
 - As of build 14361, your DPI settings will be backed up in the cloud and restored after your device is refreshed

### System
- The text prediction engine has bene improved to show candidates based on the current keyboard language, instead of the language that was used when the word was written
- 5-inch devices like the Lumia 640 and 830 can now also use the one-handed keyboard

### Apps
- The Feedback Hub has a cleaner UI
- You can now cycle through pages in the phone app infinitely

### Fixed issues
- Fixes an issue that caused phones to freeze after touching the screen immediately after Narrator was enabled
- Fixes an issue in Edge that caused the swipe-gesture to go back being partially visible for no reason
- Fixes an issue whre "Find on Page" wouldn't scoll the page to make the word visible in Edge
- Fixes an issue with videos played on Facebook flickering after rotating the phone while the video was already playing in full screen mode
- Fixes an issue where text on the Windows Insider Program-page in Settings wasn't being wrapped
- Fixes an issue that made dismissing notifications with a hero image more difficult
- Fixes an issue where Netflix would pause when peeking at a notification
- Fixes an issue where the keyboard might cover up to quick reply field
- Fixes an issue where some notifications would only appear as "New notification" after a reboot
- Fixes an issue that made the Action Center to would close quicly if a notification was expanded while starting to move the border up
- Fixes an issue where a new notificaiton would keep Action Center from being opened if you where swiping it down while it arrived
- Fixes an issue that made devices make the "now charging"-sound more than once after being plugged in
- Fixes an issue that made the "Everytime" setting for how often you should be requested to fill in your pin being blank after opening Settings from the lock screen
- Fixes an issue that made devices like the Lumia 535 and 540 not display the flash toggle in the Camera app

### Known issues
- You can't deploy an app via Visual Studio 2015 Update 2
 - You can use the Windows 10 Application Deployment command-line tool
- In some cases, the new Cortana features from build 14356 may not work
 - Restart your device to solve this issue
- The order of your Quick Actions is not maintained after updating to this build
- There is an issue with cellular data for Dual-SIM devices causing the second SIM to not function properly