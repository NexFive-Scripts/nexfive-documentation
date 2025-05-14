# Configuration

#### NPC Dialogue Options

You can configure different types of dialogue options:

```lua
options = {
    -- Simple buy option
    {text = "I want to buy items", event = "NF_talktonpc:buyItems", serverSide = false},

    -- Simple sell option
    {text = "I want to sell items", event = "NF_talktonpc:sellItems", serverSide = false},

    -- Notification option
    {text = "Show notification", serverSide = false, event = "ataTalkToNpc:notification",
    args = {title = "Notification", message = "Message text", options = "Button text",
    icon = "fas fa-university", Clickevent = "custom:event"}},

    -- Dialogue option with follow-up conversation tree
    {
        text = "Tell me about your services",
        event = "NF_talktonpc:addChat",
        serverSide = false,
        args = {"text", "We offer various services. What would you like to know?"},
        followUp = {
            {
                text = "Tell me about option 1",
                event = "NF_talktonpc:addChat",
                serverSide = false,
                args = {"text", "Option 1 information..."},
                followUp = {
                    {
                        text = "More details about option 1",
                        event = "NF_talktonpc:addChat",
                        serverSide = false,
                        args = {"text", "Here are more details about option 1..."}
                    }
                }
            },
            {
                text = "Tell me about option 2",
                event = "NF_talktonpc:addChat",
                serverSide = false,
                args = {"text", "Option 2 information..."}
            }
        }
    }
}
```

#### Job Restrictions

You can restrict NPC access to specific jobs:

```lua
jobs = {
    'police',
    'ambulance',
    'mechanic'
},
```

An empty table `jobs = {}` allows access to everyone.
