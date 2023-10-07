# North American Rockwell OV-10 Bronco Checklist

The purpose of this project is to establish a decent set of checklist items in the game menu for Microsoft Flight Simulator 2020. I'm super grateful for the work **ariebaba** has done creating the [OV-10 Bronco](https://flightsim.to/file/61093/north-american-rockwell-ov-10-bronco) and released it for free on FlightSim.to.

## Install

Open the project in "Developer Mode" in MSFS. Build the project. It will produce a `Packages/` directory in the root of the project. The contents of that directory can be moved to your `Community/` directory.

> If you just want the ouput get it from [Flightsim.to](https://flightsim.to/profile/tabletopANDROID).

## SDK Development

I found it very confusing trying to create this project. Here's what I discovered through this journey. The `PackageSources/` directory in your root project is where you **MANUALLY** add "Asset Groups". In order for the compiler to see it and output it, it needs to be defined in `PackageDefinitions/[project-name].xml`.

> Note: Any changes made to the asset definition in Developer Mode will overwrite the .xml file. Keep that in mind as you use text editors and the UI from developer mode.

### Asset Type

Because I'm simply making a single XML file for the checklist I went with "Copy" as the asset type. I made sure to have the output follow the pattern as if I created a full aircraft (SimObjects\Airplanes\ariebaba-bronco\Checklist\).

### Observations

- The checklist UI will not display your changes after a build. `Esc > Restart > Continue` will load your changes.
- The `Page` element must have at least one valid `Checkpoint` element in order to be displayed.
- The `Clue` element cannot have an empty `name` attribute. It will crash the game.

### Definitions

- cameras.cfg
- Asobo_DefaultCheckpointLibrary.xml - <Instrument/> ID's

## Flight Simulator Freelance Society

Shout out to [FS2](https://forums.flightsimulator.com/t/fs-flight-simulator-freelance-society/422849). This Discord community helped me out when I was completely lost with out development worked. Very patient and very helpful.

## References

1. https://docs.flightsimulator.com/html/Content_Configuration/Checklists/Checklists.htm
1. https://docs.flightsimulator.com/html/Developer_Mode/Project_Editor/The_Project_Editor.htm#NewProject
1. https://forums.flightsimulator.com/t/guide-aircraft-checklists/306098
1. https://www.youtube.com/watch?v=X3qyyGDRUus
1. https://docs.flightsimulator.com/html/mergedProjects/How_To_Make_An_Aircraft/Contents/Files/Checklists/Checklist_Best_Practices.htm?agt=index
1. https://forums.flightsimulator.com/t/fs-flight-simulator-freelance-society/422849