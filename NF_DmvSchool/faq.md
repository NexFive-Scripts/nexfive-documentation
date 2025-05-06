# FAQ

## General Questions

### What is NF_DmvSchool?
NF_DmvSchool is a comprehensive driving school system for FiveM servers that allows players to obtain various vehicle licenses through theory and practical tests.

### Which frameworks are supported?
The script currently supports both ESX and QBCore frameworks.

### Do I need any dependencies?
Yes, the script requires:
- ESX Framework or QBCore or Qbox
- ox_lib
- ox_target

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
Config.NPC = {
    {
        model = 'a_m_m_business_01',
        coords = vector3(240.632965, -1379.393433, 32.728149),
        heading = 136.06298,
        text = 'DRIVING SCHOOL',
        eventName = 'NexFive_Dmv:requestUI', 
        data = {},
        type = 'client',
        animation = 'idle',
        target = true,
    },
}
```

### How do I add custom theory questions?
You can add questions in the questions folder


### Can I customize the test vehicles?
Yes, you can change the test vehicles in the config file:
```lua
    driver = {
        Vehicle = "blista",
        speedLimit = 50,
        time = 15,
        spawnPoint = vector4(255.139, -1400.731, 29.537, 325.9),
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
- Our Discord server : https://discord.gg/eMR45WNT8Y


### How do I report bugs?
Please report bugs through:
- Our Discord server : https://discord.gg/eMR45WNT8Y

Include the following information:
- Server logs
- Steps to reproduce
- Expected behavior
- Actual behavior
- Screenshots or videos if possible 