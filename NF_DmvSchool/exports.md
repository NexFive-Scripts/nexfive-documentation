# Exports

The NF_DmvSchool script provides several exports that can be used by other resources to interact with the DMV system.

## Client Exports

### Check License
```lua
exports['NF_DmvSchool']:HasLicense(licenseType)
```
Checks if a player has a specific license type.
- `licenseType` (string): The type of license to check ('car', 'motorcycle', 'truck', 'bus')
- Returns: `boolean`

### Start Test
```lua
exports['NF_DmvSchool']:StartTest(licenseType)
```
Starts a DMV test for the specified license type.
- `licenseType` (string): The type of license test to start
- Returns: `boolean`

### Get License Info
```lua
exports['NF_DmvSchool']:GetLicenseInfo(licenseType)
```
Gets detailed information about a specific license.
- `licenseType` (string): The type of license to get info for
- Returns: `table`

## Server Exports

### Give License
```lua
exports['NF_DmvSchool']:GiveLicense(source, licenseType)
```
Gives a license to a player.
- `source` (number): The player's server ID
- `licenseType` (string): The type of license to give
- Returns: `boolean`

### Remove License
```lua
exports['NF_DmvSchool']:RemoveLicense(source, licenseType)
```
Removes a license from a player.
- `source` (number): The player's server ID
- `licenseType` (string): The type of license to remove
- Returns: `boolean`

### Check License
```lua
exports['NF_DmvSchool']:HasLicense(source, licenseType)
```
Checks if a player has a specific license.
- `source` (number): The player's server ID
- `licenseType` (string): The type of license to check
- Returns: `boolean`

### Get All Licenses
```lua
exports['NF_DmvSchool']:GetAllLicenses(source)
```
Gets all licenses for a player.
- `source` (number): The player's server ID
- Returns: `table`

## Events

### Client Events

```lua
-- Test started
TriggerEvent('NF_DmvSchool:TestStarted', licenseType)

-- Test completed
TriggerEvent('NF_DmvSchool:TestCompleted', licenseType, passed)

-- License updated
TriggerEvent('NF_DmvSchool:LicenseUpdated', licenseType, hasLicense)
```

### Server Events

```lua
-- Give license
TriggerServerEvent('NF_DmvSchool:GiveLicense', licenseType)

-- Remove license
TriggerServerEvent('NF_DmvSchool:RemoveLicense', licenseType)

-- Check license
TriggerServerEvent('NF_DmvSchool:CheckLicense', licenseType)
```

## Example Usage

```lua
-- Check if player has car license
local hasLicense = exports['NF_DmvSchool']:HasLicense('car')
if hasLicense then
    print('Player has car license')
end

-- Give motorcycle license to player
exports['NF_DmvSchool']:GiveLicense(1, 'motorcycle')

-- Start truck test
exports['NF_DmvSchool']:StartTest('truck')
``` 