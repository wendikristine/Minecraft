# Server Instructions

### Client-Side Mods
Remove these from the server mod list.
- Ambient Sounds
- ~Better Foliage~
- Controlling
- Enchantment Descriptions
- Hwyla
- JEI
- ~Kottle (Better Foliage dependency)~
- Light Level Overlay Reloaded
- Mod Name Tool Tip
- Mouse Tweaks
- Neat
- Swing Through Grass
- Xaero's World Map
- Xaero's Mini Map


### Server-Side Mods
- AI Improvements
- Apple Skin
- Better Signs
- Better Than Mending
- Biomes O Plenty
- Building Gadgets
- Carry On
- Clumps
- Double Doors
- Double Slabs
- Easy Elytra Takeoff
- Fast Leaf Decay
- Harvest
- Inventory Sorter
- Iron Chest
- Light Grass
- McCaw's Bridges
- Nature's Compass
- Ore Excavation
- Refined Storage
- Refined Storage Addons
- Shulker Tooltip
- Simply Backpacks
- Tool Belt
- Uppers


## Creating the Server
0. Before you start, launch your game first locally to make sure there are no errors and to generate the necessary files.
1. Export Profile. Remove client-side mods first by unchecking the boxes.
    - Save in logical location - you need to know where.
    - Go to your modpack's profile page in the Twitch Launcher.
    - Click the settings button (gear) in the upper right corner.
    - Choose open folder.
    - Copy all of the files and folders except for .curseclient, minecraftinstance.json, and mods/mod_list.json into a separate folder. Make sure the folder is empty and that it's somewhere that you will be able to find again later. (I've never seen this files present.)
3. Go to [Minecraft Forge](http://files.minecraftforge.net/).
4. Click on the Menu button and select the Minecraft version you're using.
5. Scroll until you see `Show All Versions` and click the button.
6. Find the Forge version you need (matching the Twitch Profile). Click the `Installer` to download.

**WARNING** wait for ad and click `Skip` on the top right. Dp not click on anything in the add!!

7. Click the download. Save it to a `temp` folder on the desktop (or other known location).
8. In the `temp` folder (that only contains your forge file), double click the file to install.
9. Once installation completes, open the `temp` folder and move the files to the folder that contains your exported Twitch Profile.
Note: Before launching, consider copying existing server files (config,server properties, whitelist, options, etc.) into the new server.
10. Ready to launch! Double click the `minecraft_server.1.XX.X` file to start the server. If on Windows, you'll need to create a `serverstart.bat` file with the following contents:
```
@ECHO OFF
java -Xms4G -Xmx4G -XX:+UseG1GC -XX:+UnlockExperimentalVMOptions -XX:MaxGCPauseMillis=100 -XX:+DisableExplicitGC -XX:TargetSurvivorRatio=90 -XX:G1NewSizePercent=50 -XX:G1MaxNewSizePercent=80 -XX:G1MixedGCLiveThresholdPercent=35 -XX:+AlwaysPreTouch -XX:+ParallelRefProcEnabled -jar server.jar nogui
pause
```
