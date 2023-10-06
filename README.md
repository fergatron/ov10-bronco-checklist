# North American Rockwell OV-10 Bronco Checklist

The purpose of this project is to establish a decent set of checklist items in the game menu for Microsoft Flight Simulator 2020. I'm super grateful for the work **ariebaba** has done creating the [OV-10 Bronco](https://flightsim.to/file/61093/north-american-rockwell-ov-10-bronco) and released it for free on FlightSim.to.

## Install

Open the project in "Developer Mode" in MSFS. Build the project. It will produce a "Packages/" directory in the root of the project. The contents of that directory can by moved to your "Community/" directory.

## SDK Development

I found it very confusing trying to create this project. Here's what I discovered through this journey. The `PackageSources/` directory in your project is where you manually add "Asset Groups". In order for the compiler to see it and output it, it needs to be defined in `PackageDefinitions/[project-name].xml`.

> Note: Any changes made to the asset definition in Developer Mode will overwrite the .xml file. So; make all your changes in the Developer UI.

### Asset Type

Because I'm simply making a single XML file for the checklist I went with "Copy" as the asset type. I made sure to have the output follow the pattern as if I created a full aircraft (SimObjects\Airplanes\ariebaba-bronco\Checklist\).

## References

1. https://docs.flightsimulator.com/html/Content_Configuration/Checklists/Checklists.htm
1. https://docs.flightsimulator.com/html/Developer_Mode/Project_Editor/The_Project_Editor.htm#NewProject