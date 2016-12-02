# permanotices
Replaces dbus notifications and makes them persistent

Plasma 5 does not keep unread notifications forever anymore.
If you miss that, read on.

This tool uses dbus-monitor to intercept notifications,
then it clones them as soon as possible but changes them
to never expire.

Note that:
======
* Persistent notifications are left unchanged
* notifications that carries actions are left unchanged
* notifications HINTS are silently discarded



Mandatory requirements:
======
  * dbus-monitor
  * system tray 
  * Gambas 3 (usually the very latest version)


Compiling it:
======
```
After you installed gambas 3, just checkout and compile xt7 that way:

# git clone https://github.com/kokoko3k/permanotices
# cd permanotices/
# /path/to/gambas/binaries/gbc3 -e -a -g -t -p -m
# /path/to/gambas/binaries/gba3
# ./*.gambas
