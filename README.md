# Mysterious.Crosshairs

![Mod512Round](https://user-images.githubusercontent.com/45333346/152405018-caa1be1b-f12e-42df-a62b-a7cff27a3142.png)


This is a mod for [Titanfall 2's Northstar Client](https://northstar.tf) that allows you to modify any weapons's crosshair.

I'll add more weapon types over time until I've got everything covered.

# INSTRUCTIONS

## INSTALLATION:

This mod is compatible with:

[VTOL](https://github.com/BigSpice/VTOL), 
[Viper](https://github.com/0neGal/viper) And [Thunderstore](https://northstar.thunderstore.io/)

## Manual Installation:

1: Download the latest release [From the Release Page](https://github.com/MysteriousRSA/Custom.Crosshairs/releases)

2: Extract the zip file and move the folder "Mysterious.Crosshairs" to 
    `~\Titanfall2\R2Northstar\mods\`

Common Game Install Locations:

Steam: `C:\Program Files (x86)\Steam\steamapps\common\Titanfall2`

Origin: `C:\Program Files (x86)\Origin Games\Titanfall2` 

![location](https://user-images.githubusercontent.com/45333346/149657078-86db15a0-0ecc-4d53-9265-23d80a072cea.jpg)


## How To Modify Crosshairs:

1: Go to `~/Titanfall2/R2Northstar/mods/Mysterious.Crosshairs/keyvalues/scripts/weapons/mp_weapon_[desired weapon].txt`

2: you'll see something that looks like this:

    WeaponData
    {   
        RUI_CrosshairData
        {
            Crosshair_1 
            {
                "ui"                        "ui/crosshair_alternator" //This is the part you want to change
            }
        }
    }

3: change "ui/crosshair_alternator" to your desired crosshair
    NOTE: Sometimes it helps to remove //comments


## Overlapping Crosshairs

It is possible to combine crosshairs by modifying the mp_weapon_[Desired Weapons].txt 

**Below is an example of combining the Alternator and R201 crosshairs into one**

    WeaponData
    {
        active_crosshair_count              "2" //Amount of crosshairs you want to use

        RUI_CrosshairData
        {
            Crosshair_1                                                                     //Crosshair 1 Start
            {
                "ui"                        "ui/crosshair_alternator"   //First Crosshair
            }                                                                               //Crosshair 1 End
            Crosshair_2                                                                     //Crosshair 2 Start
            {
                "ui"                        "ui/crosshair_tri"          //Second Crosshair
            }                                                                               //Crosshair 2 End
        }
    }


**To add more crosshairs add another Crosshair_*X* following the formating in the script above.**

**The limit for this seems to be 4 Crosshairs onscreen at once**

### How the script above appears:

![triandaltCH](https://user-images.githubusercontent.com/45333346/149623038-64937ab7-bb0f-450c-ba92-97c625e715bf.png)


## Adjust Crosshair Spread?

Simple add  
``
        "base_spread"               "3.0"   //This is a spread Multiplier
``
Below the "ui" line, Like this

     {   
        RUI_CrosshairData
        {
            Crosshair_1 
            {
                "ui"                        "ui/crosshair_alternator" //THis is the Croshair
                "base_spread"               "3.0"   //This is a spread Multiplier, Line doesnt exist by default
            }
        }
    }

NOTE: This only effects the visual spread of the crosshair, not actual bullet spread. Positive Values increase spread while negative decreases it.

## No Crosshair?

    WeaponData
    {   
        RUI_CrosshairData
        {
            Crosshair_1 
            {
                "ui"                        "ui/crosshair_sniper_amped" //This means NO crosshair
            }
        }
    }

## Crosshair Index:

These are the available crosshairs in game, along with their in-game reference:

![Crosshair examples][crosshairs]

Crosshairs taken from the modding guide on https://noskill.gitbook.io/titanfall2/

In Theory, any RUI can work, just don't ask me where to find them



## Examples

![CH1](https://user-images.githubusercontent.com/45333346/149503054-45eb1fa5-5e89-4bf1-bf58-b58c1bfab94b.png)
![CH2](https://user-images.githubusercontent.com/45333346/149503085-154c05b8-4a76-4d03-80aa-fe67fba1bcb1.png)

### Something Cursed...

![cursed](https://user-images.githubusercontent.com/45333346/149503158-453c8879-df8d-45ca-845e-b5ef691c5566.png)

# Extra Info

It is reccomended to test this out in a private match first.
Save any changes you made to the desired weapon's file and type `reload` in your console

All weapons that make use of special crosshairs have their defaults in place, But there is nothing preventing you from modifying them, all the files are there.

Keep in mind that some weapons have animated or dynamic crosshairs.
Weapons like the Charge Rifle, Cold Wae, Frag Grenade, etc... have specially animated crosshairs. which can cause weirdness or jank when used on other weapons or when using other crosshairs on them.

Thank you to `Cpone#0001` from the [Northstar Discord](https://northstar.tf/discord) for helping me figure this out

Any Issues? Create an issue, or message me on Discord `Mysterious#7899`


[//]: # ([crosshairs]: https://github.com/MysteriousRSA/Custom.Crosshairs/raw/main/assets/crosshairs.png "Crosshair examples")
[crosshairs]: https://github.com/Riccorbypro/Custom.Crosshairs/raw/main/assets/crosshairs.png "Crosshair examples"

More info can be found [HERE](https://youtu.be/dQw4w9WgXcQ)

Trans Rights.
