# NF_ReportSystem Configuration Guide

This guide explains how to configure the NF_ReportSystem for your server.

## Basic Configuration

### Framework Selection
```lua
Config.Framework = 'esx' -- Options: 'esx', 'qbcore', 'vrp', 'ace', 'custom', 'SteamHEX'
```

### Framework Permissions
```lua
Config.Framework_perms = {
    ['admin'] = true,
    ['headadmin'] = true,
    ['owner'] = true,
    ['headhelper'] = false,
    ['helper'] = false,
    ['user'] = false,
}
```

### Admin List (for SteamHEX)
```lua
Config.AdminList = {
    'steam:11000013cb8b8ba',
}
```

## Command Configuration

### Player Commands
```lua
Config.ReportCommand = 'report' -- Command for players to submit reports
```

### Admin Commands
```lua
Config.ReportAdminCommand = 'reports' -- Command for admins to view reports
```

## UI Configuration

### Colors
```lua
Config.mainColor = "#0a58ca" -- Main color for UI elements
```

### UI Text
```lua
Config.UI = {
    ["Press_For_Back"] = "Press For Back",
    ["Report_System"] = "Report System",
    ["PLAYER"] = "PLAYER",
    ["PLAYER_Desc"] = "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
    ["BUG"] = "BUG",
    ["BUG_Desc"] = "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
    ["QUESTION"] = "QUESTION",
    ["QUESTION_Desc"] = "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
    -- ... other UI text entries
}
```

## Screenshot Configuration

### Basic Screenshot
```lua
Config.ScreenshotBasic = true -- Enable/disable screenshot functionality
```

## API Configuration

### Discord Bot
```lua
Config.Bot_Token = 'YOUR_DISCORD_BOT_TOKEN' -- Discord bot token for avatars
Config.BotName = 'Test' -- Bot name
```

### Steam API
```lua
Config.SteamApiKey = 'YOUR_STEAM_API_KEY' -- Steam API key for avatars
```

### Server Information
```lua
Config.ServerName = 'Test' -- Server name
Config.IconURL = "" -- Server icon URL
```

## Notification System

### Notification Function
```lua
Config.Notify = function(title, message, time, types, svside, id)
    if svside then
        TriggerClientEvent('NF_ReportSystem:Notify', id, title, message, time, types)
    else 
        TriggerEvent('NF_ReportSystem:Notify', title, message, time, types)
    end
end
```

### Notification Messages
```lua
Config.Locales = {
    ['new_report_admin_announce'] = { 
        title = "Report System", 
        text = "New Report Some one needs help!", 
        type = "success" 
    },
    ['new_report_player_announce'] = { 
        title = "Report System", 
        text = "Report successfully sent to the STAFF!", 
        type = "announce"
    },
    -- ... other notification messages
}
```

## Report Types

The system supports three types of reports:
1. Player Reports
2. Bug Reports
3. Questions

## Admin Features

1. View all reports
2. Take screenshots
3. Teleport to players
4. Bring players
5. Spectate players
6. Chat with players
7. Close reports

## Player Features

1. Submit reports
2. Chat with admins
3. Cancel reports
4. View report status

## Best Practices

1. **API Keys**
   - Keep your Discord bot token and Steam API key secure
   - Never share these keys in public repositories
   - Regularly rotate keys for security

2. **Framework Selection**
   - Choose the correct framework for your server
   - Configure permissions according to your server's hierarchy
   - Test framework integration before deployment

3. **UI Customization**
   - Customize UI text to match your server's language
   - Adjust colors to match your server's theme
   - Test UI on different screen resolutions

4. **Screenshot System**
   - Test screenshot functionality before enabling
   - Ensure proper permissions for screenshot storage
   - Monitor storage usage for screenshots

5. **Admin Management**
   - Regularly update admin list when using SteamHEX
   - Review and update permission levels
   - Monitor admin actions for abuse

6. **Notification System**
   - Test notifications on different frameworks
   - Customize notification messages
   - Ensure notifications are visible but not intrusive

7. **Security**
   - Regularly update the script
   - Monitor for unauthorized access
   - Keep server information private

8. **Performance**
   - Monitor resource usage
   - Optimize screenshot storage
   - Clean up old reports periodically 