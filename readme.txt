1. Correct Round Count On Calendar Renders (With Pre-seasons)
- File location: components/event_calendar.json
- Code: R{Item.Position, Converter=NumberSubtract, Parameter=0} 
- Change number (Parameter-0) to the amount of pre-season races on your calendar
- Example: 2 pre-season races ->  R{Item.Position, Converter=NumberSubtract, Parameter=2}
- Leave value at 0 for calendars with no pre-season races

2. Add Custom Logos
- File location: images/Logos
- Name logo png image must match the name of the team it belongs to.
- Logo size must be 256x256 maximum (advised to fill 90% of the square).

3. Add Custom Avatars For Multi Tiers
- File location: images/suits (add images here)
- Name images to match the driver online username with _1 or _2 to represent seat position. Example: JohnsGaming0705 second driver -> JohnsGaming0705_2
- File locations: layouts/lineup_f1/layer1-main/layer.json | components/driver_line_cell_official.json | components/podium.json
- Replace images/suit/{Item.Team.Name}_1/2 (wriiten as images/suit/{Item.Team.Name}_{Item.SeatPosition} in other renders) with images/suit/{Item.Driver.Name}_1/2 or images/suit/{Item.Driver.Name}_{Item.SeatPosition}.
- Specificly for lineup renders, a list function is used: Line0 (left list) Line1 (right list). images/suit/{Item.Line0/1.Driver.Name}_1/2 should replace the existing team name lines.

4. Add My/New Language
- Folder location: localizations
- Copy & paste "english.json"
- Rename copied file to new Language
- Convert left-hand side text to the translation
- Example: "LAPS": "VOLTAS",
- If english translation is in uppercase, the translation must also be in uppercase
- Send new language file to Dark373 for permanent addition to the theme.

5. Theme Settings
- Position Progress: change driver/team progress to position from points.
- Real Name On Renders: Use driver name field (1) to name field (2). Example: (John Smith), John -> Smith
- In Game Name On Renders: Uses In-game name field, replacing name field (1). Example: John -> JohnsGaming0705.
- Full Name On Renders: Renders both name fields together. Example: John -> John SMITH
- Switch Name Fields: Name field (2) renders infront of name field (1). Example: John SMITH -> Smith JOHN OR John -> Smith
*if all name related settings are turned off, name only name field (1) will render. Example: (John Smith) -> John

- Champion Colour: Convert the font colour for points to gold to signify P1 has won the championship. (Entire P1 line in session results.)
- Logo Size (int): Size of the league logo on all renders.
- Driver Limit (int): Amount of positions/drvers being rendered. Example: value of 12 -> positions 1st to 12th will render.**
- Start Positions From (int): Starts counting positions from this value. Example: value of 11 -> renders will show positions from 11th and above.**
**Combination: Driver Limit (20) & Start Positions From (11), Positions from 11th to 20th will render.

- Change Word Order: Word ordering changes for different language localizations with a different word order to english,.

// Lineup Settings 
- Driver Name On Line Up & In Game Name On Line Ups: Render name fields below main name field used in line up graphics. (cannot be active at the sane time).
- Render Reserve Driver: Render reserves on universal line up render.
- Reserve Driver Max (int): Amount of lines (Pairs of reserves) should be rendered. Example: 4 reserves -> value=2.

// Calendar Settings
- Second Calendar Events In Column: Amount of events that renders in the second cloumn (set to 0 for one column). Example: 10 total rounds -> set value to 5 (half the total) for equal events in both columns.

6. Change/Switch Renders
- Desired render (example_layout2) does not appear on drop down menus due to size limits:
- example_layout1 does appear as a renderable image in the app so we need to swap index numbers between example_layout1 and example_layout2
- Index numbers are located in the layout_description.json files for each layout
- File location: layouts/example_layout1/layout_description.json
- Idex (position on drop-down menu).
- Swap Index numbers of example_layout1 and example_layout2.
- example_layout2 now appears on the drop-down menu instead of example_layout1

7. Add Official F1 2023 Team Colours To Your Database
- File location: global/global_vars.json
- Under //colors header are the official hex codes. Copy and paste them into your database (in app): Database -> Teams -> Color #1
- Note: Haas official color intended use for F1 2023 Lineups only, set to FFFFFF (White) for all other renders.

8. Lne-up/Driver Translation On F1 2023 Render Too Large
- Go to: layouts/lineup_f1.json
- Scroll to the bottom of the file
- Change "FontSize" accordingly

9. Change Font Colour For Season Names
- (In app) go to "Categories"
- Create Category "+ Add"
- Primary colour of the category determines season name font colour
- (In app) go to "Calendar", right-click on the season and "Edit"
- Apply category
