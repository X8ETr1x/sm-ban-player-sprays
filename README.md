# SourceMod: Ban Player Sprays

A fork of [TnTSCS's plugin](https://forums.alliedmods.net/showthread.php?t=195096).

This plugin will give admins the ability to permanently ban a player's ability to use the in-game spray function. Once banned, a player will not be able to spray anymore until an admin unbans them.

Admin can also view the ban list of currently connected players. Players can also view a menu to check the status of their spray ban status.

The plugin is compiled to have admins with the ban flag able to use the commands. You can override the command "AllowSprayTrace" to be whatever you want.

There is now a CVar so you can determine the ability of using sprays before cookies are cached (defaulted to NOT allow sprays).

## Commands

```
[SM] Listing commands for: Banned Sprays
  [Name]            [Type]   [Help]
  sm_banspray		     admin        Permanently remove a players ability to use spray

  sm_banspray_list	 admin        List of player's currently connected who are banned from using sprays

  sm_banspray_steam	 admin        Manually add a SteamID to the list of players who are banned from using sprays

  sm_deletespray	   admin        Remove a player's spray by either looking at it or providing a player's name

  sm_unbanspray		   admin        Permanently remove a players ability to use spray

  sm_settings        player       This is what players will use to check the status of their ban.
```

## CVars

```
"sm_bannedsprays_update" = "0"
 - Use Updater to update this plugin when updates are available?
0 = No
1 = Yes

"sm_bannedsprays_display" = "4" min. 1.000000 max. 7.000000
 - Display Options (add them up and put total in CVar)
1 = CenterText
2 = HintText
4 = HudHintText

"sm_bannedsprays_tracedist" = "25.0" min. 1.000000 max. 250.000000
 - How far away the spray is from the aim to be traced

"sm_bannedsprays_tracerate" = "3.0" min. 1.000000
 - Rate at which to check all player sprays (in seconds)

"sm_bannedsprays_trace" = "1"
 - Trace all player sprays to display info when aimed at?
0 = No
1 = Yes

"sm_bannedsprays_debug" = "0"
 - Enable some debug logging?
0 = No
1 = Yes

"sm_bannedsprays_tmploc" = "0.00 0.00 0.00"
 - Location for sprays to be moved to.
Must have 2+ decimal places to be valid

"sm_bannedsprays_auth" = "0"
 - If player's SteamID hasn't been authenticated yet, restrict sprays?
0 = No, allow
1 = Yes Do Not Allow

"sm_bannedsprays_remove" = "1"
 - Remove the player's spray after they are banned from using sprays?
0 = Leave Spray
1 = Remove Spray

"sm_bannedsprays_protection" = "0"
 - Distance, in hammer units, to not allow another user to spray next to a user's current spray.
0 = Disabled
>0 = Distance to protect sprays
```

## Installation

### Dependencies

- [More Colors](https://forums.alliedmods.net/showthread.php?t=185016)

For now, just drop the .smx in your sourcemod/plugins folder. I will be adding a translation file later on so this can get approved. I wasn't planning on releasing this plugin, but I've seen a few requests for it lately.I've updated this plugin as of 0.0.3.4 to have a translation file, make sure you place that in your translations folder. 
