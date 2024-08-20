CivIdle Building Calculator Commandline - by tiredpoet


This console app for windows was created to aid CivIdle steam game by Fish Pond Studio (https://store.steampowered.com/app/2181940/CivIdle/).

When executed it asks for a building name and desired number of that building, then it calculates number of building dependencies and it's resource needs.
 

If needed (to execute the .exe) download dotnet runtime from:
https://aka.ms/dotnet-core-applaunch?missing_runtime=true&arch=x64&rid=win-x64&os=win10&apphost_version=8.0.8

- Edit 'buildings_data.json' and add/edit:

	- building name
	- LVL » max level wanted for selected building
	- Gives (Resources Given - Supply)
		- Key » resource name
		- Value » resource value per tick
	- Needs (Resources Needed - Demand) 
		- Key » resource name
		- Value » resource value per tick
		
- Run 'CivIdleBuildingCalculator.exe'

example sample for 'buildings_data.json':		
{
  "Embassy": {
    "LVL": 20,
    "Gives": [
      {
        "Key": "Diplomacy",
        "Value": 40
      }
    ],
    "Needs": [
      {
        "Key": "Law",
        "Value": 100
      },
      {
        "Key": "Politics",
        "Value": 100
      },
      {
        "Key": "Philosophy",
        "Value": 100
      }
    ]
  }
