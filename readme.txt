To change the rendered images you need to override the default images and settings. Please do not change the files in the root folder of the app, but only in the mods folder.

If any reuqired file is not found in the mod folder, the default file will be used.

Each mod must contain a description.json file in the root folder of the mod. It must contain the name of the mod and the author, as well as the version in the format "x.x" (only in this format).

A mod may contain a small picture called 'preview.png' to roughly show what the mod does.

To distribute the mod it can be packed in a zip-archive (without the root folder mod, the archive should contains immediately folders overridden by the mod), and then placed in the folder 'mods/' of the app. At the next launch the mod will be automatically unpacked and displayed in the list of mods.

Driver name (general / displayed) -> First name or Online ID
Real name -> Second name (leave blank if you are not using real names)
Driver Description -> Team name (for fastest lap at the bottom of race results)

For pre season R0 round count:
components -> event_calendar, look for this line:

"Source": "R{Item.Position, Converter=NumberSubtract, Parameter=1}",

change number on the end to how many pre season races you have. Set 0 for none.

DriverLimit: 10 & StartPositionsFrom: 0 = Top 10
(Change DriverLimit to get any Top ... positions you wish)

DriverLimit: 20 & StartPositionsFrom: 9 = Positions 10-20
(Or all positions past P9).


To add F2 logos to renders:
user\mods\F1-2023-Theme-V2-main\images\logos (or V1)
Copy and paste all logos to the following:
RacingLeagueTools_v075_portable\images\logos\teams
