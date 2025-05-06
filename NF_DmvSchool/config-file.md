# Config File

The configuration file is located at `config.lua` in the resource folder. Here you can customize various aspects of the DMV School system.

## General Settings

```lua
Config = {}

-- Framework settings
Config.Framework = 'esx' -- 'esx' or 'qb-core'

-- Location settings
Config.DMVLocation = vector3(215.124, -1398.777, 30.587)
Config.DMVHeading = 320.0

-- License prices
Config.LicensePrices = {
    car = 1000,
    motorcycle = 800,
    truck = 2000,
    bus = 2500
}

-- Test settings
Config.TheoryQuestions = 10
Config.PracticalTime = 300 -- seconds
Config.MaxMistakes = 3

-- Vehicle spawn settings
Config.TestVehicles = {
    car = 'blista',
    motorcycle = 'faggio',
    truck = 'mule',
    bus = 'bus'
}

-- Notification settings
Config.Notifications = {
    success = 'You have passed the test!',
    fail = 'You have failed the test!',
    start = 'Test started! Good luck!',
    end = 'Test completed!'
}
```

## License Types

```lua
Config.Licenses = {
    car = {
        label = 'Car License',
        theory = true,
        practical = true,
        price = 1000
    },
    motorcycle = {
        label = 'Motorcycle License',
        theory = true,
        practical = true,
        price = 800
    },
    truck = {
        label = 'Truck License',
        theory = true,
        practical = true,
        price = 2000
    },
    bus = {
        label = 'Bus License',
        theory = true,
        practical = true,
        price = 2500
    }
}
```

## Theory Questions

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
    },
    -- Add more questions here
}
```

## Practical Test Routes

```lua
Config.TestRoutes = {
    car = {
        {
            coords = vector3(215.124, -1398.777, 30.587),
            heading = 320.0,
            type = "start"
        },
        -- Add more checkpoints here
    }
}
```

## Admin Commands

```lua
Config.AdminCommands = {
    giveLicense = 'givelicense',
    removeLicense = 'removelicense',
    checkLicense = 'checklicense'
}
```

## UI Settings

```lua
Config.UI = {
    primaryColor = '#4CAF50',
    secondaryColor = '#2196F3',
    font = 'Roboto',
    fontSize = 14
}
```

## Notifications

```lua
Config.Notifications = {
    useFramework = true, -- Use framework notifications
    useCustom = false, -- Use custom notification system
    position = 'top-right',
    duration = 5000
}
```

## Database Settings

```lua
Config.Database = {
    tableName = 'nf_dmv_licenses',
    autoCreate = true
}
```

## Debug Mode

```lua
Config.Debug = false -- Enable debug mode for development
``` 