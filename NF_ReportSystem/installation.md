# Installation

1. Download the resource from our store
2. Place the `NF_ReportSystem` folder in your server's resources directory
3. Add `ensure NF_ReportSystem` to your server.cfg
4. Configure the settings in the config file
5. Restart your server

## Dependencies

- ESX Framework or QBCore
- ox_lib
- ox_target
- ox_inventory (optional)

## Database

The script will automatically create the necessary database tables on first run. Make sure your database user has the required permissions.

## Permissions

Make sure to add the following permissions to your server:
- `report.submit` - For players to submit reports
- `report.view` - For players to view their own reports
- `report.admin` - For administrators to manage all reports
- `report.respond` - For administrators to respond to reports 