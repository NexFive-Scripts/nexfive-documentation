# Config File

The configuration file is located at `config.lua` in the resource folder. Here you can customize various aspects of the DMV School system.

## General Settings

```lua
Config = {}
Question = {}

Config.NPC = {
    {
        model = 'a_m_m_business_01',
        coords = vector3(240.632965, -1379.393433, 32.728149),
        heading = 136.06298,
        text = 'DRIVING SCHOOL',
        eventName = 'NexFive_Dmv:requestUI', 
        data = {},
        type = 'client',
        animation = 'idle',
        target = true,
    },
}

Config.Blip = {
    enabled = true,
    coords = vector3(241.041763, -1378.786865, 32.72814),
    name = 'DRIVING SCHOOL',
    icon = 225,
    color = 2,
    size = 1.0,
    display = 3,
}

Config.Marker = {
    ['color'] = {r = 255, g = 0, b = 0, a = 150},
    ['type'] = 2,
}


Config.MaxWarnings = 3
Config.TheoryPassingScore = 10
Config.PaymentMethod = 'bank'
Config.TheoryTimeLimit = 10
Config.Debug = true



Config.Exams = {
    driver = {
        Vehicle = "blista",
        speedLimit = 50,
        time = 15,
        spawnPoint = vector4(255.139, -1400.731, 29.537, 325.9),
        CheckPoints = {
            {   
                id = 1,
                position = {x = 255.139, y = -1400.731, z = 29.537},
                Action = function(playerPed, vehicle, setCurrentZoneType)
                    CreateCam(true, vector3(262.57525634766, -1383.0974121094, 34.531505584717), 233.79286193848)
                    FreezeEntityPosition(vehicle, true)
                    SpawnVehiclesForTestPark()
                    FreezeEntityPosition(vehicle, false)
                end
            },
            {
                id = 2,
                position = {x = 270.18594360352, y = -1388.6273193359, z = 30.578592300415},
                Action = function(playerPed, vehicle, setCurrentZoneType)
                    while true do
                        Citizen.Wait(500)
                        local vehicleCoords = GetEntityCoords(vehicle)
                        local heading = math.random(319,322)
                        
                        if math.floor(GetEntityHeading(vehicle)) == heading and #(vehicleCoords - vector3(270.0791015625, -1388.5401611328, 31.40558052063)) < 1 then
                            break
                        end
                    end
                    DrawMissionText(Locales['go_next_point'], 5000)
                    DeleteSpawnedVehicles()
                end
            },
            {
                id = 3,
                position = {x = 271.58572387695, y = -1370.9281005859, z = 30.933750152588},
                Action = function(playerPed, vehicle, setCurrentZoneType)
                    CreateThread(function()
                        FreezeEntityPosition(vehicle, true)
                        CreateCam(true, vector3(273.36325073242, -1360.9822998047, 35.935108184814), 321.11740112305)
                        Subtitle('~b~Driving Instructor: \n ~s~In the whole city, there are places to park which are marked with yellow and white lines', 7000)
                        Subtitle('~b~Driving Instructor: \n ~s~Just don\'t park on the line', 5000)
                        CreateCam(false)
                        FreezeEntityPosition(vehicle, false)
                    end)
                end
            },
            {
                id = 4,
                position = {x = 270.53625488281, y = -1356.0401611328, z = 30.935108184814},
                Action = function(playerPed, vehicle, setCurrentZoneType)
                    CreateThread(function()
                        Subtitle('~b~Driving Instructor: \n ~r~Follow the red line on the mini map', 5000)
                    end)
                end
            },
            {
                id = 5,
                position = {x = 252.13215637207, y = -1342.3446044922, z = 30.91828918457},
                Action = function(playerPed, vehicle, setCurrentZoneType)
                    CreateThread(function()
                        FreezeEntityPosition(vehicle, true)
                        CreateCam(true, vector3(240.10893249512, -1338.8238525391, 35.091156005859), 137.46362304688)
                        Subtitle('~b~Driving Instructor: \n ~s~Respecting pedestrians is one of the driving rules', 5000)
                        Subtitle('~b~Driving Instructor: \n ~s~Before crossing the special pedestrian crossing line\n look to the left and right', 7000)
                        CreateCam(true, vector3(235.82153320313, -1345.6762695313, 33.583976745605), 75.38468170166)
                        Wait(3000)
                        CreateCam(true, vector3(235.62078857422, -1345.5422363281, 33.582931518555), 187.1916809082)
                        CreateCam(false)
                        FreezeEntityPosition(vehicle, false)
                    end)
                end
            },
            {
                id = 6,
                position = {x = 226.54289245605, y = -1356.8919677734, z = 29.552942276001},
                Action = function(playerPed, vehicle, setCurrentZoneType)
                    DrawMissionText(Locales['go_next_point'], 5000)
                end
            },
            {
                id = 7,
                position = {x = 220.23495483398, y = -1376.1649169922, z = 29.558292388916},
                Action = function(playerPed, vehicle, setCurrentZoneType)
                    CreateThread(function()
                        FreezeEntityPosition(vehicle, true)
                        CreateCam(true, vector3(219.75506591797, -1379.4885253906, 35.547412872314), 50.816917419434)
                        Subtitle('~b~Driving Instructor: \n ~s~You have the right to park in places that are handicapped accessible', 5000)
                        CreateCam(false)
                        FreezeEntityPosition(vehicle, false)
                    end)
                end
            },
            {
                id = 8,
                position = {x = 228.04243469238, y = -1396.5788574219, z = 29.489122390747},
                Action = function(playerPed, vehicle, setCurrentZoneType)
                    DrawMissionText(Locales['go_next_point'], 5000)
                end
            },
            {
                id = 9,
                position = {x = 213.65875244141, y = -1412.9248046875, z = 28.136703491211},
                Action = function(playerPed, vehicle, setCurrentZoneType)
                    DrawMissionText(Locales['go_next_point'], 5000)
                end
            },
            {
                id = 10,
                position = {x = 186.28977966309, y = -1398.8898925781, z = 28.247911453247},
                Action = function(playerPed, vehicle, setCurrentZoneType)
                    CreateThread(function()
                        FreezeEntityPosition(vehicle, true)
                        CreateCam(true, vector3(185.6118927002, -1392.4379882813, 33.258993148804), 6.614758014679)
                        Subtitle('~b~Driving Instructor: \n ~s~You must have seen these lights', 5000)
                        Subtitle('~b~Driving Instructor: \n ~s~While driving, we should pay attention to these lights', 5000)
                        Subtitle('~b~Driving Instructor: \n ~s~Yes, yes, I know, but wait for me', 5000)
                        Subtitle('~b~Driving Instructor: \n ~g~Green ~s~means go, ~y~yellow ~s~means be careful and go if you are in the middle of the road, ~r~red ~s~means you have to stop', 5000)
                        CreateCam(false)
                        FreezeEntityPosition(vehicle, false)
                    end)
                end
            },
            {
                id = 11,
                position = {x = 185.6946105957, y = -1376.9666748047, z = 28.021179199219},
                Action = function(playerPed, vehicle, setCurrentZoneType)
                    DrawMissionText(Locales['go_next_point'], 5000)
                end
            },
            {
                id = 12,
                position = {x = 216.59298706055, y = -1332.3699951172, z = 28.052070617676},
                Action = function(playerPed, vehicle, setCurrentZoneType)
                    DrawMissionText(Locales['go_next_point'], 5000)
                end
            },
            {
                id = 13,
                position = {x = 271.43853759766, y = -1316.7668457031, z = 28.54705619812},
                Action = function(playerPed, vehicle, setCurrentZoneType)
                    DrawMissionText(Locales['go_next_point'], 5000)
                end
            },
            {
                id = 14,
                position = {x = 319.91387939453, y = -1326.5310058594, z = 30.892158508301},
                Action = function(playerPed, vehicle, setCurrentZoneType)
                    DrawMissionText(Locales['in_town_speed'], Config.Exams['driver'].speedLimit, 5000)
                end
            },
            {
                id = 15,
                position = {x = 310.79461669922, y = -1357.3802490234, z = 30.797695159912},
                Action = function(playerPed, vehicle, setCurrentZoneType)
                    DrawMissionText(Locales['gratz_stay_alert'], 5000)
                    PlaySound(-1, 'RACE_PLACED', 'HUD_AWARDS', false, 0, true)
                end
            },
            {
                id = 16,
                position = {x = 281.18450927734, y = -1377.6828613281, z = 30.694528579712},
                Action = function(playerPed, vehicle, setCurrentZoneType)
                    DeleteVehicle(vehicle)
                end
            }
        }
    },    
    bike = {
        Vehicle = "akuma",
        speedLimit = 40,
        time = 10,
        spawnPoint = vector4(-689.72, -1385.44, 4.5, 232.69),
        route = {
            { id = 1,  position  = vector3(-683.76, -1393.71, 3.35), radius = 5.0 },
            { id = 2,  position  = vector3(-703.36, -1421.01, 3.35), radius = 5.0 },
            { id = 3,  position  = vector3(-692.09, -1436.06, 3.35), radius = 5.0 },
            { id = 4,  position  = vector3(-691.06, -1453.65, 3.35), radius = 5.0 },
            { id = 5,  position  = vector3(-712.3, -1480.51, 3.35), radius = 5.0 },
            { id = 6,  position  = vector3(-728.94, -1476.91, 3.35), radius = 5.0 },
            { id = 7,  position  = vector3(-736.84, -1468.55, 3.35), radius = 5.0 },
            { id = 8,  position  = vector3(-746.13, -1460.2, 3.35), radius = 5.0 },
            { id = 9,  position  = vector3(-753.45, -1468.9, 3.35), radius = 5.0 },
            { id = 10, position = vector3(-745.21, -1476.77, 3.35), radius = 5.0 },
            { id = 11, position = vector3(-725.7, -1469.39, 3.35), radius = 5.0 },
            { id = 12, position = vector3(-705.18, -1444.01, 3.35), radius = 5.0 },
            { id = 13, position = vector3(-722.76, -1411.01, 3.35), radius = 5.0 },
            { id = 14, position = vector3(-741.76, -1419.77, 3.35), radius = 5.0 },
            { id = 15, position = vector3(-758.08, -1423.89, 3.35), radius = 5.0 },
            { id = 16, position = vector3(-766.62, -1432.75, 3.35), radius = 5.0 },
            { id = 17, position = vector3(-779.95, -1449.31, 3.35), radius = 5.0 },
            { id = 18, position = vector3(-788.88, -1471.09, 3.35), radius = 5.0 },
            { id = 19, position = vector3(-779.98, -1474.59, 3.35), radius = 5.0 },
            { id = 20, position = vector3(-710.11, -1428.04, 3.35), radius = 5.0 },
            { id = 21, position = vector3(-683.95, -1393.53, 3.35), radius = 5.0 },
        }    
    },    
    boat = {
        Vehicle = "dinghy",
        speedLimit = 80,
        time = 20,
        spawnPoint = vector4(-748.73, -1379.09, 1.12, 138.53),
        route = {
            { id = 1,  position = vector3(-808.31, -1450.92, -1.0), radius = 5.0 },
            { id = 2,  position = vector3(-839.81, -1527.52, -1.0), radius = 5.0 },
            { id = 3,  position = vector3(-914.08, -1575.32, -1.0), radius = 5.0 },
            { id = 4,  position = vector3(-931.71, -1661.91, -1.0), radius = 5.0 },
            { id = 5,  position = vector3(-1011.0, -1688.38, -1.0), radius = 5.0 },
            { id = 6,  position = vector3(-1029.86, -1768.2, -1.0), radius = 5.0 },
            { id = 7,  position = vector3(-1077.75, -1823.58, -1.0), radius = 5.0 },
            { id = 8,  position = vector3(-1181.43, -1844.83, -1.0), radius = 5.0 },
            { id = 9,  position = vector3(-1187.49, -1923.84, -1.0), radius = 5.0 },
            { id = 10, position = vector3(-1261.89, -1928.8, -1.0), radius = 5.0 },
            { id = 11, position = vector3(-1304.34, -1978.25, -1.0), radius = 5.0 },
            { id = 12, position = vector3(-1275.51, -2008.39, -1.0), radius = 5.0 },
            { id = 13, position = vector3(-1246.1, -1942.58, -1.0), radius = 5.0 },
            { id = 14, position = vector3(-900.33, -1592.99, -1.0), radius = 5.0 },
            { id = 15, position = vector3(-791.81, -1499.52, -1.0), radius = 5.0 },
        }    
    },    
    plane = {
        Vehicle = "havok",
        speedLimit = 500,
        time = 35,
        spawnPoint = vector4(-724.65, -1444.08, 5.59, 142.34),
        route = {
            { id = 1,  position = vector3(-731.9, -1451.63, 13.75), radius = 10.0 },
            { id = 2,  position = vector3(-823.69, -1538.18, 58.07), radius = 10.0 },
            { id = 3,  position = vector3(-1074.21, -1767.09, 113.65), radius = 10.0 },
            { id = 4,  position = vector3(-1316.95, -2439.21, 108.62), radius = 10.0 },
            { id = 5,  position = vector3(-1297.62, -2733.04, 97.39), radius = 10.0 },
            { id = 6,  position = vector3(-1146.99, -2865.09, 14.53), radius = 10.0 },
            { id = 7,  position = vector3(-1102.69, -2895.84, 28.21), radius = 10.0 },
            { id = 8,  position = vector3(-920.4, -2741.04, 129.21), radius = 10.0 },
            { id = 9,  position = vector3(-711.91, -2391.74, 158.64), radius = 10.0 },
            { id = 10, position = vector3(-514.04, -1900.27, 188.61), radius = 10.0 },
            { id = 11, position = vector3(-394.54, -1155.62, 196.15), radius = 10.0 },
            { id = 12, position = vector3(-208.17, -753.65, 257.22), radius = 10.0 },
            { id = 13, position = vector3(-16.22, -888.47, 310.6), radius = 10.0 },
            { id = 14, position = vector3(-179.28, -1054.1, 309.77), radius = 10.0 },
            { id = 15, position = vector3(-559.31, -1241.91, 154.17), radius = 10.0 },
            { id = 16, position = vector3(-745.89, -1468.48, 5.0), radius = 10.0 },
        }    
    },
    truck = {
        Vehicle = "phantom",
        speedLimit = 60,
        time = 30,
        spawnPoint = vector4(-701.54, -1379.51, 5.37, 322.25),
        route = {
            { id = 1,  position = vector3(-667.89, -1364.61, 9.15), radius = 5.0 },
            { id = 2,  position = vector3(-656.63, -1403.67, 9.66), radius = 5.0 },
            { id = 3,  position = vector3(-662.85, -1493.52, 9.84), radius = 5.0 },
            { id = 4,  position = vector3(-680.68, -1543.76, 13.77), radius = 5.0 },
            { id = 5,  position = vector3(-709.65, -1594.41, 20.27), radius = 5.0 },
            { id = 6,  position = vector3(-685.93, -1640.74, 23.41), radius = 5.0 },
            { id = 7,  position = vector3(-681.96, -1722.21, 24.2), radius = 5.0 },
            { id = 8,  position = vector3(-604.06, -1815.24, 22.36), radius = 5.0 },
            { id = 9,  position = vector3(-505.77, -1798.38, 21.09), radius = 5.0 },
            { id = 10, position = vector3(-430.39, -1772.2, 19.67), radius = 5.0 },
            { id = 11, position = vector3(-407.92, -1813.05, 20.41), radius = 5.0 },
            { id = 12, position = vector3(-495.67, -1875.84, 16.52), radius = 5.0 },
            { id = 13, position = vector3(-629.24, -1900.6, 30.26), radius = 5.0 },
            { id = 14, position = vector3(-597.08, -2010.03, 28.26), radius = 5.0 },
            { id = 15, position = vector3(-493.93, -2047.99, 26.31), radius = 5.0 },
            { id = 16, position = vector3(-288.32, -2126.38, 21.31), radius = 5.0 },
            { id = 17, position = vector3(-283.6, -2134.61, 20.93), radius = 5.0 },
            { id = 18, position = vector3(-299.75, -2138.8, 15.74), radius = 5.0 },
            { id = 19, position = vector3(-326.46, -2143.56, 9.4), radius = 5.0 },
            { id = 20, position = vector3(-435.76, -2153.93, 9.34), radius = 5.0 },
            { id = 21, position = vector3(-595.93, -2030.02, 5.28), radius = 5.0 },
            { id = 22, position = vector3(-790.12, -1978.87, 8.04), radius = 5.0 },
            { id = 23, position = vector3(-880.48, -2068.39, 7.89), radius = 5.0 },
            { id = 24, position = vector3(-953.72, -2142.04, 7.92), radius = 5.0 },
            { id = 25, position = vector3(-1008.4, -2101.1, 11.91), radius = 5.0 },
            { id = 26, position = vector3(-1002.39, -1867.94, 15.85), radius = 5.0 },
            { id = 27, position = vector3(-708.13, -1531.89, 12.05), radius = 5.0 },
            { id = 28, position = vector3(-642.92, -1437.0, 9.62), radius = 5.0 },
            { id = 29, position = vector3(-707.08, -1374.85, 4.29), radius = 5.0 },
        }
    }
}    

Config.DefaultLicense = {
    ['driver'] = {
        label = 'Car License',
        price = 150,
        theoryPrice = 600,
        expire = 365,
    },    
    ['bike'] = {
        label = 'Bike License',
        price = 250,
        theoryPrice = 150,
        expire = 365,
    },
    ['plane'] = {
        label = 'Plane License',
        price = 1200,
        theoryPrice = 5500,
        expire = 365,
    },     
    ['boat'] = {
        label = 'Boat License',
        price = 250,
        theoryPrice = 280,
        expire = 365,
    },    
    ['truck'] = {
        label = 'Truck License',
        price = 200,
        theoryPrice = 700,
        expire = 365,
    },     
}    

function Debug(text)
    if Config.Debug then
        print(text)
    end
end


```