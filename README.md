-- Gui to Lua
-- Version: 3.2

-- Instances:

local PlayerList = Instance.new("ScreenGui")
local Frame = Instance.new("ImageLabel")
local LightBlue = Instance.new("ImageLabel")
local Corner = Instance.new("UICorner")
local ImageLabel = Instance.new("ImageLabel")
local Corner_2 = Instance.new("UICorner")
local Heading = Instance.new("TextLabel")
local Corner_3 = Instance.new("UICorner")
local List = Instance.new("ScrollingFrame")
local Template = Instance.new("Frame")
local TemplateCorner = Instance.new("UICorner")
local Avatar = Instance.new("ImageLabel")
local UserName = Instance.new("TextLabel")
local UIGridLayout = Instance.new("UIGridLayout")

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

Corner_2.CornerRadius = UDim.new(0.150000006, 0)
Corner_2.Name = "Corner"
Corner_2.Parent = ImageLabel

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

Corner_3.CornerRadius = UDim.new(0.150000006, 0)
Corner_3.Name = "Corner"
Corner_3.Parent = Heading

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
		Template.Parent = List
		TemplateCorner.Parent = Template
		Template.Visible = true
		Avatar.Parent = Template
		UserName.Parent = Template
		Avatar.Image = game.Players:GetUserThumbnailAsync(Player.UserId, Enum.ThumbnailType.AvatarThumbnail, Enum.ThumbnailSize.Size420x420)
		UserName.Text = Player.Name
		Avatar.BackgroundTransparency = 1.000
	end
end

Fill()

while wait(0.1) do
	Fill()
	Heading.Text = "Players in this server " .. game.Players.NumPlayers .. "/" .. game.Players.MaxPlayers
end
