--script example











-- Require the UI Library module
local UILibrary = loadstring(game:HttpGet(('https://raw.githubusercontent.com/FOGOTY/test-ui-lib/refs/heads/main/lib')))()
-- Create a ScreenGui
local screenGui = Instance.new("ScreenGui")
screenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")

-- Create a frame
local frame = UILibrary.CreateFrame(screenGui)

-- Create buttons
UILibrary.CreateButton(frame, "Button 1", function()
    print("Button 1 clicked!")
end)

UILibrary.CreateButton(frame, "Button 2", function()
    print("Button 2 clicked!")
end)

-- Create an input field with a submit button
UILibrary.CreateInput(frame, "Enter your name", "Submit", function(inputValue)
    print("Input Value: " .. inputValue)
end)

-- Create a slider with a callback
UILibrary.CreateSlider(frame, "Volume", 0, 100, function(value)
    print("Slider Value: " .. value)
end)
