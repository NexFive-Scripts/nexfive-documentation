# NF-Shop

A comprehensive shop system for FiveM servers with advanced features including shop ownership, robbery mechanics, and inventory management.

## Features

### Core Features
- Multiple shop types support
- Shop ownership system
- Advanced inventory integration
- Customizable shop appearances
- Post box delivery system
- Shop robbery mechanics
- Boss management system
- Sales tracking and analytics

### Shop Management
- Create and manage different shop types
- Customize shop appearances with themes
- Set shop prices and inventory
- Track sales and profits
- Manage shop ownership
- Withdraw shop balance

### Robbery System
- Dynamic robbery mechanics
- Police notification system
- Cash register theft
- Safe cracking mechanics
- Reward system
- Cooldown periods

### Post Box System
- Order items for delivery
- Vehicle delivery mechanics
- Delivery tracking
- Cooldown system
- Custom delivery locations

## Dependencies

- ESX or QBCore Framework
- One of the following inventory systems:
  - ox_inventory
  - qb-inventory
  - qs-inventory
  - esx_inventory
- One of the following SQL systems:
  - oxmysql
  - ghmattimysql
  - mysql-async

## Installation

1. Download the resource
2. Place it in your server's resources folder
3. Import the SQL file to your database
4. Add the following to your server.cfg:
```cfg
ensure NF-Shop
```

## Configuration

### Framework Setup
```lua
Config.Framework = "esx" -- or "qb-core"
```

### Inventory System
```lua
Config.inventory = "ox_inventory" -- or "qb_inventory", "qs_inventory", "esx_inventory"
```

### SQL Configuration
```lua
Config.SQL = "oxmysql" -- or "ghmattimysql", "mysql-async"
```

### Shop Types
You can create different types of shops with unique:
- Backgrounds
- Color themes
- Item inventories
- Prices
- Special events

### Robbery Configuration
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

### Post Box System
```lua
Config.PostBoxSpawnRadius = 100 -- Radius for post box vehicle spawn
Config.PostBoxCoolDown = 15 -- Cooldown in minutes
```

## Usage

### Creating a Shop
1. Use the `/openconfig` command
2. Navigate to "Shop Types"
3. Create a new shop type
4. Set up shop inventory and prices
5. Add the shop to the map

### Managing a Shop
1. Approach your owned shop
2. Use the target system to access:
   - Shop inventory
   - Boss menu
   - Shop settings

### Robbing a Shop
1. Visit the robbery boss
2. Select a shop to rob
3. Follow the robbery mechanics
4. Collect rewards

### Using Post Box
1. Access shop management
2. Order items
3. Wait for delivery
4. Collect items from delivery vehicle

## Database Structure

### Tables
- NF_shop_types
- NF_shops_active

### Required Fields
- Shop ID
- Owner information
- Inventory data
- Sales data
- Location data

## Support

For support, please:
1. Check the documentation
2. Review the configuration options
3. Contact support if needed

## License

This resource is licensed under the MIT License. See LICENSE file for details.

## Credits

Created by MiLaD 