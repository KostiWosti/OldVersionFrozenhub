local ScreenGui = Instance.new("ScreenGui")
local FrozenHub = Instance.new("Frame")
local UICorner = Instance.new("UICorner")
local CloseButton = Instance.new("TextButton")
local UICorner_2 = Instance.new("UICorner")
local TextLabel = Instance.new("TextLabel")
local UICorner_3 = Instance.new("UICorner")
local FlyButton = Instance.new("TextButton")
local UICorner_4 = Instance.new("UICorner")
local TeleportSection = Instance.new("TextLabel")
local UICorner_5 = Instance.new("UICorner")
local BankTP = Instance.new("TextButton")
local UICorner_6 = Instance.new("UICorner")
local CasinoTP = Instance.new("TextButton")
local UICorner_7 = Instance.new("UICorner")
local ABAllGuns = Instance.new("TextButton")
local UICorner_8 = Instance.new("UICorner")
local AB = Instance.new("TextButton")
local UICorner_9 = Instance.new("UICorner")
local SchoolTP = Instance.new("TextButton")
local UICorner_10 = Instance.new("UICorner")
local HoodFitTP = Instance.new("TextButton")
local UICorner_11 = Instance.new("UICorner")
local HoodKicksTp = Instance.new("TextButton")
local UICorner_12 = Instance.new("UICorner")
local UPShop = Instance.new("TextButton")
local UICorner_13 = Instance.new("UICorner")
local DHShop = Instance.new("TextButton")
local UICorner_14 = Instance.new("UICorner")
local TrainTp = Instance.new("TextButton")
local UICorner_15 = Instance.new("UICorner")
local SewerTP = Instance.new("TextButton")
local UICorner_16 = Instance.new("UICorner")
local TopBankTP = Instance.new("TextButton")
local UICorner_17 = Instance.new("UICorner")
local Credits = Instance.new("TextLabel")
local UICorner_18 = Instance.new("UICorner")
local SpeedButton = Instance.new("TextButton")
local UICorner_19 = Instance.new("UICorner")
local JumpPower = Instance.new("TextButton")
local UICorner_20 = Instance.new("UICorner")
local GunsTP = Instance.new("TextButton")
local UICorner_21 = Instance.new("UICorner")

--Properties:

ScreenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

FrozenHub.Name = "FrozenHub"
FrozenHub.Parent = ScreenGui
FrozenHub.BackgroundColor3 = Color3.fromRGB(45, 45, 45)
FrozenHub.Position = UDim2.new(0.00987092033, 0, 0.620938599, 0)
FrozenHub.Size = UDim2.new(0, 450, 0, 280)
FrozenHub.Selectable = true 
FrozenHub.Active = true 
FrozenHub.Draggable = true 

UICorner.Parent = FrozenHub

CloseButton.Name = "CloseButton"
CloseButton.Parent = FrozenHub
CloseButton.BackgroundColor3 = Color3.fromRGB(11, 243, 255)
CloseButton.Position = UDim2.new(0.0155555559, 0, 0.021428572, 0)
CloseButton.Size = UDim2.new(0, 50, 0, 33)
CloseButton.Font = Enum.Font.SourceSans
CloseButton.Text = ""
CloseButton.TextColor3 = Color3.fromRGB(0, 0, 0)
CloseButton.TextSize = 14.000

UICorner_2.Parent = CloseButton

TextLabel.Parent = FrozenHub
TextLabel.BackgroundColor3 = Color3.fromRGB(11, 243, 255)
TextLabel.Position = UDim2.new(0.137777805, 0, 0.021428572, 0)
TextLabel.Size = UDim2.new(0, 256, 0, 41)
TextLabel.Font = Enum.Font.SciFi
TextLabel.Text = "Frozen Hub"
TextLabel.TextColor3 = Color3.fromRGB(0, 0, 0)
TextLabel.TextSize = 35.000

UICorner_3.Parent = TextLabel

