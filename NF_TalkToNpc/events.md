# Events

#### Client Events

| Event                        | Description                |
| ---------------------------- | -------------------------- |
| `NF_talktonpc:addChat`      | Add message to chat        |
| `NF_talktonpc:buyItems`     | Open buy menu              |
| `NF_talktonpc:sellItems`    | Open sell menu             |
| `NF_talktonpc:interact`     | Start interaction with NPC |
| `NF_talktonpc:closeUI`      | Close dialogue UI          |
| `NF_talktonpc:notification` | Display notification       |

#### Server Events

| Event               | Description                 |
| ------------------- | --------------------------- |
| `buyitemsCash`      | Buy items with cash         |
| `buyitemsBank`      | Buy items with bank money   |
| `sellitemsCash`     | Sell items for cash         |
| `sellitemsBank`     | Sell items for bank deposit |
| `getInventoryItems` | Get player inventory list   |

### Custom Events

You can create custom events to extend functionality:

```lua
RegisterNetEvent('custom:event')
AddEventHandler('custom:event', function()
    TriggerEvent('NF_talktonpc:addChat', "text", 'Message text')
    Wait(1000)
    -- Custom code
    TriggerEvent('NF_talktonpc:closeUI')
end)
```
