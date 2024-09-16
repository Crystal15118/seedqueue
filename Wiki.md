# FAQs
## Related to SeedQueue Settings

**What Settings should I use?**  
Background Pingu's (discord bot in the [SeedQueue Discord](https://discord.gg/9P6PJkHCdU)) `recommended_settings` command gives a good starting point for testing the best settings you can have. If you want to learn about all the settings read below.

**What are `Max Queued Seeds`?**  
The seeds which are ready in the background to come up once you reset seeds on your wall are the Max Queued Seeds (*note that Max Queued Seeds also include the seeds visible on your wall screen*).

**How many Max Queued Seeds can I have?**  
The number of Max Queued Seeds you can have, depend upon the amount of RAM you can allocate (*note that there is no need to allocate anymore than 13000 MB of RAM*). To find out the value based on the RAM you can allocate use the following formula: `Max Queued Seeds = (Max RAM - 2000) / 250`  
*It is recommended to not put Max Queued Seeds any less than the amount of Max Generating Seeds (Wall) you have*.

**What are `Max Generating Seeds (Wall)` ?**  
The amount of seeds that will concurrently be generating while your on the wall screen are called Max Generating Seeds (Wall).

**How many Max Generating Seeds (Wall) would be best for me?**  
The number of Max Generating Seeds (Wall) you can have, depend upon the amount of logical processors you have. To find out the best value based on the amount of logical processors you have, you can test by benchmarking with values which are 50%, 55%, 60%, ... or 100% of the amount of logical processors you have.  
*Note that its recommended that you don't put its value above the amount of logical processors you have*.

**What are `Max Generating Seeds`?**  
The amount of seeds that will concurrently be generating while your playing a seed are called Max Generating Seeds.

**How many Max Generating Seeds would be best for me?**  
To find out the best value, play out seeds using SeedQueue and look for the highest value that doesn't make you lag while playing a seed.

**What is `Max World Generation %` ?**  
Stops generating a seed at the set percentage unless it is locked.  
*Note that it will still wait for WorldPreview to be configured before stopping generation.*

**What do I put Max World Generation % at?**  
Max World Generation % always depends on your style of playing. Usually people put it between 10-30 but there isn't really one good percentage for it.  
*People put it between 10-30 because they don't want to generate seeds that they are going to reset 100% as it's a loss of time and resources.*

**What does `Resume On Filled Queue` do?**  
Once the Queue has filled then this option if enabled would override the Max World Generation % value i.e. previews will start generating beyond the Max World Generation % value.

**What are `Background Previews`?**  
The amount of previews that will show up on the Wall Screen (from Max Queued Seeds when they start generating).

**What does `Freeze Locked Preview` do?**  
If this option is enabled then if a preview is locked, it stops generating chunks on the preview.

## Related to Wall

**How can I quit to Title Screen from the Wall?**  
Shift + Esc

**How can I make my previews pause with F3 on wall?**  
Go to StandardSettings and enable F3 Pause on World Load.

**How do I change textures/sounds/wall layout?**  
You can customize using a resourcepack,
I recommend checking out #resourcepacks or downloading the example pack here: https://github.com/KingContaria/julti-dynamic-resourcepack/releases/tag/1.0
You can find out everything you need to know in the wiki: https://github.com/KingContaria/seedqueue/wiki/Customization  
*If you have any more questions about stuff that isn't working the way you want it to please create a post in #support-forum of* [SeedQueue Discord](https://discord.gg/9P6PJkHCdU).

**Why are no previews showing up in the 'preparing' group of my custom layout?**  
Go to `Performance Settings > Background Previews` and set it to the size of your preparing group.

**How can I remove secondary/blocking keys?**  
You can unbind them using Escape.

**How can I limit reset sounds?**  
By default, SeedQueue will play one reset sound for every preview that gets reset.
You can add a Reset All sound that will play instead of a bunch of individual reset sounds with a resource pack.

**How can I play next lock?**  
By enabling `Bypass Wall Screen` in SeedQueue Config Settings.

**Why do chunks stop generating on my previews?**
This could be due to `Freeze Background Previews` option being enabled in SeedQueue Config Settings.  
*This setting when enabled, stops chunks from generating on a preview if it's locked*.

## Related to Performance

**Why do I lag for x seconds when I enter a world?**  
This could be due to the value of Max Generating Seeds being too high because the CPU is using its power to generate seeds while you're playing another seed and increasing this value too much causes lag spikes while playing.  
*Note that the lag spikes stop once the queue of seeds has filled so that is why the lag is for a certain amount of time*.

**Why are my previews taking so much time to come up on the SeedQueue Wall Screen?**  
This could be due to the value of Max Generating Seeds (Wall) being too high.
*Note that it is recommended to not be put above the number of logical processors on your system*.

## Related to Recording

**How can I show my reset counter on OBS?**  
`.minecraft/config/mcsr/atum/rsg-attempts.txt`

## Misc

**When will SeedQueue be ported to other versions?**  
SeedQueue relies on porting a bunch of other mods first, so it's going to take a while. Additionally, there will be at the very least a month of time between release and starting porting efforts to catch any issues or implement important feedback.