# Exports

{% hint style="warning" %}
ALL OF EXPORTS FOR SERVER SIDE (TO MORE SECURITY)
{% endhint %}

## Check License

```lua
exports['ata_dmvschool_v2']:CheckLicense(source, license) 
-- this exports just return TRUE or FALSE
```

{% tabs %}
{% tab title="ESX" %}
```javascript
ESX.RegisterServerCallback('esx_policejob:checkDriverLicense', function(source, cb)
    local hasLicense = exports['ata_dmvschool_v2']:CheckLicense(source, 'driver')
    cb(hasLicense)
end)
```
{% endtab %}

{% tab title="QBcore" %}
```python
QBCore.Functions.CreateCallback('qb-policejob:checkBoatLicense', function(source, cb)
    local hasLicense = exports['ata_dmvschool_v2']:CheckLicense(source, 'boat')
    cb(hasLicense)
end)
```
{% endtab %}
{% endtabs %}

***

## **Give License To Player**

```lua
exports['ata_dmvschool_v2']:GiveLicenseToPlayer(source, license)
-- this exports just give to a player a license
-- note this export don't need to give theory license to player (is automaticly)
```

{% tabs %}
{% tab title="ESX" %}
```javascript
ESX.RegisterServerCallback('esx_dmvschool:giveTruckLicense', function(source, cb)
    local success = exports['ata_dmvschool_v2']:GiveLicenseToPlayer(source, 'truck')
    cb(success)
end)
```
{% endtab %}

{% tab title="QBcore" %}
```lua
QBCore.Functions.CreateCallback('qb-dmvschool:giveBoatLicense', function(source, cb)
    local success = exports['ata_dmvschool_v2']:GiveLicenseToPlayer(source, 'boat')
    cb(success)
end)
```
{% endtab %}
{% endtabs %}

***

## **Remove License From Player**

```lua
exports['ata_dmvschool_v2']:RemoveLicenseFromPlayer(source, license)
-- this export just revoke a license from player
```

{% tabs %}
{% tab title="ESX" %}
```javascript
ESX.RegisterServerCallback('esx_policejob:revokeLicense', function(source, cb, target, license)
    local success = exports['ata_dmvschool_v2']:RemoveLicenseFromPlayer(target, license)
    cb(success)
end)
```
{% endtab %}

{% tab title="QBcore" %}
```lua
QBCore.Functions.CreateCallback('qb-policejob:revokeLicense', function(source, cb, target, license)
    local success = exports['ata_dmvschool_v2']:RemoveLicenseFromPlayer(target, license)
    cb(success)
end)
```
{% endtab %}
{% endtabs %}

***

## Check All License

```lua
exports['ata_dmvschool_v2']:CheckAllLicense(source)
-- this export just return all of license a player 
-- return e.g. {"driver","boat","truck"} 
-- or if don't have any license return {}
```

{% tabs %}
{% tab title="ESX" %}
```javascript
ESX.RegisterServerCallback('esx_policejob:getAllLicenses', function(source, cb, target)
    local licenses = exports['ata_dmvschool_v2']:CheckAllLicense(target)
    cb(licenses)
end)
```
{% endtab %}

{% tab title="QBcore" %}
```lua
QBCore.Functions.CreateCallback('qb-policejob:getAllLicenses', function(source, cb, target)
    local licenses = exports['ata_dmvschool_v2']:CheckAllLicense(target)
    cb(licenses)
end)
```
{% endtab %}
{% endtabs %}

