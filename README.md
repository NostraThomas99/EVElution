
# EVElution

Evolving your EVE experience

EVElution is a (currently semi-autonomous) bot for EVE Online. It requires Innerspace and ISXEVE in order to operate. Drop the .exe and config file into your InnerSpace/.NET Programs folder and run "dotnet evelution" from the in-game console.
## Behaviors

The bot will autonomously switch between various "behaviors" as the conditions for those behaviors are met. If you would like the bot to not perform a particular behavior, please disable it in the settings menu.

#### NPC Combat

The bot will attempt to attack and kill any nearby NPC enemies. This includes rats in belts, combat site NPCs, or mission enemies. Anything that is any NPC and shows up red on your overview. This behavior takes priority over all others and the bot will not do anything else until all enemies are dead.

#### Player Combat

Not yet implemented

#### Mining

Not yet implemented

#### Defense Measures

The bot will enable/disable defensive modules (armor repairers, shield extenders, etc.) to try and stay alive. Boosters and repairers are run as-needed while other modules are kept on constantly.

NOTE: Not all modules are currently supported, please submit an issue if something is not firing that you think should be.

#### Looting

Bot will loot any nearby lootable wrecks and containers (assuming it has loot rights)

#### Salvaging

Bot will use any equipped salvaging equipment (both tractor beams and salvagers) to salvage any nearby wrecks

#### Drones

Bot will use drones in bay during the relevent behaviors

NOTE: While all types of drones will eventually be supported, combat drones during NPC combat are currently the only working ones

#### Target priority

Used during NPC combat, the bot will prioritize targets either based on distance, or based on capabilities (targeting jammers, webbers, particularly dangerous enemies first).

#### AP Assist

If enabled, the bot will automatically engage autopilot 60 seconds after finishing all other tasks. Useful if you wanna get up and walk away while it cleans up the salvage at the end of a mission. This option will always disable itself after it has been activated to allow for proper switching between behaviors afterwards.
## Caches and the Re-spring button

The bot uses internal caches to keep track of which entities it has targeted with which modules, and this implementation is currently imperfect. Entities will sometimes get stuck in the cache, and modules will not fire at it. This is particularly common at the end of a salvaging run, where the last wreck might not get a salvager on it if only one is equipped. To solve this, I've put a "Re-spring" button (bonus points to you if you get the reference) on the main page to clear any caches on request and allow the bot to start fresh. This is one of the main reasons the bot is currently semi-autonomous. It's best to keep an eye on it for the time being.

The bot will also attempt to clear the caches itself if it thinks it's stuck, but this is also imperfect. This entire implementation is under heavy development.


## Important Notes

#### YOUR SHIP SHOULD BE CAP STABLE
The bot will not currently detect capacitor level nor will it attempt to adjust its behaviors based on capcitor level. If your cap dies, you die.

#### Movement

The bot does not do any movement currently, other than to orbit/keep at range targets during combat or to approach salvage/loot. You will need to get the bot on the grid you want to work on yourself, whether that's a mission pocket or a combat site or a belt.
## Future Capabilities

#### Movement

The bot will be able to navigate on its own the future.

#### Fleet support

While the bot does work (and excels) in fleets, this will be much expanded in the future. The bot will be able to manage fleets of toons easily from one interface, without the need to setup innerspace relays. Stay tuned on this one.

#### {Your Suggestion Here}

Want something you don't see on here? Suggest it! I'm always open to good ideas!
## License and Copyright
Copyright © 2023 NostraThomas Industries. All rights reserved.

This software and associated documentation files (the "Software") are provided for educational purposes only. The Software is provided "as is" without warranty of any kind, express or implied, including but not limited to the warranties of merchantability, fitness for a particular purpose, and non-infringement. In no event shall the copyright holder or contributors be liable for any claim, damages, or other liability, whether in an action of contract, tort, or otherwise, arising from, out of, or in connection with the Software or the use or other dealings in the Software.

Redistribution, modification, sublicensing, or use of the Software for commercial purposes is strictly prohibited without the express written consent of the copyright holder. All rights to the Software are retained by the copyright holder.

This copyright notice applies exclusively to the Software and does not extend to any third-party libraries or software that may have been used in the development of the Software. Third-party libraries are subject to their own licenses and copyright terms.