FlyButton.Name = "FlyButton"
FlyButton.Parent = FrozenHub
FlyButton.BackgroundColor3 = Color3.fromRGB(11, 243, 255)
FlyButton.Position = UDim2.new(0.0155555559, 0, 0.221428558, 0)
FlyButton.Size = UDim2.new(0, 120, 0, 36)
FlyButton.Font = Enum.Font.SciFi
FlyButton.Text = "Fly"
FlyButton.TextColor3 = Color3.fromRGB(0, 0, 0)
FlyButton.TextSize = 35.000
FlyButton.MouseButton1Click:Connect(function()
	repeat wait() until game.Players.LocalPlayer.Character

	local player = game.Players.LocalPlayer
	local character = player.Character
	local humanoid = character:WaitForChild("Humanoid")
	local torso = character:WaitForChild("LowerTorso")
	local mouse = player:GetMouse()

	local enabled = false 

	mouse.KeyDown:Connect(function(key)
		if key == "x" then
			if enabled == false then
				enabled = true 
				local bodyvelocity = Instance.new("BodyVelocity", torso)
				bodyvelocity.MaxForce = Vector3.new(math.huge,math.huge,math.huge)

				while enabled == true do
					bodyvelocity.Velocity = mouse.Hit.lookVector * 100
					wait()
				end


			end

			if enabled == true then
				enabled = false 
				torso:FindFirstChild("BodyVelocity"):Destroy()
			end
		end
	end)
end)

UICorner_4.Parent = FlyButton

TeleportSection.Name = "TeleportSection"
TeleportSection.Parent = FrozenHub
TeleportSection.BackgroundColor3 = Color3.fromRGB(11, 243, 255)
TeleportSection.Position = UDim2.new(0.0155555559, 0, 0.596428573, 0)
TeleportSection.Size = UDim2.new(0, 198, 0, 26)
TeleportSection.Font = Enum.Font.SciFi
TeleportSection.Text = "Teleport Section"
TeleportSection.TextColor3 = Color3.fromRGB(0, 0, 0)
TeleportSection.TextSize = 25.000

UICorner_5.Parent = TeleportSection

BankTP.Name = "BankTP"
BankTP.Parent = FrozenHub
BankTP.BackgroundColor3 = Color3.fromRGB(11, 243, 255)
BankTP.Position = UDim2.new(0.0155555559, 0, 0.724999964, 0)
BankTP.Size = UDim2.new(0, 55, 0, 26)
BankTP.Font = Enum.Font.SciFi
BankTP.Text = "Bank"
BankTP.TextColor3 = Color3.fromRGB(0, 0, 0)
BankTP.TextSize = 20.000
BankTP.MouseButton1Click:Connect(function()
	game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-443.827301, 38.9954453, -283.855194, 0.0213130936, 8.4739753e-08, -0.999772847, 2.06969055e-08, 1, 8.52002273e-08, 0.999772847, -2.25080843e-08, 0.0213130936) 
end)

UICorner_6.Parent = BankTP

CasinoTP.Name = "CasinoTP"
CasinoTP.Parent = FrozenHub
CasinoTP.BackgroundColor3 = Color3.fromRGB(11, 243, 255)
CasinoTP.Position = UDim2.new(0.159999996, 0, 0.724999964, 0)
CasinoTP.Size = UDim2.new(0, 55, 0, 26)
CasinoTP.Font = Enum.Font.SciFi
CasinoTP.Text = "Casino"
CasinoTP.TextColor3 = Color3.fromRGB(0, 0, 0)
CasinoTP.TextSize = 20.000
CasinoTP.MouseButton1Click:Connect(function()
	game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1005.64337, 49.5979729, -140.114838, 0.999962509, -2.49530423e-08, -0.00865768455, 2.45369538e-08, 1, -4.8166374e-08, 0.00865768455, 4.79521347e-08, 0.999962509)
end)


UICorner_7.Parent = CasinoTP

