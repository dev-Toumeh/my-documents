This guide provides detailed instructions on configuring and using keybindings for system actions in the i3 window manager. 
It covers how to configure lock, logout, suspend, hibernate, reboot, and shutdown functionalities.

### add the following to the i3 config file

set $mode_system System (l) lock, (e) logout, (s) suspend, (h) hibernate, (r) reboot, (Shift+s) shutdown
mode "$mode_system" {
    bindsym l exec --no-startup-id i3exit lock, mode "default"
    bindsym e exec --no-startup-id i3exit logout, mode "default"
    bindsym s exec --no-startup-id i3exit suspend, mode "default"
    bindsym h exec --no-startup-id i3exit hibernate, mode "default"
    bindsym r exec --no-startup-id i3exit reboot, mode "default"
    bindsym Shift+s exec --no-startup-id i3exit shutdown, mode "default"

    # back to normal: Enter or Escape
    bindsym Return mode "default"
    bindsym Escape mode "default"
}
bindsym $mod+Pause mode "$mode_system"

### add the following script to /usr/local/bin 
#!/bin/sh
lock() {
    i3lock
}

case "$1" in
    lock)
        lock
        ;;
    logout)
        i3-msg exit
        ;;
    suspend)
        lock && systemctl suspend
        ;;
    hibernate)
        lock && systemctl hibernate
        ;;
    reboot)
        systemctl reboot
        ;;
    shutdown)
        systemctl poweroff
        ;;
    *)
        echo "Usage: $0 {lock|logout|suspend|hibernate|reboot|shutdown}"
        exit 2
esac

exit 0

### explanation

To activate $mode_system, you need to press the key combination defined in your configuration ($mod+Pause). Usually, $mod refers to a key like Mod4 (which is typically the Windows or Super key) or Mod1 (Alt key).

Here's a quick guide:

Activate $mode_system Mode:
Press the $mod key (e.g., Super key or Alt key) and the Pause key together (in my laptop pause = Fn + p).
This activates the $mode_system mode.
Perform Specific System Actions:
While in $mode_system mode, press one of the following keys to trigger the corresponding action:
l: Lock the screen (i3exit lock)
e: Log out (i3exit logout)
s: Suspend the computer (i3exit suspend)
h: Hibernate the computer (i3exit hibernate)
r: Reboot the computer (i3exit reboot)
Shift+s: Shut down the computer (i3exit shutdown)
Exit $mode_system Mode:
Press Return (Enter key) or Escape to exit the $mode_system mode and return to the default mode.



