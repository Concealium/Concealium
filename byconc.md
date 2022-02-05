-- Made by Conc

if game.PlaceId == 6284583030 then
    local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
    local Window = Library.CreateLib("Pet Simulator X", "Sentinel")

    -- Main
    local Scripts = Window:NewTab("Scripts")
    local ScriptsSection = Scripts:NewSection("Scripts")
    ScriptsSection:NewButton("BK Pet Script", "BK Pet Script", function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/BLACKGAMER1221/Pet-Simulator-X/main/BK%20Pet.lua"))()
        print("Clicked")
    end)
    
    -- Player
    local Player = Window:NewTab("Player")
    local PlayerSection = Player:NewSection("Player")
    PlayerSection:NewSlider("Walkspeed", "Changes Walkspeed", 500, 16, function(v) -- 500 (MaxValue) | 0 (MinValue)
        game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = v
    end)
    PlayerSection:NewSlider("Jumppower", "Changes Jumppower", 500, 50, function(v) -- 500 (MaxValue) | 0 (MinValue)
        game.Players.LocalPlayer.Character.Humanoid.JumpPower = v
    end)
end
