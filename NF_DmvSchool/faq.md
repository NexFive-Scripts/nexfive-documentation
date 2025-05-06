# FAQ

## General Questions

### What is NF_DmvSchool?
NF_DmvSchool is a comprehensive driving school system for FiveM servers that allows players to obtain various vehicle licenses through theory and practical tests.

### Which frameworks are supported?
The script currently supports both ESX and QBCore frameworks.

### Do I need any dependencies?
Yes, the script requires:
- ESX Framework or QBCore
- ox_lib
- ox_target
- ox_inventory (optional)

## Installation

### How do I install the script?
1. Download the resource from our store
2. Place the `NF_DmvSchool` folder in your server's resources directory
3. Add `ensure NF_DmvSchool` to your server.cfg
4. Configure the settings in the config file
5. Restart your server

### Do I need to set up a database?
No, the script will automatically create the necessary database tables on first run.

## Configuration

### How do I change the DMV location?
You can change the location in the config file:
```lua
Config.DMVLocation = vector3(215.124, -1398.777, 30.587)
Config.DMVHeading = 320.0
```

### How do I add custom theory questions?
You can add questions in the config file under `Config.TheoryQuestions`:
```lua
Config.TheoryQuestions = {
    {
        question = "Your question here?",
        options = {
            "Option 1",
            "Option 2",
            "Option 3",
            "Option 4"
        },
        correct = 1
    }
}
```

### Can I customize the test vehicles?
Yes, you can change the test vehicles in the config file:
```lua
Config.TestVehicles = {
    car = 'blista',
    motorcycle = 'faggio',
    truck = 'mule',
    bus = 'bus'
}
```

## Usage

### How do players take the test?
Players can start the test by:
1. Going to the DMV location
2. Using the target system to interact with the DMV NPC
3. Selecting the desired license type
4. Paying the fee
5. Taking the theory test
6. Completing the practical test

### What happens if a player fails the test?
Players can retake the test after a cooldown period. The cooldown time can be configured in the config file.

### How do admins give licenses?
Admins can use the following commands:
- `/givelicense [id] [type]` - Give a license to a player
- `/removelicense [id] [type]` - Remove a license from a player
- `/checklicense [id] [type]` - Check a player's license

## Troubleshooting

### The script isn't working after installation
1. Check if all dependencies are installed
2. Verify the resource is started in server.cfg
3. Check the server console for errors
4. Ensure the config file is properly configured

### Players can't start the test
1. Check if the player has enough money
2. Verify the DMV location is accessible
3. Check if the player has any existing licenses
4. Ensure the player has the required permissions

### Theory test questions aren't showing
1. Check if questions are properly configured in the config file
2. Verify the UI is working correctly
3. Check for any JavaScript errors in the console

## Support

### Where can I get help?
You can get support through:
- Our Discord server
- The script's store page
- Our support ticket system

### How do I report bugs?
Please report bugs through:
1. Our Discord server
2. The script's GitHub issues page
3. Our support ticket system

Include the following information:
- Server logs
- Steps to reproduce
- Expected behavior
- Actual behavior
- Screenshots or videos if possible 