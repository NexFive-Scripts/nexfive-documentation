# FAQ

## General Questions

### What is NF_ReportSystem?
NF_ReportSystem is a comprehensive reporting solution for FiveM servers that allows players to submit and manage reports efficiently. It helps server administrators maintain order and address player concerns promptly.

### Which frameworks are supported?
The script currently supports both ESX and QBCore frameworks.

### Do I need any dependencies?
Yes, the script requires:
- ESX Framework or QBCore
- ox_lib
- ox_target
- ox_inventory (optional)

## Installation

### How do I install the script?
1. Download the resource from our store
2. Place the `NF_ReportSystem` folder in your server's resources directory
3. Add `ensure NF_ReportSystem` to your server.cfg
4. Configure the settings in the config file
5. Restart your server

### Do I need to set up a database?
No, the script will automatically create the necessary database tables on first run.

## Configuration

### How do I add custom report categories?
You can add categories in the config file:
```lua
Config.Categories = {
    your_category = {
        label = 'Your Category',
        color = '#your_color',
        priority = 1
    }
}
```

### How do I change the report limits?
You can modify the limits in the config file:
```lua
Config.MaxReports = 5 -- Maximum active reports per player
Config.ReportCooldown = 300 -- Cooldown between reports
```

### Can I customize the UI?
Yes, you can customize the UI in the config file:
```lua
Config.UI = {
    primaryColor = '#your_color',
    secondaryColor = '#your_color',
    font = 'your_font',
    fontSize = 14
}
```

## Usage

### How do players submit reports?
Players can submit reports by:
1. Using the `/report` command
2. Selecting a category
3. Entering a description
4. Submitting the report

### What happens when a report is submitted?
1. The report is saved to the database
2. Admins receive a notification
3. The report appears in the admin panel
4. The player receives a confirmation

### How do admins manage reports?
Admins can use the following commands:
- `/reports` - View all reports
- `/closereport [id] [reason]` - Close a report
- `/respondreport [id] [message]` - Respond to a report

## Troubleshooting

### The script isn't working after installation
1. Check if all dependencies are installed
2. Verify the resource is started in server.cfg
3. Check the server console for errors
4. Ensure the config file is properly configured

### Players can't submit reports
1. Check if the player has the required permissions
2. Verify the report cooldown hasn't expired
3. Check if the player has reached the report limit
4. Ensure the database is properly set up

### Reports aren't showing in the admin panel
1. Check if the admin has the required permissions
2. Verify the database connection
3. Check for any JavaScript errors in the console
4. Ensure the UI is properly configured

## Support

### Where can I get help?
You can get support through:
- Our Discord server
- The script's store page
- Our support ticket system

### How do I report bugs?
Please report bugs through:
1. Our Discord server
2. The script's GitHub issues page
3. Our support ticket system

Include the following information:
- Server logs
- Steps to reproduce
- Expected behavior
- Actual behavior
- Screenshots or videos if possible

## Best Practices

### For Server Owners
1. Regularly review and update report categories
2. Set appropriate cooldown times
3. Configure auto-close settings
4. Monitor report volume
5. Train admins on report management

### For Players
1. Use appropriate categories
2. Provide detailed descriptions
3. Be patient for responses
4. Follow up if needed
5. Report only relevant issues

### For Admins
1. Respond to reports promptly
2. Use appropriate status updates
3. Provide clear responses
4. Follow up on resolved issues
5. Maintain professional communication 