
![](examples/2.jpg)
> *status*: currently stable, writing documentation


# drmon
monitor and failsafe automation for your draconic reactor

### what is this
this is a computercraft LUA script that monitors everything about a draconic reactor, with a couple features to help keep it from exploding
NB: This is for Minecraft 1.21.1. You will need to edit references within the code for any version higher to reflect any changes made to Draconic Evolution past its 1.21.1 release.


### tutorial
you can find a very well made youtube tutorial on how to set this up [here](https://youtu.be/m4ePCa6vE70)

### features
* uses a 3x3 advanced computer touchscreen monitor to interact with your reactor
* automated regulation of the input gate for the targeted field strength of 30%
  * adjustable
* immediate shutdown and charge upon your field strength going below 5%
  * adjustable
  * reactor will activate upon a successful charge
* immediate shutdown when your temperature goes above 8000C
  * adjustable
  * reactor will activate upon temperature cooling down to 3000C [CURRENTLY BUGGED, requires manual reactivation]
    * adjustable

* easily tweak your output flux gate via touchscreen buttons
  * +/-100k, 10k, and 1k increments
* NEW: Automatic output flux gate mode 
  * Uses a PID to automatically adjust the output gate


### requirements
* one fully setup draconic reactor with fuel
* 1 advanced computer
* 9 advanced monitors
* 3 wired modems, wireless will not work
* a bunch of network cable
* 2 Flux Gates
* 3 Flux Plugs
* 3 Flux Points
* A giant energy storage
* At least 100M FE to kickstart

### installation
* your advanced computer should be setup with flux gates on both sides. The tutorial will make things clearer.
  * if you want to use different sides you need to modify `startup` after you have installed this and specify the sides
* connect a modem to your advanced computer
* setup your monitors to be a 3x3 and connect a modem to anywhere but the front
* run network cable to the monitor
* install this code via running the install script using these commands :

```
> wget https~//raw.githubusercontent.com/Derd328/All-the-Mods-ATM-10-Draconic-Reactor-Computer-Craft-Code-2025-2026/master/install.lua install
> install
```
* modify `startup` if you wish to configure/alter any variables mentioned in the feature list, you'll find them at the top of the file
```
> edit startup
```
* you should see stats in your term, and on your monitor

### upgrading to the latest version
* right click your computer
* hold ctrl+t until you get a `>`

```
> install
> startup
```

### known issues
* there is some cleaning up to do in general. Nothing that breaks the functions themselves, mind you.
