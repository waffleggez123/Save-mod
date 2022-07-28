
--Made by : https://v3rmillion.net/member.php?action=profile&uid=244024
-- init
local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/zxciaz/VenyxUI/main/Reuploaded"))() --someone reuploaded it so I put it in place of the original back up so guy can get free credit.
local venyx = library.new("Emerald Hub", 5013109572)

-- themes
local themes = {
Background = Color3.fromRGB(24, 24, 24),
Glow = Color3.fromRGB(0, 0, 0),
Accent = Color3.fromRGB(10, 10, 10),
LightContrast = Color3.fromRGB(20, 20, 20),
DarkContrast = Color3.fromRGB(14, 14, 14),  
TextColor = Color3.fromRGB(255, 255, 255)
}

-- first page
local page = venyx:addPage("Auto", 5012544693)
local section1 = page:addSection("Aoto Fram Money")
local section2 = page:addSection("Section 2")

section1:addToggle("Auto fram White Team", nil, function(value)
---white Team

local TweenService = game:GetService("TweenService")

local Tw = TweenService:Create(game.Players.LocalPlayer.Character.HumanoidRootPart, TweenInfo.new(2, Enum.EasingStyle.Linear, Enum.EasingDirection.Out,0,false,0),
{CFrame = CFrame.new(-54.20122528076172, 38.59809494018555, 38.39418029785156)}):Play()
_G.WARO = true
       wait(2)

local Tw = TweenService:Create(game.Players.LocalPlayer.Character.HumanoidRootPart, TweenInfo.new(15, Enum.EasingStyle.Linear, Enum.EasingDirection.Out,0,false,0),
{CFrame = CFrame.new(-146.6790008544922, 82.03258514404297, 8803.408203125)}):Play()
_G.WARO = true
       wait(14)

local Tw = TweenService:Create(game.Players.LocalPlayer.Character.HumanoidRootPart, TweenInfo.new(2, Enum.EasingStyle.Linear, Enum.EasingDirection.Out,0,false,0),
{CFrame = CFrame.new(-55.72788619995117, -360.4100646972656, 9489.38671875)}):Play()
end)

section1:addButton("Button", function()
print("Clicked")
end)
section1:addTextbox("Notification", "Default", function(value, focusLost)
print("Input", value)

if focusLost then
venyx:Notify("Title", value)
end
end)

section2:addKeybind("Toggle Keybind", Enum.KeyCode.RightControl, function()
print("Activated Keybind")
venyx:toggle()
end, function()
print("Changed Keybind")
end)
section2:addColorPicker("ColorPicker", Color3.fromRGB(50, 50, 50))
section2:addColorPicker("ColorPicker2")
section2:addSlider("Slider", 0, -100, 100, function(value)
print("Dragged", value)
end)
section2:addDropdown("Dropdown", {"Hello", "World", "Hello World", "Word", 1, 2, 3})
section2:addDropdown("Dropdown", {"Hello", "World", "Hello World", "Word", 1, 2, 3}, function(text)
   print("Selected", text)
end)
section2:addButton("Button")

-- second page
local theme = venyx:addPage("Theme", 5012544693)
local colors = theme:addSection("Colors")

for theme, color in pairs(themes) do -- all in one theme changer, i know, im cool
colors:addColorPicker(theme, color, function(color3)
venyx:setTheme(theme, color3)
end)
end

-- load
venyx:SelectPage(venyx.pages[1], true) -- no default for more freedom
