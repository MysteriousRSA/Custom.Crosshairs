# Mysterious.Crosshairs

This is a mod for [Titanfall 2's Northstar Client](https://northstar.tf) that allows you to modify any weapons's crosshair.

By default, this will set all crosshairs to the Alternator's crosshair.

I'll add more weapon types over time until I've got everything covered.

# INSTRUCTIONS

### How To Modify Crosshairs:

1: Go to /Mysterious.Crosshairs/keyvalues/scripts/weapons/mp_weapon_[desired weapon].txt

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



### Overlapping Crosshairs

It is possible to combine crosshairs by modifying the mp_weapon_[Desired Weapons].txt 

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


//The sections can be repeated to add more Crosshairs

//This example will combine the Alternator and R201 crosshairs into one

//Limit seems to be 4 crosshairs



### No Crosshair?

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

### Crosshair Index:

These are the available crosshairs in game, along with their in-game reference:

![Crosshair examples][crosshairs]

Crosshairs taken from the modding guide on https://noskill.gitbook.io/titanfall2/

In Theory, any RUI can work, just don't ask me where to find them



# Extra Info

All Weapon Names and their corrosponding file can be found in here: https://pastebin.com/pessGZh9

All weapons that make use of special crosshairs have their defaults in place, But there is nothing preventing you from modifying them, all the files are there.

Keep in mind that some weapons have animated or dynamic crosshairs.
Weapons like the Charge Rifle, Cold Wae, Frag Grenade, etc... have specially animated crosshairs. which can cause weirdness or jank when used on other weapons or when using other crosshairs on them.

Thank you to `Cpone#0001` from the [Northstar Discord](https://northstar.tf/discord) for helping me figure this out

Any Issues? Create an issue, or message me on Discord `Mysterious#7899`


[//]: # ([crosshairs]: https://github.com/MysteriousRSA/Custom.Crosshairs/raw/main/assets/crosshairs.png "Crosshair examples")
[crosshairs]: https://github.com/Riccorbypro/Custom.Crosshairs/raw/main/assets/crosshairs.png "Crosshair examples"
