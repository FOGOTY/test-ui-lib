--how tto use this ui

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


