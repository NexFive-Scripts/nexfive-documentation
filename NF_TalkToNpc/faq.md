# FAQ

#### How do I change the NPC animation?

In the `client.lua` file, modify the `animation type` parameter in the `CreateNPCWithKey` function:

```lua
local npc = exports['NF_core']:CreateNPCWithKey(
    v.npc,           -- NPC model
    v.coordinates,   -- Coordinates
    v.heading,       -- Heading
    v.textUI,        -- Interaction text
    'NF_talktonpc:interact', -- Event name
    v,               -- Data
    'client',        -- Event type
    'animation_type', -- Change this value
    true             -- Other settings
)
```

#### How do I enable/disable the target system?

In `Config.lua`, change `Config.NPCinteraction` to either `'target'` or `'default'`.

#### Can I set job restrictions?

Yes, in the `jobs` array you can add jobs that have access to the NPC. An empty array means everyone has access.

#### How do I create complex dialogues?

Use the `followUp` system in options to create multi-stage dialogues with different options. You can nest these as deep as needed for complex conversation trees.
