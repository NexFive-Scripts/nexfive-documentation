# NF_ReportSystem Configuration

This document outlines the configuration options available for the NF_ReportSystem.

## Basic Settings

```lua
Config = {}

-- Command Settings
Config.ReportCommand = 'report' -- Command for players to submit reports
Config.ReportAdminCommand = 'reports' -- Command for admins to view reports

-- Framework Settings
Config.Framework = 'esx' -- Options: 'esx', 'qbcore', 'vrp', 'ace', 'custom', 'SteamHEX'
Config.Framework_perms = {
    ['admin'] = true,
    ['headadmin'] = true,
    ['owner'] = true,
    ['headhelper'] = false,
    ['helper'] = false,
    ['user'] = false,
}

-- Admin List (for SteamHEX framework)
Config.AdminList = {
    'steam:11000013cb8b8ba',
}

-- UI Settings
Config.mainColor = "#0a58ca" -- Main color for UI elements

-- Screenshot Settings
Config.ScreenshotBasic = true -- Enable/disable screenshot functionality

-- API Keys
Config.Bot_Token = 'YOUR_DISCORD_BOT_TOKEN' -- Discord bot token for avatars
Config.SteamApiKey = 'YOUR_STEAM_API_KEY' -- Steam API key for avatars

-- Server Information
Config.BotName = 'Test' -- Bot name
Config.ServerName = 'Test' -- Server name
Config.IconURL = "" -- Server icon URL
```

## Notification System

```lua
Config.Notify = function(title, message, time, types, svside, id)
    if svside then
        TriggerClientEvent('NF_ReportSystem:Notify', id, title, message, time, types)
    else 
        TriggerEvent('NF_ReportSystem:Notify', title, message, time, types)
    end
end
```

## Localization

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
    -- ... other locale entries
}
```

## UI Text

```lua
Config.UI = {
    ["Press_For_Back"] = "Press For Back",
    ["Report_System"] = "Report System",
    ["PLAYER"] = "PLAYER",
    ["PLAYER_Desc"] = "Lorem ipsum dolor sit amet consectetur adipisicing elit.",
    -- ... other UI text entries
}
```

## Features

1. **Report Types**:
   - Player Reports
   - Bug Reports
   - Questions

2. **Admin Features**:
   - View all reports
   - Take screenshots
   - Teleport to players
   - Bring players
   - Spectate players
   - Chat with players
   - Close reports

3. **Player Features**:
   - Submit reports
   - Chat with admins
   - Cancel reports
   - View report status

4. **Framework Support**:
   - ESX
   - QBCore
   - vRP
   - ACE
   - Custom
   - SteamHEX

## Best Practices

1. Always keep your API keys secure and never share them
2. Regularly update the admin list when using SteamHEX framework
3. Customize the UI text to match your server's language
4. Adjust notification settings based on your server's needs
5. Test the screenshot functionality before enabling it in production 