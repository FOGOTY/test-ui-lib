--how to use this ui

-- Require the UI Library module
local UILibrary = loadstring(game:HttpGet(('https://raw.githubusercontent.com/FOGOTY/test-ui-lib/refs/heads/main/lib')))()


-- Create a ScreenGui
local screenGui = Instance.new("ScreenGui")
screenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")


--create frame
local frame = UILibrary.CreateFrame(screenGui)

--create button
UILibrary.CreateButton(frame, "buttonname", function()
    print("executed")
end)


-- Create an input field with a submit button
UILibrary.CreateInput(frame, "inputname", "confirmname", function(inputValue)
    print("Input Value: " .. inputValue)
end)


-- Create a slider with a callback
UILibrary.CreateSlider(frame, "slidername", 0, 100, function(value)
    print("Slider Value: " .. value)
end)

-- Create a toggle button
UILibrary.CreateToggle(frame, "Enable/Disable", function(state)
    if state then
        print("Toggle is ON")
    else
        print("Toggle is OFF")
    end
end)

-- Create another label
UILibrary.CreateLabel(frame, "This is a label")


-- Create a keybind button
UILibrary.CreateKeybind(frame, "Bind Key", function()
    print("Keybind activated!")
end)


-- Create a color picker
UILibrary.CreateColorPick(frame, "Pick Background Color", function(selectedColor)
    print("Selected Color: ", selectedColor)
    -- Example: Use the color to change the background of the ScreenGui
    screenGui.BackgroundColor3 = selectedColor
end)


-- Create a toggle UI keybind button inside the frame
UILibrary.ToggleUIBind(frame, Enum.KeyCode.LeftAlt)  -- Default keybind to "LeftAlt"

