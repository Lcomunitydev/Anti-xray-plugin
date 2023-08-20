# Anti-xray-plugin

How does it work?

Basically, players are limited in the amount of valuable ores they can mine, based on their play time on the server. Legitimate, non-cheating players probably won't notice because the default limits are generous, but xrayers will be blocked from mining ore too quickly. So cheaters can still cheat, but they can't take more than a non-cheating player's reasonable share of ore. So their only gain is avoiding monsters while digging. They can't mine their first diamonds/"other good stuff" sooner than non-cheating players, and they can't take more total than they could if they weren't cheating.

How does this compare to Spigot AntiXRay and Orebfuscator?
The trouble with these and similar plugins is that while they're incredibly effective, they're very, very expensive to run. They consume a lot of CPU cycles doing deep packet inspection and manipulation, and they consume a lot of RAM trying to cache the results in memory. Small servers simply can't afford it, and larger servers have to cut back on their max players or other plugins. Any server which doesn't have enough CPU or memory may suffer heavy lag and crashes, other servers are simply spending too many cycles to stop a few cheaters - it's not a good trade-off.

In contrast, Anti-XRay is extremely cheap. It doesn't do any heavy processing, and consumes very little memory. It's true that technically cheaters can still use xray to find ores and dungeon chests (Mojang hasn't really made those worth hiding), but they're limited in how much advantage they get out of it. Basically, you're allowing players to cheat (but only very little!) to save immensely on CPU cycles and RAM.

How does this compare to ore loggers and ratio reporters?
Those simply don't work. Viewing a report to determine who has been x-raying only helps you catch players AFTER they've done permanent damage, removing massive amounts of diamonds so that non-cheating players can't find any. Banning the cheaters doesn't actually solve the problem, because it doesn't put the diamonds back in the ground AND more cheaters will soon replace those guys, so the problem continues. Also, this approach requires administrators to actively work to catch cheaters. An automatic approach like that provided by this plugin makes more sense.

Anti X-Ray keeps ores in the ground so that non-cheating players can find them. By placing limits on the amount of valuable resources a player can mine based on his play time on the server, Anti X-Ray guarantees that cheaters don't get greedy. They can still cheat a little, but not to the extreme of ruining the fun of other players. In fact, most new-to-server cheaters just leave the server to find another server where they can cheat without limits, solving your cheating problem very well.

Versus ore loggers, you're actually SOLVING the problem, and doing it in a fully automated fashion. Versus ore obfuscation solutions, you're saving RAM and CPU.

The Details
Players have an invisible currency which grows while they play (up to a maximum amount). Players who aren't actively playing (idling) don't gain any. When players break a valuable block, their total is reduced. If they don't have enough to break the block, they get a message explaining that they've reached their limit, and will have to wait X minutes before they can break that block.

Players who have been playing on your server since before you installed this plugin will start maxed-out to make the transition go smoothly.

Players who are NEW to your server after you install this plugin will start with a negative amount. This will prevent players from logging in and immediately x-raying to get valuables like diamond, because they won't have played enough yet to reasonably mine diamonds without cheating.

Yes, it's possible that some players who aren't cheating will run into the limits. It's my goal to adjust the default limits to minimize the chance of impacting legitimate players, while at the same time stopping xrayers from going crazy and taking all the valuable ore for themselves. If a player complains, these are the common scenarios:

That player is a cheater, and is trying to convince you to disable the plugin or give him permission to bypass it so that he can cheat more.
That player has "raided" someone else's existing mine instead of exploring on his own, allowing him to find diamond within the first hour of joining the server for the first time. Tell him to stop being lazy and earn his own diamonds.
The player is EXTREMELY lucky, and managed to survive a reckless cave diving expedition without bothering to grow food or make armor and weapons. This is extremely unlikely - the player is probably cheating.
That player is "branch mining", which involves tediously mining in long, straight, parallel tunnels near bedrock to collect lots of diamond. Chances are that player has an unhealthy obsession with diamonds, and already has a million more diamonds than he can possibly use. For this case, I recommend advising the player to take a break from mining when he hits the limit. If you give a player like this the bypass permission, he will grab most of the diamond in the area, robbing other players of the opportunity (even though he's not cheating, he's potentially causing a problem).
