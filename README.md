# External (usb) cameras not working with Teams in MacOS
Microsoft remove support for external webcams, you can fix it! :)

## This is the problem:
https://techcommunity.microsoft.com/t5/microsoft-teams/7-17-2020-latest-teams-update-breaks-virtual-cameras-microsoft/m-p/1527271

## And here is the solution:

```sh
// not all files need to exist
$ xcode-select --install
$ sudo codesign --remove-signature "/Applications/Microsoft Teams.app"
$ sudo codesign --remove-signature "/Applications/Microsoft Teams.app/Contents/Frameworks/Microsoft Teams Helper.app"
$ sudo codesign --remove-signature "/Applications/Microsoft Teams.app/Contents/Frameworks/Microsoft Teams Helper (GPU).app"
$ sudo codesign --remove-signature "/Applications/Microsoft Teams.app/Contents/Frameworks/Microsoft Teams Helper (Plugin).app"
$ sudo codesign --remove-signature "/Applications/Microsoft Teams.app/Contents/Frameworks/Microsoft Teams Helper (Renderer).app"
```
> ######### WARNING ##########\
> Test your Teams video-call before first use!\
> MacOS request you again for app permissions.

## Use your Android phone as external usb webcam for MacOS

Here: https://iriun.com/
- download app for Mac
- download app for Android 
-- you need enable "Developer options" and allow "USB debugging"
-- how to enable Developer options: https://www.digitaltrends.com/mobile/how-to-get-developer-options-on-android/
- install Teams app for desktop
- run commands mentioned in this README.md (top)

## Camera in action
![Alt text](teams-external-webcam.png?raw=true "Teams detect external webcam")
