# Linux (xkb) support

I gracefully ripped MadRabbit's working layout and vandalized it with the characters I wanted.
I commented a random line at the end of symbols/halmak because it broke my AltGr key, even tho it looks like that line was SUPPOSED to be there in order to make AltGr work...
...yikes :D 

I was almost too lazy to make a script to automatically install the layout.
(X updates probably reset everything in the xdg folder)

layer1 and layer2 - the querty modifiers layer (ctrl,alt,super)
layer3 and layer4 - the actual Halmak keyboard
layer5 and layer6 - mac style special symbols for the ralt switch
^it took me 1 hour to realize that ralt=right alt=AltGr :,,,,)

~~It kind of works system wide, but not everywhere, some electron apps
are fucked. I have no other solution for VS Code other than manually
remap key bindings because it reads keycodes directly off the chrome
DOM events and messes it up.~~

I'll pretend it works perfectly until it doesn't. 

~~Also, apparently xkb gets broken now and then. I've tested this on Ubnutu 20.04, 
and have no guarantee that it will keep working. Fucking programmers, man...~~

./install_pralmak goes brrr
(I'm probably gonna commit a change to the original halmak in order to add this script)

## Installation

~~Copy the `symbols` and `types` folders into `/usr/share/X11/xkb`.
You'll have to overwrite the `types/complete` to make this work.

After that add `halmak` into the `rules/evdev.xml` wherever you
want this layout.~~
No! Noobs like me just want to start typing. I almost had to learn how xdg works in order to make pralmak.
Just run the script :) I promise I didn't put any covid in there!

Restart. Or press Alt+F2 in Gnome and type 'r' to restart the shell. 
Or log out then log back in.
Or type 'setxkbmap pralmak' in the command line. 

## Alternate Install ( without qwerty layer )
Naaaah noone needs this. I'll just delete this section.
