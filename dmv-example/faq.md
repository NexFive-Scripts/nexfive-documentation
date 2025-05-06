# FAQ

**1. What is the Ata DMV School System?**

The Ata DMV School System is a FiveM script that simulates a driving school experience, allowing players to obtain various vehicle licenses through theory and practical exams.

***

**2. How do I install the Ata DMV School System?**

1. Place the `ata_dmvschool_v2` folder in your server's `resources` directory.
2. Add `ensure ata_core` and `ensure ata_dmvschool_v2`  to your `server.cfg`.
3. Configure the `config.lua` file to suit your server's needs.
4. Restart your server.

***

**3. What licenses can players obtain?**

Players can obtain licenses for driving cars, bikes, planes, boats, and trucks. Each license has a theory and practical component.

***

**4. How do I give a player a license?**

Use the `GiveLicenseToPlayer` export function. For example, in ESX:

```lua
ESX.RegisterServerCallback('esx_dmvschool:giveTruckLicense', function(source, cb)
    local success = exports['ata_dmvschool_v2']:GiveLicenseToPlayer(source, 'truck')
    cb(success)
end)
```

***

**5. How can I check if a player has a specific license?**

Use the `CheckLicense` export function. For example, in QBCore:

```lua
QBCore.Functions.CreateCallback('qb-policejob:checkBoatLicense', function(source, cb)
    local hasLicense = exports['ata_dmvschool_v2']:CheckLicense(source, 'boat')
    cb(hasLicense)
end)
```

***

**6. Can I remove a license from a player?**

Yes, use the `RemoveLicenseFromPlayer` export function. For example, in ESX:

```lua
ESX.RegisterServerCallback('esx_policejob:revokeLicense', function(source, cb, target, license)
    local success = exports['ata_dmvschool_v2']:RemoveLicenseFromPlayer(target, license)
    cb(success)
end)
```

***

**7. How do I customize the exam questions?**

Edit the question files (e.g., `questions/driver.lua or questions/truck.lua`) to add or modify questions. Ensure each question has a `question`, `a`, `b`, `c`, and `correct` field.

***

**8. What happens if a player fails an exam?**

Players can retake exams. The script can be configured to allow multiple attempts and set cooldown periods between attempts.

***

**9. How do I change the language of the script?**

Modify the `locale.lua` file to change text strings. You can add new languages by creating additional entries in the `Locale` table

