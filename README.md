# Linux (xkb) support

I gracefully ripped MadRabbit's working layout and vandalized it with the characters I wanted.
I commented a random line at the end of symbols/halmak because it broke my AltGr key, even tho it looks like that line was SUPPOSED to be there in order to make AltGr work...
...yikes 

I made a script to automatically install the layout.
(sometimes, the layout gets randomly removed and you need to run the script again; X11 updates are probably to blame)

Layers:
- layer1 and layer2 - the querty modifiers layer (ctrl,alt,super)  
- layer3 and layer4 - the actual Halmak keyboard  
- layer5 and layer6 - mac style special symbols for the ralt switch  
^it took me 1 hour to realize that ralt="right alt"=AltGr :,)

~~It kind of works system wide, but not everywhere, some electron apps
are fucked. I have no other solution for VS Code other than manually
remap key bindings because it reads keycodes directly off the chrome
DOM events and messes it up.~~

I'll pretend it works perfectly until it doesn't. 

~~Also, apparently xkb gets broken now and then. I've tested this on Ubnutu 20.04, 
and have no guarantee that it will keep working. Fucking programmers, man...~~

./install_pralmak for the win  
(I've pushed the script to the original halmak repo, still missing any reference in the "Readme" tho)

## Installation

~~Copy the `symbols` and `types` folders into `/usr/share/X11/xkb`.
You'll have to overwrite the `types/complete` to make this work.~~
~~After that add `halmak` into the `rules/evdev.xml` wherever you
want this layout.~~

I almost had to learn how xdg works in order to make pralmak.
Just run the script :) I promise I didn't put any covid in there!

After running the script, press Alt+F2 in Gnome and type 'r' to restart the shell, or Restart.
Or log out then log back in.
Or type 'setxkbmap pralmak' in the command line. 

## Alternate Install ( without qwerty layer )
Look at the original halmak repo for other info. 
