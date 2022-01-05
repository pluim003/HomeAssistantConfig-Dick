# HomeAssistantConfig-Dick

## Description

Here you'll find my HomeAssistant-configuration.
This is a working and tested configuration in my environment

Note: as Dutch is my main language names/aliases/friendly_names will be Dutch.

## Getting started

### Background

I started using HomeAssistant November 2021. First on my laptop where it would obviously only work when the laptop was powered on, but just to play around.
Early December 2021 I got a Raspberry Pi 4B with 4Gb of memory. Installed Docker, grabbed a HomeAssistant-image and started there continuing what I started before.

But it was time to enhance, make it better and continued. Found stuff somewhere on the internet, modified it, or wrote stuff myself.

Because of all this help I decided to put my stuff up here so that others might benefit from it.

### Dependencies

Some of the included stuff is dependent of custom integrations. You'll need HACS installed and browse for repositories. I'll try to put all information as comments in the YAML-files. But I might overlook sometimes something. :-)

### Installing

DON'T install this set of files over your existing configuration, as it will definitely break your configuration as I guess every configuration is different. Just store all the files in a seperate folder and use stuff from it as you like.

## The files

#### configuration.yaml

The main configuration-file. Editing this file always requires you to restart the whole HomeAssistant-system.

#### automations (folder)

I split up my automations.yaml in separate yaml-files so that it is easier to maintain. 
This has an advantage and also a disadvante.
Advantage is that it is better manageable and you don't have to plunge through a large automations.yaml-file. The disadvantage however is that you can't edit automations within the HomeAssistant itself anymore. Sometimes it might be convenient to see what is really happening, triggering and modifying it through a GUI. On the other hand there is a disadvantage that when modifying within the GUI and saving it your saved automations.yaml won't show your added comments in it and empty lines will also be removed making it even harder to read. So you can also see it as an advantage as this won't happen anymore. Ofcourse it's always wise to have a backup of your whole configuration.

- ##### aanwezigheid.yaml

Check on presence of the family members. These can have different statusses. I used the example from Phil Hawthorne o https://philhawthorne.com/making-home-assistants-presence-detection-not-so-binary/ . Only to find out that after a restart of the system the presence of any family-member would be set to Home, as in the input_select.yaml that was the default value.

- ##### automations.yaml

The automations which haven't been put in a separate file yet.

- ##### lampen.yaml

Automations with respect to light bulbs.

- ##### schakelaar.yaml

Automations with respect to switches.

- ##### verwarming.yaml

Automations with respect to the heating. Here comes in mind that we have a Honeywell Lyric T6-thermostat.

#### binary_sensor.yaml

The binary sensors.

#### camera.yaml

The camera's being used.

#### customize.yaml

Customizations to the system

#### device_track.yaml

Information for tracking devices. For privacy reasons I only use the ping to track if someone is at home or away. If someone is not connected to the local Wifi-network I assume this person is away. Another reason to use this method is that the household isn't keen in installig this HomeAssistant-app, although they could install it without using it.

#### groups.yaml

Grouping of stuff

#### input_select.yaml

The input_selects being used by automations and so.

#### localtuya.yaml

The information for my Tuya-devices. When added to the system the information is stored internally but I moved them from the core.config_entries to this file to easily maintain. Currently I can't get all Tuya-devices functioning as designed. Like RGB-lightbulbs. I can't get the color-stuff in yet.

#### logger.yaml

How to log stuff, currently not in use as I haven't figured out how to get what I really want. Might be added later.

#### notify.yaml

Information about to notify.

#### proximity.yaml

Check if someone is near home. Wanted to implement this so that f.e. heating can go on or off, but I need to check that further. The Honeywell Lyric T6-thermostat has the geofencing option but then everyone in the household needs to have the Honeywell-app installed and they don't want that.

#### resources.yaml

Resources.

#### scenes.yaml

For scenes. Not in use yet.

#### script.yaml

Scripts. Not in use yet.

#### sensor.yaml

Information about different sensors.

#### switches.yaml

Information about different switches.

### Not included

- secrets.yaml

For obvious reasons as this contains all my 'secret' information.


