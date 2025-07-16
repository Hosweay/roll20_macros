# Trigger Traps

This setup uses [ScriptCards Triggers](https://wiki.roll20.net/Script:ScriptCards#Triggers) to trigger actions when a token enters or moves through a trigger token's area.

## Setup

1. Install ScriptCards - minimum version of 3.0.12
2. Create a character named ScriptCards_Triggers - must be a non-Beacon character sheet currently
3. Create a character named ScriptCards_Storage - must be a non-Beacon character sheet currently
4. Mod API Sandbox must be restarted after creating ScriptCards_Triggers character and ScriptCards_Storage character
5. Create ability named `change:graphic` on ScriptCards_Triggers character
6. Copy change_graphic_trigger.scard contents into `change:graphic` ability on ScriptCards_Triggers character
7. Run trigger_manager.scard to edit configuration to your desired state. Pay particular attention to the FlyMarker variable to use whatever marker you have to mark a flying character

## Configuration

### General Configuration

* LogLevel
* EnableTriggerDetection
* ReturnTokenOnStop
* FlyMarker
* ActivationMarker
* CustomAbilityMule
* triggerTokenNamePrefix
* scStoredVariablePrefix

### Action Configuration

* WhisperToTriggererLocation
* WhisperToGMLocation
* BroadcastToChatLocation
* VisualEffectLocation
* PlayaudioLocation
* TeleportLocation
* AmbushLocation

## Utility Script

In addition to the trigger, there is also another ScriptCard to help manage triggers. The Trigger Manager utility will spawn a new trigger token, activate existing triggers, and edit and save trigger trap configuration variables.
