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


## Example Usage

```lua
-- Check if player has car license
local hasLicense = exports['NF_DmvSchool']:HasLicense('car')
if hasLicense then
    print('Player has car license')
end

-- Give motorcycle license to player
exports['NF_DmvSchool']:GiveLicense(1, 'motorcycle')
