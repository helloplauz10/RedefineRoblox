# Using the CLI Tool
You need a Terminal app to use it or a custom one. You can use the default Terminal app preinstalled in your Mac.
```
modifiedb [command] [args]
```

# Joining a game
Joins a specific game. To be more specific, add job id if needed.
```
modifiedb join [placeid] [jobid optional]
```
* placeid: the place id to join, it will raise ValueError if you input a string value (int)
* jobid: the job id of a public place id to join, (str, UUID)

# Fast Flags
Write, create, or get a Fast Flag.
Find fast flags at [Bloxstrap's Discord Server](https://discord.gg/nKjV3mGq6R)
```
modifiedb fflags [write/get] [fflag] [value (for write)]
```
* write: write or create a fast flag
* get: get the value of a fast flag

## Writing a Fast Flag
```
modifiedb fflags write [fflag] [value]
```
* fflag: the fast flag to write or create
* value: the value to set

## Getting the value of the Fast Flag
It will print the value of the fast flag specified
```
modifiedb fflags get [fflag]
```
* fflag: fast flag to get the value

# Settings
Modify ModifiedBlox by modifying a setting.
```
modifiedb settings [modify/get] [setting] [value (for write)]
```

Here are the list of settings:
```
preferredCDN (str)
preferredMod (str)
channel (str)
notifyServerInfo (bool)
monitorEnabled (bool)
remakeMissingFiles (bool)
```
* preferredCDN: the CDN to use (default: https://setup.roblox.com)
* preferredMod: the mod that ModifiedBlox will apply to Roblox each time it launches
* channel: the channel to use (default: LIVE)
* notifyServerInfo: a toggle that will notify about the information of the server you joined
* monitorInfo: a toggle that will monitor Roblox consecutively
* remakeMissingFiles: a toggle that makes a new file or folder whenever some of the parts of ModifiedBlox are missing (will notify the user whenever remaking)

## Modifying a setting
```
modifiedb settings modify [setting] [value]
```
* setting: setting to modify
* value: value to set, raises an error when the value mismatches the type needed

## Getting the value of a setting
It will print the value of a setting like the Fast Flag one
```
modifiedb settings get [setting]
```
* setting: setting to get

# Modifications
For short "mod". Give Roblox a new look with mods.
Find mods at [Bloxstrap's Discord Server](https://discord.gg/nKjV3mGq6R)

Mods are located at:
```
~/ModifiedBlox/modifications/
```

```
modifiedb mods [list/use] [mod (for use)]
```

## Listing the mods installed
Prints out the mods you installed.
```
modifiedb mods list
```

## Using a mod
An alternative command to:
```
modifiedb settings modify preferredMod [mod]
```

```
modifiedb mods use [mod]
```
* mod: the **name** of the mod's folder, raises FileNotFoundError whenever the folder doesnt exist

# Updating Roblox
Update Roblox to the latest version. Fast Flags and mods retain after.

## Updating
```
modifiedb update [channel optional] [cdn optional]
```
* channel: the channel to use (default: setting channel)
* cdn: the CDN that the updator will use (default: setting preferredCDN)
