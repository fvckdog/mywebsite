---
title: "autoexec.cfg"
date: 2024-06-28T11:01:27-04:00
---
[download](/autoexec.cfg)



{{< highlight Shell "linenos=table" >}}
//	================================================================
//	This supposedly optimizes the accuracy of directional sound:
//	https://steamcommunity.com/sharedfiles/filedetails/?id=487027371 
//	================================================================

	exec sounds.cfg

//	===============================================
//	Automatically records and timestamps a demo     
//	Brining up the scoreboard will start recording
//	NOTE: This requires a really stupid dependency 
//	when you could just automate this bash/batch. 
//	===============================================

	alias +showexec "+showscores; exec sander.cfg" 
	alias -showexec "-showscores" 
	bind TAB +showexec

//	==================
//	Crosshair Configs
//	==================

	alias "purple" "cl_crosshair_red 255; cl_crosshair_green 0; cl_crosshair_blue 255"
	alias "red" "cl_crosshair_red 255; cl_crosshair_green 0; cl_crosshair_blue 0"
	alias "green" "cl_crosshair_red 0; cl_crosshair_green 255; cl_crosshair_blue 0"
	cl_crosshair_dynamic 1 

//	=================
//	Custom Viewmodel 
//	=================

//	==================================================================================
//	180 fov completely removes the model that you're carrying from your screen
//	It sort of throws me off with melee and throwables so these will reset fov to 80
//	whenever you equip utility
//	==================================================================================	

	bind 1 "slot1;cl_viewmodelfovsurvivor 180
	bind 3 "slot3;cl_viewmodelfovsurvivor 80
	bind 4 "slot4;cl_viewmodelfovsurvivor 80
	bind 5 "slot5;cl_viewmodelfovsurvivor 80

//	=======================================
//	Toggles  fov + mousewheel to hide item 
//	=======================================

	bind f4 "toggle cl_viewmodelfovsurvivor 180 80"
	bind mwheelup "cl_viewmodelfovsurvivor 180"; bind mwheeldown "cl_viewmodelfovsurvivor 180"

//	=======================================================================
//	Connects to server through lobby in case steam groups are broken
//	=======================================================================

	mm_dedicated_force_servers <ip-address>:27015

//	=======================================================================
// 	Creates an alias for any server you want conveniently connect to
//	=======================================================================

	alias "<server/command-name>" "connect  <ip-address>:27015"
	bind f3 "sm_acc" // check accuracy 
	bind f2 "sm_slaysafe;sm_breakglass"

//	====================================================================
//	Easier and faster than kicking someone with an open mic or something 
//	====================================================================

	bind f11 "toggle voice_modenable 1 0"

//	======
//	Misc.	
//	======

	fps_max 144
	
{{< /highlight >}}
