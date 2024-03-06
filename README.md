local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/therealzeek/cat/main/README.lua"))() --you can go into the github link and copy all of it and modify it for yourself.
local Window = Library:CreateWindow("unison.cc", Vector2.new(398, 310), Enum.KeyCode.P)

local AimingTab = Window:CreateTab("main")


local testSection = AimingTab:CreateSector("main", "left")  --you can  change the section code, for example "testsection" can be changed to "FunnyCoolSection" etc.

testSection:AddTextbox("Prediction", nil, function(State)

-- Function to change accommodation factor based on textbox input
local function changeAccommodationFactor(value)
    getgenv().accomidationfactor = tonumber(value) or 0.123732
    print("Accommodation factor changed to:", getgenv().accomidationfactor)
end

-- Remove the existing textbox
testSection:RemoveTextbox("Prediction")

-- Add a new textbox for input
testSection:AddTextbox("Prediction", nil, function(value)
    changeAccommodationFactor(value)
end)
end)

testSection:AddButton("Enable", function()
  loadstring(game:HttpGet('https://pastebin.com/raw/Ex8TLDm7'))()
end)

local miscTab = Window:CreateTab("msc")

local miscSection = miscTab:CreateSector("misc", "left")

miscSection:AddButton("rightclick", function()
  loadstring(game:HttpGet('https://raw.githubusercontent.com/BalligusapoTT/BalligusapoTT/main/Leftclickballi'))()
end)

miscSection:AddButton("qtool", function()
loadstring(game:HttpGet('https://pastebin.com/raw/RgWV4UFv'))()
end)

local ToggleBind = miscSection:AddToggle("Keybind w/Toggle", false, function(e)

end)

ToggleBind:AddKeybind()

AimingTab:CreateConfigSystem("right") --this is the config system

loadstring(game:HttpGet("https://raw.githubusercontent.com/therealzeek/unison/main/README.md", true))()
