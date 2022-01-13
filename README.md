### Custom.Crosshairs

This is a mod for Titnafall 2's Norhtstar client that allows you to modify any weapons's crosshair

By default, this will set all crosshairs the Alternator's crosshair.

Thanks a lot to Cpone#0001 from the Norhtstar Discord for helpinf me figure it out

I'll add more weapon types over time untill im covering everything

# INSTRUCTIONS

Instructions

//How To Modify Crosshairs:

1: Go to /Mysterious.Crosshairs/keyvalues/scripts/weapons/mp_weapon_[desired weapon].text

2: you'll see something that looks like this:

    WeaponData
    {   
	    RUI_CrosshairData
	    {
		    Crosshair_1 
		    {
			    "ui"						"ui/crosshair_alternator" //This is the part you want to change
		    }
	    }
    }

3: change "ui/crosshair_alternator" to your desired Crosshair



// WHERE TO FIND CROSSHARS?

A list of crosshairs can be found in /Mysterious.crosshairs/INSTRUCTIONS/Crosshair Examples
Crosshairs taken from the modding guide on noskill.gitbook.io

In Theory, and RUI can work, just dont ask me where to find them



// Multiple Crosshairs at the same time?

In Theory, you can overlap crosshairs like this

    WeaponData
    {   
	    RUI_CrosshairData
	    {
		    Crosshair_2 //Set this to the amount of crosshairs you want to use
		    {
			    "ui"						"ui/crosshair_alternator"   //First Crosshair
                "ui"						"ui/crosshair_tri"          //Second Crosshair
		    }
	    }
    }

This should overlap the Alternator and the R201's crosshairs with eachother



// Extra Info

Keep in mind that some weapons have animated or dyynamic crosshairs.
Weapons like the Charge Rifle, Cold Wae, Frag Grenade, etc... have specially animated crosshairs. which can cause weirdness or jank when used on other weapons or when using other crosshairs on them.

Thank you to Cpone#0001 from the Northstar Discord for helping me figure this out

Any Issues? Message me on discord Mysterious#7899
