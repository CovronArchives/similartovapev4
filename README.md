Lets get to the point, no yapping.
# make an custom theme
```lua
_G.CustomTheme = {
    -- Tab Settings
    Tab_Color = Color3.fromRGB(255, 255, 255), -- Background color for the tab
    Tab_Text_Color = Color3.fromRGB(0, 0, 0), -- Text color for the tab

    -- Description Settings
    Description_Color = Color3.fromRGB(255, 255, 255), -- Background color for descriptions
    Description_Text_Color = Color3.fromRGB(0, 0, 0), -- Text color for descriptions

    -- Container Settings
    Container_Color = Color3.fromRGB(255, 255, 255), -- Background color for containers
    Container_Text_Color = Color3.fromRGB(0, 0, 0), -- Text color for containers

    -- Button Settings
    Button_Text_Color = Color3.fromRGB(0, 0, 0), -- Text color for buttons

    -- Toggle Settings
    Toggle_Box_Color = Color3.fromRGB(243, 243, 243), -- Background color of the toggle box
    Toggle_Inner_Color = Color3.fromRGB(94, 255, 180), -- Inner color of the toggle box
    Toggle_Text_Color = Color3.fromRGB(0, 0, 0), -- Text color for toggle labels
    Toggle_Border_Color = Color3.fromRGB(225, 225, 225), -- Border color for the toggle

    -- Slider Settings
    Slider_Bar_Color = Color3.fromRGB(243, 243, 243), -- Color of the slider bar
    Slider_Inner_Color = Color3.fromRGB(94, 255, 180), -- Color of the inner slider bar
    Slider_Text_Color = Color3.fromRGB(0, 0, 0), -- Text color for the slider
    Slider_Border_Color = Color3.fromRGB(255, 255, 255), -- Border color for the slider

    -- Dropdown Settings
    Dropdown_Text_Color = Color3.fromRGB(0, 0, 0), -- Text color for dropdown options
    Dropdown_Option_BorderSize = 1, -- Border size for dropdown options
    Dropdown_Option_BorderColor = Color3.fromRGB(235, 235, 235), -- Border color for dropdown options
    Dropdown_Option_Color = Color3.fromRGB(255, 255, 255), -- Background color for dropdown options
    Dropdown_Option_Text_Color = Color3.fromRGB(0, 0, 0) -- Text color for dropdown options
}
```
# library
```lua
local Library = loadstring(game:HttpGet("https://pastebin.com/raw/2xDTKdpV", true))()
```
# tab
```lua
local AimbotTab = Library:CreateTab("Aimbot", "This is where you modify the Aimbot")
```
# textbox
```lua
AimbotTab:CreateTextbox("Whitelist Player", function(arg)
    -- arg is the value typed into the textbox
    print("Whitelisted: " .. arg)
end)
```
# button
```lua
AimbotTab:CreateButton("Inf Jump", function()
    -- Action to perform when the button is clicked
    print("Inf Jump is now permanently on.")
end)
```
# slider
```lua
AimbotTab:CreateSlider("Fov Radius", 0, 600, function(arg)
    -- arg is the value of the slider
    print("Fov Radius is set to:", arg)
end)
```
# dropdown
```lua
AimbotTab:CreateDropDown("Aimbot Part", {"Head", "Torso"}, function(arg)
    -- arg is the selected option
    if arg == "Head" then
        print("Headshot")
    elseif arg == "Torso" then
        print("Torso shot")
    end
end)
```
# toggle
```lua
AimbotTab:CreateToggle("Enable Aimbot", function(arg)
    -- arg is true if the toggle is on, false if it is off
    if arg then
        print("Aimbot is now: Enabled")
    else
        print("Aimbot is now: Disabled")
    end
end)
```
