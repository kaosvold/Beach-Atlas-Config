# Beach-Atlas-Config
 Atlas JSON Config
![image](https://user-images.githubusercontent.com/24537644/164844940-bc0981a5-82e7-4560-9a96-544b999a4412.png)

This configurator does several things.  When you select your ServerGrid.json file, it will pull the number of x grids and y grids, and begin to populate suggested ports that would need to be forwarded  You can modify the start port and it will calculate the ending port.  The ip address is retrieved from amazon aws.

Game, Query and RCON ports will do port number +1.  This may be removed in future releases, but keeping in place for the moment.  Seamless increments by 1 for each grid.  These ports and the external ip are saved to the json.  This program uses amazonaws to retrieve your external ip address.  

Using the check box for Fill in Discovery Zones will only add discovery names from the discozones text file located in the resources folder.  It assigns the names from the top of the file downward, so if you decide you want some of yours assigned, put them at the top of the file.  Names will be repeated if you have more discovery zones than the number of lines in the file.

The Give Server Names From Templates option will, if server templates used when creating the servergrid, make the server name be named as server template name_increment, e.g. Polar_1, Low Desert_2.  This only writes to names that are not set.  This option is useful if you want to give your players a heads up for what type of template the grid they are going is.

The Populate Power Stones and Essences will set the quest entries to the correct islands.  The quest location points just to the island itself, not to the specific location on the island.  This option is disabled if when you specify your json it does not contai each of the PVE islands and at least 9 trenches.  This will also set the quest location for the kraken if one of your grids has the extraSublevels set for EndBossLevel.

The add transient nodes check box will add cursed and sulfurous ground to the islands specified in the transient.txt file inside the resources folder.  These islands were pulled from the official json, but can add additional islands to the file.  This will alternate between the two transient types.

Selecting the overwrite option will overwrite all the changes to the json.  This is not recommended in early versions of the program.

This was written in java but wrapped with the jre using launch4j, so no java should be necessary to run this application.

Caveats:
This program will check if you have one of each of the distinct PVE islands and 9 trenches.  Currently didn't have a plan to allow for duplicating powerstone islands, but may if there is enough request for it.

Beach#2483 on discord for support.
