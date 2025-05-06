# Configuration

This guide will help you configure the NF_DmvSchool script to match your server's needs.

## Basic Configuration

### Framework Selection
```lua
Config.Framework = 'esx' -- Change to 'qb-core' if using QBCore
```

### Location Settings
The DMV location can be customized by changing the coordinates and heading:
```lua
Config.DMVLocation = vector3(215.124, -1398.777, 30.587)
Config.DMVHeading = 320.0
```

### License Prices
Adjust the prices for different license types:
```lua
Config.LicensePrices = {
    car = 1000,
    motorcycle = 800,
    truck = 2000,
    bus = 2500
}
```

## Advanced Configuration

### Test Settings
Customize the test parameters:
```lua
Config.TheoryQuestions = 10 -- Number of theory questions
Config.PracticalTime = 300 -- Time limit for practical test in seconds
Config.MaxMistakes = 3 -- Maximum allowed mistakes
```

### Vehicle Settings
Configure test vehicles for each license type:
```lua
Config.TestVehicles = {
    car = 'blista',
    motorcycle = 'faggio',
    truck = 'mule',
    bus = 'bus'
}
```

### Theory Questions
Add or modify theory questions:
```lua
Config.TheoryQuestions = {
    {
        question = "What does a red traffic light mean?",
        options = {
            "Stop",
            "Go",
            "Slow down",
            "Proceed with caution"
        },
        correct = 1
    }
    -- Add more questions here
}
```

### Practical Test Routes
Define test routes for each license type:
```lua
Config.TestRoutes = {
    car = {
        {
            coords = vector3(215.124, -1398.777, 30.587),
            heading = 320.0,
            type = "start"
        }
        -- Add more checkpoints
    }
}
```

## UI Configuration

### Colors
```lua
Config.UI = {
    primaryColor = '#4CAF50',
    secondaryColor = '#2196F3',
    font = 'Roboto',
    fontSize = 14
}
```

### Notifications
```lua
Config.Notifications = {
    useFramework = true,
    useCustom = false,
    position = 'top-right',
    duration = 5000
}
```

## Database Configuration

### Table Settings
```lua
Config.Database = {
    tableName = 'nf_dmv_licenses',
    autoCreate = true
}
```

## Permission Configuration

### Admin Commands
```lua
Config.AdminCommands = {
    giveLicense = 'givelicense',
    removeLicense = 'removelicense',
    checkLicense = 'checklicense'
}
```

## Debug Mode

Enable debug mode for development:
```lua
Config.Debug = false -- Set to true for debug information
```

## Best Practices

1. Always backup your configuration before making changes
2. Test changes in a development environment first
3. Keep your theory questions up to date
4. Regularly review and update test routes
5. Monitor server performance after configuration changes 