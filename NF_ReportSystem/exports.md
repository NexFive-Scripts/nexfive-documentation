# NF_ReportSystem Exports and Events

This document outlines the available exports and events in the NF_ReportSystem.

## Client Events

### Report Submission
```lua
TriggerEvent("NF_ReportSystem:NewReport", {
    title = "Report Title",
    desc = "Report Description",
    type = "PLAYER", -- or "BUG" or "QUESTION"
    playerId = targetPlayerId -- Required for player reports
})
```

### Report Management
```lua
-- View reports (admin only)
TriggerEvent("NF_ReportSystem:SyncReportsTable")

-- Take screenshot of target player
TriggerEvent("NF_ReportSystem:takeScreenShot", targetPlayerId, reportId)

-- Send chat message to report
TriggerEvent("NF_ReportSystem:chatmsg2", message, imageUrl)

-- Cancel report
TriggerEvent("NF_ReportSystem:ReportCancel", reportId)
```

## Server Events

### Report Handling
```lua
-- New report received
RegisterNetEvent("NF_ReportSystem:NewReport")
AddEventHandler("NF_ReportSystem:NewReport", function(data)
    -- data contains: title, desc, type, playerId
end)

-- Sync reports table
RegisterNetEvent("NF_ReportSystem:SyncReportsTable")
AddEventHandler("NF_ReportSystem:SyncReportsTable", function()
    -- Returns ReportList and staff status
end)

-- Chat messages
RegisterNetEvent("NF_ReportSystem:chatmsg")
AddEventHandler("NF_ReportSystem:chatmsg", function(msg, reportid)
    -- Admin chat message
end)

RegisterNetEvent("NF_ReportSystem:chatmsg2")
AddEventHandler("NF_ReportSystem:chatmsg2", function(msg, img)
    -- Player chat message
end)
```

### Admin Actions
```lua
-- Check report
RegisterNetEvent("NF_ReportSystem:checkingReport")
AddEventHandler("NF_ReportSystem:checkingReport", function(id)
    -- Set report status to "Checking"
end)

-- Set report to waiting
RegisterNetEvent("NF_ReportSystem:waitingReport")
AddEventHandler("NF_ReportSystem:waitingReport", function(id)
    -- Set report status to "Waiting"
end)

-- Teleport to player
RegisterNetEvent("NF_ReportSystem:Goto")
AddEventHandler("NF_ReportSystem:Goto", function(reportid)
    -- Teleport admin to reporting player
end)

-- Spectate player
RegisterNetEvent("NF_ReportSystem:SpectRequest")
AddEventHandler("NF_ReportSystem:SpectRequest", function(reportid)
    -- Start spectating reporting player
end)

-- Bring player
RegisterNetEvent("NF_ReportSystem:Bring")
AddEventHandler("NF_ReportSystem:Bring", function(reportid)
    -- Teleport reporting player to admin
end)

-- Return to previous position
RegisterNetEvent("NF_ReportSystem:Goto-Back")
AddEventHandler("NF_ReportSystem:Goto-Back", function(reportid)
    -- Return admin to previous position
end)

RegisterNetEvent("NF_ReportSystem:Bring-Back")
AddEventHandler("NF_ReportSystem:Bring-Back", function(reportid)
    -- Return player to previous position
end)
```

## Report Structure

```lua
{
    id = number,
    playerid = number,
    title = string,
    desc = string,
    type = string,
    loc = vector3,
    targetid = number,
    playername = string,
    status = string, -- "Waiting", "Checking", "Solved"
    discord = string,
    identifier = string,
    steam = string,
    playerprofile = string,
    screenshot = string,
    chats = table,
    adminid = number,
    adminprofile = string,
    lastCoordsGoto = vector3,
    lastCoordsBring = vector3
}
```

## Example Usage

### Submitting a Report
```lua
-- Client side
TriggerEvent("NF_ReportSystem:NewReport", {
    title = "Player Report",
    desc = "Player is breaking rules",
    type = "PLAYER",
    playerId = 1
})
```

### Admin Checking Reports
```lua
-- Client side
TriggerEvent("NF_ReportSystem:SyncReportsTable")

-- Server side
RegisterNetEvent("NF_ReportSystem:checkingReport")
AddEventHandler("NF_ReportSystem:checkingReport", function(id)
    if staffs[source].isAdmin then
        -- Handle report checking
    end
end)
```

### Chat in Report
```lua
-- Admin chat
TriggerEvent("NF_ReportSystem:chatmsg", "Admin message", reportId)

-- Player chat
TriggerEvent("NF_ReportSystem:chatmsg2", "Player message", imageUrl)
```

## Best Practices

1. Always check admin permissions before handling admin events
2. Use appropriate report types for better organization
3. Handle errors gracefully when players are offline
4. Keep chat messages professional and relevant
5. Use screenshots when necessary for player reports 