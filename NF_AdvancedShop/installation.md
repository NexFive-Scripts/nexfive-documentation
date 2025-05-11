# NF-AdvancedShop Installation Guide

## Prerequisites
Before installing NF-AdvancedShop, ensure you have the following:

1. A working FiveM server
2. One of the supported frameworks:
   - ESX Framework
   - QBCore Framework
3. One of the supported inventory systems:
   - ox_inventory
   - qb-inventory
   - qs-inventory
   - esx_inventory
4. One of the supported SQL systems:
   - oxmysql
   - ghmattimysql
   - mysql-async
5. One of the supported target systems:
   - ox_target
   - qb-target
   - Default target

## Installation Steps

### 1. Download and Extract
1. Download the latest release from the GitHub repository
2. Extract the contents to your server's resources folder
3. Rename the folder to `NF-AdvancedShop` if it's not already named as such

### 2. Database Setup
1. Open your database management tool (e.g., HeidiSQL, phpMyAdmin)
2. Create a new database if you haven't already
3. Import the `sql.sql` file located in the `sql` folder
4. Verify that the following tables have been created:
   - `NF_shop_types`
   - `NF_shops_active`

### 3. Configuration
1. Navigate to the `config` folder
2. Open `config.lua` in your preferred text editor
3. Configure the following settings:
   ```lua
   Config.Framework = 'esx' -- or 'qbcore'
   Config.Inventory = 'ox_inventory' -- or your preferred inventory system
   Config.SQL = 'oxmysql' -- or your preferred SQL system
   Config.Target = 'ox_target' -- or your preferred target system
   ```
4. Adjust other settings according to your server's needs

### 4. Server Configuration
1. Open your `server.cfg`
2. Add the following line:
   ```cfg
   ensure NF-AdvancedShop
   ```
3. Make sure the resource is started after your framework and inventory system


### 5. Resource Verification
1. Start your server
2. Check the server console for any errors
3. Verify the resource is running with:
   ```
   /refresh
   /start NF-AdvancedShop
   ```

## Post-Installation

### Testing
1. In-game, use the following commands to verify installation:
   ```
   /openconfig -- Should open the configuration menu (if you have admin permissions)
   ```
2. Check if shops are spawning at their configured locations
3. Verify that the inventory system is working by purchasing items
4. Test the robbery system (if enabled)
5. Test the post box system (if enabled)

### Troubleshooting
If you encounter any issues:

1. Check the server console for error messages
2. Verify all dependencies are properly installed and running
3. Ensure the database tables are created correctly
4. Check file permissions in the resource folder
5. Verify your framework version is compatible

### Common Issues

#### Database Connection Errors
- Verify your database credentials in the framework configuration
- Check if the database server is running
- Ensure the database user has proper permissions

#### Resource Not Starting
- Check if all dependencies are started before NF-AdvancedShop
- Verify the resource name in server.cfg matches the folder name
- Check for any syntax errors in the configuration files

#### Inventory Integration Issues
- Verify the inventory system is properly configured
- Check if the inventory system is started before NF-AdvancedShop
- Ensure the item names match between the shop and inventory system

## Support
If you need additional help:

1. Check the documentation in the `docs` folder
2. Join our Discord server for community support

## Updates
To update the resource:

1. Backup your current configuration
2. Download the latest release
3. Replace the old files with the new ones
4. Keep your custom configuration
5. Restart the resource

---

*For additional support, please join our Discord server or create an issue on GitHub.* 