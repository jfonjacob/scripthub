local Rayfield = loadstring(game:HttpGet('https://sirius.menu/rayfield'))()

Theme Name - ThemeIdentifier

local Window = Rayfield:CreateWindow({
    Name = "RoboHub",
    Icon = 0,
    LoadingTitle = "RoboHub",
    LoadingSubtitle = "by JFon",
    Theme = "Default",
 
    DisableRayfieldPrompts = false,
    DisableBuildWarnings = false,
 
    ConfigurationSaving = {
       Enabled = true,
       FolderName = nil,
       FileName = "Big Hub"
    },
 
    Discord = {
       Enabled = false,
       Invite = "noinvitelink",
       RememberJoins = true
    },
 
    KeySystem = false,
    KeySettings = {
       Title = "Untitled",
       Subtitle = "Key System",
       Note = "No method of obtaining the key is provided",
       FileName = "Key",
       SaveKey = true,
       GrabKeyFromSite = false,
       Key = {"Hello"}
    }
 })

 local PlayerTab = Window:CreateTab("Player", 4483362458)

 local Slider = PlayerTab:CreateSlider({
    Name = "WalkSpeed",
    Range = {1, 100},
    Increment = 1,
    Suffix = "Speed",
    CurrentValue = 10,
    Flag = "Slider1",
    Callback = function(Value)
     game.Players.LocalPlayer.Character:SetAttribute("SpeedMultiplier", Value)
    end,
 })

 local Slider = PlayerTab:CreateSlider({
    Name = "Dash length",
    Range = {1, 500},
    Increment = 1,
    Suffix = "Length",
    CurrentValue = 10,
    Flag = "Slider2",
    Callback = function(Value)
     game.Players.LocalPlayer.Character:SetAttribute("DashLength", Value)
    end,
 })

 local Slider = PlayerTab:CreateSlider({
    Name = "Jump Height",
    Range = {1, 500},
    Increment = 1,
    Suffix = "Height",
    CurrentValue = 10,
    Flag = "Slider3",
    Callback = function(Value)
     game.Players.LocalPlayer.Character.Humanoid.JumpPower = Value
    end,
 })
