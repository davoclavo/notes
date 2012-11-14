MacOS X Notes
=============

10.8.2
------

#General

###MAC Spoofing

Get the current MAC Address

    ifconfig en0 | grep ether
    networksetup -listallhardwareports

Disassociate from any network

    sudo ln -s /System/Library/PrivateFrameworks/Apple80211.framework/Versions/Current/Resources/airport /usr/sbin/airport
    airport -z

Spoof!

    sudo ifconfig en0 ether 00:e2:e3:e4:e5:e6
or

    sudo ifconfig en0 Wi-Fi aa:bb:cc:dd:ee:ff

> Mayyyybe you need to turn wireless NIC off and on again using the following:
>
>     sudo ifconfig en0 down
>
>Now re-enable the NIC:
>
>     sudo ifconfig en0 up

[Source](http://osxdaily.com/2008/01/17/how-to-spoof-your-mac-address-in-mac-os-x/)

#Dashboard

###Get rid of dashboard

    defaults write com.apple.dashboard mcx-disabled -boolean YES
    killall Dock

###Get dashboard back

    defaults write com.apple.dashboard mcx-disabled -boolean NO
    killall Dock

#Messages.app

###Change shortcut in Messages app for cmd+backspace

    defaults write com.apple.iChat NSUserKeyEquivalents -dict-add "Close Conversation…" '~$a'

#Notes.app

###If the app herp derps when trying to sync:

    rm -rf /Library/Caches/*
    rm -rf ~/Library/Caches/*
    rm -rf ~/Library/Containers/com.apple.Notes/*
> RESTART

> EMPTY TRASH?

> open Notes.app

[Source](https://discussions.apple.com/docs/DOC-4441)

#TotalTerminal.app

###Show totalterminal while using fullscreen apps

    sudo sublime /Applications/Utilities/Terminal.app/Contents/Info.plist

>write this:

    <key>LSUIElement</key>
    <string>1</string>

[Source](http://apple.stackexchange.com/questions/40575/totalterminal-doesnt-work-with-full-screen-apps)

###On load it opens a new window, to automatically close it

    defaults write com.apple.Terminal TotalTerminalCloseWindowsOnStart -bool YES

[Source](https://github.com/binaryage/totalterminal/issues/40#issuecomment-4258450)