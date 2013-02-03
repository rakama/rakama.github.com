==============================================================================
Crafting Azeroth - v0.1 beta - October 7th, 2012
==============================================================================

The Crafting Azeroth project is a full-scale reproduction of the World of 
Warcraft environment inside Minecraft. This is an unofficial fan project and
is not in any way affiliated with Blizzard entertainment.

This version includes the maps of Eastern Kingdoms and Kalimdor, excluding
zones that were added in the Burning Crusade expansion pack. The files 
included in this download are,

- Azeroth-v0.1-beta.rar
- Kalimdor-v0.1-beta.rar
- Plugins-v0.1-beta.rar

You are free to use these files as you wish, but I am not responsible for
any damages resulting from their use. You do not need to ask my permission 
to host this map on your server, post a video, etc. I only ask that you give 
the proper attribution and link to my thread on the Minecraft forums:

http://www.minecraftforum.net/topic/997352-crafting-azeroth/

If you have any technical issues, post about your problem in the forum thread
and I will try to provide an answer as soon as possible. If you have questions 
for me personally, you can send me a private message on the forum or contact 
me via email. I hope you enjoy testing the map, and I look forward to posting 
updates in the future.

- RamsesA (ramsesakama@gmail.com)

==============================================================================
Instructions
==============================================================================

This map must be hosted on a Bukkit server to be experienced properly. You 
will need the following items:

- The latest version of CraftBukkit (http://dl.bukkit.org/)
- Multiverse-Core plugin (http://dev.bukkit.org/server-mods/multiverse-core/)

Two additional plugins are included in "Plugins-v0.1-beta.rar":

- CA-Teleport, teleports players across altitude boundaries
- CA-Static, stops blocks from updating (e.g. water, grass growth, etc.)

All three plugins should be extracted to the /plugins folder in your Bukkit
directory. The "Plugins-v0.1-beta.rar" archive also includes configuration 
files for Multiverse, which should be extracted along with the plugins.

Once your server is running, new players should appear in Kalimdor near the 
Southfury river. You can use Multiverse commands to swap between continents, 

/mvtp Kalimdor
/mvtp Azeroth

Specific waypoints will not be included in the beta release, but you should 
be able to create your own using Multiverse. 

==============================================================================
Known Issues
==============================================================================

Since this is a beta version, you may encounter problems exploring the map. 
Below are some major issues that I have already identified.

- Minecraft may experience a sudden drop in frame rate when exploring detailed
  areas of the map (e.g. large forests). This is likely due to memory issues
  and can be avoided by reducing the view distance and setting the graphics 
  quality to "fast", or increasing the amount of available memory.

- Many structures are hollow on the inside (e.g. large trees, buildings). This
  is due to a limitation in the algorithm. I plan to release a tool that will 
  let users manually fill in the interior of these objects.

- Zones that lie on the boundary between altitude layers can be difficult to 
  navigate. I plan to improve CA-Teleport in the future so that the boundary 
  between altitude layers better matches the layout of the environment.

If you have any major problems not listed here, please post them in the forum
thread and I will I see if I can find a solution.