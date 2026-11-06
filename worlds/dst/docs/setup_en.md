# Don't Starve Together Randomizer Setup Guide

## Required Software

- [Archipelago](https://github.com/ArchipelagoMW/Archipelago/releases/latest)
- [Don't Starve Together](https://store.steampowered.com/app/322330/Dont_Starve_Together/)
- The most recent [dontstarvetogether.apworld](https://github.com/DragonWolfLeo/Archipelago-DST/releases)
- [Archipelago Randomizer Steam Workshop mod for Don't Starve Together](https://steamcommunity.com/sharedfiles/filedetails/?id=3218471273)

## Installation
- Install Archipelago.
- Add dontstarvetogether.apworld to custom_worlds folder of your Archipelago install, or double click the .apworld to do so automatically.
- Follow Archipelago's basic tutorial on how to generate a game. [Basic Multiworld Setup Guide](/tutorial/Archipelago/setup/en)
    * Since this is a custom implementation, you can't generate your game on the website. Generate locally on your machine, and *then*
      you can upload the resulting zip to the website to host.
    * Only a single YAML is needed for a Don't Starve Together server regardless of how many players will play on it.
    * Other players joining your world do not require Archipelago themselves.

## Setting up your world
- Open the Archipelago launcher and run the Don't Starve Together client. Connect to the Archipelago server.
    * Check the client for your world configuration if you cannot refer to your YAML (or if your settings are randomized).
    * It's also safe to launch the Don't Starve Together world before connecting the client if you don't need the info. You can do this
      to make sure your group is logged in and ready before connecting to Archipelago, for example.
- Start Don't Starve Together and choose Host Game.
- Click on "Create New World".
    * A new world is recommended, though using an existing world is also perfectly fine.
- You may be prompted to choose a server playstyle for your world. If you're not sure which to pick, Relaxed is recommended.
    * Endless, Survival, and Wilderness are also fine if you want more of a challenge.
    * World resets and character resets are fine, though will reset your progress for the Survival goal if that's your victory condition.
    * Lights Out is only appropriate if you have only night enabled in your YAML.
- On the Settings tab, make sure your Save Type is "Local Save".
    * If your world is already created, you can change this on the previous screen in the Manage World window.
- You may be prompted to choose whether or not to add Caves. Refer to the client if you don't remember.
    * It's also fine to always add Caves, even if your logic doesn't include it.
- Click on the Mods tab. Enable Archipelago Randomizer, from the Server Mods category.
    * If you don't see it, make sure you subscribe to it on the Steam Workshop. Don't worry, you don't have to restart Don't Starve Together.
    * You may also click on the Configure Mod icon to customize settings such as damage multipliers, and crafting mode and death link overrides.
    * You may also install other mods if you like.
- If you chose a starting season other than Autumn in your YAML, make sure to change it in your World Generation settings.
    * Click on the Forest tab.
    * Click on the World Generation sub-tab. Starting season should be the first option.
- If you toggled any of the seasons or day phases in your YAML, make sure to change it in your World Settings.
    * Click on the Forest tab and World Settings sub-tab.
    * Turn off any seasons or day phases that should be disabled.
    * If Season Flow in your YAML is "Unlockable", you may optionally choose the longest setting for your seasons.
- Load your world and select your character. If everything is fine, the client should automatically connect to DST and you can start playing!

## Recommended setup for new players (Please read!)
Here's some tips for new players to improve your experience with this mod:
- Don't Starve Together is a survival game designed for multiplayer, meaning it is a lot harder than other games. 
  While you definitely can play solo, you may want to adjust your settings to be on par with a single-player adventure game for Archipelago.
- Again, the Relaxed or Endless settings preset is recommended!
- Death Link is brutal for Don't Starve Together. If you insist on enabling it, consider:
    * Lowering "Percentage Health Loss on Death" in the mod configuration.
    * Disabling "Max Health Penalty" in the World Settings (in the Survivors section).
- If you're already playing your world and find things too difficult, you can adjust world settings and the mod configuration, or add mods,
  with no need to regenerate your world.

## Troubleshooting
If Don't Starve Together fails to connect after loading your world, follow these steps:
- If you're playing the beta branch, see the section "Setting a custom save data directory" below.
- Verify the mod is enabled. You will see an Archipelago icon on your screen when you load into your world.
- Verify your client says `Running Don't Starve Together Client Version 1.3.3` or newer.
- Verify that your world's Save Type is "Local Save".
- If you're on Steam Deck, play the Linux build of Don't Starve Together.
- Try disabling all other mods. Once you've successfully connected, then you can re-enable mods if it isn't the issue.

### Verify the client is looking for the correct save data directory
- On Don't Starve Together's title screen, press the Data button.
- Verify that your save data is located in these paths:
    * `Documents/Klei/DoNotStarveTogether` or `C:/DontStarveTogether/DoNotStarveTogether` on Windows
    * `~/Documents/Klei/DoNotStarveTogether` on Mac
    * `~/.klei/DoNotStarveTogether` or `~/.var/app/com.valvesoftware.Steam` on Linux and Steam Deck
- If your save data is not located in any of these folders, proceed to the instructions below.

## Setting a custom save data directory
- Locate `host.yaml` in your Archipelago installation. Open the file in a text editor.
- Find the section `dontstarvetogether_settings`. If it's not there, then add it.
```
dontstarvetogether_settings:
  save_data_directory: "PATH HERE"
```
- Put the correct save data path in the `save_data_directory` field. Make sure to use `/` instead of `\`. Save the file, and re-open Archipelago.    

## Playing the game
- You can see your checks in the built-in tracker. Press the Archipelago icon and press Open Tracker.
  - Depending on your YAML's settings, your checks can include interacting with or killing creatures, researching at a Science Machine,
    and cooking dishes with a Crock Pot.
- If you enabled Warly's dishes in your YAML's cooking locations option, at least one player should choose Warly.
    * If you have a mod that allows other characters to use the Portable Crock Pot, this also works. Logic expects you to have the Portable
      Crock Pot right away.
- Most of your received items are recipe unlocks. Check your crafting menu for your items.
- Once you've connected your world to Archipelago for the first time, it's possible to continue even if not connected. Progress syncs when
  you connect to Archipelago again. However, take caution to not regenerate your world before reconnecting, otherwise you will lose unsaved progress!
- It is fine to play the same Archipelago slot on multiple worlds, even by multiple people at the same time.
    * You cannot play multiple slots on a single world. The DST's Archipelago client only connects to the DST server on the same machine.
- You cannot connect a different slot/multiworld to your existing Archipelago DST world. Your client will tell you if you have a mismatch.
