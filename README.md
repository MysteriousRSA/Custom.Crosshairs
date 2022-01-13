# Custom.Crosshairs

This is a mod for Titnafall 2's Norhtstar client that allows you to modify any weapons's crosshair

By default, this will set all crosshairs the Alternator's crosshair.

I'll add more weapon types over time untill im covering everything

# INSTRUCTIONS

### How To Modify Crosshairs:

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

//This example will combine the Alternator and R201 crossahirs into one



### No Crosshair?

    WeaponData
    {   
	    RUI_CrosshairData
	    {
		    Crosshair_1 
		    {
			    "ui"						"ui/crosshair_sniper_amped" //This means NO crosshair
		    }
	    }
    }

### WHERE TO FIND CROSSHARS?

A list of crosshairs can be found in /Mysterious.crosshairs/INSTRUCTIONS/Crosshair Examples
Crosshairs taken from the modding guide on https://noskill.gitbook.io/titanfall2/

In Theory, and RUI can work, just dont ask me where to find them



# Extra Info

Keep in mind that some weapons have animated or dyynamic crosshairs.
Weapons like the Charge Rifle, Cold Wae, Frag Grenade, etc... have specially animated crosshairs. which can cause weirdness or jank when used on other weapons or when using other crosshairs on them.

Thank you to Cpone#0001 from the Northstar Discord for helping me figure this out

Any Issues? Message me on discord Mysterious#7899