ABAllGuns.Name = "ABAllGuns"
ABAllGuns.Parent = FrozenHub
ABAllGuns.BackgroundColor3 = Color3.fromRGB(11, 243, 255)
ABAllGuns.Position = UDim2.new(0.295555562, 0, 0.724999964, 0)
ABAllGuns.Size = UDim2.new(0, 55, 0, 26)
ABAllGuns.Font = Enum.Font.SciFi
ABAllGuns.Text = "AB 1"
ABAllGuns.TextColor3 = Color3.fromRGB(0, 0, 0)
ABAllGuns.TextSize = 20.000
ABAllGuns.MouseButton1Click:Connect(function()
	game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-875.140991, -33.8614006, -537.132446, -0.999922991, 8.72552786e-09, -0.0124095315, 8.01801203e-09, 1, 5.70636658e-08, 0.0124095315, 5.69597738e-08, -0.999922991)
end)

UICorner_8.Parent = ABAllGuns

AB.Name = "AB"
AB.Parent = FrozenHub
AB.BackgroundColor3 = Color3.fromRGB(11, 243, 255)
AB.Position = UDim2.new(0.437777758, 0, 0.724999964, 0)
AB.Size = UDim2.new(0, 55, 0, 26)
AB.Font = Enum.Font.SciFi
AB.Text = "AB 2"
AB.TextColor3 = Color3.fromRGB(0, 0, 0)
AB.TextSize = 20.000
AB.MouseButton1Click:Connect(function()
	game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-797.612305, -39.6511879, -898.220642, -0.977431357, 2.66475997e-08, 0.211253226, 2.53373837e-08, 1, -8.90895446e-09, -0.211253226, -3.3552876e-09, -0.977431357)
end)

UICorner_9.Parent = AB

SchoolTP.Name = "SchoolTP"
SchoolTP.Parent = FrozenHub
SchoolTP.BackgroundColor3 = Color3.fromRGB(11, 243, 255)
SchoolTP.Position = UDim2.new(0.575555563, 0, 0.724999964, 0)
SchoolTP.Size = UDim2.new(0, 55, 0, 26)
SchoolTP.Font = Enum.Font.SciFi
SchoolTP.Text = "School"
SchoolTP.TextColor3 = Color3.fromRGB(0, 0, 0)
SchoolTP.TextSize = 20.000
SchoolTP.MouseButton1Click:Connect(function()
	game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-619.982422, 21.2480221, 208.335999, -0.996029675, 5.03382296e-08, -0.0890220851, 4.26572058e-08, 1, 8.81846987e-08, 0.0890220851, 8.40371399e-08, -0.996029675)
end)

UICorner_10.Parent = SchoolTP

HoodFitTP.Name = "HoodFitTP"
HoodFitTP.Parent = FrozenHub
HoodFitTP.BackgroundColor3 = Color3.fromRGB(11, 243, 255)
HoodFitTP.Position = UDim2.new(0.159999967, 0, 0.853571415, 0)
HoodFitTP.Size = UDim2.new(0, 55, 0, 26)
HoodFitTP.Font = Enum.Font.SciFi
HoodFitTP.Text = "Hood Fit"
HoodFitTP.TextColor3 = Color3.fromRGB(0, 0, 0)
HoodFitTP.TextSize = 15.000
HoodFitTP.MouseButton1Click:Connect(function()
	game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-75.7986984, 21.7530231, -599.938843, 0.985586643, -2.58283865e-08, 0.169171333, 2.27611654e-08, 1, 2.00700985e-08, -0.169171333, -1.59302846e-08, 0.985586643)
end)

UICorner_11.Parent = HoodFitTP

HoodKicksTp.Name = "HoodKicksTp"
HoodKicksTp.Parent = FrozenHub
HoodKicksTp.BackgroundColor3 = Color3.fromRGB(11, 243, 255)
HoodKicksTp.Position = UDim2.new(0.0155555606, 0, 0.853571415, 0)
HoodKicksTp.Size = UDim2.new(0, 55, 0, 26)
HoodKicksTp.Font = Enum.Font.SciFi
HoodKicksTp.Text = "Hood Kicks"
HoodKicksTp.TextColor3 = Color3.fromRGB(0, 0, 0)
HoodKicksTp.TextSize = 10.000
HoodKicksTp.MouseButton1Click:Connect(function()
	game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-187.337204, 21.7530231, -410.240051, -0.0507876165, -6.08253217e-08, 0.9987095, 3.77629945e-08, 1, 6.28242915e-08, -0.9987095, 4.09049576e-08, -0.0507876165)
