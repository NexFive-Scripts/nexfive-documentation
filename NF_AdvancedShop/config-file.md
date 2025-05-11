```lua

Config = {}

Config.SQL = 'oxmysql' --   mysql-async -- oxmysql -- ghmattimysql  -- pls fxmanifest and open requirement

Config.Framework = 'qb-core' -- esx / qb-core

Config.inventory = 'qb_inventory' -- ox_inventory -- qb_inventory -- qs_inventory -- esx_inventory

Config.inventoryPath = 'nui://qb-inventory/html/images/' -- ox_inventory: nui://ox_inventory/web/images/ -- qb-inventory: nui://qb-inventory/html/images/

Config.Target = "qb-target" -- ox_target -- qb-target -- default

Config.userprogress = false -- if you set true, download latest version from here: https://github.com/Mobius1/rprogress

Config.displayShopOwnerName = true

Config.PostBoxCoolDown = 30 -- time per minutes, for example : Config.PostBoxCoolDown = 30, can`t request a PostBox for up to 30 minutes after requesting it.

Config.PostBoxSpawnRadius = 100 -- 

Config.Debug = false 

Config.Framework_perms = { --You can choose multiple permission group to have access to use the config UI.
  	['admin'] = true,
    ['headadmin'] = true,
    ['owner'] = true,
}

Config.Robbery = {
    ['BossSpawn'] = { ped = "cs_lestercrest", Pos = {x = 705.38, y = -964.12, z = 30.4, h = 244.71} },
    CopsNeed = 1, -- cops need for start rob
    price = 5000, -- price for start robbery
}

Config.Notification = {
  ["add_type"] =                   { text = "Type successfully added, Now You can Create New Shop", type = "success" },
  ["edit_type"] =                  { text = "success save Changes [typename] Type", type = "success" },
  ["delete_type"] =                { text = "success Deleted [Typename] Type", type = "success" },
  ["add_shop"] =                   { text = "success Create a Shop", type = "success" },
  ["edit_shop"] =                  { text = "success save Changes [shopName] Shop", type = "success" },
  ["delete_shop"] =                { text = "success Deleted Active Shop: [shopName]", type = "success" },
  ["withdraw_balance"] =           { text = "withdraw Balance amount : amount", type = "success" },
  ["buy_shop"] =                   { text = "successfully Buyed [name] Shop", type = "success" },
  ["save_boss_action"] =           { text = "successfully save Changes Shop Settings", type = "success" },
  ["money"] =                      { text = "You don't have enough money", type = "error" },
  ["postbox_request"] =            { text = "The PostBox is on the way.", type = "success" },
  ["postbox_cooldown"] =           { text = "PostBox is CollDown, You Can request every 15min", type = "error" },
  ["robbery_pickup_cash"] =        { text = "Cash ready to be picked up", type = "success" },
  ["robbery_notify_for_police"] =  { text = "Someone took out a gun in the store", type = "warning" },
  ["robbery_far"] =                { text = "You've run too far", type = "error" },
  ["shop_not_found"] =             { text = "Not Found Shop For Start robbery", type = "error" },
  ["cant_add_item"] =              { text = "Not enough weight available", type = "error" },
}

Config.UI = {
  ["Add_To_Basket"] = "Add To Basket",
  ["Not_Available!"] = "Not Available!",
  ["BASKET"] = "BASKET",
  ["Set_Color_Range"] = "Set Color Range",
  ["BUY"] = "BUY",
  ["Done"] = "Done",
  ["Items"] = "Items",
  ["Do_you_want_to_buy_this_store"] = "Do you want to buy this store?",
  ["Store_Settings"] = "Store Settings",
  ["Post_Box"] = "Post Box",
  ["Shop_Management"] = "Shop Management",
  ["Sales_profit"] = "Sales profit",
  ["sell_factor"] = "sell factor",
  ["img"] = "img",
  ["Name"] = "Name",
  ["sold_Count"] = "sold Count",
  ["sold_income"] = "sold income",
  ["Total_income"] = "Total income",
  ["Shop_Sell"] = "Shop Sell",
  ["Shop_Name"] = "Shop Name",
  ["SHOP_INVENTORY"] = "SHOP INVENTORY",
  ["Shop_Balance"] = "Shop Balance",
  ["Withdraw"] = "Withdraw",
  ["Save_Changes"] = "Save Changes",
  ["Limited_Inventory"] = "Limited Inventory!",
  ["Shop_Types"] = "Shop Types",
  ["Active_Shops"] = "Active Shops",
  ["Add_Type"] = "Add Type",
  ["Custom_BG"] = "Custom BG",
  ["Preview_Change_Theme"] = "Preview & Change Theme",
  ["Categories"] = "Categories",
  ["Max_In_Shop"] = "Max In Shop",
  ["Sell_Price"] = "Sell Price",
  ["Order_Price"] = "Order Price",
  ["Add_New"] = "Add New",
  ["Item_Image"] = "Item Image",
  ["Enter_Category"] = "Enter Category",
  ["Type"] = "Type",
  ["TP_To_Shop"] = "TP To Shop",
  ["Standing_ped_coord"] = "Standing ped coord",
  ["Buy_Marker"] = "Buy Marker",
  ["Ped_Type"] = "Ped Type",
  ["Active_Robbery"] = "Active Robbery",
  ["Shop_For_Sell"] = "Shop For Sell",
  ["postboxCoords"] = "postboxCoords",
  ["Set_Coords"]  = "Set Coords",
  ["deliver_post_box_items"]  = "for deliver post box items",
  ["owner"]  = "Owner:",
  ["open_boss_action"]  = "Open Boss Action",
  ["buy_shop"]  = "Buy Shop",
  ["open_shop"]  = "Open Shop",
  ["Set_Location"]  = "Press E To Set Location",
  ["start_rob"]  = "To start a job on shop robbery, press",
  ["get_postbox"]  = "to get the package Press",
  ["rob_help"]  = "Hello, how can I help you?",
  ["already_opening"]  = "I'm already opening",
  ["take_money"]  = "To take the money, press",
  ["cassette"]  = "To rob a cassette",
  ["open_shop_E"]  = "Press [E] To Open Shop",

}

```