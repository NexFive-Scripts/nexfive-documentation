# Config File

```lua

Config = {}
Question = {}

Config.Debug = false

Config.WarningCount = 3 -- warning count for the practical exam
Config.TheoryExamCurrentPercent = 10 -- current percent of theory exam for example 10% of the the question will be current answered
Config.MoneyRemoved = 'bank' -- cash or bank
Config.Language = 'en'
Config.TheoryExamTime = 10 -- 10 minutes

Config.Blip = {
    haveBlip = true,
    coords = vector3(-700.2, -1401.29, 4.5),
    name = 'DMV SCHOOL',
    sprite = 545,
    color = 30,
    scale = 0.8,
    display = 4,
}


Config.NPC = {
    {
        model = 'a_m_y_business_03',
        coords = vector3(-700.2, -1401.29, 4.5),
        heading = 146.73,
        text = 'DMV SCHOOL',
        eventName = 'ata_dmvschool_v2:openNui', 
        eventData = {},
        eventType = 'client',
        animation = 'guard',
        target = true,  ---  if false it will be text ui instead of target and if true it will be target (like qb-target and ox-target)
    },
}


Config.CheckPoint = {
    ['color'] = {r = 0, g = 255, b = 255, a = 100},
    ['type'] = 1,
}


-- Test configurations for practical exams
Config.Tests = {
    driver = {
        Vehicle = "sultan",
        speedLimit = 60,
        time = 10, --- minutes !! if you dont want to use timer just set it to 0
        VehicleSpawn = vector4(-701.54, -1379.48, 4.65, 320.73),
        Checkpoints = {
            { id = 1, coords = vector3(-666.7, -1365.1, 8.65), radius = 5.0 },
            { id = 2, coords = vector3(-656.19, -1391.79, 8.99), radius = 5.0 },
            { id = 3, coords = vector3(-677.3, -1462.19, 8.69), radius = 5.0 },
            { id = 4, coords = vector3(-841.57, -1694.67, 16.98), radius = 5.0 },
            { id = 5, coords = vector3(-1097.63, -1976.98, 11.49), radius = 5.0 },
            { id = 6, coords = vector3(-970.53, -2146.85, 7.24), radius = 5.0 },
            { id = 7, coords = vector3(-888.35, -2085.32, 7.36), radius = 5.0 },
            { id = 8, coords = vector3(-628.87, -2004.28, 6.62), radius = 5.0 },
            { id = 9, coords = vector3(-369.17, -2153.77, 8.7), radius = 5.0 },
            { id = 10, coords = vector3(-269.15, -2169.93, 8.55), radius = 5.0 },
            { id = 11, coords = vector3(-157.07, -2152.02, 15.09), radius = 5.0 },
            { id = 12, coords = vector3(-30.87, -2106.26, 15.1), radius = 5.0 },
            { id = 13, coords = vector3(-29.55, -2084.55, 15.1), radius = 5.0 },
            { id = 14, coords = vector3(-162.67, -2127.85, 15.1), radius = 5.0 },
            { id = 15, coords = vector3(-170.77, -2152.18, 15.1), radius = 5.0 },
            { id = 16, coords = vector3(-274.41, -2169.39, 8.58), radius = 5.0 },
            { id = 17, coords = vector3(-257.34, -2200.15, 8.68), radius = 5.0 },
            { id = 18, coords = vector3(-4.27, -2120.4, 8.63), radius = 5.0 },
            { id = 19, coords = vector3(-141.5, -1927.87, 22.76), radius = 5.0 },
            { id = 20, coords = vector3(-238.76, -1844.36, 27.56), radius = 5.0 },
            { id = 21, coords = vector3(-277.08, -1820.24, 25.73), radius = 5.0 },
            { id = 22, coords = vector3(-363.99, -1814.18, 20.87), radius = 5.0 },
            { id = 23, coords = vector3(-394.58, -1779.77, 19.58), radius = 5.0 },
            { id = 24, coords = vector3(-424.37, -1765.13, 18.95), radius = 5.0 },
            { id = 25, coords = vector3(-693.11, -1610.05, 20.65), radius = 5.0 },
            { id = 26, coords = vector3(-645.15, -1482.63, 9.01), radius = 5.0 },
            { id = 27, coords = vector3(-639.34, -1370.43, 8.98), radius = 5.0 },
            { id = 28, coords = vector3(-708.01, -1376.38, 3.56), radius = 5.0 },
        }    
    },    
    bike = {
        Vehicle = "bati",
        speedLimit = 30,
        time = 15, --- minutes !! if you dont want to use timer just set it to 0
        VehicleSpawn = vector4(-689.72, -1385.44, 4.5, 232.69),
        Checkpoints = {
            { id = 1, coords = vector3(-683.76, -1393.71, 3.35), radius = 5.0 },
            { id = 2, coords = vector3(-703.36, -1421.01, 3.35), radius = 5.0 },
            { id = 3, coords = vector3(-692.09, -1436.06, 3.35), radius = 5.0 },
            { id = 4, coords = vector3(-691.06, -1453.65, 3.35), radius = 5.0 },
            { id = 5, coords = vector3(-712.3, -1480.51, 3.35), radius = 5.0 },
            { id = 6, coords = vector3(-728.94, -1476.91, 3.35), radius = 5.0 },
            { id = 7, coords = vector3(-736.84, -1468.55, 3.35), radius = 5.0 },
            { id = 8, coords = vector3(-746.13, -1460.2, 3.35), radius = 5.0 },
            { id = 9, coords = vector3(-753.45, -1468.9, 3.35), radius = 5.0 },
            { id = 10, coords = vector3(-745.21, -1476.77, 3.35), radius = 5.0 },
            { id = 11, coords = vector3(-725.7, -1469.39, 3.35), radius = 5.0 },
            { id = 12, coords = vector3(-705.18, -1444.01, 3.35), radius = 5.0 },
            { id = 13, coords = vector3(-722.76, -1411.01, 3.35), radius = 5.0 },
            { id = 14, coords = vector3(-741.76, -1419.77, 3.35), radius = 5.0 },
            { id = 15, coords = vector3(-758.08, -1423.89, 3.35), radius = 5.0 },
            { id = 16, coords = vector3(-766.62, -1432.75, 3.35), radius = 5.0 },
            { id = 17, coords = vector3(-779.95, -1449.31, 3.35), radius = 5.0 },
            { id = 18, coords = vector3(-788.88, -1471.09, 3.35), radius = 5.0 },
            { id = 19, coords = vector3(-779.98, -1474.59, 3.35), radius = 5.0 },
            { id = 20, coords = vector3(-710.11, -1428.04, 3.35), radius = 5.0 },
            { id = 21, coords = vector3(-683.95, -1393.53, 3.35), radius = 5.0 },

        }    
    },    
    boat = {
        Vehicle = "dinghy",
        speedLimit = 100,
        time = 15, --- minutes !! if you dont want to use timer just set it to 0
        VehicleSpawn = vector4(-748.73, -1379.09, 1.12, 138.53),
        Checkpoints = {
            { id = 1, coords = vector3(-808.31, -1450.92, -1.0), radius = 5.0 },
            { id = 2, coords = vector3(-839.81, -1527.52, -1.0), radius = 5.0 },
            { id = 3, coords = vector3(-914.08, -1575.32, -1.0), radius = 5.0 },
            { id = 4, coords = vector3(-931.71, -1661.91, -1.0), radius = 5.0 },
            { id = 5, coords = vector3(-1011.0, -1688.38, -1.0), radius = 5.0 },
            { id = 6, coords = vector3(-1029.86, -1768.2, -1.0), radius = 5.0 },
            { id = 7, coords = vector3(-1077.75, -1823.58, -1.0), radius = 5.0 },
            { id = 8, coords = vector3(-1181.43, -1844.83, -1.0), radius = 5.0 },
            { id = 9, coords = vector3(-1187.49, -1923.84, -1.0), radius = 5.0 },
            { id = 10, coords = vector3(-1261.89, -1928.8, -1.0), radius = 5.0 },
            { id = 11, coords = vector3(-1304.34, -1978.25, -1.0), radius = 5.0 },
            { id = 12, coords = vector3(-1275.51, -2008.39, -1.0), radius = 5.0 },
            { id = 13, coords = vector3(-1246.1, -1942.58, -1.0), radius = 5.0 },
            { id = 14, coords = vector3(-900.33, -1592.99, -1.0), radius = 5.0 },
            { id = 15, coords = vector3(-791.81, -1499.52, -1.0), radius = 5.0 },
        }    
    },    
    plane = {
        Vehicle = "havok",
        speedLimit = 600,
        time = 30, --- minutes !! if you dont want to use timer just set it to 0
        VehicleSpawn = vector4(-724.65, -1444.08, 5.59, 142.34),
        Checkpoints = {
            { id = 1, coords = vector3(-731.9, -1451.63, 13.75), radius = 10.0 },
            { id = 2, coords = vector3(-823.69, -1538.18, 58.07), radius = 10.0 },
            { id = 3, coords = vector3(-1074.21, -1767.09, 113.65), radius = 10.0 },
            { id = 4, coords = vector3(-1316.95, -2439.21, 108.62), radius = 10.0 },
            { id = 5, coords = vector3(-1297.62, -2733.04, 97.39), radius = 10.0 },
            { id = 6, coords = vector3(-1146.99, -2865.09, 14.53), radius = 10.0 },
            { id = 7, coords = vector3(-1102.69, -2895.84, 28.21), radius = 10.0 },
            { id = 8, coords = vector3(-920.4, -2741.04, 129.21), radius = 10.0 },
            { id = 9, coords = vector3(-711.91, -2391.74, 158.64), radius = 10.0 },
            { id = 10, coords = vector3(-514.04, -1900.27, 188.61), radius = 10.0 },
            { id = 11, coords = vector3(-394.54, -1155.62, 196.15), radius = 10.0 },
            { id = 12, coords = vector3(-208.17, -753.65, 257.22), radius = 10.0 },
            { id = 13, coords = vector3(-16.22, -888.47, 310.6), radius = 10.0 },
            { id = 14, coords = vector3(-179.28, -1054.1, 309.77), radius = 10.0 },
            { id = 15, coords = vector3(-559.31, -1241.91, 154.17), radius = 10.0 },
            { id = 16, coords = vector3(-745.89, -1468.48, 5.0), radius = 10.0 },
        }    
    },
    truck = {
        Vehicle = "phantom",
        speedLimit = 70,
        time = 25, --- minutes !! if you dont want to use timer just set it to 0
        VehicleSpawn = vector4(-701.54, -1379.51, 5.37, 322.25),
        Checkpoints = {
            { id = 1, coords = vector3(-667.89, -1364.61, 9.15), radius = 5.0 },
            { id = 2, coords = vector3(-656.63, -1403.67, 9.66), radius = 5.0 },
            { id = 3, coords = vector3(-662.85, -1493.52, 9.84), radius = 5.0 },
            { id = 4, coords = vector3(-680.68, -1543.76, 13.77), radius = 5.0 },
            { id = 5, coords = vector3(-709.65, -1594.41, 20.27), radius = 5.0 },
            { id = 6, coords = vector3(-685.93, -1640.74, 23.41), radius = 5.0 },
            { id = 7, coords = vector3(-681.96, -1722.21, 24.2), radius = 5.0 },
            { id = 8, coords = vector3(-604.06, -1815.24, 22.36), radius = 5.0 },
            { id = 9, coords = vector3(-505.77, -1798.38, 21.09), radius = 5.0 },
            { id = 10, coords = vector3(-430.39, -1772.2, 19.67), radius = 5.0 },
            { id = 11, coords = vector3(-407.92, -1813.05, 20.41), radius = 5.0 },
            { id = 12, coords = vector3(-495.67, -1875.84, 16.52), radius = 5.0 },
            { id = 13, coords = vector3(-629.24, -1900.6, 30.26), radius = 5.0 },
            { id = 14, coords = vector3(-597.08, -2010.03, 28.26), radius = 5.0 },
            { id = 15, coords = vector3(-493.93, -2047.99, 26.31), radius = 5.0 },
            { id = 16, coords = vector3(-288.32, -2126.38, 21.31), radius = 5.0 },
            { id = 17, coords = vector3(-283.6, -2134.61, 20.93), radius = 5.0 },
            { id = 18, coords = vector3(-299.75, -2138.8, 15.74), radius = 5.0 },
            { id = 19, coords = vector3(-326.46, -2143.56, 9.4), radius = 5.0 },
            { id = 20, coords = vector3(-435.76, -2153.93, 9.34), radius = 5.0 },
            { id = 21, coords = vector3(-595.93, -2030.02, 5.28), radius = 5.0 },
            { id = 22, coords = vector3(-790.12, -1978.87, 8.04), radius = 5.0 },
            { id = 23, coords = vector3(-880.48, -2068.39, 7.89), radius = 5.0 },
            { id = 24, coords = vector3(-953.72, -2142.04, 7.92), radius = 5.0 },
            { id = 25, coords = vector3(-1008.4, -2101.1, 11.91), radius = 5.0 },
            { id = 26, coords = vector3(-1002.39, -1867.94, 15.85), radius = 5.0 },
            { id = 27, coords = vector3(-708.13, -1531.89, 12.05), radius = 5.0 },
            { id = 28, coords = vector3(-642.92, -1437.0, 9.62), radius = 5.0 },
            { id = 29, coords = vector3(-707.08, -1374.85, 4.29), radius = 5.0 },
            
            
            
        }
    }
}    

Config.DefaultLicense = {
    [1] = {
        name = 'driver',
        label = Locale[Config.Language]['driver_license'],
        description = Locale[Config.Language]['driver_license_description'],
        img = './imgs/vehicles/4.png',
        price = 100,
        theoryPrice = 530,
        expire = 365, -- 365 days
    },    
    [2] = {
        name = 'bike',
        label = Locale[Config.Language]['bike_license'],
        description = Locale[Config.Language]['bike_license_description'],
        img = './imgs/vehicles/5.png',
        price = 200,
        theoryPrice = 130,
        expire = 365,
    },
    [3] = {
        name = 'plane',
        label = Locale[Config.Language]['plane_license'],
        description = Locale[Config.Language]['plane_license_description'],
        img = './imgs/vehicles/1.png',
        price = 1000,
        theoryPrice = 5000,
        expire = 365,
    },     
    [4] = {
        name = 'boat',
        label = Locale[Config.Language]['boat_license'],
        description = Locale[Config.Language]['boat_license_description'],
        img = './imgs/vehicles/3.png',
        price = 200,
        theoryPrice = 230,
        expire = 365,
    },    
    [5] = {
        name = 'truck',
        label = Locale[Config.Language]['truck_license'],
        description = Locale[Config.Language]['truck_license_description'],
        img = './imgs/vehicles/2.png',
        price = 150,
        theoryPrice = 600,
        expire = 365, -- 365 days
    },    
    [6] = {
        name = 'driver_theory',
        label = Locale[Config.Language]['drive_theory'],
        description = Locale[Config.Language]['drive_theory_description'],
    },    
    [7] = {
        name = 'bike_theory',
        label = Locale[Config.Language]['bike_theory'],
        description = Locale[Config.Language]['bike_theory_description'],
    },    
    [8] = {
        name = 'plane_theory',
        label = Locale[Config.Language]['plane_theory'],
        description = Locale[Config.Language]['plane_theory_description'],
    },    
    [9] = {
        name = 'boat_theory',
        label = Locale[Config.Language]['boat_theory'],
        description = Locale[Config.Language]['boat_theory_description'],
    },    
    [10] = {
        name = 'truck_theory',
        label = Locale[Config.Language]['truck_theory'],
        description = Locale[Config.Language]['truck_theory_description'],
    },    
}    



function Debug(text)
    if Config.Debug then
        print(text)
    end
end
```
