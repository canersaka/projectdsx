# Day 0: 
## Completed work:
  - Bought DS Lite + GBA Game/DS Game
  - Created initial draft of flow chart showing components
  - Began CAD for shell to get a rough idea on ergonomics
## Notes
  - I'm not quite sure where the idea for this came to me but I know it was at 9 AM in my Embedded Design class
  - I'm really excited for this idea and am full-sending it, I have already purchased the DS lite and am planning out what else I will purchase and I am researching everything I may need
  - While I wait, I'm going to sketch out schematics, first I think I'm going just get a rough idea of what needs to connect to what
  - If I'm bored I may try to start some CAD for the shell, I'm not 100% sure on the components I will use, so I'm not certain on what the size constraints will be but I will try to get a rough idea of the overall size of the components, but also I might just design it with ergonomics as top priority, and try to work the components around the shell's design.
# Day 1: 
## Completed work:
  - Recreated the rough schematic to reflect changed plans, offloading more of the switching to the FDGA, which has for now been decided to be the Tang Nano 9k
  - Purchased all components that are required (as of now)
     - Will update list of materials later
## Notes
  - The project has shifted to be strongly reliant on a single FPGA. There is RGB parallel to HDMI adapters, and switches I could use, but this project was never meant to be easy, it's going to take a lot more embedded design than I originally planned, but I believe it will be worth it for saving space, as the DS's own hardware already takes up a decent chunk of space, and whatever I end up doing for the emulator side will likely take up a good amount of space too, as the PI5 that is being used for testing is huge on its own. That's why all of the switching hardware and software being on a single smaller chip like the Tang Nano 9k will be ideal. This wasn't planned extremely throughoughly, so I guess I'll just have to wait and see what roadblocks come up, I'm sure there will be no shortage of them.
  - The screen I bought ended up being a lot bigger than I expected, but all the better for the emulator side. Might make OG DS a bit wonky since theres a good amount of games that use both screens and the bezel in between them as a spacer so that the two screens line up to make one large vertical (or in some specific games horizontal: see mario&luigi bis) screen. Because the top screen will be a lot larger now relative to the bottom screen they may not line up well, but the aspect ratio will be determined in software and will not be too off-putting for the DS mode.
  - Also gyro controls would be awesome?? Shouldn't be too hard after everything else
# 10/21:
  - I had made a great deal of progress on what I want the shell design to be however Solidworks decided to crash right as I was almost finished, and I naturally hadn't saved in over an hour, so that was frustrating. It won't take too long to get it done, however it's Midterm season right now and I am really trying to focus on studying, so this project is on the backburner, most components won't arrive for another few weeks anyways.
