# teams-external-webcam-fix-for-mac-os
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