end)

UICorner_12.Parent = HoodKicksTp

UPShop.Name = "UP Shop"
UPShop.Parent = FrozenHub
UPShop.BackgroundColor3 = Color3.fromRGB(11, 243, 255)
UPShop.Position = UDim2.new(0.295555562, 0, 0.853571415, 0)
UPShop.Size = UDim2.new(0, 55, 0, 26)
UPShop.Font = Enum.Font.SciFi
UPShop.Text = "UP Shop"
UPShop.TextColor3 = Color3.fromRGB(0, 0, 0)
UPShop.TextSize = 15.000
UPShop.MouseButton1Click:Connect(function()
	game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(480.919006, 48.0030136, -596.770691, 0.999710441, -2.7938988e-08, -0.0240638703, 3.04541956e-08, 1, 1.04155745e-07, 0.0240638703, -1.04858429e-07, 0.999710441)
end)

UICorner_13.Parent = UPShop

DHShop.Name = "DH Shop"
DHShop.Parent = FrozenHub
DHShop.BackgroundColor3 = Color3.fromRGB(11, 243, 255)
DHShop.Position = UDim2.new(0.437777787, 0, 0.853571415, 0)
DHShop.Size = UDim2.new(0, 55, 0, 26)
DHShop.Font = Enum.Font.SciFi
DHShop.Text = "DH Shop"
DHShop.TextColor3 = Color3.fromRGB(0, 0, 0)
DHShop.TextSize = 15.000
DHShop.MouseButton1Click:Connect(function()
	game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-557.427612, 7.99787045, -736.275879, 0.03801734, 6.72411318e-08, 0.999277055, -4.68214516e-08, 1, -6.55084662e-08, -0.999277055, -4.42971455e-08, 0.03801734)
end)

UICorner_14.Parent = DHShop

TrainTp.Name = "TrainTp"
TrainTp.Parent = FrozenHub
TrainTp.BackgroundColor3 = Color3.fromRGB(11, 243, 255)
TrainTp.Position = UDim2.new(0.713333368, 0, 0.853571415, 0)
TrainTp.Size = UDim2.new(0, 55, 0, 26)
TrainTp.Font = Enum.Font.SciFi
TrainTp.Text = "Train"
TrainTp.TextColor3 = Color3.fromRGB(0, 0, 0)
TrainTp.TextSize = 20.000
TrainTp.MouseButton1Click:Connect(function()
	game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(583.734863, 34.4980125, -133.031525, 0.897819638, -8.82528539e-08, 0.440363318, 9.73705596e-08, 1, 1.88855998e-09, -0.440363318, 4.11828367e-08, 0.897819638)
end)

UICorner_15.Parent = TrainTp

SewerTP.Name = "SewerTP"
SewerTP.Parent = FrozenHub
SewerTP.BackgroundColor3 = Color3.fromRGB(11, 243, 255)
SewerTP.Position = UDim2.new(0.713333309, 0, 0.724999964, 0)
SewerTP.Size = UDim2.new(0, 55, 0, 26)
SewerTP.Font = Enum.Font.SciFi
SewerTP.Text = "Sewer"
SewerTP.TextColor3 = Color3.fromRGB(0, 0, 0)
SewerTP.TextSize = 20.000
SewerTP.MouseButton1Click:Connect(function()
	game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-421.873993, -21.2519798, 37.4928894, -0.999464154, -8.69155503e-09, -0.032732822, -9.90285987e-09, 1, 3.68436943e-08, 0.032732822, 3.71480979e-08, -0.999464154)
end)

UICorner_16.Parent = SewerTP

