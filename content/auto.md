---
title: "Auto"
date: 2024-06-28T11:01:27-04:00
---
[download](autoexec.cfg)

```
// This supposedly optimizes the accuracy of directional sound. //
// https://steamcommunity.com/sharedfiles/filedetails/?id=487027371 //
exec sounds.cfg

// Automatically records and timestamps a demo //
// Brining up the scoreboard will start recording //
alias +showexec "+showscores; exec sander.cfg" 
alias -showexec "-showscores" 
bind TAB +showexec

// Crosshair Aliases //
alias "purple" "cl_crosshair_red 255; cl_crosshair_green 0; cl_crosshair_blue 255"
alias "red" "cl_crosshair_red 255; cl_crosshair_green 0; cl_crosshair_blue 0"
alias "green" "cl_crosshair_red 0; cl_crosshair_green 255; cl_crosshair_blue 0"
cl_crosshair_dynamic 1 

// Toggles your weapon model on off //
bind f4 "toggle cl_viewmodelfovsurvivor 180 80"

// Connects to Bleedz server through lobby in case steam groups are broken
mm_dedicated_force_servers ip:port
bind f3 "say /acc" // check accuracy on server

fps_max 144
// Easier and faster than kicking someone with an open mic or something //
bind f3 "toggle voice_modenable 1 0"
```
