local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("Muisk HUB", "BloodTheme")

-- MAIN
local Main = Window:NewTab("Menu")
local MainSection = Main:NewSection("Menu")


MainSection:NewButton("Mortal", "tu vai dar um mortal n sei se funciona ainda", function()
  loadstring(game:HttpGet('https://pastebin.com/raw/7wDcPtLk'))()
end)


MainSection:NewToggle("Humano pika", "mais pika do que o hominho de bunda", function(state)
    if state then
        game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 120
        game.Players.LocalPlayer.Character.Humanoid.JumpPower = 200
    else
        game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 16
        game.Players.LocalPlayer.Character.Humanoid.JumpPower = 50
    end
end)



MainSection:NewButton("Inf Yield", "Admin Cmds", function()
    loadstring(game:HttpGet('https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source'))()
  end)

--Player
local Player = Window:NewTab("Player")
local PlayerSection = Player:NewSection("Player")

PlayerSection:NewSlider("corre rapidao", "corre como o flash", 500, 16, function(s) -- 500 (MaxValue) | 0 (MinValue)
    game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = s
end)

PlayerSection:NewSlider("muie canguru", "faz da um super pulo", 500, 50, function(s) -- 500 (MaxValue) | 0 (MinValue)
    game.Players.LocalPlayer.Character.Humanoid.JumpPower = s
end)

  PlayerSection:NewSlider("Vida no maximo", "recupera o seu hp", 9999999999999, 100, function(s) -- 500 (MaxValue) | 0 (MinValue)
    game.Players.LocalPlayer.Character.Humanoid.MaxHealth = s
end)
