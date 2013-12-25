==============================================================================
Crafting Azeroth - v1.0 - December 24th, 2013
==============================================================================

The Crafting Azeroth project is a full-scale reproduction of the World of 
Warcraft environment inside Minecraft. This is an unofficial fan project and 
is not in any way affiliated with Blizzard Entertainment.

Version 1.0 includes map data for all non-instanced outdoor zones up to and 
including the Cataclysm expansion pack. These areas include the continents of 
Eastern Kingdoms, Kalimdor, Outland, Northrend, and the islands in the Great 
Sea. Additionally, many zones that originally appeared in the beta have been 
re-generated using newly added blocks and features.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR 
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, 
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE 
AUTHORS OR CONTRIBUTORS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, 
WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR 
IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE. 

==============================================================================
CONTENTS
==============================================================================

The two zipped-archive files included in this download are,

- CraftingAzeroth-v1.0-Map.7z
- CA-v1.0-ServerSetup.7z

You are free to use these files as you wish, but I am not responsible for
any damages or other liabilities resulting from their use. You *do not* need 
to ask permission to host this map on your server, post a video, etc. I only 
ask that you give proper attribution and link to the official project URL:

http://www.craftingazeroth.org

If you encounter a technical problem, post about your issue on the forum and 
I will try to provide an answer as soon as possible. If you have questions 
for me personally, you can send me a private message on the forum or contact 
me via email. I hope you enjoy exploring the map, and I look forward to 
posting more updates in the future.

- Rumsey/RamsesA (craftingazerothproject@gmail.com)

==============================================================================
Instructions
==============================================================================

To be experienced properly, the map must be hosted using a Bukkit server that 
is compatible with Minecraft 1.7.2 or greater. As of December 24th, 2013, only 
the beta version of Bukkit is compatible with this version of Minecraft.

You can download the beta version, "craftbukkit-1.7.2-R0.1.jar", or a more
recent version (if one exists), from the Bukkit website:

http://dl.bukkit.org/downloads/craftbukkit/

Once you've downloaded the jar file, place it in a folder along with the
contents of "CraftingAzeroth-v1.0-Map.7z" and "CA-v1.0-ServerSetup.7z". These 
archive files include the map data as well as configuration files and plugins 
for the Bukkit server. The map data requires 22 GB of free hard drive space, 
so be aware of your available drive space before extracting.

Although these files should already be pre-configured, you will still need to 
know how to operate a Bukkit server. If you do not have experience running a 
Bukkit server, please consult the installation guide on the Bukkit website:

http://wiki.bukkit.org/Setting_up_a_server

Once your Bukkit server is running, new players should spawn in Outland near 
the Dark Portal. If you have added your username to the ops.txt file, you 
should be able to use the /tp command to teleport around the map. Listed 
below are some interesting coordinates to explore:

/tp -10539 123 4137     Orgrimmar
/tp 4150 155 57703      Ironforge
/tp -53787 77 1069      Shattrath
/tp -3327 76 -1695      Wyrmrest
/tp -14734 97 203831    Darnassus
/tp 6641 48 -950        Silvermoon

Of course, there are many more areas to explore beyond just those. You might
find these online maps a useful reference:

http://map.craftingazeroth.org
http://overviewer.org/wow/

==============================================================================
Plugin Commands
==============================================================================

The "CA-ServerSetup-v1.0.7z" archive includes two Bukkit plugins specifically
designed for the Crafting Azeroth project:

- CA-Teleport-v1.0: Automatically teleports players betweeen altitude layers, 
artificially increasing the height limit of the map. Also includes special 
routines for teleporting to Stormwind and the Dark Portal.

- CA-Static-v1.0: Prevents certain block updates from occurring, such as
water flow and vine growth. This is important for game performance as well as
for maintaining the appearance of the original map.

Both of these plugins are essential to experiencing the map properly. That 
is why they are included in the download and why running a Bukkit server is
not considered optional.

CA-Teleport has two commands that may be useful to map editors:

/catp [enable/disable] (playername)

The /catp command can be used to enable or disable the teleportation feature 
for some or all players on the server. This is useful if you want to reach 
areas that are contained within the overlap between altitude layers.

/casync [enable/disable] (playername)

The /casync command can be used to enable or disable block synchronization
across altitude layers. Turning this feature off will allow players to edit 
one altitude layer without equivalent changes appearing in the overlapping 
sections of the adjacent altitude layers.

CA-Static has no console commands, but it does have a configuration file
called "prohibited.yml". Editing the list of blocks in this file will
determine which block updates are prevented. The block names in the list 
must match the names of existing Bukkit Material enum types.

==============================================================================
Map Coordinate Space
==============================================================================

Unlike the beta version of the project, all the map data is contained within 
a single world. Here are some details about how the map is partitioned.

The map is divided into x/z grid sections each with an area of 51200 * 51200 
blocks. The data for Azeroth at sea-level is placed inside the region from 
(-25600, -25600) to (25599, 25599), with the origin at (0, 0) positioned near 
Valgarde in Northrend. Azeroth has a total of 7 altitude layers; one below 
sea-level, one at sea-level, and five above. Each additional altitude layer 
adds 51200 to the z-coordinate, so the matching coordinate for Valgarde at 
one altitude level higher is (0, 51200) and the matching coordinate for one 
altitude level lower is (0, -51200). Each altitude layer will appear to shift 
the world up or down by 192 blocks in the y-direction, with 64 blocks of
overlap at the top and bottom of the map.

Outland is positioned west of Azeroth, -51200 blocks in the x-direction. The 
sea-level data for Outland is placed inside the region from (-76800, -25600) 
to (-25601, 25599) and centered at (-51200, 0). There are a total of four 
altitude layers for Outland; one below sea-level, one at sea-level, and two 
above. Altitude layers for Outland are also handled by adding or subtracting 
51200 from the z-coordinate.

The sections east of Azeroth, at x-coordinates >= 25600, are designated for 
instances and battlegrounds. The only instance in v1.0 is the rotated 
version of Stormwind, centered at (51200, 0).

Note, the coordinates for locations in Eastern Kingdoms at sea level are 
unchanged from the beta, while the coordinates for Kalimdor have been offset 
by (-16208, -2416). This offset is divisible by 16, so it aligns with the 
existing chunk layout.

==============================================================================
Project Credits
==============================================================================

Software/Documentation: 
Rumsey (RamsesA)

Minecraft Server Hosting: 
Martin Benjamins (Marlamin), Cursecraft

Download Hosting: 
Wozarib, PhonicUK

Stormwind Build Support:
Joe Paolilli, Zeckdorl, Marlamin

Overviewer Software Support: 
Aaron Griffith (agrif), Alex Chin (achin), Andrew Brown (brownan), 
other contributing members of the Overviewer team

Additional Overviewer Support:
pibm, Gizmokid2005

Special Thanks:
Blizzard Entertainment
Mojang AB
Chupathingy of Akama
WowDev contributors
Ladislav Zezula (Ladik)
Curse Inc.
Minecraft Overviewer
John Carmack
#overviewer on freenode
Stefan Gustavson
Peter Eastman
mundocani (BLP2PNG)