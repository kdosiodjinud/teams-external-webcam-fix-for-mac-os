# External (usb) cameras not working with Teams in MacOS
Microsoft remove support for external webcams, you can fix it! :)

## This is the problem:
https://techcommunity.microsoft.com/t5/microsoft-teams/7-17-2020-latest-teams-update-breaks-virtual-cameras-microsoft/m-p/1527271

## And here is the solutions:

```sh
$ xcode-select --install (only if you haven't already)
$ sudo codesign --remove-signature "/Applications/Microsoft Teams.app"
$ sudo codesign --remove-signature "/Applications/Microsoft Teams.app/Contents/Frameworks/Microsoft Teams Helper.app"
$ sudo codesign --remove-signature "/Applications/Microsoft Teams.app/Contents/Frameworks/Microsoft Teams Helper (GPU).app"
$ sudo codesign --remove-signature "/Applications/Microsoft Teams.app/Contents/Frameworks/Microsoft Teams Helper (Plugin).app"
$ sudo codesign --remove-signature "/Applications/Microsoft Teams.app/Contents/Frameworks/Microsoft Teams Helper (Renderer).app"
```

## Use your Android phone as external usb webcam for MacOS

Here: https://iriun.com/
- download app for Mac
- download app for Android
- install Teams app for desktop
- run commands mentioned in this README.md (top)
