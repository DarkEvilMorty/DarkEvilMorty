
local screenGui = Instance.new("ScreenGui")
screenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")


local frame = Instance.new("Frame")
frame.Size = UDim2.new(0.3, 0, 0.35, 0) 
frame.Position = UDim2.new(0.5, 0, 0.5, 0)  
frame.AnchorPoint = Vector2.new(0.5, 0.5)  
frame.BackgroundColor3 = Color3.fromRGB(255, 255, 255) 
frame.BorderSizePixel = 2
frame.BorderColor3 = Color3.fromRGB(0, 0, 0)
frame.Parent = screenGui
local usernameLabel = Instance.new("TextLabel")
usernameLabel.Size = UDim2.new(1, 0, 0.2, 0)
usernameLabel.Position = UDim2.new(0, 0, 0, 0)
usernameLabel.Text = "Username:"
usernameLabel.TextSize = 24
usernameLabel.Parent = frame

local usernameTextBox = Instance.new("TextBox")
usernameTextBox.Size = UDim2.new(1, -20, 0.2, 0)
usernameTextBox.Position = UDim2.new(0, 10, 0.2, 0)
usernameTextBox.PlaceholderText = "Enter your username"
usernameTextBox.Parent = frame

-- TextLabel และ TextBox สำหรับ Password
local passwordLabel = Instance.new("TextLabel")
passwordLabel.Size = UDim2.new(1, 0, 0.2, 0)
passwordLabel.Position = UDim2.new(0, 0, 0.4, 0)
passwordLabel.Text = "PassWord:"
passwordLabel.TextSize = 24
passwordLabel.Parent = frame

local passwordTextBox = Instance.new("TextBox")
passwordTextBox.Size = UDim2.new(1, -20, 0.2, 0)
passwordTextBox.Position = UDim2.new(0, 10, 0.6, 0)
passwordTextBox.PlaceholderText = "Enter your password"
passwordTextBox.Parent = frame
passwordTextBox.Text = ""
passwordTextBox.TextWrapped = true
passwordTextBox.TextScaled = true
passwordTextBox.ClearTextOnFocus = false

local loginButton = Instance.new("TextButton")
loginButton.Size = UDim2.new(0.5, 0, 0.2, 0)
loginButton.Position = UDim2.new(0.25, 0, 0.8, 0)
loginButton.Text = "Login"
loginButton.TextSize = 24
loginButton.Parent = frame

-- LocalScript เพื่อตรวจสอบ Username และ Password
local localScript = Instance.new("LocalScript", loginButton)

