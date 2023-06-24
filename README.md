# better-video-splitter.nut
Edited version of Valve's `video-splitter.nut` for Portal 2. Changes made to improve usability and customization!

Valve's video splitter is very robust, but it only really works easily in Valve's own maps. I had a lot of trouble using `video-splitter.nut`, so I thought I'd edit chunks of it to make it more user friendly. Enjoy!

How-to (the easy way!):

1) Setup the `logic_script` in your elevator and have a trigger ready (to turn the screens on)
2) Ensure all of your `vgui_movie_display`s have Force Precache enabled, and apart from the `@arrival_sign_1` they should all have Force Slave enabled too
3) Give all your `vgui_movie_display`s the video you want and setup their width/height/rotation
4) Give your `logic_script` the `health` keyvalue and set it to a number corresponding to the video scale type you want (see below)
5) Make your trigger send the `logic_script` a RunScriptCode input with the parameter `StartVideo(screentype, width, height)`, where screentype is picked from the below list, width is the width in # of screens, and height is the height in # of screens.
6) Enjoy!

VIDEO SCALE TYPES LIST
0) Full Elevator
1) Stretch
2) Mirror
3) Ouroboros (good for making it look broken)
4) Upside Down
5) Tiled
6) Tiled "Really Big"
7) Tiled "Big"
8) Tiled "Single"
9) Tiled "Double"
10) Two by Two
11) Tiled off 1
12) Tiled 2x4
13) Tiled Double "With Two Blank"
14) Bluescreen
15) HyperDash Request - 3Screen

SCREENTYPE LIST
0) `ARRIVAL`
Normal arrival elevator. Chooses all signs with the form `@arrival_sign_#`
1) `DEPARTURE`
Normal departure elevator. Chooses all signs with the form `@departure_sign_#`
2) BROKEN ARRIVAL
Busted arrival elevator. Works the same as `ARRIVAL`, but randomly kills signs to appear fragmented.
3) `BROKEN DEPARTURE`
Busted departure elevator. Works the same as `DEPARTURE`, but randomly kills signs to appear fragmented.
