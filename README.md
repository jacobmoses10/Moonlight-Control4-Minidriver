Moonlight - PC Game Streaming Universal Minidriver
==================================================

Version 29

This is the Universal Minidriver for Moonlight based on Control4 Universal Minidriver Version 29. Use the Moonlight client on your TV to stream PC games. Ensure that you have a host such as Sunshine or Apollo installed on your PC, and both devices are paired correctly.

It can be connected to the following player devices:

*   Sony TV
*   NVIDIA SHIELD
*   Samsung 2021 (and later) TV

Setup
-----

*   Add the driver to the project.
    
*   Connect the RF\_MINI\_APP connection to the player(s) you would like to use to playback this service.
    
*   Make sure that the room(s) that the driver is available in show a valid audio route for the minidriver (this is required for passthrough mode to work).
    

**Note**: If there is no valid audio path, after selecting the minidriver, you will not be able to control the media player/TV. Confirm you have a valid audio path by selecting the room in System Design and verifying audio path is yes for each minidriver.

*   Refresh Navigators to show the driver in the room(s) it is now available in.

It is possible for there to be multiple ways for a minidriver to be selected in a room. For example, a theater could have a Roku media player, a compatible receiver and a smart TV. Only make connections from this minidriver to the player(s) you would like to trigger selection of this service on.

Using Universal Minidrivers
---------------------------

The player device that is used with this driver will determine the behavior when selecting this driver. It is often possible for the player driver to take over as the selected device in the room. This is likely to be present on media player devices and less likely on TV and receiver devices, due to the Navigator controls for those devices.

If a player device supports taking over the selected device in the room, then there will be a property on that player driver for Passthrough Mode.

If Passthrough Mode is set to On (or is not present), this minidriver will remain as the selected device for the room, but will passthrough all control commands through to the player driver to process.

If Passthrough Mode is set to Off, the player driver will switch the player to this service, but will then take over as the selected device in the room. The advantage of doing this is that it makes programming on the selected device simpler when there are many service minidrivers in a project.

It is not recommended to have minidrivers visible under Listen, as the UI control of the selected device requires a TV to be able to operate reliably. For using in audio-only secondary zones, it is recommended to start the content in the main zone using the minidriver and then use the zones page to group rooms together once the required content is playing.