local function onLoginButtonClicked()
    local username = usernameTextBox.Text
    local password = passwordTextBox.Text
    
    -- เช็คว่า username และ password ไม่เป็นค่าว่าง
    if username ~= "" and password ~= "" then
        -- ตรวจสอบว่า Username และ Password ถูกต้อง
        if username == "GodBlackHole" and password == "1598753" then
            frame.Visible = false
            do
                local ui = game:GetService("CoreGui"):FindFirstChild("ui") if ui then ui:Destroy()
                end
                end
                ------------------------------------------------------------------------------------------------------------------------
                local NotifyLib = loadstring(game:HttpGet("https://raw.githubusercontent.com/vKhonshu/intro/main/ui"))()
                NotifyLib.prompt('Welcome', 'Enjoy hurting others', 3)
                wait(2)
                game:GetService("StarterGui"):SetCore("SendNotification", { 
                    Title = "By:GodBlackHole";
                    Text = "Succesfully loaded";
                    Icon = "rbxthumb://type=Asset&id=5107182114&w=150&h=150"})
                Duration = 2;
                wait(1)
                local lib = loadstring(game:HttpGet"https://raw.githubusercontent.com/dawid-scripts/UI-Libs/main/Vape.txt")()
                local win = lib:Window("GodBlackHole",Color3.fromRGB(223, 255, 0), Enum.KeyCode.T)
                local tab = win:Tab("Basic Fram Horse")
                tab:Toggle("Hide LeaderboardGui",false, function()
                            _G.AutoTime = true
                                if _G.AutoTime then
                                    local playerName = game.Players.LocalPlayer.Name
                                    local leaderboardGui = game:GetService("Players")[playerName].PlayerGui.LeaderboardGui
                                    leaderboardGui.Enabled = not leaderboardGui.Enabled  -- เปลี่ยนค่า Enabled ให้เป็นตรงข้ามกัน
                            end
                  end)
                tab:Toggle("collect",false, function(v)
                    _G.collect = v
                    while _G.collect do wait()
                    game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("SendDropsRemote"):FireServer("\1")
                    end
                end)
                tab:Toggle("Boot Speed Horse",false, function(v)
                    _G.A = v
                    while _G.A do wait()
                workspace:WaitForChild("BoostPads"):WaitForChild("Speed"):WaitForChild("RemoteEvent"):FireServer()
                
                    end
                end) 
                tab:Toggle("Fram Horse Jump",false, function()
                    _G.Auto = true
                    while _G.Auto do wait()
                    game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("JumpedObstacleRemote"):FireServer(workspace:WaitForChild("Jumps"):WaitForChild("TallJumpFence"))
                        wait(.1)
                    end
                end)
                tab:Button("ClaimLoyaltyRewardRemote", function()
                    game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("ClaimLoyaltyRewardRemote"):InvokeServer()
                    end)
                tab:Slider("Walk Speed Player",25,150,25, function(v)
                    getgenv().WalkSpeedValue = v; --set your desired walkspeed here
                local Player = game:service'Players'.LocalPlayer;
                Player.Character.Humanoid:GetPropertyChangedSignal'WalkSpeed':Connect(function()
                Player.Character.Humanoid.WalkSpeed = getgenv().WalkSpeedValue;
                end)
                Player.Character.Humanoid.WalkSpeed = getgenv().WalkSpeedValue;
                    end)
                    tab:Slider("CameraMaxZoom",0,500,100, function(v)
                        spawn(function()
                            pcall(function()
                            name = tostring(game.Players.LocalPlayer.Name)
                            game:GetService("Players")[name].CameraMaxZoomDistance = v
                            end)
                            end)
                        end)
                    
                
                
                ---------------------------------------------------------------
                local tab = win:Tab("ESP Horse")
                tab:Label("                              Common Zone")
                tab:Button("ESP Horse", function()
                    local ESP = loadstring(game:HttpGet("https://kiriot22.com/releases/ESP.lua"))()
                    ESP.Players = false
                    ESP.Boxes = false 
                    ESP.Names = true
                    ESP:Toggle(true)
                    ESP:AddObjectListener(Workspace.MobFolder, {
                        Name = "Horse",
                        CustomName = "Horse",
                        Color = Color3.fromRGB(255, 255, 255),
                        IsEnabled = "Enable"
                    })
                    ESP.Enable = true
                    end)
                tab:Button("ESP Pony", function()
                    local ESP = loadstring(game:HttpGet("https://kiriot22.com/releases/ESP.lua"))()
                    ESP.Players = false
                    ESP.Boxes = false 
                    ESP.Names = true
                    ESP:Toggle(true)
                    ESP:AddObjectListener(Workspace.MobFolder, {
                        Name = "Pony",
                        CustomName = "Pony",
                        Color = Color3.fromRGB(255, 255, 255),
                        IsEnabled = "Enable"
                    })
                    ESP.Enable = true
                    end)
                tab:Button("ESP Equus", function()
                    local ESP = loadstring(game:HttpGet("https://kiriot22.com/releases/ESP.lua"))()
                    ESP.Players = false
                    ESP.Boxes = false 
                    ESP.Names = true
                    ESP:Toggle(true)
                    ESP:AddObjectListener(Workspace.MobFolder, {
                        Name = "Equus",
                        CustomName = "Equus",
                        Color = Color3.fromRGB(255, 255, 255),
                        IsEnabled = "Enable"
                    })
                    ESP.Enable = true
                    end)
                    tab:Button("ESP Bisorse", function()
                        local ESP = loadstring(game:HttpGet("https://kiriot22.com/releases/ESP.lua"))()
                        ESP.Players = false
                        ESP.Boxes = false 
                        ESP.Names = true
                        ESP:Toggle(true)
                        ESP:AddObjectListener(Workspace.MobFolder, {
                            Name = "Bisorse",
                            CustomName = "Bisorse",
                            Color = Color3.fromRGB(103, 25, 8 ),
                            IsEnabled = "Enable"
                        })
                        ESP.Enable = true
                end)
                    tab:Button("ESP Caprine", function()
                        local ESP = loadstring(game:HttpGet("https://kiriot22.com/releases/ESP.lua"))()
                        ESP.Players = false
                        ESP.Boxes = false 
                        ESP.Names = true
                        ESP:Toggle(true)
                        ESP:AddObjectListener(Workspace.MobFolder, {
                            Name = "Caprine",
                            CustomName = "Caprine",
                            Color = Color3.fromRGB(103, 25, 8 ),
                            IsEnabled = "Enable"
                        })
                        ESP.Enable = true
                end)
                tab:Button("ESP Unicorn", function()
                    local ESP = loadstring(game:HttpGet("https://kiriot22.com/releases/ESP.lua"))()
                    ESP.Players = false
                    ESP.Boxes = false 
                    ESP.Names = true
                    ESP:Toggle(true)
                    ESP:AddObjectListener(Workspace.MobFolder, {
                        Name = "Unicorn",
                        CustomName = "Unicorn",
                        Color = Color3.fromRGB(223, 255, 0),
                        IsEnabled = "Enable"
                    })
                    ESP.Enable = true
                    end)
                tab:Button("ESP Gargoyle", function()
                    local ESP = loadstring(game:HttpGet("https://kiriot22.com/releases/ESP.lua"))()
                    ESP.Players = false
                    ESP.Boxes = false 
                    ESP.Names = true
                    ESP:Toggle(true)
                    ESP:AddObjectListener(Workspace.MobFolder, {
                        Name = "Gargoyle",
                        CustomName = "Gargoyle",
                        Color = Color3.fromRGB(13, 3, 1 ),
                        IsEnabled = "Enable"
                    })
                    ESP.Enable = true
                    end)
                    tab:Label("                              NEW Horse")
                    tab:Button("ESP Kelpie", function()
                        local ESP = loadstring(game:HttpGet("https://kiriot22.com/releases/ESP.lua"))()
                        ESP.Players = false
                        ESP.Boxes = false 
                        ESP.Names = true
                        ESP:Toggle(true)
                        ESP:AddObjectListener(Workspace.MobFolder, {
                            Name = "Kelpie",
                            CustomName = "Kelpie",
                            Color = Color3.fromRGB(13, 3, 1 ),
                            IsEnabled = "Enable"
                        })
                        ESP.Enable = true
                        end)
                    
                
                
                
                   
                    
                local tab = win:Tab("ESP Item")
                tab:Button("ESP BerryBush", function()
                    local ESP = loadstring(game:HttpGet("https://kiriot22.com/releases/ESP.lua"))()
                    ESP.Players = false
                    ESP.Boxes = false 
                    ESP.Names = true
                    ESP:Toggle(true)
                    ESP:AddObjectListener(Workspace.Interactions.Resource, {
                        Name = "BerryBush",
                        CustomName = "BerryBush",
                        Color = Color3.fromRGB(255, 13, 13),
                        IsEnabled = "Enable"
                    })
                    ESP.Enable = true
                    end)
                
                    tab:Button("ESP AppleBarrel", function()
                        local ESP = loadstring(game:HttpGet("https://kiriot22.com/releases/ESP.lua"))()
                        ESP.Players = false
                        ESP.Boxes = false 
                        ESP.Names = true
                        ESP:Toggle(true)
                        ESP:AddObjectListener(Workspace.Interactions.Resource, {
                            Name = "AppleBarrel",
                            CustomName = "AppleBarrel",
                            Color = Color3.fromRGB(147, 226, 181),
                            IsEnabled = "Enable"
                        })
                        ESP.Enable = true
                    end)
                    tab:Button("ESP FoodPallet", function()
                        local ESP = loadstring(game:HttpGet("https://kiriot22.com/releases/ESP.lua"))()
                        ESP.Players = false
                        ESP.Boxes = false 
                        ESP.Names = true
                        ESP:Toggle(true)
                        ESP:AddObjectListener(Workspace.Interactions.Resource, {
                            Name = "FoodPallet",
                            CustomName = "FoodPallet",
                            Color = Color3.fromRGB(204, 204, 0),
                            IsEnabled = "Enable"
                        })
                        ESP.Enable = true
                    end)
                    tab:Button("ESP Treasure", function()
                        local ESP = loadstring(game:HttpGet("https://kiriot22.com/releases/ESP.lua"))()
                        ESP.Players = false
                        ESP.Boxes = false 
                        ESP.Names = true
                        ESP:Toggle(true)
                        ESP:AddObjectListener(Workspace.Interactions.Resource, {
                            Name = "Treasure",
                            CustomName = "Treasure",
                            Color = Color3.fromRGB(255, 255, 255),
                            IsEnabled = "Enable"
                        })
                        ESP.Enable = true
                    end)
                    tab:Button("ESP Fallen Tree", function()
                        local ESP = loadstring(game:HttpGet("https://kiriot22.com/releases/ESP.lua"))()
                        ESP.Players = false
                        ESP.Boxes = false 
                        ESP.Names = true
                        ESP:Toggle(true)
                        ESP:AddObjectListener(Workspace.Interactions.Resource, {
                            Name = "Fallen Tree",
                            CustomName = "Fallen Tree",
                            Color = Color3.fromRGB(204, 0, 0),
                            IsEnabled = "Enable"
                        })
                        ESP.Enable = true
                    end)
                    tab:Button("ESP LargeBerryBush", function()
                        local ESP = loadstring(game:HttpGet("https://kiriot22.com/releases/ESP.lua"))()
                        ESP.Players = false
                        ESP.Boxes = false 
                        ESP.Names = true
                        ESP:Toggle(true)
                        ESP:AddObjectListener(Workspace.Interactions.Resource, {
                            Name = "LargeBerryBush",
                            CustomName = "LargeBerryBush",
                            Color = Color3.fromRGB(51, 255, 255),
                            IsEnabled = "Enable"
                        })
                        ESP.Enable = true
                    end)
                        tab:Button("ESP Stump", function()
                            local ESP = loadstring(game:HttpGet("https://kiriot22.com/releases/ESP.lua"))()
                    ESP.Players = false
                    ESP.Boxes = false 
                    ESP.Names = true
                    ESP:Toggle(true)
                    ESP:AddObjectListener(Workspace.Interactions.Resource, {
                        Name = "Stump",
                        CustomName = "Stump",
                        Color = Color3.fromRGB(255, 102, 255),
                        IsEnabled = "Enable"
                    })
                    ESP.Enable = true
                    end)
                        tab:Button("ESP StoneDeposit", function()
                            local ESP = loadstring(game:HttpGet("https://kiriot22.com/releases/ESP.lua"))()
                    ESP.Players = false
                    ESP.Boxes = false 
                    ESP.Names = true
                    ESP:Toggle(true)
                    ESP:AddObjectListener(Workspace.Interactions.Resource, {
                        Name = "StoneDeposit",
                        CustomName = "StoneDeposit",
                        Color = Color3.fromRGB(255, 102, 255),
                        IsEnabled = "Enable"
                    })
                    ESP.Enable = true
                    end)
                local tab = win:Tab("Tp-Fram Plus TP-Horse")
                    tab:Label("                              TP item")
                   tab:Textbox("Use number HorseEquip-Unequip 10 sec ,If it's open, it can't be closed",false, function(v)
                        _G.Equip = true
                        while _G.Equip do wait()
                        game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("EquipAnimalRemote"):InvokeServer(v)
                        wait(10)
                        game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("UnequipAnimalRemote"):InvokeServer(v)
                            end
                        end)
                    tab:Toggle("Tp AppleBarrel",false, function(v)
                        _G.AutoFram = v;
                        while _G.AutoFram do wait()
                        pcall(function()
                        for i,v in pairs(game:GetService("Workspace").Interactions.Resource.AppleBarrel:GetDescendants()) do
                        if v.Name == "Particles" then
                        repeat task.wait()
                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.Parent.CFrame * CFrame.new(0,4,3)
                        until _G.AutoFram == false or v.Humanoid.Health <= 0
                                    end
                                end
                            end)
                        end
                        end)
                    tab:Toggle("Tp FoodPallet",false, function(v)
                        _G.AutoFram = v;
                        while _G.AutoFram do wait()
                        pcall(function()
                        for i,v in pairs(game:GetService("Workspace").Interactions.Resource.FoodPallet:GetDescendants()) do
                        if v.Name == "Particles" then
                        repeat task.wait()
                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.Parent.CFrame * CFrame.new(0,4,3)
                        until _G.AutoFram == false or v.Humanoid.Health <= 0
                                    end
                                end
                            end)
                        end
                        end)
                    tab:Toggle("Tp Stump",false, function(v)
                        _G.AutoFram = v;
                        while _G.AutoFram do wait()
                        pcall(function()
                        for i,v in pairs(game:GetService("Workspace").Interactions.Resource.Stump:GetDescendants()) do
                        if v.Name == "Particles" then
                        repeat task.wait()
                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.Parent.CFrame * CFrame.new(0,4,3)
                        until _G.AutoFram == false or v.Humanoid.Health <= 0
                                    end
                                end
                            end)
                        end
                        end)
                    tab:Toggle("Tp Treasure",false, function(v)
                        _G.AutoFram = v;
                        while _G.AutoFram do wait()
                        pcall(function()
                        for i,v in pairs(game:GetService("Workspace").Interactions.Resource.Treasure:GetDescendants()) do
                        if v.Name == "Particles" then
                        repeat task.wait()
                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.Parent.CFrame * CFrame.new(0,4,3)
                        until _G.AutoFram == false or v.Humanoid.Health <= 0
                                    end
                                end
                            end)
                        end
                        end)
                    tab:Toggle("Tp BerryBush",false, function(v)
                        _G.AutoFram = v;
                        while _G.AutoFram do wait()
                        pcall(function()
                        for i,v in pairs(game:GetService("Workspace").Interactions.Resource.BerryBush:GetDescendants()) do
                        if v.Name == "Particles" then
                        repeat task.wait()
                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.Parent.CFrame * CFrame.new(0,4,3)
                        until _G.AutoFram == false or v.Humanoid.Health <= 0
                                    end
                                end
                            end)
                        end
                        end)
                    tab:Toggle("Tp LargeBerryBush",false, function(v)
                        _G.AutoFram = v;
                        while _G.AutoFram do wait()
                        pcall(function()
                        for i,v in pairs(game:GetService("Workspace").Interactions.Resource.LargeBerryBush:GetDescendants()) do
                        if v.Name == "Particles" then
                        repeat task.wait()
                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.Parent.CFrame * CFrame.new(0,4,3)
                        until _G.AutoFram == false or v.Humanoid.Health <= 0
                                    end
                                end
                            end)
                        end
                        end)
                    tab:Toggle("Tp FallenTree",false, function(v)
                        _G.AutoFram = v;
                        while _G.AutoFram do wait()
                        pcall(function()
                        for i,v in pairs(game:GetService("Workspace").Interactions.Resource.FallenTree:GetDescendants()) do
                        if v.Name == "Particles" then
                        repeat task.wait()
                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.Parent.CFrame * CFrame.new(0,4,3)
                        until _G.AutoFram == false or v.Humanoid.Health <= 0
                                    end
                                end
                            end)
                        end
                        end)
                    tab:Toggle("Tp StoneDeposit",false, function(v)
                        _G.AutoFram = v;
                        while _G.AutoFram do wait()
                        pcall(function()
                        for i,v in pairs(game:GetService("Workspace").Interactions.Resource.StoneDeposit:GetDescendants()) do
                        if v.Name == "Particles" then
                        repeat task.wait()
                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.Parent.CFrame * CFrame.new(0,4,3)
                        until _G.AutoFram == false or v.Humanoid.Health <= 0
                                    end
                                end
                            end)
                        end
                        end)
                tab:Label("                              Tp Horse Common-Rare")
                tab:Toggle("Horse",false, function(v)
                    _G.AutoTP = v
                    while _G.AutoTP do wait()
                    local rootPart = game.Players.LocalPlayer.Character.HumanoidRootPart
                    rootPart.CFrame = game:GetService("Workspace").MobFolder.Horse.CFrame * CFrame.new(0,0,3)
                    end
                    end)
                    tab:Toggle("Pony",false, function(v)
                        _G.AutoTP = v
                        while _G.AutoTP do wait()
                    local rootPart = game.Players.LocalPlayer.Character.HumanoidRootPart
                    rootPart.CFrame = game:GetService("Workspace").MobFolder.Pony.CFrame * CFrame.new(0,0,3)
                        end
                    end)
                    tab:Toggle("Equus",false, function(v)
                        _G.AutoTP = v
                        while _G.AutoTP do wait()
                    local rootPart = game.Players.LocalPlayer.Character.HumanoidRootPart
                    rootPart.CFrame = game:GetService("Workspace").MobFolder.Equus.CFrame * CFrame.new(0,0,3)
                        end
                    end)
                    tab:Toggle("Bisorse",false, function(v)
                        _G.AutoTP = v
                        while _G.AutoTP do wait()
                        local rootPart = game.Players.LocalPlayer.Character.HumanoidRootPart
                        rootPart.CFrame = game:GetService("Workspace").MobFolder.Bisorse.CFrame * CFrame.new(0,0,3)
                            end
                        end)
                    tab:Label("                                Epic-Legendary Zone")
                    tab:Toggle("Caprine",false, function(v)
                        _G.AutoTP = v
                        while _G.AutoTP do wait()
                        local rootPart = game.Players.LocalPlayer.Character.HumanoidRootPart
                        rootPart.CFrame = game:GetService("Workspace").MobFolder.Caprine.CFrame * CFrame.new(0,0,3)
                        end
                        end)
                        tab:Toggle("Unicorn",false, function(v)    _G.AutoTP = v
                            while _G.AutoTP do wait()
                        local rootPart = game.Players.LocalPlayer.Character.HumanoidRootPart
                        rootPart.CFrame = game:GetService("Workspace").MobFolder.Unicorn.CFrame * CFrame.new(0,0,3)
                            end
                        end)
                        tab:Toggle("Gargoyle",false, function(v)
                            _G.AutoTP = v
                            while _G.AutoTP do wait()
                        local rootPart = game.Players.LocalPlayer.Character.HumanoidRootPart
                        rootPart.CFrame = game:GetService("Workspace").MobFolder.Gargoyle.CFrame * CFrame.new(0,0,3)
                            end
                        end)
                        tab:Toggle("Kelpie",false, function(v)
                            _G.AutoTP = v
                            while _G.AutoTP do wait()
                        local rootPart = game.Players.LocalPlayer.Character.HumanoidRootPart
                        rootPart.CFrame = game:GetService("Workspace").MobFolder.Kelpie.CFrame * CFrame.new(0,0,3)
                            end
                        end)
                        tab:Toggle("🦄 Peryton",false, function(v)
                            _G.AutoTP = v
                            while _G.AutoTP do wait()
                        local rootPart = game.Players.LocalPlayer.Character.HumanoidRootPart
                        rootPart.CFrame = game:GetService("Workspace").MobFolder.Peryton.CFrame * CFrame.new(0,0,3)
                            end
                        end)
                        local tab = win:Tab("TameHorse Update!!")
                        tab:Label("                              tame Food")
                        tab:Toggle("Hide DisplayAnimalGui",false, function(v)
                            _G.AutoDis = v
                            while _G.AutoDis do wait()
                            name = tostring(game.Players.LocalPlayer.Name)
                            game:GetService("Players")[name].PlayerGui.DisplayAnimalGui.Enabled = false
                            end
                        end)
                        tab:Toggle("Sell Horse",false, function(v)
                            _G.AutoSell = v
                                spawn(function()
                                    pcall(function()
                                    while _G.AutoSell do
                                        wait()
                                        local sellSlots = 500
                                        local args = {}
                                        for i = 1, sellSlots do
                                        table.insert(args, tostring(i))
                                    end
                                    game:GetService("ReplicatedStorage").Remotes.SellSlotsRemote:InvokeServer(args)
                                    wait(.1)
                                    end
                                    end)
                                    end)
                        end)
                
                        tab:Toggle("Tame Food Horse",false, function(v)
                            _G.Lv1 = v
                            while _G.Lv1 do wait()
                                workspace:WaitForChild("MobFolder"):WaitForChild("Horse"):WaitForChild("TameEvent"):FireServer("Begin")
                                workspace:WaitForChild("MobFolder"):WaitForChild("Horse"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed")
                                wait(.2)
                            end
                        end)
                        tab:Toggle("Tame Food Nomal Pony ",false, function(v)
                            _G.Lv1 = v
                            while _G.Lv1 do wait()
                                workspace:WaitForChild("MobFolder"):WaitForChild("Pony"):WaitForChild("TameEvent"):FireServer("Begin")
                                workspace:WaitForChild("MobFolder"):WaitForChild("Pony"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed")
                                wait(.2)
                            end
                        end)
                        tab:Toggle("Tame Food Equus",false, function(v)
                            _G.Lv2 = v
                            while _G.Lv2 do wait(2)
                                workspace:WaitForChild("MobFolder"):WaitForChild("Equus"):WaitForChild("TameEvent"):FireServer("Begin")
                                workspace:WaitForChild("MobFolder"):WaitForChild("Equus"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed")
                                wait(.2)
                            end
                        end)
                        tab:Toggle("Tame Food Caprine",false, function(v)
                            _G.Lv3 = v
                            while _G.Lv3 do wait()
                                workspace:WaitForChild("MobFolder"):WaitForChild("Caprine"):WaitForChild("TameEvent"):FireServer("Begin")
                                workspace:WaitForChild("MobFolder"):WaitForChild("Caprine"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed")
                                wait(.2)
                            end
                        end)
                        tab:Toggle("Tame Food Unicorn",false, function(v)
                            _G.Lv3 = v
                            while _G.Lv3 do wait()
                                workspace:WaitForChild("MobFolder"):WaitForChild("Unicorn"):WaitForChild("TameEvent"):FireServer("Begin")
                                workspace:WaitForChild("MobFolder"):WaitForChild("Unicorn"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed")
                                wait(.2)
                            end
                        end)
                        tab:Toggle("Tame Food Gargoyle",false, function(v)
                            _G.Lv4 = v
                            while _G.Lv4 do wait()
                                workspace:WaitForChild("MobFolder"):WaitForChild("Gargoyle"):WaitForChild("TameEvent"):FireServer("Begin")
                                workspace:WaitForChild("MobFolder"):WaitForChild("Gargoyle"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed")
                                wait(.2)
                            end
                            end)
                            tab:Toggle("Tame Food Bisorse",false, function(v)
                                _G.Lv5 = v
                                while _G.Lv5 do wait()
                                    workspace:WaitForChild("MobFolder"):WaitForChild("Bisorse"):WaitForChild("TameEvent"):FireServer("Begin")
                                    workspace:WaitForChild("MobFolder"):WaitForChild("Bisorse"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed")
                                    wait(.2)
                                end
                                end)
                            tab:Toggle("Tame Food Kelpie",false, function(v)
                            _G.Lv5 = v
                            while _G.Lv5 do wait()
                                workspace:WaitForChild("MobFolder"):WaitForChild("Kelpie"):WaitForChild("TameEvent"):FireServer("Begin")
                                workspace:WaitForChild("MobFolder"):WaitForChild("Kelpie"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed")
                                wait(.2)
                            end
                            end)
                            tab:Toggle("Tame Food Peryton",false, function(v)
                            _G.Lv5 = v
                            while _G.Lv5 do wait()
                                workspace:WaitForChild("MobFolder"):WaitForChild("Peryton"):WaitForChild("TameEvent"):FireServer("Begin")
                                workspace:WaitForChild("MobFolder"):WaitForChild("Peryton"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed")
                                wait(.2)
                            end
                            end)
                
                            tab:Label("                              tame Lasso Common")
                            tab:Toggle("HideDisplayAnimalGui",false, function(v)
                                _G.AutoDis = v
                                while _G.AutoDis do wait()
                                name = tostring(game.Players.LocalPlayer.Name)
                                game:GetService("Players")[name].PlayerGui.DisplayAnimalGui.Enabled = false
                                end
                            end)
                            tab:Toggle("Sell Horse",false, function(v)
                                _G.AutoSell = v
                                spawn(function()
                                    pcall(function()
                                    while _G.AutoSell do
                                        wait()
                                        local sellSlots = 500
                                        local args = {}
                                        for i = 1, sellSlots do
                                        table.insert(args, tostring(i))
                                    end
                                    game:GetService("ReplicatedStorage").Remotes.SellSlotsRemote:InvokeServer(args)
                                    end
                                    end)
                                    end)
                            end)
                
                            
                            
                tab:Button("Sell Horse", function()
                    local sellSlots = 500
                    local args = {}
                    for i = 1, sellSlots do
                        table.insert(args, tostring(i))
                end
                    game:GetService("ReplicatedStorage").Remotes.SellSlotsRemote:InvokeServer(args)
                end)
                            tab:Toggle("Tame Horse",false, function(v)
                                _G.Auto = v
                        while _G.Auto do wait()
                        workspace:WaitForChild("MobFolder"):WaitForChild("Horse"):WaitForChild("TameEvent"):FireServer("BeginAggro","TornLasso")
                        workspace:WaitForChild("MobFolder"):WaitForChild("Horse"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed","TornLasso")
                        workspace:WaitForChild("MobFolder"):WaitForChild("Horse"):WaitForChild("TameEvent"):FireServer("BeginAggro","StringLasso")
                        workspace:WaitForChild("MobFolder"):WaitForChild("Horse"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed","StringLasso")
                        workspace:WaitForChild("MobFolder"):WaitForChild("Horse"):WaitForChild("TameEvent"):FireServer("BeginAggro","WovenLasso")
                        workspace:WaitForChild("MobFolder"):WaitForChild("Horse"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed","WovenLasso")
                        wait(.2)
                            end
                        end)
                            
                        tab:Toggle("Tame TornLasso,,StringLassoWovenLasso ,Equus",false, function(v)
                            _G.Auto = v
                        while _G.Auto do wait()
                        workspace:WaitForChild("MobFolder"):WaitForChild("Equus"):WaitForChild("TameEvent"):FireServer("BeginAggro","TornLasso")
                        workspace:WaitForChild("MobFolder"):WaitForChild("Equus"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed","TornLasso")
                        workspace:WaitForChild("MobFolder"):WaitForChild("Equus"):WaitForChild("TameEvent"):FireServer("BeginAggro","StringLasso")
                        workspace:WaitForChild("MobFolder"):WaitForChild("Equus"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed","StringLasso")
                        workspace:WaitForChild("MobFolder"):WaitForChild("Equus"):WaitForChild("TameEvent"):FireServer("BeginAggro","WovenLasso")
                        workspace:WaitForChild("MobFolder"):WaitForChild("Equus"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed","WovenLasso")
                        wait(.2)
                            end
                        end)
                        tab:Toggle("Tame RopeLasso,WesternLasso , Bisorse",false, function(v)
                            _G.Auto = v
                        while _G.Auto do wait()
                        workspace:WaitForChild("MobFolder"):WaitForChild("Bisorse"):WaitForChild("TameEvent"):FireServer("BeginAggro","RopeLasso")
                        workspace:WaitForChild("MobFolder"):WaitForChild("Bisorse"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed","RopeLasso")
                        workspace:WaitForChild("MobFolder"):WaitForChild("Bisorse"):WaitForChild("TameEvent"):FireServer("BeginAggro","WesternLasso")
                        workspace:WaitForChild("MobFolder"):WaitForChild("Bisorse"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed","WesternLasso")
                        wait(.2)
                            end
                        end) 
                        --------------------------------------------------------------------------
                        tab:Label("                              tame Lasso Epic-Legendary")
                        tab:Toggle("Tame WeakMagicLasso,MagicalLasso ,Unicorn",false, function(v)
                            _G.Auto = v
                        while _G.Auto do wait()
                        workspace:WaitForChild("MobFolder"):WaitForChild("Unicorn"):WaitForChild("TameEvent"):FireServer("BeginAggro","WeakMagicLasso")
                        workspace:WaitForChild("MobFolder"):WaitForChild("Unicorn"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed","WeakMagicLasso")
                        workspace:WaitForChild("MobFolder"):WaitForChild("Unicorn"):WaitForChild("TameEvent"):FireServer("BeginAggro","MagicalLasso")
                        workspace:WaitForChild("MobFolder"):WaitForChild("Unicorn"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed","MagicalLasso")
                        wait(.2)
                            end
                        end)  
                        tab:Toggle("Tame Vibrant Lasso, ,Caprine",false, function(v)
                            _G.Auto = v
                        while _G.Auto do wait()
                        workspace:WaitForChild("MobFolder"):WaitForChild("Caprine"):WaitForChild("TameEvent"):FireServer("BeginAggro","VibrantLasso")
                        workspace:WaitForChild("MobFolder"):WaitForChild("Caprine"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed","VibrantLasso")
                        wait(.2)
                            end
                        end)
                        tab:Toggle("Tame StoneLasso,OvergrownLasso , Gargoyle",false, function(v)
                            _G.Auto = v  
                        while _G.Auto do wait()
                        workspace:WaitForChild("MobFolder"):WaitForChild("Gargoyle"):WaitForChild("TameEvent"):FireServer("BeginAggro","StoneLasso")
                        workspace:WaitForChild("MobFolder"):WaitForChild("Gargoyle"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed","StoneLasso")
                        workspace:WaitForChild("MobFolder"):WaitForChild("Gargoyle"):WaitForChild("TameEvent"):FireServer("BeginAggro","OvergrownLasso")
                        workspace:WaitForChild("MobFolder"):WaitForChild("Gargoyle"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed","OvergrownLasso")
                        wait(.2)
                            end
                        end) 
                        tab:Toggle("Tame KelpLasso, Kelpie",false, function(v)
                            _G.Auto = v
                        while _G.Auto do wait() 
                        workspace:WaitForChild("MobFolder"):WaitForChild("Kelpie"):WaitForChild("TameEvent"):FireServer("BeginAggro","KelpLasso")
                        workspace:WaitForChild("MobFolder"):WaitForChild("Kelpie"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed","KelpLasso")
                        wait(.2)
                            end
                        end) 
                        tab:Toggle("Tame MysticCloudLasso, Peryton",false, function(v)
                            _G.Auto = v
                        while _G.Auto do wait() 
                        workspace:WaitForChild("MobFolder"):WaitForChild("Peryton"):WaitForChild("TameEvent"):FireServer("BeginAggro","MysticCloudLasso")
                        workspace:WaitForChild("MobFolder"):WaitForChild("Peryton"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed","Peryton")
                        wait(.2)
                            end
                        end) 
                        local tab = win:Tab("Boss")
                        tab:Label("                              ESP")
                        tab:Bind("Fishing",Enum.KeyCode.V, function()
                            game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("ClientCaughtFish"):InvokeServer()
                        end)
                        
                    
                    tab:Toggle("Tp BossTotem",false, function(v)
                        _G.AutoTP = v
                        while _G.AutoTP do wait(1)
                            local rootPart = game.Players.LocalPlayer.Character.HumanoidRootPart
                            rootPart.CFrame = game:GetService("Workspace").Terrain.TotemModel.BasePart.CFrame * CFrame.new(0,0,3)
                        end
                    end)
                    tab:Button("ESP BossTotem", function()
                        local ESP = loadstring(game:HttpGet("https://kiriot22.com/releases/ESP.lua"))()
                        ESP.Players = false
                        ESP.Boxes = false 
                        ESP.Names = true
                        ESP:Toggle(true)
                        ESP:AddObjectListener(workspace.Terrain.TotemModel, {
                            Name = "BossTotem",
                            CustomName = "BossTotem",
                            Color = Color3.fromRGB(231, 47, 8),
                            IsEnabled = "Enable"
                        })
                        ESP.Enable = true
                        end)
                        tab:Toggle("Hide DisplayAnimalGui",false, function()
                            _G.AutoDis = true
                            while _G.AutoDis do wait()
                            name = tostring(game.Players.LocalPlayer.Name)
                            game:GetService("Players")[name].PlayerGui.DisplayAnimalGui.Enabled = false
                            end
                        end)
                        tab:Toggle("Tame Horse",false, function(v)
                            _G.Auto = v
                    while _G.Auto do wait()
                    workspace:WaitForChild("MobFolder"):WaitForChild("Horse"):WaitForChild("TameEvent"):FireServer("BeginAggro","TornLasso")
                    workspace:WaitForChild("MobFolder"):WaitForChild("Horse"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed","TornLasso")
                    workspace:WaitForChild("MobFolder"):WaitForChild("Horse"):WaitForChild("TameEvent"):FireServer("BeginAggro","StringLasso")
                    workspace:WaitForChild("MobFolder"):WaitForChild("Horse"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed","StringLasso")
                    workspace:WaitForChild("MobFolder"):WaitForChild("Horse"):WaitForChild("TameEvent"):FireServer("BeginAggro","WovenLasso")
                    workspace:WaitForChild("MobFolder"):WaitForChild("Horse"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed","WovenLasso")
                    wait(.2)
                        end
                    end)
                        tab:Toggle("Donate Horse All lock Horse",false, function(v)
                            _G.AutoSell = v
                            spawn(function()
                                pcall(function()
                                while _G.AutoSell do
                                    wait()
                                    local sellSlots = 500
                                    local args = {}
                                    for i = 1, sellSlots do
                                    table.insert(args, tostring(i))
                                end
                                game:GetService("ReplicatedStorage").Remotes.BossDonateSlotsRemote:InvokeServer(args)
                                end
                                end)
                                end)
                        end)
                        tab:Label("                               Fight Boss")
                        tab:Button("ATK Boss Pony", function()
                            _G.Auto = true
                            while _G.Auto do wait()
                            workspace:WaitForChild("MobFolder"):WaitForChild("Pony"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed")
                            wait(0.1)
                            end
                        end)
                        tab:Button("ATK Boss Kelpie", function()
                            _G.Auto = true
                            while _G.Auto do wait()
                            workspace:WaitForChild("MobFolder"):WaitForChild("Kelpie"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed")
                            wait(0.1)
                            end
                        end)
                        tab:Button("ATK Boss Horse", function()
                            _G.Auto = true
                            while _G.Auto do wait()
                            workspace:WaitForChild("MobFolder"):WaitForChild("Horse"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed")
                            wait(0.1)
                            end
                        end)
                        tab:Button("ATK Boss Equus", function()
                            _G.Auto = true
                            while _G.Auto do wait()
                                workspace:WaitForChild("MobFolder"):WaitForChild("Equus"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed")
                            wait(0.1)
                            end
                        end)
                        tab:Button("ATK Boss Bisorse", function()
                            _G.Auto = true
                            while _G.Auto do wait()
                                workspace:WaitForChild("MobFolder"):WaitForChild("Bisorse"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed")
                            wait(0.1)
                            end
                        end)
                        tab:Button("ATK Boss Caprine", function()
                            _G.Auto = true
                            while _G.Auto do wait()
                                workspace:WaitForChild("MobFolder"):WaitForChild("Caprine"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed")
                            wait(0.1)
                            end
                        end)
                        tab:Button("ATK Boss Unicorn", function()
                            _G.Auto = true
                            while _G.Auto do wait()
                                workspace:WaitForChild("MobFolder"):WaitForChild("Unicorn"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed")
                            wait(0.1)
                            end
                        end)
                        tab:Button("ATK Boss Gargoyle", function()
                            _G.Auto = true
                            while _G.Auto do wait()
                                workspace:WaitForChild("MobFolder"):WaitForChild("Gargoyle"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed")
                            wait(0.1)
                            end
                        end)
                        tab:Label("                              New Fight Boss")
            
                    tab:Dropdown("ATK Boss",{"Stop","Horse","Pony","Equus","Caprine","Bisorse","Unicorn","Gargoyle","Kelpie"}, function(v)
                        getgenv().ATK = v
                    end) 
                
                    spawn(function(v)
                        while task.wait() do
                        if getgenv().ATK then
                    if getgenv().ATK == "Stop" then 
                    
                    elseif getgenv().ATK == "Horse" then                        
                        workspace:WaitForChild("MobFolder"):WaitForChild("Horse"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed")
                    elseif getgenv().ATK == "Pony" then
                        workspace:WaitForChild("MobFolder"):WaitForChild("Pony"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed")
                    elseif getgenv().ATK == "Equus" then
                        workspace:WaitForChild("MobFolder"):WaitForChild("Equus"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed")
                    elseif getgenv().ATK == "Caprine" then
                        workspace:WaitForChild("MobFolder"):WaitForChild("Caprine"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed")
                    elseif getgenv().ATK == "Bisorse" then
                        workspace:WaitForChild("MobFolder"):WaitForChild("Bisorse"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed")
                    elseif getgenv().ATK == "Unicorn" then
                        workspace:WaitForChild("MobFolder"):WaitForChild("Unicorn"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed")
                    elseif getgenv().ATK == "Gargoyle" then
                        workspace:WaitForChild("MobFolder"):WaitForChild("Gargoyle"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed")
                    elseif getgenv().ATK == "Kelpie" then
                        workspace:WaitForChild("MobFolder"):WaitForChild("Kelpie"):WaitForChild("TameEvent"):FireServer("SuccessfulFeed")
                                end
                            end
                        end
                    end)
                
                    
                    
                    
                    
                
                        -------------------------------------------------------------------
                        local tab = win:Tab("Buy Item")
                        tab:Dropdown("Item",{"Stop","TornLasso","StringLasso","WovenLasso","RopeLasso","WesternLasso","Bright","VibrantLasso","WeakMagicLasso","MagicalLasso","StoneLasso","OvergrownLasso","KelpLasso"}, function(v)
                            getgenv().eggtype = v
                        end)  
                        tab:Dropdown("Food",{"Stop","OatMuffin 10$","SugarMuffin 25$","MintMuffin 50$","BasicFeed 75$","CarrotMuffin 100$","GoodFeed 150$","AppleMuffin 200$","PremiumFeed 300$","ExclusiveFeed 600$"}, function(v)
                            getgenv().food = v
                        end)  
                        Plr = {}
                        name = tostring(game.Players.LocalPlayer.Name)
                    for i,v in pairs(game:GetService("Workspace").Characters[name].Animals:GetChildren()) do
                    table.insert(Plr,v.Name) 
                end
                local drop = tab:Dropdown("NumBer Horse",Plr, function(t)
                     PlayerTP = t
                end)
                --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
                ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
                
                spawn(function(v)
                    while task.wait(0.5) do
                    if getgenv().food then
                if getgenv().food == "Stop" then 
                
                elseif getgenv().food == "OatMuffin 10$" then                        
                    game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("PurchaseItemRemote"):InvokeServer("OatMuffin")
                elseif getgenv().food == "SugarMuffin 25$" then
                    game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("PurchaseItemRemote"):InvokeServer("SugarMuffin")
                elseif getgenv().food == "MintMuffin 50$" then
                    game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("PurchaseItemRemote"):InvokeServer("BasicFeed")
                elseif getgenv().food == "BasicFeed 75$" then
                    game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("PurchaseItemRemote"):InvokeServer("MintMuffin")
                elseif getgenv().food == "CarrotMuffin 100$" then
                    game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("PurchaseItemRemote"):InvokeServer("CarrotMuffin")
                elseif getgenv().food == "GoodFeed 150$" then
                    game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("PurchaseItemRemote"):InvokeServer("GoodFeed")
                elseif getgenv().food == "AppleMuffin 200$" then
                    game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("PurchaseItemRemote"):InvokeServer("AppleMuffin")
                elseif getgenv().food == "PremiumFeed 300$" then
                    game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("PurchaseItemRemote"):InvokeServer("PremiumFeed")
                elseif getgenv().food == "ExclusiveFeed 600$" then
                    game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("PurchaseItemRemote"):InvokeServer("ExclusiveFeed")
                            end
                        end
                    end
                end)
                spawn(function(v)
                    while task.wait(0.8) do
                    if getgenv().eggtype then
                if getgenv().eggtype == "Stop" then 
                
                elseif getgenv().eggtype == "TornLasso" then                        
                    game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("PurchaseItemRemote"):InvokeServer("TornLasso")
                elseif getgenv().eggtype == "StringLasso" then
                    game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("PurchaseItemRemote"):InvokeServer("StringLasso")
                elseif getgenv().eggtype == "WovenLasso" then
                    game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("PurchaseItemRemote"):InvokeServer("WovenLasso")
                elseif getgenv().eggtype == "RopeLasso" then
                    game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("PurchaseItemRemote"):InvokeServer("RopeLasso")
                elseif getgenv().eggtype == "WesternLasso" then
                    game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("PurchaseItemRemote"):InvokeServer("WesternLasso")
                elseif getgenv().eggtype == "Bright" then
                    game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("PurchaseItemRemote"):InvokeServer("Bright")
                elseif getgenv().eggtype == "VibrantLasso" then
                    game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("PurchaseItemRemote"):InvokeServer("VibrantLasso")
                elseif getgenv().eggtype == "WeakMagicLasso" then
                    game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("PurchaseItemRemote"):InvokeServer("WeakMagicLasso")
                elseif getgenv().eggtype == "MagicalLasso" then
                    game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("PurchaseItemRemote"):InvokeServer("MagicalLasso")
                elseif getgenv().eggtype == "StoneLasso" then
                    game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("PurchaseItemRemote"):InvokeServer("StoneLasso")
                elseif getgenv().eggtype == "OvergrownLasso" then
                    game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("PurchaseItemRemote"):InvokeServer("OvergrownLasso")
                elseif getgenv().eggtype == "KelpLasso" then
                    game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("PurchaseItemRemote"):InvokeServer("KelpLasso")
                            end
                        end
                    end
                end)
                    
                
                --------------------------------------------------------------------------------------------------------------------------
                        local tab = win:Tab("Rejoin")
                        tab:Button("Rejoin", function()
                            local ts = game:GetService("TeleportService")
                            local p = game:GetService("Players").LocalPlayer
                            ts:TeleportToPlaceInstance(game.PlaceId, game.JobId, p)
                            end)
                        tab:Button("SEVER LOWANDHigh", function()
                            loadstring(game:HttpGet("https://www.scriptblox.com/raw/Server-Browser_80", true))();
                            end)
                        tab:Button("Hopserver", function()
                            local Player = game.Players.LocalPlayer    
                            local Http = game:GetService("HttpService")
                            local TPS = game:GetService("TeleportService")
                            local Api = "https://games.roblox.com/v1/games/"
                            
                            local _place,_id = game.PlaceId, game.JobId
                            local _servers = Api.._place.."/servers/Public?sortOrder=Desc&limit=100"
                            function ListServers(cursor)
                               local Raw = game:HttpGet(_servers .. ((cursor and "&cursor="..cursor) or ""))
                               return Http:JSONDecode(Raw)
                            end
                            
                            local Next; repeat
                               local Servers = ListServers(Next)
                               for i,v in next, Servers.data do
                                   if v.playing < v.maxPlayers and v.id ~= _id then
                                       local s,r = pcall(TPS.TeleportToPlaceInstance,TPS,_place,v.id,Player)
                                       if s then break end
                                   end
                               end
                               
                               Next = Servers.nextPageCursor
                            until not Next
                        end)
                        
                        tab:Button("HopServer Low", function()
                            Time = 1 -- seconds
                            repeat wait() until game:IsLoaded()
                            wait(Time)
                            local PlaceID = game.PlaceId
                            local AllIDs = {}
                            local foundAnything = ""
                            local actualHour = os.date("!*t").hour
                            local Deleted = false
                            function TPReturner()
                               local Site;
                               if foundAnything == "" then
                                   Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' .. PlaceID .. '/servers/Public?sortOrder=Asc&limit=100'))
                               else
                                   Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' .. PlaceID .. '/servers/Public?sortOrder=Asc&limit=100&cursor=' .. foundAnything))
                               end
                               local ID = ""
                               if Site.nextPageCursor and Site.nextPageCursor ~= "null" and Site.nextPageCursor ~= nil then
                                   foundAnything = Site.nextPageCursor
                               end
                               local num = 0;
                               for i,v in pairs(Site.data) do
                                   local Possible = true
                                   ID = tostring(v.id)
                                   if tonumber(v.maxPlayers) > tonumber(v.playing) then
                                       for _,Existing in pairs(AllIDs) do
                                           if num ~= 0 then
                                               if ID == tostring(Existing) then
                                                   Possible = false
                                               end
                                           else
                                               if tonumber(actualHour) ~= tonumber(Existing) then
                                                   local delFile = pcall(function()
                                                       delfile("NotSameServers.json")
                                                       AllIDs = {}
                                                       table.insert(AllIDs, actualHour)
                                                   end)
                                               end
                                           end
                                           num = num + 1
                                       end
                                       if Possible == true then
                                           table.insert(AllIDs, ID)
                                           wait()
                                           pcall(function()
                                               writefile("NotSameServers.json", game:GetService('HttpService'):JSONEncode(AllIDs))
                                               wait()
                                               game:GetService("TeleportService"):TeleportToPlaceInstance(PlaceID, ID, game.Players.LocalPlayer)
                                           end)
                                           wait(4)
                                       end
                                   end
                               end
                            end
                            
                            function Teleport()
                               while wait() do
                                   pcall(function()
                                       TPReturner()
                                       if foundAnything ~= "" then
                                           TPReturner()
                                       end
                                   end)
                               end
                            end
                            
                            -- If you'd like to use a script before server hopping (Like a Automatic Chest collector you can put the Teleport() after it collected everything.
                            Teleport()
                        end)
                        local tab = win:Tab("RemoteSpy")
                            tab:Button("RSPY", function()
                                wait(2)
                                loadstring(game:HttpGet("https://raw.githubusercontent.com/78n/SimpleSpy/main/SimpleSpySource.lua"))()
                                end)  
                            tab:Button("infiniteyield ", function()
                                wait(2)
                                loadstring(game:HttpGet("https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source"))()
                                end)  
                        --- AFK
                wait(3)
                local VirtualUser=game:service'VirtualUser'
                game:service('Players').LocalPlayer.Idled:connect(function()
                VirtualUser:CaptureController()
                VirtualUser:ClickButton2(Vector2.new())
                end)
                --- AFK
                
        else
            local NotifyLib = loadstring(game:HttpGet("https://raw.githubusercontent.com/vKhonshu/intro/main/ui"))()
            NotifyLib.prompt('Password wrong', 'I cant help but enjoy hurting other people.', 3)
        end
    else
        local NotifyLib = loadstring(game:HttpGet("https://raw.githubusercontent.com/vKhonshu/intro/main/ui"))()
        NotifyLib.prompt('Enter the code, you idiot.', 'So you cant enjoy hurting other people.', 3)
    end
end

loginButton.MouseButton1Click:Connect(onLoginButtonClicked)