TopBankTP.Name = "TopBankTP"
TopBankTP.Parent = FrozenHub
TopBankTP.BackgroundColor3 = Color3.fromRGB(11, 243, 255)
TopBankTP.Position = UDim2.new(0.577777743, 0, 0.853571415, 0)
TopBankTP.Size = UDim2.new(0, 55, 0, 26)
TopBankTP.Font = Enum.Font.SciFi
TopBankTP.Text = "Top Bank"
TopBankTP.TextColor3 = Color3.fromRGB(0, 0, 0)
TopBankTP.TextSize = 14.000
TopBankTP.MouseButton1Click:Connect(function()
	game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-330.669373, 80.4318924, -289.412445, -0.0181988254, 1.17059592e-07, 0.999834359, 8.39122816e-09, 1, -1.16926245e-07, -0.999834359, 6.26191854e-09, -0.0181988254)
end)

UICorner_17.Parent = TopBankTP

Credits.Name = "Credits"
Credits.Parent = FrozenHub
Credits.BackgroundColor3 = Color3.fromRGB(11, 243, 255)
Credits.Position = UDim2.new(0.713333428, 0, 0.032142859, 0)
Credits.Size = UDim2.new(0, 128, 0, 34)
Credits.Font = Enum.Font.SciFi
Credits.Text = "Made by: Kostas#0001"
Credits.TextColor3 = Color3.fromRGB(0, 0, 0)
Credits.TextSize = 12.000

UICorner_18.Parent = Credits

SpeedButton.Name = "SpeedButton"
SpeedButton.Parent = FrozenHub
SpeedButton.BackgroundColor3 = Color3.fromRGB(11, 243, 255)
SpeedButton.Position = UDim2.new(0.0155555559, 0, 0.403571427, 0)
SpeedButton.Size = UDim2.new(0, 120, 0, 36)
SpeedButton.Font = Enum.Font.SciFi
SpeedButton.Text = "Change Speed(100)"
SpeedButton.TextColor3 = Color3.fromRGB(0, 0, 0)
SpeedButton.TextSize = 15.000
SpeedButton.MouseButton1Click:Connect(function()
	game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 100 
end)

UICorner_19.Parent = SpeedButton

JumpPower.Name = "JumpPower"
JumpPower.Parent = FrozenHub
JumpPower.BackgroundColor3 = Color3.fromRGB(11, 243, 255)
JumpPower.Position = UDim2.new(0.308888882, 0, 0.221428573, 0)
JumpPower.Size = UDim2.new(0, 120, 0, 36)
JumpPower.Font = Enum.Font.SciFi
JumpPower.Text = "Jump Power(100)"
JumpPower.TextColor3 = Color3.fromRGB(0, 0, 0)
JumpPower.TextSize = 15.000
JumpPower.MouseButton1Click:Connect(function()
	game.Players.LocalPlayer.Character.Humanoid.CharacterJumpPower = 100 
end)

UICorner_20.Parent = JumpPower

GunsTP.Name = "Guns TP"
GunsTP.Parent = FrozenHub
GunsTP.BackgroundColor3 = Color3.fromRGB(11, 243, 255)
GunsTP.Position = UDim2.new(0.475555509, 0, 0.596428573, 0)
GunsTP.Size = UDim2.new(0, 120, 0, 26)
GunsTP.Font = Enum.Font.SciFi
GunsTP.Text = "Guns TP"
GunsTP.TextColor3 = Color3.fromRGB(0, 0, 0)
GunsTP.TextSize = 30.000

UICorner_21.Parent = GunsTP

-- Scripts:

local function LZUXP_fake_script() -- CloseButton.LocalScript 
	local script = Instance.new('LocalScript', CloseButton)

	script.Parent.MouseButton1Click:Connect(function()
		script.Parent.Parent.Visible = false 
	end)
	
end
coroutine.wrap(LZUXP_fake_script)()
local function IYQDTHN_fake_script() -- CloseButton.LocalScript 
	local script = Instance.new('LocalScript', CloseButton)

	print("Hello world!")
	
end
coroutine.wrap(IYQDTHN_fake_script)()
