# NF-AdvancedShop Configuration Guide

## Basic Configuration

### Framework Selection
```lua
Config.Framework = "esx" -- Choose between "esx" or "qb-core"
```

### Inventory System
```lua
Config.inventory = "ox_inventory" -- Choose between:
-- "ox_inventory"
-- "qb_inventory"
-- "qs_inventory"
-- "esx_inventory"
```

### SQL Configuration
```lua
Config.SQL = "oxmysql" -- Choose between:
-- "oxmysql"
-- "ghmattimysql"
-- "mysql-async"
```

### Debug Mode
```lua
Config.Debug = false -- Set to true for debug information
```

## Shop Configuration

### Target System
```lua
Config.Target = "default" -- Choose between:
-- "default"
-- "ox_target"
-- "qb-target"
```

### Shop Display Settings
```lua
Config.displayShopOwnerName = true -- Display owner name above shop
```

### UI Configuration
```lua
Config.UI = {
    ["Add_To_Basket"] = "Add To Basket",
    ["Not_Available!"] = "Not Available!",
    ["BASKET"] = "BASKET",
    -- Add more UI strings as needed
}
```

### Notification System
```lua
Config.Notification = {
    ["add_type"] = { text = "Type successfully added", type = "success" },
    ["edit_type"] = { text = "Changes saved", type = "success" },
    -- Add more notification types
}
```

## Robbery System Configuration

### Basic Settings
```lua
Config.Robbery = {
    CopsNeed = 2, -- Minimum cops required
    price = 1000, -- Price to start robbery
    BossSpawn = {
        ped = "s_m_m_doctor_01",
        Pos = vector4(x, y, z, h)
    }
}
```

### Robbery Mechanics
```lua
Config.Robbery = {
    -- Add robbery-specific settings
    time_to_success = 30, -- Time in seconds
    defender = "police", -- Job that gets notified
    steal_from_shop_cashier = {
        active = true,
        coords = {
            -- Add cashier positions
        },
        random_reward_between = {
            min = 100,
            max = 500
        }
    }
}
```

## Post Box System Configuration

### Basic Settings
```lua
Config.PostBoxSpawnRadius = 100 -- Radius for vehicle spawn
Config.PostBoxCoolDown = 15 -- Cooldown in minutes
```

### Vehicle Settings
```lua
Config.PostBox = {
    vehicle = "boxville2",
    driver = "csb_prologuedriver"
}
```

## Shop Types Configuration

### Creating a Shop Type
```lua
-- Example shop type structure
{
    name = "General Store",
    customBackground = false,
    backgroundLink = "",
    TriggerEvent = "",
    colorDeg = "45deg",
    bgLink = "",
    items = {
        {
            name = "bread",
            count = "10",
            max_in_shop = "50",
            sell_price = "5",
            order_price = "3",
            img = "bread.png"
        }
        -- Add more items
    }
}
```

## Database Configuration

### Required Tables

#### NF_shop_types
```sql
CREATE TABLE IF NOT EXISTS `NF_shop_types` (
    `id` int(11) NOT NULL AUTO_INCREMENT,
    `name` varchar(50) NOT NULL,
    `customBackground` tinyint(1) NOT NULL,
    `backgroundLink` text,
    `TriggerEvent` text,
    `colorDeg` varchar(50),
    `bgLink` text,
    `items` text,
    PRIMARY KEY (`id`)
);
```

#### NF_shops_active
```sql
CREATE TABLE IF NOT EXISTS `NF_shops_active` (
    `id` int(11) NOT NULL AUTO_INCREMENT,
    `owner` varchar(50),
    `owner_name` varchar(50),
    `type` varchar(50),
    `ped_type` varchar(50),
    `buy_marker` text,
    `shop_for_sell` tinyint(1),
    `name` varchar(50),
    `robbery` text,
    `standing_ped_coord` text,
    `shop_price` int(11),
    `salesProfit` int(11),
    `chartData` text,
    `items` text,
    `balance` int(11),
    `postboxcoords` text,
    PRIMARY KEY (`id`)
);
```

## Advanced Configuration

### Custom Events
```lua
-- Add custom events for shop interactions
Config.CustomEvents = {
    onShopPurchase = "custom:onShopPurchase",
    onShopRobbery = "custom:onShopRobbery"
}
```

### Permission System
```lua
Config.Framework_perms = {
    ["admin"] = true,
    ["superadmin"] = true
}
```

## Troubleshooting

### Common Issues

1. **Inventory Not Working**
   - Check if the correct inventory system is selected
   - Verify inventory exports are available
   - Check item names match your inventory system

2. **Database Errors**
   - Verify SQL configuration
   - Check table structure
   - Ensure proper permissions

3. **Framework Issues**
   - Verify framework selection
   - Check framework exports
   - Ensure proper initialization

### Debug Mode

Enable debug mode for detailed logging:
```lua
Config.Debug = true
```

## Performance Optimization

### Recommended Settings
```lua
Config.Optimization = {
    updateInterval = 1000, -- Update interval in ms
    maxShops = 50, -- Maximum number of shops
    cacheTimeout = 300 -- Cache timeout in seconds
}
```

## Security Considerations

1. Always validate user input
2. Use proper permission checks
3. Implement rate limiting
4. Secure database queries
5. Validate item transactions

## Support

For additional support:
1. Check the documentation
2. Review error logs
3. Contact support with:
   - Error messages
   - Configuration details
   - Steps to reproduce 