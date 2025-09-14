**About Convoy**

<img width="1920" height="1080" alt="cr1" src="https://github.com/user-attachments/assets/b9c1e0e0-236e-4b6b-ad12-9a8b828e2d05" />

Set your server apart with a roaming mobile event that has nearly endless configuration options! Configure the loot truck as well as the Convoy of protection vehicles ranging from sedans, module cars, Bradley tanks, motorbikes, vendor trucks, to a patrol helicopter! The plugin runs on custom and procedural generated maps, can use custom routes or let the plugin find a random route based on your configuration.

You can make yours an aggressive or a peaceful Convoy, who shoots first? You can set all kinds of parameters regarding the many pieces of the event, how to beat it, whether destroying the loot truck destroys the loot or not for example. There are many compatible plugins like TruePVE, GUIAnnouncements, Notify, DiscordMessages, and RustCord to name a few. The plugin has a built in UI that will give you important information about the event as you are inside it's zone. Check the map to see the location of the event as a marker and even see the timer on the event! All of the ground vehicles are driven and filled with NPCs. Every vehicle, the NPCs, and the loot as well as all timers can be configured to suit your server. A PvP zone can be created within the event area for those of you who use TruePVE to control damage on your servers. The limits are nearly endless!

If you have some players on your server that you want to really send everything you have at, this is the plugin for you. Watch players crap their pants when they first encounter a full Convoy with multiple tanks and a Patrol Heli all attacking at once. Sit back and delight in their fear as all of the vehicles empty their occupants and NPCs swarm them mercilessly! 

**Required Dependency (must install this free plugin)**

    NpcSpawn – link is included and can be found in the ReadMe file included with download

**Chat commands (admin only)**

    /convoystart - launches the event using a random preset based on your configuration
    /convoystart PresetName - add the name of a preset from the configuration to launch a specific preset
    /convoystop - stops the event
    /convoyroadblock - the event will not be held on the road where you are standing (clear the Blocked roads section of config when you change maps)
    /convoypathstart - stand at starting point and enter command to start recording a custom route
    /convoypathsave RoutePresetName - to save a custom route (enter anything you'd like in place of RoutePresetName)
        multiple routes can be added to one route preset, one will be selected at random in this case
    /convoypathcancel - to reset the route

**Console commands (RCON only)**

    convoystart - launches the event using a random preset based on your configuration
    convoystart PresetName - add the name of a preset from the configuration to launch a specific preset
    convoystop - stops the event

**Plugin Config**

    en  –  example of plugin configuration in English
    ru  –  example of plugin configuration in Russian

**API**

    bool IsConvoyVehicle(BaseEntity entity)
    bool IsConvoyCrate(BaseEntity crate)
    bool IsConvoyHeli(BaseHelicopter baseHelicopter)
    bool IsConvoyNpc(ScientistNPC scientistNPC)

**Hooks**

    void OnConvoyStart() - called when a convoy appears
    void OnConvoyStop() - called when a convoy disappears
    void OnPlayerEnterConvoy(BasePlayer player) - called when a player enters the event area
    void OnPlayerExitConvoy(BasePlayer player) - called when the player leaves the event area
    void OnConvoyEventWin(ulong userId) - called at the end of the event and informs about its winner
    void OnConvoyStartMoving(Vector3 convoyPosition)
    void OnConvoyStopMoving(Vector3 convoyPosition)
    void OnConvoyAttacked(BasePlayer player, Vector3 convoyPosition)
