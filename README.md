repeat wait() until game:IsLoaded()
repeat wait() until game:GetService("Players")

----------------------------------- save
function loadcheck()
    local fileName = "RebornXer Hub King Lagacy [" .. game.Players.LocalPlayer.Name .. "].json"
    
    if not isfile(fileName) then
        writefile(fileName, game:GetService("HttpService"):JSONEncode(_G.SST))
        return
    end
end

pcall(function()
    _G.SST = {
        Select_Weapon = "Sword",Select_Method = "Upper",DistanceMob = "10",Auto_Sea_King = false,Auto_Ghost_Ship = false,Auto_Hydra = false,Hop_Mix = false,Auto_Hydra_Hop = false,Auto_Sea_King_Hop = false,Auto_Ghost_Ship_Hop = false,Auto_Skill = false,Black_Screen = false,Auto_Haki = true,Auto_Mr_Morther_Hop = false,Auto_Mr_Morther = false
    }
end)


function LoadSetting()
    local fileName = "RebornXer Hub King Lagacy [" .. game.Players.LocalPlayer.Name .. "].json"
    if isfile(fileName) then
        local fileContent = readfile(fileName)
        local success, decoded = pcall(function()
            return game:GetService("HttpService"):JSONDecode(fileContent)
        end)
        
        if success then
            _G.SST = decoded
        end
    else
        SS()
    end
end

function SS()
    local fileName = "RebornXer Hub King Lagacy [" .. game.Players.LocalPlayer.Name .. "].json"
    
    if isfile(fileName) then
        writefile(fileName, game:GetService("HttpService"):JSONEncode(_G.SST))
    else
        loadcheck()
    end
end

loadcheck()
LoadSetting()



	local OCui = game.CoreGui:FindFirstChild("RebormXerOC")
if OCui then
	OCui:Destroy()
end

local RebornXer = Instance.new("ScreenGui")
local Open = Instance.new("TextButton")
local fuckshit = Instance.new("UICorner")
local MODILEMAGE = Instance.new("ImageLabel")
local posto = Instance.new("UIStroke")

local ScreenGui = Instance.new("ScreenGui")
local ImageButton = Instance.new("ImageButton")

-- กำหนดค่าเริ่มต้น
ScreenGui.Parent = game.CoreGui
ScreenGui.Name = "RebormXerOC"
ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

ImageButton.Parent = ScreenGui
ImageButton.Name = "Open/CloseUi"
ImageButton.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
ImageButton.BorderSizePixel = 0
ImageButton.Position = UDim2.new(0.1, 0, 0.1, 0)
ImageButton.Size = UDim2.new(0, 45, 0, 45)
ImageButton.Draggable = true
ImageButton.Image = "rbxassetid://108287073891881"

-- ฟังก์ชันสำหรับการคลิก
local TweenService = game:GetService("TweenService")
ImageButton.MouseButton1Click:Connect(function()
    local ui = game:GetService("CoreGui"):FindFirstChild("RebornXer Hub") -- ค้นหา UI
    if ui and ui:FindFirstChild("Main") then -- ตรวจสอบว่ามี "Main" อยู่ใน UI
        local main = ui.Main
        if main.Size.X.Offset == 600 and main.Size.Y.Offset == 400 then
            local tween = TweenService:Create(
                main,
                TweenInfo.new(0.20, Enum.EasingStyle.Sine, Enum.EasingDirection.In), -- กำหนดเวลา 0.35 วินาที
                {Size = UDim2.new(0, 0, 0, 0)}
            )
            tween:Play() -- เล่น Tween
        else
            local tween = TweenService:Create(
                main,
                TweenInfo.new(0.20, Enum.EasingStyle.Sine, Enum.EasingDirection.Out), -- กำหนดเวลา 0.35 วินาที
                {Size = UDim2.new(0, 600, 0, 400)}
            )
            tween:Play() -- เล่น Tween
        end
    end
end)


fuckshit.Parent = Open

 MODILEMAGE.Name = "MODILEMAGE"
 MODILEMAGE.Parent = Open
 MODILEMAGE.BackgroundColor3 = Color3.fromRGB(51,255,255)
 MODILEMAGE.BackgroundTransparency = 1.000
 MODILEMAGE.BorderSizePixel = 0
 MODILEMAGE.Position = UDim2.new(0, 0.5, 0, 0)
 MODILEMAGE.Size = UDim2.new(0, 38, 0, 31)
 MODILEMAGE.Image = "rbxassetid://"
 
posto.Name = "posto"
 posto.Parent = Open
 posto.ApplyStrokeMode = Enum.ApplyStrokeMode.Border
 posto.Color = Color3.fromRGB(51,255,255)
 posto.LineJoinMode = Enum.LineJoinMode.Round
 posto.Thickness = 1
 posto.Transparency = 0
 posto.Enabled = true
 posto.Archivable = true



 _G.WindowBackgroundColor = Color3.fromRGB(0, 0, 0) -- พื้นหลังหน้าต่าง (ดำ)
 _G.BackgroundItemColor = Color3.fromRGB(30, 30, 30) -- พื้นหลังของไอเทม (ดำเข้ม)
 _G.TabWindowColor = Color3.fromRGB(20, 20, 20) -- สีแท็บหน้าต่าง (ดำเข้ม)
 _G.ContainerColor = Color3.fromRGB(40, 40, 40) -- สีคอนเทนเนอร์ (ดำเข้ม)
 _G.TitleTextColor = Color3.fromRGB(255, 255, 255) -- สีข้อความหัวเรื่อง (ขาว)
 _G.ImageColor = Color3.fromRGB(255, 255, 255) -- สีของรูปภาพ (ขาว)
 _G.LineThemeColor = Color3.fromRGB(255, 255, 255) -- สีเส้น (ขาว)
 _G.TabTextColor = Color3.fromRGB(255, 255, 255) -- สีข้อความในแท็บ (ขาว)
 _G.TabImageColor = Color3.fromRGB(255, 255, 255) -- สีรูปภาพในแท็บ (ขาว)
 _G.TabThemeColor = Color3.fromRGB(255, 255, 255) -- สีธีมของแท็บ (ขาว)
 _G.SectionColor = Color3.fromRGB(30, 30, 30) -- สีพื้นหลังของ Section (ดำเข้ม)
 _G.SectionImageColor = Color3.fromRGB(255, 255, 255) -- สีรูปภาพใน Section (ขาว)
 _G.SectionTextColor = Color3.fromRGB(255, 255, 255) -- สีข้อความใน Section (ขาว)
 _G.SectionOn = Color3.fromRGB(0, 255, 0) -- สีสถานะเปิดของ Section (เขียว)
 
_G.Color1 = Color3.fromRGB(255,255,255)
do local GUI = game.CoreGui:FindFirstChild("RebornXer Hub");if GUI then GUI:Destroy();end;if _G.Color == nil then
_G.Color = Color3.fromRGB(255,255,255)
end 
end

local tween = game:GetService("TweenService")
local tweeninfo = TweenInfo.new
local input = game:GetService("UserInputService")
local run = game:GetService("RunService")
local plr = game.Players.LocalPlayer
local mouse = plr:GetMouse()

local UserInputService = game:GetService("UserInputService")
local TweenService = game:GetService("TweenService")

local function MakeDraggable(topbarobject, object)
	local Dragging = nil
	local DragInput = nil
	local DragStart = nil
	local StartPosition = nil

	local function Update(input)
		local Delta = input.Position - DragStart
		local pos = UDim2.new(StartPosition.X.Scale, StartPosition.X.Offset + Delta.X, StartPosition.Y.Scale, StartPosition.Y.Offset + Delta.Y)
		local Tween = TweenService:Create(object, TweenInfo.new(0.15), {Position = pos})
		Tween:Play()
	end

	topbarobject.InputBegan:Connect(
		function(input)
			if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
				Dragging = true
				DragStart = input.Position
				StartPosition = object.Position

				input.Changed:Connect(
					function()
						if input.UserInputState == Enum.UserInputState.End then
							Dragging = false
						end
					end
				)
			end
		end
	)

	topbarobject.InputChanged:Connect(
		function(input)
			if
				input.UserInputType == Enum.UserInputType.MouseMovement or
				input.UserInputType == Enum.UserInputType.Touch
			then
				DragInput = input
			end
		end
	)

	UserInputService.InputChanged:Connect(
		function(input)
			if input == DragInput and Dragging then
				Update(input)
			end
		end
	)
end

local Update = {}

function Update:AddWindow(name,logo,keybind)
	local uihide = false
	local abc = false
	local logo = logo or 0
	local currentpage = ""
	local keybind = keybind or Enum.KeyCode.RightControl
	local yoo = string.gsub(tostring(keybind),"Enum.KeyCode.","")
	
	local RebornXer_Hub = Instance.new("ScreenGui")
	RebornXer_Hub.Name = "RebornXer Hub"
	RebornXer_Hub.Parent = game.CoreGui
	RebornXer_Hub.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

local osfunc = {}
 local osfunc2 = {}
	local Main = Instance.new("Frame")
	local WindowStrokemain = Instance.new("UIStroke")
	Main.Name = "Main"
	Main.Parent = RebornXer_Hub
	Main.ClipsDescendants = true
	Main.AnchorPoint = Vector2.new(0.5,0.5)
	Main.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
	Main.Position = UDim2.new(0.5, 0, 0.5, 0)
	Main.Size = UDim2.new(0, 0, 0, 0)
	
	WindowStrokemain.Name = "WindowStroke"
 WindowStrokemain.Parent = Main
 WindowStrokemain.ApplyStrokeMode = Enum.ApplyStrokeMode.Border
 WindowStrokemain.Color = Color3.fromRGB(255,255,255)
 WindowStrokemain.LineJoinMode = Enum.LineJoinMode.Round
 WindowStrokemain.Thickness = 1
 WindowStrokemain.Transparency = 0
 WindowStrokemain.Enabled = true
 WindowStrokemain.Archivable = true
	
	Main:TweenSize(UDim2.new(0, 600, 0, 400),"Out","Quad",0,true)

	local MCNR = Instance.new("UICorner")
	MCNR.Name = "MCNR"
	MCNR.Parent = Main

	local Top = Instance.new("Frame")
	Top.Name = "Top"
	Top.Position = UDim2.new(0,0,0,4)
	Top.Parent = Main
	Top.BackgroundColor3 = Color3.fromRGB(45, 45, 45)
	Top.Size = UDim2.new(0, 560, 0, 28)



	local Logo = Instance.new("ImageLabel")
	Logo.Name = "Logo"
	Logo.Parent = Top
	Logo.BackgroundColor3 = Color3.fromRGB(255,255,255)
	Logo.BackgroundTransparency = 1.000
	Logo.Position = UDim2.new(0, 9, 0, 1)
	Logo.Size = UDim2.new(0, 30, 0, 25)
	Logo.Image = "rbxassetid://"..tostring(logo)

	local Name = Instance.new("TextLabel")
	Name.Name = "Name"
	Name.Parent = Top
	Name.BackgroundColor3 = Color3.fromRGB(0,255,255)
	Name.BackgroundTransparency = 1.000
	Name.Position = UDim2.new(0.1, 0, 0, 0)
	Name.Size = UDim2.new(0, 80, 0, 27)
	Name.Font = Enum.Font.Code
	Name.RichText = true;
	Name.Text = name
	Name.TextColor3 = Color3.fromRGB(225, 225, 225)
	Name.TextSize = 15.000

local LocalizationService = game:GetService("LocalizationService")
 local Players = game:GetService("Players")
 local player = Players.LocalPlayer
 local name = player.Name
 local result, code = pcall(function()
	 return LocalizationService:GetCountryRegionForPlayerAsync(player)
 end)
 
function osfunc:Refresh(textadd)
 ServerTime.Text = textadd
 end
 function osfunc2:Refresh(textadd2)
 ServerDate.Text = textadd2
 end

 
local ListNof = Instance.new("Frame")
	local NofList = Instance.new("UIListLayout")

	ListNof.Name = "ListNof"
	ListNof.Parent = RebornXer_Hub
	ListNof.BackgroundColor3 = Color3.fromRGB(255,255,255)
	ListNof.BackgroundTransparency = 1.000
	ListNof.Position = UDim2.new(0.778017223, 0, -0.00217864919, 0)
	ListNof.Size = UDim2.new(0, 206, 0, 400)

	NofList.Name = "NofList"
	NofList.Parent = ListNof
	NofList.SortOrder = Enum.SortOrder.LayoutOrder
	NofList.VerticalAlignment = Enum.VerticalAlignment.Top
	
	function Update:Nof(txt,tine)
		spawn(function()
			local Nof1 = Instance.new("Frame")
			local Nof2 = Instance.new("Frame")
			local Nof3 = Instance.new("Frame")
			local NofLabel = Instance.new("TextLabel")
			local slidenof = Instance.new("Frame")
			local Slide2 = Instance.new("Frame")

			Nof1.Name = "Nof1"
			Nof1.Parent = ListNof
			Nof1.BackgroundColor3 = Color3.fromRGB(51,255,255)
			Nof1.BackgroundTransparency = 1.000
			Nof1.BorderSizePixel = 0
			Nof1.Size = UDim2.new(0, 206, 0, 83)

			Nof2.Name = "Nof2"
			Nof2.Parent = Nof1
			Nof2.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
			Nof2.BorderColor3 = Color3.fromRGB(0, 0, 0)
			Nof2.Position = UDim2.new(0, 0, 0.0120481923, 0)
			Nof2.Size = UDim2.new(0, 189, 0, 65)
			Instance.new("UICorner",Nof2)
			Instance.new("UICorner",slidenof)
			Instance.new("UICorner",Slide2)


			Nof3.Name = "Nof3"
			Nof3.Parent = Nof1
			Nof3.BackgroundColor3 = Color3.fromRGB(90, 90, 255)
			Nof3.BackgroundTransparency = 1
			Nof3.BorderSizePixel = 0
			Nof3.Position = UDim2.new(0, 0, 0.638554215, 0)
			Nof3.Size = UDim2.new(0, 189, 0, 7)

			NofLabel.Name = "NofLabel"
			NofLabel.Parent = Nof1
			NofLabel.BackgroundColor3 = Color3.fromRGB(51,255,255)
			NofLabel.BackgroundTransparency = 1.000
			NofLabel.BorderSizePixel = 0
			NofLabel.Position = UDim2.new(0, 0, 0.00463949936, 0)
			NofLabel.Size = UDim2.new(0, 188, 0, 52)
			NofLabel.ZIndex = 4
			NofLabel.Font = Enum.Font.Code
			NofLabel.TextColor3 = main_color or Color3.fromRGB(51,255,255)
			NofLabel.TextScaled = false
			NofLabel.TextSize = 18.000
			NofLabel.TextStrokeTransparency = 0.100
			NofLabel.TextTransparency = 0.100
			NofLabel.TextWrapped = true
			NofLabel.Text = txt or ""

			slidenof.Name = "slidenof"
			slidenof.Parent = Nof1
			slidenof.BackgroundColor3 = Color3.fromRGB(100, 100, 255)
			slidenof.BorderSizePixel = 0
			slidenof.Position = UDim2.new(0, 0, 0.638554215, 0)
			slidenof.Size = UDim2.new(0, 189, 0, 7)

			Slide2.Name = "Slide2"
			Slide2.Parent = Nof1
			Slide2.BorderSizePixel = 0
			Slide2.BackgroundColor3 = main_color or Color3.fromRGB(51,255,255)
			Slide2.BorderColor3 = Color3.fromRGB(0, 0, 0)
			Slide2.Position = UDim2.new(0, 0, 0.0120481923, 0)
			Slide2.Size = UDim2.new(0, 0, 0, 65)
			Slide2.ZIndex = 15
			Slide2.Visible = false

			tween:Create(slidenof,tweeninfo(tine or 2),{Size = UDim2.new(0, 0, 0, 7)}):Play()
			wait(tine or 2)
			Slide2.Visible = true
			tween:Create(Slide2,tweeninfo(0.2),{Size = UDim2.new(0, 190, 0, 65)}):Play()
			wait(0.2)
			tween:Create(Slide2,tweeninfo(0.2),{Size = UDim2.new(0, 0, 0, 65)}):Play()
			tween:Create(Nof3,tweeninfo(0.2),{Size = UDim2.new(0, 0, 0, 7)}):Play()
			tween:Create(NofLabel,tweeninfo(0.2),{Size = UDim2.new(0, 0, 0, 52)}):Play()
			tween:Create(Nof2,tweeninfo(0.2),{Size = UDim2.new(0, 0, 0, 65)}):Play()
			wait(0.2)
			Nof2.Visible = false
			game.Debris:AddItem(Nof1,0)
		end)
	end

 
function Update:AddNotification(textdesc)
    local NotificationFrame = Instance.new("Frame")
    local OkayBtn = Instance.new("TextButton")
    local OkayBtnCorner = Instance.new("UICorner")
    local NotificationTitle = Instance.new("TextLabel")
    local NotificationDesc = Instance.new("TextLabel")
    local NotifCorner = Instance.new("UICorner")
    local NotifHolderUIStroke = Instance.new("UIStroke")
    local Line = Instance.new("Frame")

    local SectionColor = _G.SectionColor or Color3.fromRGB(255, 255, 255)
    local defaultOkayColor = Color3.fromRGB(12, 12, 12)

    NotificationFrame.Name = "NotificationFrame"
    NotificationFrame.Parent = RebornXer_Hub
    NotificationFrame.AnchorPoint = Vector2.new(0.5, 0.5) -- ตั้งจุดยึดตรงกลาง
    NotificationFrame.BackgroundColor3 = Color3.fromRGB(15, 15, 15)
    NotificationFrame.BorderColor3 = SectionColor
    NotificationFrame.BorderSizePixel = 0
    NotificationFrame.ClipsDescendants = true
    NotificationFrame.Position = UDim2.new(0.5, 0, 0.5, 0) -- ตั้งตำแหน่งตรงกลางจอ
    NotificationFrame.Size = UDim2.new(0, 0, 0, 0)

    NotificationFrame:TweenSize(UDim2.new(0, 400, 0, 200), Enum.EasingDirection.Out, Enum.EasingStyle.Quart, .6, true)

    NotifCorner.Parent = NotificationFrame
    NotifCorner.CornerRadius = UDim.new(0, 10) -- เพิ่มความโค้งเล็กน้อย

    NotifHolderUIStroke.Parent = NotificationFrame
    NotifHolderUIStroke.ApplyStrokeMode = Enum.ApplyStrokeMode.Border
    NotifHolderUIStroke.Color = SectionColor
    NotifHolderUIStroke.Thickness = 1

    OkayBtn.Name = "OkayBtn"
    OkayBtn.Parent = NotificationFrame
    OkayBtn.BackgroundColor3 = defaultOkayColor
    OkayBtn.BorderSizePixel = 1
    OkayBtn.BorderColor3 = SectionColor
    OkayBtn.Position = UDim2.new(0.95, -25, 0.02, 0) -- ปุ่มปิดอยู่มุมขวาบน
    OkayBtn.Size = UDim2.new(0, 30, 0, 30)
    OkayBtn.Text = "X"
    OkayBtn.TextColor3 = Color3.fromRGB(255, 0, 0)
    OkayBtn.TextSize = 22.000

    OkayBtnCorner.CornerRadius = UDim.new(0, 5)
    OkayBtnCorner.Parent = OkayBtn

    NotificationTitle.Parent = NotificationFrame
    NotificationTitle.BackgroundTransparency = 1.000
    NotificationTitle.Position = UDim2.new(0.5, -200, 0, 20) -- ตำแหน่งกลาง
    NotificationTitle.Size = UDim2.new(0, 400, 0, 40)
    NotificationTitle.Font = Enum.Font.Code
    NotificationTitle.Text = "Notification"
    NotificationTitle.TextColor3 = Color3.fromRGB(0, 255, 255)
    NotificationTitle.TextSize = 28.000
    NotificationTitle.TextXAlignment = Enum.TextXAlignment.Center

    Line.Parent = NotificationFrame
    Line.BackgroundColor3 = SectionColor
    Line.BorderSizePixel = 0
    Line.Position = UDim2.new(0, 0, 0, 70)
    Line.Size = UDim2.new(1, 0, 0, 2)

    NotificationDesc.Parent = NotificationFrame
    NotificationDesc.BackgroundTransparency = 1.000
    NotificationDesc.Position = UDim2.new(0.5, -180, 0, 80)
    NotificationDesc.Size = UDim2.new(0, 360, 0, 100) -- ปรับขนาดข้อความให้เหมาะกับกรอบ
    NotificationDesc.Font = Enum.Font.Code
    NotificationDesc.Text = textdesc
    NotificationDesc.TextColor3 = _G.SectionTextColor or Color3.fromRGB(255, 255, 255)
    NotificationDesc.TextSize = 18.000
    NotificationDesc.TextWrapped = true
    NotificationDesc.TextXAlignment = Enum.TextXAlignment.Center

    OkayBtn.MouseEnter:Connect(function()
        TweenService:Create(OkayBtn, TweenInfo.new(.3, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), {BackgroundColor3 = Color3.fromRGB(30, 30, 30)}):Play()
    end)

    OkayBtn.MouseLeave:Connect(function()
        TweenService:Create(OkayBtn, TweenInfo.new(.2, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), {BackgroundColor3 = defaultOkayColor}):Play()
    end)

    OkayBtn.MouseButton1Click:Connect(function()
        NotificationFrame:TweenSize(UDim2.new(0, 0, 0, 0), Enum.EasingDirection.Out, Enum.EasingStyle.Quart, .6, true)
        wait(0.6)
        NotificationFrame:Destroy()
    end)
end



local Tab = Instance.new("ImageLabel")
local WindowStrokelol = Instance.new("UIStroke")
 Tab.Name = "Tab"
 Tab.Parent = Top
 Tab.BackgroundColor3 = Color3.fromRGB(42, 42, 42)
 Tab.ImageTransparency = 1
 Tab.Position = UDim2.new(0, 160, 0, -2)
 Tab.Size = UDim2.new(0, 410, 0, 29)
 Tab.Image = "rbxassetid://6675147486"
 
 WindowStrokelol.Name = "WindowStroke"
 WindowStrokelol.Parent = Tab
 WindowStrokelol.ApplyStrokeMode = Enum.ApplyStrokeMode.Border
 WindowStrokelol.Color = Color3.fromRGB(255,255,255)
 WindowStrokelol.LineJoinMode = Enum.LineJoinMode.Round
 WindowStrokelol.Thickness = 1
 WindowStrokelol.Transparency = 0
 WindowStrokelol.Enabled = true
 WindowStrokelol.Archivable = true
 
 local TCNR = Instance.new("UICorner")
 TCNR.Name = "TCNR"
 TCNR.Parent = Tab
 
 local ScrollTab = Instance.new("ScrollingFrame")
 ScrollTab.Name = "ScrollTab"
 ScrollTab.Parent = Tab
 ScrollTab.Active = true
 ScrollTab.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
 ScrollTab.BackgroundTransparency = 0
 ScrollTab.Size = UDim2.new(0, 433, 0, 29)
 ScrollTab.CanvasSize = UDim2.new(0, 0, 0, 0)
 ScrollTab.ScrollBarThickness = 0
 
 local PLL = Instance.new("UIListLayout")
 PLL.Name = "PLL"
 PLL.Parent = ScrollTab
 PLL.FillDirection = Enum.FillDirection.Horizontal
 PLL.SortOrder = Enum.SortOrder.LayoutOrder
 PLL.Padding = UDim.new(0)
 
 local PPD = Instance.new("UIPadding")
 PPD.Name = "PPD"
 PPD.Parent = ScrollTab
 PPD.PaddingLeft = UDim.new(0.01)
 
 local Page = Instance.new("Frame")
 local WindowStrokeshit = Instance.new("UIStroke")
 Page.Name = "Page"
 Page.Parent = Main
 Page.BackgroundColor3 = Color3.fromRGB(42, 42, 42)
 Page.BackgroundTransparency = 1
 Page.Position = UDim2.new(0, 1, 0.100000003, -5)
 Page.Size = UDim2.new(0, 300, 0, 380)
 
 WindowStrokeshit.Name = "WindowStroke"
 WindowStrokeshit.Parent = Page
 WindowStrokeshit.ApplyStrokeMode = Enum.ApplyStrokeMode.Border
 WindowStrokeshit.Color = Color3.fromRGB(255,255,255)
 WindowStrokeshit.LineJoinMode = Enum.LineJoinMode.Round
 WindowStrokeshit.Thickness = 1
 WindowStrokeshit.Transparency = 0
 WindowStrokeshit.Archivable = false
 WindowStrokeshit.Enabled = true
 
 local lolshit = Instance.new("UICorner")
 
 lolshit.Parent = Top1
 
 
 local PCNR = Instance.new("UICorner")
 PCNR.Name = "PCNR"
 PCNR.Parent = Page
 
 local MainPage = Instance.new("Frame")
 MainPage.Name = "MainPage"
 MainPage.Parent = Page
 MainPage.ClipsDescendants = true
 MainPage.BackgroundColor3 = Color3.fromRGB(255,255,255)
 MainPage.BackgroundTransparency = 1.000
 MainPage.Size = UDim2.new(0, 300, 0, 380)
 
 local PageList = Instance.new("Folder")
 PageList.Name = "PageList"
 PageList.Parent = MainPage
 
 local UIPageLayout = Instance.new("UIPageLayout")
 
 UIPageLayout.Parent = PageList
 UIPageLayout.SortOrder = Enum.SortOrder.LayoutOrder
 UIPageLayout.EasingDirection = Enum.EasingDirection.InOut
 UIPageLayout.EasingStyle = Enum.EasingStyle.Quad
 UIPageLayout.FillDirection = Enum.FillDirection.Vertical
 UIPageLayout.Padding = UDim.new(0, 15)
 UIPageLayout.TweenTime = 0.400
 UIPageLayout.GamepadInputEnabled = false
 UIPageLayout.ScrollWheelInputEnabled = false
 UIPageLayout.TouchInputEnabled = false

local Page2 = Instance.new("Frame")
 local WindowStrokeshit2 = Instance.new("UIStroke")
 Page2.Name = "Page2"
 Page2.Parent = Main
 Page2.BackgroundColor3 = Color3.fromRGB(42, 42, 42)
 Page2.BackgroundTransparency = 1
 Page2.Position = UDim2.new(0, 302, 0.100000003, -5)
 Page2.Size = UDim2.new(0, 300, 0, 378)
 
 WindowStrokeshit2.Name = "WindowStroke"
 WindowStrokeshit2.Parent = Page2
 WindowStrokeshit2.ApplyStrokeMode = Enum.ApplyStrokeMode.Border
 WindowStrokeshit2.Color = Color3.fromRGB(255,255,255)
 WindowStrokeshit2.LineJoinMode = Enum.LineJoinMode.Round
 WindowStrokeshit2.Thickness = 1
 WindowStrokeshit2.Transparency = 0
 WindowStrokeshit2.Archivable = false
 WindowStrokeshit2.Enabled = true
 
 local lolshit2 = Instance.new("UICorner")
 
 lolshit2.Parent = Top1
 
 
 local PCNR2 = Instance.new("UICorner")
 PCNR2.Name = "PCNR"
 PCNR2.Parent = Page2
 
 local MainPage2 = Instance.new("Frame")
 MainPage2.Name = "MainPage"
 MainPage2.Parent = Page2
 MainPage2.ClipsDescendants = true
 MainPage2.BackgroundColor3 = Color3.fromRGB(255,255,255)
 MainPage2.BackgroundTransparency = 1.000
 MainPage2.Size = UDim2.new(0, 300, 0, 378)
 
 local PageList2 = Instance.new("Folder")
 PageList2.Name = "PageList"
 PageList2.Parent = MainPage2
 
 local UIPageLayout2 = Instance.new("UIPageLayout")
 
 UIPageLayout2.Parent = PageList2
 UIPageLayout2.SortOrder = Enum.SortOrder.LayoutOrder
 UIPageLayout2.EasingDirection = Enum.EasingDirection.InOut
 UIPageLayout2.EasingStyle = Enum.EasingStyle.Quad
 UIPageLayout2.FillDirection = Enum.FillDirection.Vertical
 UIPageLayout2.Padding = UDim.new(0, 15)
 UIPageLayout2.TweenTime = 0.400
 UIPageLayout2.GamepadInputEnabled = false
 UIPageLayout2.ScrollWheelInputEnabled = false
 UIPageLayout2.TouchInputEnabled = false
 
 MakeDraggable(Top,Main)
 
local TweenService = game:GetService("TweenService")
local UserInputService = game:GetService("UserInputService")

local uihide = false
UserInputService.InputBegan:Connect(function(input)
    if input.KeyCode == Enum.KeyCode[yoo] then -- แก้ไขเป็น KeyCode ที่ต้องการ
        if uihide == false then
            uihide = true
            local tween = TweenService:Create(
                Main,
                TweenInfo.new(0.35, Enum.EasingStyle.Sine, Enum.EasingDirection.In), -- กำหนดเวลา 1 วินาที
                {Size = UDim2.new(0, 0, 0, 0)}
            )
            tween:Play()
        else
            uihide = false
            local tween = TweenService:Create(
                Main,
                TweenInfo.new(0.35, Enum.EasingStyle.Sine, Enum.EasingDirection.Out), -- กำหนดเวลา 1 วินาที
                {Size = UDim2.new(0, 600, 0, 400)}
            )
            tween:Play()
        end
    end
end)
	


 
	local uitab = {}
	
	function uitab:AddTab(text, img)
		local TabButton = Instance.new("TextButton")
		local TabImage = Instance.new("ImageLabel")
		local WindowStroke = Instance.new("UIStroke")
		local Label3 = Instance.new("TextLabel")
		local LabelTitle = Instance.new("TextLabel")
local LabelTitle = Instance.new("TextLabel")

		TabButton.Parent = ScrollTab
		TabButton.Name = text.."Server"
		TabButton.Text = text
		TabButton.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
		TabButton.BackgroundTransparency = 0.1
		TabButton.Position = UDim2.new(0, 2, 0, 0)
		TabButton.Size = UDim2.new(0, 100, 0, 28)
		TabButton.Font = Enum.Font.Code
		TabButton.TextColor3 = Color3.fromRGB(255, 225, 225)
		TabButton.TextSize = 12.000
		TabButton.TextTransparency = 0
		
		
local MCNR1 = Instance.new("UICorner")
	MCNR1.Name = "MCNR"
	MCNR1.Parent = TabButton

WindowStroke.Name = "WindowStroke"
 WindowStroke.Parent = TabButton
 WindowStroke.ApplyStrokeMode = Enum.ApplyStrokeMode.Border
 WindowStroke.Color = Color3.fromRGB(45,45,45)
 WindowStroke.LineJoinMode = Enum.LineJoinMode.Round
 WindowStroke.Thickness = 1
 WindowStroke.Transparency = 0
 WindowStroke.Enabled = true
 WindowStroke.Archivable = true

		local MainFramePage = Instance.new("ScrollingFrame")
		MainFramePage.Name = text.."_Page"
		MainFramePage.Parent = PageList
		MainFramePage.Active = true
		MainFramePage.BackgroundColor3 = Color3.fromRGB(51,255,255)
		MainFramePage.BackgroundTransparency = 1.000
		MainFramePage.BorderSizePixel = 1
		MainFramePage.Size = UDim2.new(0, 390, 0, 370)
		MainFramePage.CanvasSize = UDim2.new(0, 0, 0, 0)
		MainFramePage.ScrollBarThickness = 0
		

		
		local UIPadding = Instance.new("UIPadding")
		local UIListLayout = Instance.new("UIListLayout")
		
		UIPadding.Parent = MainFramePage
		UIPadding.PaddingLeft = UDim.new(0, 10)
		UIPadding.PaddingTop = UDim.new(0, 10)

		UIListLayout.Padding = UDim.new(0,4)
		UIListLayout.Parent = MainFramePage
		UIListLayout.SortOrder = Enum.SortOrder.LayoutOrder
		
		TabButton.MouseButton1Click:Connect(function()
        Sound = Instance.new("Sound", game:GetService("Workspace")) -- ตรงนี้ไม่ต้องไปสน นาจา ;0;
Sound.Name = "Notify" -- ชื่อเสียง \;
Sound.SoundId = "rbxassetid://903267862" -- เลขขขขขเสียง ;/
Sound.Looped = false -- วนลูป :>
Sound.Playing = true -- เล่นเสียง :<
Sound.Volume = 1 -- ระดับเสียงงงงงงง ;-;
			for i,v in next, ScrollTab:GetChildren() do
				if v:IsA("TextButton") then
					TweenService:Create(
						v,
						TweenInfo.new(0,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
						{TextTransparency = 0}
					):Play()
				end
				TweenService:Create(
					TabButton,
					TweenInfo.new(0,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
					{TextTransparency = 0}
				):Play()
			end
			for i,v in next, PageList:GetChildren() do
				currentpage = string.gsub(TabButton.Name,"Server","").."_Page"
				if v.Name == currentpage then
					UIPageLayout:JumpTo(v)
				end
			end
		end)

		if abc == false then
            
			for i,v in next, ScrollTab:GetChildren() do
				if v:IsA("TextButton") then
					TweenService:Create(
						v,
						TweenInfo.new(0,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
						{TextTransparency = 0}
					):Play()
				end
				TweenService:Create(
					TabButton,
					TweenInfo.new(0,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
					{TextTransparency = 0}
				):Play()
			end
			UIPageLayout:JumpToIndex(0)
			abc = true
		end
		
		game:GetService("RunService").Stepped:Connect(function()
			pcall(function()
				MainFramePage.CanvasSize = UDim2.new(0,0,0,UIListLayout.AbsoluteContentSize.Y + 20)
				ScrollTab.CanvasSize = UDim2.new(0,PLL.AbsoluteContentSize.X + 20,0,0)
			end)
		end)
 
 coroutine.wrap(function()
 while wait() do
 end
 end)()
 
	 
 
 coroutine.wrap(function()
 while wait() do
 end
 end)()
	
	
	local MainFramePage2 = Instance.new("ScrollingFrame")
		MainFramePage2.Name = text.."_Page"
		MainFramePage2.Parent = PageList2
		MainFramePage2.Active = true
		MainFramePage2.BackgroundColor3 = Color3.fromRGB(51,255,255)
		MainFramePage2.BackgroundTransparency = 1.000
		MainFramePage2.BorderSizePixel = 0
		MainFramePage2.Size = UDim2.new(0, 320, 0, 370)
		MainFramePage2.CanvasSize = UDim2.new(0, 0, 0, 0)
		MainFramePage2.ScrollBarThickness = 0
		
		local UIPadding2 = Instance.new("UIPadding")
		local UIListLayout2 = Instance.new("UIListLayout")
		
		UIPadding2.Parent = MainFramePage2
		UIPadding2.PaddingLeft = UDim.new(0, 10)
		UIPadding2.PaddingTop = UDim.new(0, 10)

		UIListLayout2.Padding = UDim.new(0,4)
		UIListLayout2.Parent = MainFramePage2
		UIListLayout2.SortOrder = Enum.SortOrder.LayoutOrder
		
		TabButton.MouseButton1Click:Connect(function()
			for i,v in next, ScrollTab:GetChildren() do
				if v:IsA("TextButton") then
					TweenService:Create(
						v,
						TweenInfo.new(0,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
						{TextTransparency = 0}
					):Play()
				end
				TweenService:Create(
					TabButton,
					TweenInfo.new(0,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
					{TextTransparency = 0}
				):Play()
			end
			for i,v in next, PageList2:GetChildren() do
				currentpage = string.gsub(TabButton.Name,"Server","").."_Page"
				if v.Name == currentpage then
					UIPageLayout2:JumpTo(v)
				end
			end
		end)

		if abc == false then
			for i,v in next, ScrollTab:GetChildren() do
				if v:IsA("TextButton") then
					TweenService:Create(
						v,
						TweenInfo.new(0,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
						{TextTransparency = 0}
					):Play()
				end
				TweenService:Create(
					TabButton,
					TweenInfo.new(0,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
					{TextTransparency = 0}
				):Play()
			end
			UIPageLayout2:JumpToIndex(0)
			abc = true
		end
		
		game:GetService("RunService").Stepped:Connect(function()
			pcall(function()
				MainFramePage2.CanvasSize = UDim2.new(0,0,0,UIListLayout2.AbsoluteContentSize.Y + 20)
				ScrollTab.CanvasSize = UDim2.new(0,PLL.AbsoluteContentSize.X + 20,0,0)
			end)
		end)
 
 coroutine.wrap(function()
 while wait() do
 end
 end)()
 
	 
 
 coroutine.wrap(function()
 while wait() do
 end
 end)()
	local abcd = false
	 function uitab:AddTabH(text,img)
	 local mainDiscord = Instance.new("ImageButton")

	 mainDiscord.Name = "mainDiscord"
    mainDiscord.Parent = Top
    mainDiscord.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    mainDiscord.BackgroundTransparency = 1.000
    mainDiscord.Position = UDim2.new(0, 565, 0, 0)
    mainDiscord.Size = UDim2.new(0, 30, 0, 30)
    mainDiscord.Image = "rbxassetid://"..tostring(img)
    mainDiscord.ImageColor3 = Color3.fromRGB(200, 200, 200)
    
        local MainFramePage = Instance.new("ScrollingFrame")
		MainFramePage.Name = text.."_Page"
		MainFramePage.Parent = PageList
		MainFramePage.Active = true
		MainFramePage.BackgroundColor3 = Color3.fromRGB(51,255,255)
		MainFramePage.BackgroundTransparency = 1.000
		MainFramePage.BorderSizePixel = 1
		MainFramePage.Size = UDim2.new(0, 390, 0, 370)
		MainFramePage.CanvasSize = UDim2.new(0, 0, 0, 0)
		MainFramePage.ScrollBarThickness = 0
		

		
		local UIPadding = Instance.new("UIPadding")
		local UIListLayout = Instance.new("UIListLayout")
		
		UIPadding.Parent = MainFramePage
		UIPadding.PaddingLeft = UDim.new(0, 10)
		UIPadding.PaddingTop = UDim.new(0, 10)

		UIListLayout.Padding = UDim.new(0,4)
		UIListLayout.Parent = MainFramePage
		UIListLayout.SortOrder = Enum.SortOrder.LayoutOrder
		
		mainDiscord.MouseButton1Click:Connect(function()
        Sound = Instance.new("Sound", game:GetService("Workspace")) -- ตรงนี้ไม่ต้องไปสน นาจา ;0;
Sound.Name = "Notify" -- ชื่อเสียง \;
Sound.SoundId = "rbxassetid://3020841054" -- เลขขขขขเสียง ;/
Sound.Looped = false -- วนลูป :>
Sound.Playing = true -- เล่นเสียง :<
Sound.Volume = 1 -- ระดับเสียงงงงงงง ;-;
			for i,v in next, ScrollTab:GetChildren() do
				if v:IsA("TextButton") then
					TweenService:Create(
						v,
						TweenInfo.new(0,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
						{TextTransparency = 0}
					):Play()
				end
				TweenService:Create(
					TabButton,
					TweenInfo.new(0,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
					{TextTransparency = 0}
				):Play()
			end
			for i,v in next, PageList:GetChildren() do
				currentpage2 = string.gsub(TabButton.Name,"Server","").."_Page"
				if v.Name == currentpage2 then
					UIPageLayout:JumpTo(v)
				end
			end
		end)

		if abc == false then
            
			for i,v in next, ScrollTab:GetChildren() do
				if v:IsA("TextButton") then
					TweenService:Create(
						v,
						TweenInfo.new(0,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
						{TextTransparency = 0}
					):Play()
				end
				TweenService:Create(
					TabButton,
					TweenInfo.new(0,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
					{TextTransparency = 0}
				):Play()
			end
			UIPageLayout:JumpToIndex(0)
			abc = true
		end
		
		game:GetService("RunService").Stepped:Connect(function()
			pcall(function()
				MainFramePage.CanvasSize = UDim2.new(0,0,0,UIListLayout.AbsoluteContentSize.Y + 20)
				ScrollTab.CanvasSize = UDim2.new(0,PLL.AbsoluteContentSize.X + 20,0,0)
			end)
		end)
 
 coroutine.wrap(function()
 while wait() do
 end
 end)()
 
	 
 
 coroutine.wrap(function()
 while wait() do
 end
 end)()
	
	
	local MainFramePage2 = Instance.new("ScrollingFrame")
		MainFramePage2.Name = text.."_Page"
		MainFramePage2.Parent = PageList2
		MainFramePage2.Active = true
		MainFramePage2.BackgroundColor3 = Color3.fromRGB(51,255,255)
		MainFramePage2.BackgroundTransparency = 1.000
		MainFramePage2.BorderSizePixel = 0
		MainFramePage2.Size = UDim2.new(0, 320, 0, 370)
		MainFramePage2.CanvasSize = UDim2.new(0, 0, 0, 0)
		MainFramePage2.ScrollBarThickness = 0
		
		local UIPadding2 = Instance.new("UIPadding")
		local UIListLayout2 = Instance.new("UIListLayout")
		
		UIPadding2.Parent = MainFramePage2
		UIPadding2.PaddingLeft = UDim.new(0, 10)
		UIPadding2.PaddingTop = UDim.new(0, 10)

		UIListLayout2.Padding = UDim.new(0,4)
		UIListLayout2.Parent = MainFramePage2
		UIListLayout2.SortOrder = Enum.SortOrder.LayoutOrder
		
		mainDiscord.MouseButton1Click:Connect(function()
			for i,v in next, ScrollTab:GetChildren() do
				if v:IsA("TextButton") then
					TweenService:Create(
						v,
						TweenInfo.new(0,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
						{TextTransparency = 0}
					):Play()
				end
				TweenService:Create(
					TabButton,
					TweenInfo.new(0,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
					{TextTransparency = 0}
				):Play()
			end
			for i,v in next, PageList2:GetChildren() do
				currentpage2 = string.gsub(TabButton.Name,"Server","").."_Page"
				if v.Name == currentpage2 then
					UIPageLayout2:JumpTo(v)
				end
			end
		end)

		if abc == false then
			for i,v in next, ScrollTab:GetChildren() do
				if v:IsA("TextButton") then
					TweenService:Create(
						v,
						TweenInfo.new(0,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
						{TextTransparency = 0}
					):Play()
				end
				TweenService:Create(
					mainDiscord,
					TweenInfo.new(0,Enum.EasingStyle.Quad,Enum.EasingDirection.Out),
					{TextTransparency = 0}
				):Play()
			end
			UIPageLayout2:JumpToIndex(0)
			abc = true
		end
		
		game:GetService("RunService").Stepped:Connect(function()
			pcall(function()
				MainFramePage2.CanvasSize = UDim2.new(0,0,0,UIListLayout2.AbsoluteContentSize.Y + 20)
				ScrollTab.CanvasSize = UDim2.new(0,PLL.AbsoluteContentSize.X + 20,0,0)
			end)
		end)
 
 coroutine.wrap(function()
 while wait() do
 end
 end)()

 
	 
 
 coroutine.wrap(function()
 while wait() do
 end
 end)()
	end
	
		local main = {}
		local TweenService = game:GetService("TweenService")

function main:AddButtonR(text, callback)
    if not MainFramePage2 then
        warn("MainFramePage2 is not defined")
        return
    end
    
    local Button2 = Instance.new("Frame")
    local UICorner2 = Instance.new("UICorner")
    local TextBtn2 = Instance.new("TextButton")
    local UICorner_1 = Instance.new("UICorner")
    local Black2 = Instance.new("Frame")
    local UICorner_2 = Instance.new("UICorner")
    
    Button2.Name = "Button"
    Button2.Parent = MainFramePage2
    Button2.BackgroundColor3 = _G.Color or Color3.new(1, 1, 1)
    Button2.Size = UDim2.new(0, 280, 0, 28)
    
    UICorner2.CornerRadius = UDim.new(0, 5)
    UICorner2.Parent = Button2
    
    TextBtn2.Name = "TextBtn"
    TextBtn2.Parent = Button2
    TextBtn2.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
    TextBtn2.Position = UDim2.new(0, 1, 0, 1)
    TextBtn2.Size = UDim2.new(0, 278, 0, 26)
    TextBtn2.AutoButtonColor = false
    TextBtn2.Font = Enum.Font.Code
    TextBtn2.Text = text
    TextBtn2.TextColor3 = Color3.fromRGB(225, 225, 225)
    TextBtn2.TextSize = 12
    
    UICorner_1.CornerRadius = UDim.new(0, 5)
    UICorner_1.Parent = TextBtn2
    
    Black2.Name = "Black"
    Black2.Parent = Button2
    Black2.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
    Black2.BackgroundTransparency = 1
    Black2.BorderSizePixel = 0
    Black2.Position = UDim2.new(0, 1, 0, 1)
    Black2.Size = UDim2.new(0, 280, 0, 26)
    
    UICorner_2.CornerRadius = UDim.new(0, 5)
    UICorner_2.Parent = Black2

    TextBtn2.MouseEnter:Connect(function()
        local tween = TweenService:Create(
            Black2,
            TweenInfo.new(0.4, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
            {BackgroundTransparency = 0.7}
        )
        tween:Play()
    end)
    
    TextBtn2.MouseLeave:Connect(function()
        local tween = TweenService:Create(
            Black2,
            TweenInfo.new(0.4, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
            {BackgroundTransparency = 1}
        )
        tween:Play()
    end)
    
    TextBtn2.MouseButton1Click:Connect(function()
        TextBtn2.TextSize = 0
        local tween = TweenService:Create(
            TextBtn2,
            TweenInfo.new(0.4, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
            {TextSize = 12}
        )
        tween:Play()
        if callback then
            callback()
        else
            warn("Callback function is not defined")
        end
    end)
end

function main:AddButtonL(text, callback)
    if not MainFramePage then
        warn("MainFramePage is not defined")
        return
    end

    local Button = Instance.new("Frame")
    local UICorner = Instance.new("UICorner")
    local TextBtn = Instance.new("TextButton")
    local UICorner_2 = Instance.new("UICorner")
    local Black = Instance.new("Frame")
    local UICorner_3 = Instance.new("UICorner")
    
    Button.Name = "Button"
    Button.Parent = MainFramePage
    Button.BackgroundColor3 = _G.Color or Color3.new(1, 1, 1)
    Button.Size = UDim2.new(0, 280, 0, 28)
    
    UICorner.CornerRadius = UDim.new(0, 5)
    UICorner.Parent = Button
    
    TextBtn.Name = "TextBtn"
    TextBtn.Parent = Button
    TextBtn.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
    TextBtn.Position = UDim2.new(0, 1, 0, 1)
    TextBtn.Size = UDim2.new(0, 278, 0, 26)
    TextBtn.AutoButtonColor = false
    TextBtn.Font = Enum.Font.Code
    TextBtn.Text = text
    TextBtn.TextColor3 = Color3.fromRGB(225, 225, 225)
    TextBtn.TextSize = 12
    
    UICorner_2.CornerRadius = UDim.new(0, 5)
    UICorner_2.Parent = TextBtn
    
    Black.Name = "Black"
    Black.Parent = Button
    Black.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
    Black.BackgroundTransparency = 1
    Black.BorderSizePixel = 0
    Black.Position = UDim2.new(0, 1, 0, 1)
    Black.Size = UDim2.new(0, 280, 0, 26)
    
    UICorner_3.CornerRadius = UDim.new(0, 5)
    UICorner_3.Parent = Black

    TextBtn.MouseEnter:Connect(function()
        local tween = TweenService:Create(
            Black,
            TweenInfo.new(0.4, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
            {BackgroundTransparency = 0.7}
        )
        tween:Play()
    end)
    
    TextBtn.MouseLeave:Connect(function()
        local tween = TweenService:Create(
            Black,
            TweenInfo.new(0.4, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
            {BackgroundTransparency = 1}
        )
        tween:Play()
    end)
    
    TextBtn.MouseButton1Click:Connect(function()
        TextBtn.TextSize = 0
        local tween = TweenService:Create(
            TextBtn,
            TweenInfo.new(0.4, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
            {TextSize = 12}
        )
        tween:Play()
        if callback then
            callback()
        else
            warn("Callback function is not defined")
        end
    end)
end
function main:AddToggle(text, config, callback, parentFrame)
    config = config or false
    local toggled = config
    local Toggle = Instance.new("Frame", parentFrame)
    local Button = Instance.new("TextButton", Toggle)
    local Label = Instance.new("TextLabel", Toggle)
    local ToggleImage = Instance.new("Frame", Toggle)
    local Circle = Instance.new("ImageLabel", ToggleImage)
    local True = Instance.new("TextLabel", Circle)
    
    Toggle.BackgroundColor3 = _G.Color
    Toggle.Size = UDim2.new(0, 280, 0, 28)
    Button.Size, Button.Position, Button.Text = UDim2.new(0, 278, 0, 26), UDim2.new(0, 1, 0, 1), ""
    Label.Text, Label.Size, Label.Position = text, UDim2.new(0, 278, 0, 26), UDim2.new(0, 1, 0, 1)
    ToggleImage.Size, ToggleImage.Position, ToggleImage.BackgroundColor3 = UDim2.new(0, 22, 0, 20), UDim2.new(0, 250, 0, 4), Color3.fromRGB(20, 20, 20)
    Circle.Size, Circle.Position, Circle.BackgroundColor3 = UDim2.new(0, 18, 0, 16), UDim2.new(0, 2, 0, 2), Color3.fromRGB(30, 30, 30)
    True.Size, True.Text = UDim2.new(0, 18, 0, 16), ""
    
    Button.MouseButton1Click:Connect(function()
        toggled = not toggled
        True.Text = toggled and "✔" or ""
        TweenService:Create(Circle, TweenInfo.new(0.2, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
            {BackgroundColor3 = toggled and Color3.fromRGB(0, 255, 0) or Color3.fromRGB(30, 30, 30)}):Play()
        pcall(callback, toggled)
    end)
    
    if config then
        True.Text = "✔"
        TweenService:Create(Circle, TweenInfo.new(0.4, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
            {BackgroundColor3 = Color3.fromRGB(0, 255, 0)}):Play()
        pcall(callback, toggled)
    end
end

function main:AddToggleL(text, config, callback)
    self:AddToggle(text, config, callback, MainFramePage)
end

function main:AddToggleR(text, config, callback)
    self:AddToggle(text, config, callback, MainFramePage2)
end

		

		
		-- Helper function สำหรับสร้าง Dropdown
local function createDropdown(params)
    local parent    = params.parent or error("Parent is required")
    local title     = params.title or "Dropdown"
    local list      = params.list or {}
    local default   = params.config or "Select First"
    local callback  = params.callback or function() end
    local style     = params.style or "L"  -- "L" หรือ "R" เพื่อปรับสไตล์

    local dropdown = {}
    local toggled = false
    local itemCount = 0
    local frameExtra = 0  -- ส่วนเพิ่มความสูงของ frame ตามจำนวน item

    -- สร้าง Main Container (DropSizeFrame)
    local dropSizeFrame = Instance.new("Frame")
    dropSizeFrame.Name = title
    dropSizeFrame.Parent = parent
    dropSizeFrame.BackgroundColor3 = _G.SectionColor
    dropSizeFrame.BackgroundTransparency = 1
    dropSizeFrame.Size = UDim2.new(0, 280, 0, 60)

    -- สร้าง Frame ภายใน
    local frame = Instance.new("Frame")
    frame.Name = "Frame"
    frame.Parent = dropSizeFrame
    frame.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
    frame.BorderSizePixel = 0
    frame.Position = UDim2.new(0, 3, 0, 0)
    frame.Size = UDim2.new(0, 278, 0, 60)

    local uiStroke = Instance.new("UIStroke")
    uiStroke.Name = "UIStroke"
    uiStroke.Parent = frame
    uiStroke.ApplyStrokeMode = Enum.ApplyStrokeMode.Border
    uiStroke.Color = Color3.fromRGB(255, 255, 255)
    uiStroke.LineJoinMode = Enum.LineJoinMode.Round
    uiStroke.Thickness = 0.7
    uiStroke.Transparency = 0

    local uiCorner = Instance.new("UICorner")
    uiCorner.Parent = frame
    uiCorner.CornerRadius = UDim.new(0, 3)

    -- สร้าง DropCover (ส่วนหัวของ dropdown)
    local dropCover = Instance.new("Frame")
    dropCover.Name = "DropCover"
    dropCover.Parent = frame
    dropCover.BackgroundColor3 = _G.BackgroundItemColor
    dropCover.BackgroundTransparency = 1
    dropCover.BorderSizePixel = 0
    dropCover.Position = UDim2.new(0, 0, 0, 0)
    dropCover.Size = UDim2.new(0, 202, 0, 30)

    local imageLabel = Instance.new("ImageLabel")
    imageLabel.Name = "ImageLabel"
    imageLabel.Parent = dropCover
    imageLabel.BackgroundColor3 = _G.SectionColor
    imageLabel.BackgroundTransparency = 1
    imageLabel.BorderSizePixel = 0
    imageLabel.Position = UDim2.new(0, 5, 0, 6)
    imageLabel.Size = UDim2.new(0, 18, 0, 18)
    imageLabel.Image = "rbxassetid://8825010231"
    imageLabel.ImageColor3 = Color3.fromRGB(255, 255, 255)

    local space = Instance.new("TextLabel")
    space.Name = "Space"
    space.Parent = dropCover
    space.BackgroundColor3 = _G.SectionColor
    space.BackgroundTransparency = 1
    space.Position = UDim2.new(0, 30, 0, 0)
    space.Size = UDim2.new(0, 15, 0, 30)
    space.Font = Enum.Font.Code
    space.Text = "|"
    space.TextSize = 13
    space.TextColor3 = Color3.fromRGB(255, 255, 255)
    space.TextXAlignment = Enum.TextXAlignment.Center

    local titleLabel = Instance.new("TextLabel")
    titleLabel.Name = "Title"
    titleLabel.Parent = dropCover
    titleLabel.BackgroundColor3 = _G.SectionColor
    titleLabel.BackgroundTransparency = 1
    titleLabel.Position = UDim2.new(0, 50, 0, 0)
    titleLabel.Size = UDim2.new(0, 207, 0, 30)
    titleLabel.Font = Enum.Font.Code
    titleLabel.Text = title
    titleLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
    titleLabel.TextSize = 12
    titleLabel.TextXAlignment = Enum.TextXAlignment.Left

    local imageButton = Instance.new("ImageButton")
    imageButton.Name = "ImageButton"
    imageButton.Parent = dropCover
    imageButton.BackgroundColor3 = _G.WindowBackgroundColor
    imageButton.BackgroundTransparency = 1
    imageButton.Position = UDim2.new(0, 250, 0, 7)
    imageButton.Size = UDim2.new(0, 23, 0, 18)
    imageButton.Image = "rbxassetid://6583628103"
    imageButton.ImageColor3 = Color3.fromRGB(51, 255, 255)
    imageButton.Rotation = 180

    -- สร้าง TextList ที่แสดง item ที่ถูกเลือก
    local dropTextList = Instance.new("TextLabel")
    dropTextList.Name = "DropTextList"
    dropTextList.Parent = frame
    dropTextList.BackgroundColor3 = _G.BackgroundItemColor
    dropTextList.BackgroundTransparency = 1
    dropTextList.Position = UDim2.new(0, 3, 0, 30)
    dropTextList.Size = UDim2.new(0, 278, 0, 25)
    dropTextList.Font = Enum.Font.Code
    dropTextList.Text = default
    dropTextList.TextColor3 = Color3.fromRGB(255, 255, 255)
    dropTextList.TextSize = 12
    dropTextList.TextXAlignment = Enum.TextXAlignment.Center

    local uiCorner2 = Instance.new("UICorner")
    uiCorner2.Parent = dropTextList
    uiCorner2.CornerRadius = UDim.new(0, 0)

    local dropStrokeList = Instance.new("UIStroke")
    dropStrokeList.Name = "DropStrokeList"
    dropStrokeList.Parent = dropTextList
    dropStrokeList.ApplyStrokeMode = Enum.ApplyStrokeMode.Border
    dropStrokeList.Color = Color3.fromRGB(255, 255, 255)
    dropStrokeList.LineJoinMode = Enum.LineJoinMode.Round
    dropStrokeList.Thickness = 0.2
    dropStrokeList.Transparency = 0

    -- สร้าง ScrollingFrame สำหรับรายการ item
    local dropItemScroll = Instance.new("ScrollingFrame")
    dropItemScroll.Name = "DropItemScroll"
    dropItemScroll.Parent = frame
    dropItemScroll.BackgroundColor3 = _G.SectionColor
    dropItemScroll.BackgroundTransparency = 1
    dropItemScroll.Position = UDim2.new(0, 3, 0, 60)
    dropItemScroll.Size = UDim2.new(0, 280, 0, 0)
    dropItemScroll.ScrollBarThickness = 0
    dropItemScroll.CanvasSize = UDim2.new(0, 0, 0, 0)

    local dropItemLayout = Instance.new("UIListLayout")
    dropItemLayout.Name = "DropItemLayout"
    dropItemLayout.Parent = dropItemScroll
    dropItemLayout.SortOrder = Enum.SortOrder.LayoutOrder
    dropItemLayout.Padding = UDim.new(0, 0)

    local dropItemStroke = Instance.new("UIStroke")
    dropItemStroke.Name = "DropItemStroke"
    dropItemStroke.Parent = dropItemScroll
    dropItemStroke.ApplyStrokeMode = Enum.ApplyStrokeMode.Border
    dropItemStroke.Color = Color3.fromRGB(51, 255, 255)
    dropItemStroke.LineJoinMode = Enum.LineJoinMode.Round
    dropItemStroke.Thickness = 0
    dropItemStroke.Transparency = 0

    local function updateCanvasSize()
        dropItemScroll.CanvasSize = UDim2.new(0, 0, 0, dropItemLayout.AbsoluteContentSize.Y)
    end

    local function collapseDropdown()
        toggled = false
        dropSizeFrame:TweenSize(UDim2.new(0, 278, 0, 60), 'InOut', 'Linear', 0.08)
        frame:TweenSize(UDim2.new(0, 278, 0, 60), 'InOut', 'Linear', 0.08)
        dropItemScroll:TweenSize(UDim2.new(0, 278, 0, 0), 'InOut', 'Linear', 0.08)
        game.TweenService:Create(imageButton, TweenInfo.new(0.08, Enum.EasingStyle.Linear, Enum.EasingDirection.InOut), {Rotation = 180}):Play()
        game.TweenService:Create(imageButton, TweenInfo.new(0.08, Enum.EasingStyle.Linear, Enum.EasingDirection.InOut), {ImageColor3 = Color3.fromRGB(51, 255, 255)}):Play()
    end

    -- Toggle dropdown เมื่อคลิกปุ่ม
    imageButton.MouseButton1Click:Connect(function()
        if toggled then
            collapseDropdown()
        else
            toggled = true
            dropSizeFrame:TweenSize(UDim2.new(0, 278, 0, 65 + frameExtra), 'InOut', 'Linear', 0.08)
            frame:TweenSize(UDim2.new(0, 278, 0, 65 + frameExtra), 'InOut', 'Linear', 0.08)
            dropItemScroll:TweenSize(UDim2.new(0, 278, 0, frameExtra), 'InOut', 'Linear', 0.08)
            game.TweenService:Create(imageButton, TweenInfo.new(0.08, Enum.EasingStyle.Linear, Enum.EasingDirection.InOut), {Rotation = 0}):Play()
            game.TweenService:Create(imageButton, TweenInfo.new(0.08, Enum.EasingStyle.Linear, Enum.EasingDirection.InOut), {ImageColor3 = Color3.fromRGB(51, 255, 255)}):Play()
        end
    end)

    -- ฟังก์ชันสำหรับเพิ่ม item เข้าไปใน dropdown
    local function addItem(itemText)
        itemText = itemText or "None..."
        itemCount = itemCount + 1
        -- กำหนดความสูงของ dropdown ตามจำนวน item
        if itemCount == 1 then
            frameExtra = 30
        elseif itemCount == 2 then
            frameExtra = 60
        elseif itemCount == 3 then
            frameExtra = 90
        else
            frameExtra = 120
        end

        local itemButton = Instance.new("TextButton")
        itemButton.Name = "ItemList"
        itemButton.Parent = dropItemScroll
        -- ปรับสไตล์ของ dropdown ตามแบบ L หรือ R
        if style == "R" then
            itemButton.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
            itemButton.TextColor3 = Color3.fromRGB(51, 255, 255)
        else
            itemButton.BackgroundColor3 = Color3.fromRGB(51, 255, 255)
            itemButton.TextColor3 = Color3.fromRGB(51, 255, 255)
        end
        itemButton.BackgroundTransparency = 1
        itemButton.Size = UDim2.new(0, 278, 0, 30)
        itemButton.AutoButtonColor = false
        itemButton.Font = Enum.Font.Code
        itemButton.TextSize = 12
        itemButton.Text = itemText
        itemButton.TextXAlignment = Enum.TextXAlignment.Center

        itemButton.MouseEnter:Connect(function()
            game.TweenService:Create(itemButton, TweenInfo.new(0.08, Enum.EasingStyle.Linear, Enum.EasingDirection.InOut), {BackgroundTransparency = 0.8}):Play()
        end)
        itemButton.MouseLeave:Connect(function()
            game.TweenService:Create(itemButton, TweenInfo.new(0.08, Enum.EasingStyle.Linear, Enum.EasingDirection.InOut), {BackgroundTransparency = 1}):Play()
        end)
        itemButton.MouseButton1Click:Connect(function()
            dropTextList.Text = itemText
            pcall(callback, itemText)
            collapseDropdown()
        end)
        updateCanvasSize()
    end

    -- เพิ่ม item เริ่มต้นจาก list
    for _,v in ipairs(list) do
        addItem(v)
    end

    -- API สำหรับ dropdown
    function dropdown:Clear()
        for _,child in ipairs(dropItemScroll:GetChildren()) do
            if child:IsA("TextButton") then
                child:Destroy()
            end
        end
        frameExtra = 0
        itemCount = 0
        dropTextList.Text = "Reset Successfully..."
        toggled = false
        collapseDropdown()
    end

    function dropdown:Add(newItem)
        addItem(newItem)
    end

    return dropdown
end

-- สร้าง Dropdown ซ้าย (L)
function main:AddDropdownL(droptitle, list, config, callback)
    return createDropdown({
        parent = MainFramePage,
        title = droptitle,
        list = list,
        config = config,
        callback = callback,
        style = "L"
    })
end

-- สร้าง Dropdown ขวา (R)
function main:AddDropdownR(droptitle, list, config, callback)
    return createDropdown({
        parent = MainFramePage2,
        title = droptitle,
        list = list,
        config = config,
        callback = callback,
        style = "R"
    })
end

local function createMultiDropdown(params)
    local parent    = params.parent or error("Parent is required")
    local title     = params.title or "MultiDropdown"
    local list      = params.list or {}
    local default   = params.config or "Select Items"
    local callback  = params.callback or function() end
    local style     = params.style or "L"
    
    local dropdown = {}
    local selectedItems = {}
    
    local dropSizeFrame = Instance.new("Frame")
    dropSizeFrame.Name = title
    dropSizeFrame.Parent = parent
    dropSizeFrame.BackgroundTransparency = 1
    dropSizeFrame.Size = UDim2.new(0, 280, 0, 60)
    
    local frame = Instance.new("Frame")
    frame.Parent = dropSizeFrame
    frame.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
    frame.Size = UDim2.new(0, 278, 0, 60)
    
    local dropTextList = Instance.new("TextLabel")
    dropTextList.Parent = frame
    dropTextList.Size = UDim2.new(0, 278, 0, 25)
    dropTextList.Text = default
    dropTextList.TextColor3 = Color3.fromRGB(255, 255, 255)
    dropTextList.TextSize = 12
    dropTextList.TextXAlignment = Enum.TextXAlignment.Center
    
    local dropItemScroll = Instance.new("ScrollingFrame")
    dropItemScroll.Parent = frame
    dropItemScroll.Position = UDim2.new(0, 3, 0, 60)
    dropItemScroll.Size = UDim2.new(0, 280, 0, 0)
    dropItemScroll.ScrollBarThickness = 0
    dropItemScroll.CanvasSize = UDim2.new(0, 0, 0, 0)
    
    local dropItemLayout = Instance.new("UIListLayout")
    dropItemLayout.Parent = dropItemScroll
    
    local function updateSelectedText()
        dropTextList.Text = #selectedItems > 0 and table.concat(selectedItems, ", ") or default
    end
    
    local function addItem(itemText)
        local itemButton = Instance.new("TextButton")
        itemButton.Parent = dropItemScroll
        itemButton.Size = UDim2.new(0, 278, 0, 30)
        itemButton.Text = itemText
        
        itemButton.MouseButton1Click:Connect(function()
            local index = table.find(selectedItems, itemText)
            if index then
                table.remove(selectedItems, index)
                itemButton.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
            else
                table.insert(selectedItems, itemText)
                itemButton.BackgroundColor3 = Color3.fromRGB(51, 255, 255)
            end
            updateSelectedText()
            callback(selectedItems)
        end)
    end
    
    for _, v in ipairs(list) do
        addItem(v)
    end
    
    return dropdown
end

function main:AddMultiDropdownL(droptitle, list, config, callback)
    return createMultiDropdown({
        parent = MainFramePage,
        title = droptitle,
        list = list,
        config = config,
        callback = callback,
        style = "L"
    })
end

function main:AddMultiDropdownR(droptitle, list, config, callback)
    return createMultiDropdown({
        parent = MainFramePage2,
        title = droptitle,
        list = list,
        config = config,
        callback = callback,
        style = "R"
    })
end


local function createSlider(parent, text, min, max, set, callback)
    local Slider = Instance.new("Frame")
    local slidercorner = Instance.new("UICorner")
    local sliderr = Instance.new("Frame")
    local sliderrcorner = Instance.new("UICorner")
    local SliderLabel = Instance.new("TextLabel")
    local AHEHE = Instance.new("TextButton")
    local bar = Instance.new("Frame")
    local bar1 = Instance.new("Frame")
    local bar1corner = Instance.new("UICorner")
    local circlebar = Instance.new("Frame")
    local UICorner = Instance.new("UICorner")
    local slidervalue = Instance.new("Frame")
    local valuecorner = Instance.new("UICorner")
    local TextBox = Instance.new("TextBox")
    local UICorner_2 = Instance.new("UICorner")

    Slider.Parent = parent
    Slider.BackgroundColor3 = _G.Color
    Slider.Size = UDim2.new(0, 280, 0, 51)

    slidercorner.CornerRadius = UDim.new(0, 5)
    slidercorner.Parent = Slider

    sliderr.Parent = Slider
    sliderr.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
    sliderr.Position = UDim2.new(0, 1, 0, 1)
    sliderr.Size = UDim2.new(0, 278, 0, 49)

    sliderrcorner.CornerRadius = UDim.new(0, 5)
    sliderrcorner.Parent = sliderr

    SliderLabel.Parent = sliderr
    SliderLabel.BackgroundTransparency = 1.0
    SliderLabel.Position = UDim2.new(0, 15, 0, 0)
    SliderLabel.Size = UDim2.new(0, 100, 0, 26)
    SliderLabel.Font = Enum.Font.Code
    SliderLabel.Text = text
    SliderLabel.TextColor3 = Color3.fromRGB(225, 225, 225)
    SliderLabel.TextSize = 16.0
    SliderLabel.TextXAlignment = Enum.TextXAlignment.Left

    AHEHE.Parent = sliderr
    AHEHE.BackgroundTransparency = 1.0
    AHEHE.Position = UDim2.new(0, 10, 0, 35)
    AHEHE.Size = UDim2.new(0, 260, 0, 5)

    bar.Parent = AHEHE
    bar.BackgroundColor3 = Color3.fromRGB(45, 45, 45)
    bar.Size = UDim2.new(0, 260, 0, 5)

    bar1.Parent = bar
    bar1.BackgroundColor3 = _G.Color
    bar1.Size = UDim2.new(set / max, 0, 0, 5)

    bar1corner.CornerRadius = UDim.new(0, 5)
    bar1corner.Parent = bar1

    circlebar.Parent = bar1
    circlebar.BackgroundColor3 = Color3.fromRGB(225, 225, 225)
    circlebar.Position = UDim2.new(1, -2, 0, -3)
    circlebar.Size = UDim2.new(0, 10, 0, 10)

    UICorner.CornerRadius = UDim.new(0, 100)
    UICorner.Parent = circlebar

    slidervalue.Parent = sliderr
    slidervalue.BackgroundColor3 = _G.Color
    slidervalue.Position = UDim2.new(0, 220, 0, 5)
    slidervalue.Size = UDim2.new(0, 50, 0, 15)

    valuecorner.CornerRadius = UDim.new(0, 5)
    valuecorner.Parent = slidervalue

    TextBox.Parent = slidervalue
    TextBox.BackgroundColor3 = Color3.fromRGB(35, 35, 35)
    TextBox.Position = UDim2.new(0, 1, 0, 1)
    TextBox.Size = UDim2.new(0, 48, 0, 13)
    TextBox.Font = Enum.Font.Code
    TextBox.TextColor3 = Color3.fromRGB(225, 225, 225)
    TextBox.TextSize = 9.0
    TextBox.Text = set

    UICorner_2.CornerRadius = UDim.new(0, 5)
    UICorner_2.Parent = TextBox

    local uis = game:GetService("UserInputService")

    local function updateSlider(input)
        local pos = math.clamp(input.Position.X - bar.AbsolutePosition.X, 0, 260)
        bar1.Size = UDim2.new(0, pos, 0, 5)
        circlebar.Position = UDim2.new(0, pos - 2, 0, -3)

        local Value = math.floor(((max - min) / 260) * pos + min)
        TextBox.Text = Value
        pcall(callback, Value)
    end

    AHEHE.InputBegan:Connect(function(input)
        if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
            updateSlider(input)

            local moveConnection
            local releaseConnection

            moveConnection = uis.InputChanged:Connect(function(movingInput)
                if movingInput.UserInputType == Enum.UserInputType.MouseMovement or movingInput.UserInputType == Enum.UserInputType.Touch then
                    updateSlider(movingInput)
                end
            end)

            releaseConnection = uis.InputEnded:Connect(function(endedInput)
                if endedInput.UserInputType == Enum.UserInputType.MouseButton1 or endedInput.UserInputType == Enum.UserInputType.Touch then
                    moveConnection:Disconnect()
                    releaseConnection:Disconnect()
                end
            end)
        end
    end)

    TextBox.FocusLost:Connect(function()
        local Value = tonumber(TextBox.Text) or set
        if Value < min then Value = min end
        if Value > max then Value = max end
        TextBox.Text = Value
        bar1.Size = UDim2.new((Value - min) / (max - min), 0, 0, 5)
        pcall(callback, Value)
    end)
end

function main:AddSliderLeft(text, min, max, set, callback)
    createSlider(MainFramePage, text, min, max, set, callback)
end

function main:AddSliderRight(text, min, max, set, callback)
    createSlider(MainFramePage2, text, min, max, set, callback)
end



function main:AddTextbox(position, parentFrame, text, texts, disappear, callback)
    local Textbox = Instance.new("Frame")
    local TextboxCorner = Instance.new("UICorner")
    local TextboxInner = Instance.new("Frame")
    local TextboxInnerCorner = Instance.new("UICorner")
    local TextboxLabel = Instance.new("TextLabel")
    local txtbtn = Instance.new("TextButton")
    local RealTextbox = Instance.new("TextBox")
    local UICorner = Instance.new("UICorner")

    -- Textbox Properties
    Textbox.Name = "Textbox"
    Textbox.Parent = parentFrame
    Textbox.BackgroundColor3 = _G.Color
    Textbox.Size = UDim2.new(0, 280, 0, 57)

    TextboxCorner.CornerRadius = UDim.new(0, 5)
    TextboxCorner.Parent = Textbox

    -- Inner Frame
    TextboxInner.Name = "TextboxInner"
    TextboxInner.Parent = Textbox
    TextboxInner.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
    TextboxInner.Position = UDim2.new(0, 1, 0, 1)
    TextboxInner.Size = UDim2.new(0, 278, 0, 55)

    TextboxInnerCorner.CornerRadius = UDim.new(0, 5)
    TextboxInnerCorner.Parent = TextboxInner

    -- Label
    TextboxLabel.Name = "TextboxLabel"
    TextboxLabel.Parent = Textbox
    TextboxLabel.BackgroundTransparency = 1.0
    TextboxLabel.Position = UDim2.new(0, 15, 0, 8)
    TextboxLabel.Size = UDim2.new(0, 250, 0, 12)
    TextboxLabel.Font = Enum.Font.Code
    TextboxLabel.Text = text
    TextboxLabel.TextColor3 = Color3.fromRGB(225, 225, 225)
    TextboxLabel.TextStrokeColor3 = Color3.fromRGB(0, 0, 0) -- Shadow Effect
    TextboxLabel.TextStrokeTransparency = 0.5
    TextboxLabel.TextSize = 12.0
    TextboxLabel.TextXAlignment = Enum.TextXAlignment.Left

    -- Input Box
    RealTextbox.Name = "RealTextbox"
    RealTextbox.Parent = Textbox
    RealTextbox.BackgroundColor3 = Color3.fromRGB(45, 45, 45)
    RealTextbox.Position = UDim2.new(0, 3, 0, 30)
    RealTextbox.Size = UDim2.new(0, 276, 0, 24)
    RealTextbox.Font = Enum.Font.Code
    RealTextbox.Text = texts
    RealTextbox.TextColor3 = Color3.fromRGB(255, 225, 225)
    RealTextbox.TextScaled = true
    RealTextbox.TextStrokeColor3 = Color3.fromRGB(0, 0, 0) -- Shadow Effect
    RealTextbox.TextStrokeTransparency = 0.5
    RealTextbox.TextSize = 11.0

    -- Disappear Effect
    RealTextbox.FocusLost:Connect(function()
        callback(RealTextbox.Text)
        if disappear then
            for i = 0, 1, 0.1 do
                RealTextbox.TextTransparency = i
                TextboxLabel.TextTransparency = i
                task.wait(0.05)
            end
            RealTextbox.Text = ""
            TextboxLabel.TextTransparency = 0
            RealTextbox.TextTransparency = 0
        end
    end)

    -- Rounded Corners
    UICorner.CornerRadius = UDim.new(0, 5)
    UICorner.Parent = RealTextbox
end

-- Function Wrapper for Left & Right
function main:AddTextboxLeft(text, texts, disappear, callback)
    self:AddTextbox("Left", MainFramePage, text, texts, disappear, callback)
end

function main:AddTextboxRight(text, texts, disappear, callback)
    self:AddTextbox("Right", MainFramePage2, text, texts, disappear, callback)
end

		
		function main:AddLabelLeft(text)
			local Label = Instance.new("TextLabel")
			local PaddingLabel = Instance.new("UIPadding")
			local labelfunc = {}
	
			Label.Name = "Label"
			Label.Parent = MainFramePage
			Label.BackgroundColor3 = Color3.fromRGB(51,255,255)
			Label.BackgroundTransparency = 1.000
			Label.Size = UDim2.new(0, 360, 0, 20)
			Label.Font = Enum.Font.Code
			Label.TextColor3 = Color3.fromRGB(225, 225, 225)
			Label.TextSize = 14.000
			Label.Text = text
			Label.TextXAlignment = Enum.TextXAlignment.Left

			PaddingLabel.PaddingLeft = UDim.new(0,15)
			PaddingLabel.Parent = Label
			PaddingLabel.Name = "PaddingLabel"
	
			function labelfunc:Set(newtext)
			Label.Text = newtext
		end
		return labelfunc
		end

		function main:AddLabelRight(text)
			local Labell = Instance.new("TextLabel")
			local PaddingLabell = Instance.new("UIPadding")
			local labelfunc = {}
	
			Labell.Name = "Label"
			Labell.Parent = MainFramePage2
			Labell.BackgroundColor3 = Color3.fromRGB(51,255,255)
			Labell.BackgroundTransparency = 1.000
			Labell.Size = UDim2.new(0, 360, 0, 20)
			Labell.Font = Enum.Font.Code
			Labell.TextColor3 = Color3.fromRGB(225, 225, 225)
			Labell.TextSize = 14.000
			Labell.Text = text
			Labell.TextXAlignment = Enum.TextXAlignment.Left

			PaddingLabell.PaddingLeft = UDim.new(0,15)
			PaddingLabell.Parent = Labell
			PaddingLabell.Name = "PaddingLabel"
	
			function labelfunc:Set(newtext)
			Labell.Text = newtext
		end
		return labelfunc
		end


function main:Label1(text)
			local Label1 = Instance.new("TextLabel")
			local PaddingLabel1 = Instance.new("UIPadding")
			local Label1func = {}
	
			Label1.Name = "Label1"
			Label1.Parent = MainFramePage
			Label1.BackgroundColor3 = Color3.fromRGB(51,255,255)
			Label1.BackgroundTransparency = 1.000
			Label1.Size = UDim2.new(0, 360, 0, 20)
			Label1.Font = Enum.Font.Code
			Label1.TextColor3 = Color3.fromRGB(225, 225, 225)
			Label1.TextSize = 15.000
			Label1.Text = text
			Label1.TextXAlignment = Enum.TextXAlignment.Left

			PaddingLabel1.PaddingLeft = UDim.new(0,15)
			PaddingLabel1.Parent = Label1
			PaddingLabel1.Name = "PaddingLabel1"
function Label1func:Refresh(tochange)
 Label1.Text = tochange
end

return Label1func
end

		function main:AddSeperatorLeft(text)
			local Seperator = Instance.new("Frame")
			local Sep1 = Instance.new("Frame")
			local Sep2 = Instance.new("TextLabel")
			local Sep3 = Instance.new("Frame")
			
			Seperator.Name = "Seperator"
			Seperator.Parent = MainFramePage
			Seperator.BackgroundColor3 = Color3.fromRGB(51,255,255)
			Seperator.BackgroundTransparency = 1.000
			Seperator.Size = UDim2.new(0, 280, 0, 20)
			
			Sep1.Name = "Sep1"
			Sep1.Parent = Seperator
			Sep1.BackgroundColor3 = _G.Color
			Sep1.BorderSizePixel = 0
			Sep1.Position = UDim2.new(0, 0, 0, 10)
			Sep1.Size = UDim2.new(0, 20, 0, 1)
			
			Sep2.Name = "Sep2"
			Sep2.Parent = Seperator
			Sep2.BackgroundColor3 = Color3.fromRGB(51,255,255)
			Sep2.BackgroundTransparency = 1.000
			Sep2.Position = UDim2.new(0, 0.01, 0, 0)
			Sep2.Size = UDim2.new(0, 280, 0, 20)
			Sep2.Font = Enum.Font.Code
			Sep2.Text = text
			Sep2.TextColor3 = Color3.fromRGB(51,255,255)
			Sep2.TextSize = 20.000
			
			Sep3.Name = "Sep3"
			Sep3.Parent = Seperator
			Sep3.BackgroundColor3 = _G.Color
			Sep3.BorderSizePixel = 0
			Sep3.Position = UDim2.new(0, 260, 0, 10)
			Sep3.Size = UDim2.new(0, 20, 0, 1)
		end

		function main:AddSeperatorRight(text)
			local Seperator2 = Instance.new("Frame")
			local Sep4 = Instance.new("Frame")
			local Sep5 = Instance.new("TextLabel")
			local Sep6 = Instance.new("Frame")
			
			Seperator2.Name = "Seperator"
			Seperator2.Parent = MainFramePage2
			Seperator2.BackgroundColor3 = Color3.fromRGB(51,255,255)
			Seperator2.BackgroundTransparency = 1.000
			Seperator2.Size = UDim2.new(0, 280, 0, 20)
			
			Sep4.Name = "Sep1"
			Sep4.Parent = Seperator2
			Sep4.BackgroundColor3 = _G.Color
			Sep4.BorderSizePixel = 0
			Sep4.Position = UDim2.new(0, 0, 0, 10)
			Sep4.Size = UDim2.new(0, 20, 0, 1)
			
			Sep5.Name = "Sep2"
			Sep5.Parent = Seperator2
			Sep5.BackgroundColor3 = Color3.fromRGB(51,255,255)
			Sep5.BackgroundTransparency = 1.000
			Sep5.Position = UDim2.new(0, 0.01, 0, 0)
			Sep5.Size = UDim2.new(0, 280, 0, 20)
			Sep5.Font = Enum.Font.Code
			Sep5.Text = text
			Sep5.TextColor3 = Color3.fromRGB(51,255,255)
			Sep5.TextSize = 20.000
			
			Sep6.Name = "Sep3"
			Sep6.Parent = Seperator2
			Sep6.BackgroundColor3 = _G.Color
			Sep6.BorderSizePixel = 0
			Sep6.Position = UDim2.new(0, 260, 0, 10)
			Sep6.Size = UDim2.new(0, 20, 0, 1)
		end


		function main:AddLineLeft()
			local Linee = Instance.new("Frame")
			local Line = Instance.new("Frame")
			
			Linee.Name = "Linee"
			Linee.Parent = MainFramePage
			Linee.BackgroundColor3 = Color3.fromRGB(255,0,0)
			Linee.BackgroundTransparency = 1.000
			Linee.Position = UDim2.new(0, 0, 0.119999997, 0)
			Linee.Size = UDim2.new(0, 280, 0, 20)
			
			Line.Name = "Line"
			Line.Parent = Linee
			Line.BackgroundColor3 = _G.Color
			Line.BorderSizePixel = 0
			Line.Position = UDim2.new(0, 0, 0, 10)
			Line.Size = UDim2.new(0, 280, 0, 1)
		end
		
		function main:AddLineRight()
			local Lineee = Instance.new("Frame")
			local Line1 = Instance.new("Frame")
			
			Lineee.Name = "Linee"
			Lineee.Parent = MainFramePage2
			Lineee.BackgroundColor3 = Color3.fromRGB(255,0,0)
			Lineee.BackgroundTransparency = 1.000
			Lineee.Position = UDim2.new(0, 0, 0.119999997, 0)
			Lineee.Size = UDim2.new(0, 280, 0, 20)
			
			Line1.Name = "Line"
			Line1.Parent = Lineee
			Line1.BackgroundColor3 = _G.Color
			Line1.BorderSizePixel = 0
			Line1.Position = UDim2.new(0, 0, 0, 10)
			Line1.Size = UDim2.new(0, 280, 0, 1)
		end
		
		return main
	end
	return uitab
end
--------------------------------------------- Function ----------------------------------------------

spawn(function()
    while task.wait(0) do
        pcall(function()
            if Auto_Click or Auto_Ghost_Ship or Auto_Hydra or Auto_Sea_King then         
                game:GetService("ReplicatedStorage").Chest.Remotes.Functions.SkillAction:InvokeServer(TypeWeapon .."_"..WeaPon_Select.."_M1")
            end
        end)
    end
end)
 

 


spawn(function()
    while wait() do -- รอเวลาระหว่างแต่ละรอบ
        pcall(function()
            local player = game:GetService("Players").LocalPlayer
            local character = player.Character
            local humanoidRootPart = character and character:FindFirstChild("HumanoidRootPart")
            local humanoid = character and character:FindFirstChild("Humanoid")

            if Auto_Ghost_Ship or Auto_Hydra or Auto_Sea_King then
                if humanoidRootPart and humanoid then
                    -- ตรวจสอบว่ามี BodyClip อยู่หรือไม่
                    local noclip = humanoidRootPart:FindFirstChild("BodyClip")
                    if not noclip then
                        local Noclip = Instance.new("BodyVelocity")
                        Noclip.Name = "BodyClip"
                        Noclip.Parent = humanoidRootPart
                        Noclip.MaxForce = Vector3.new(1000000, 1000000, 1000000)
                        Noclip.Velocity = Vector3.new(0, 0, 0)

                        -- เปลี่ยนสถานะของ Humanoid เป็น Physics
                        humanoid:ChangeState(14)
                    end
                end
            else
                -- หากปิด Auto_Ghost_Ship, Auto_Hydra หรือ Auto_Sea_King ให้ลบ BodyClip หากมีอยู่
                if humanoidRootPart then
                    local noclip = humanoidRootPart:FindFirstChild("BodyClip")
                    if noclip then
                    end
                end
            end
        end)
    end
end)


spawn(function()
	while wait() do
		if Auto_Ghost_Ship or Auto_Hydra or Auto_Sea_King then
			pcall(function()
				if game:GetService("Workspace").PlayerCharacters.NamePlayer.Services.KenOpen.Value == false then
					game:GetService("ReplicatedStorage"):WaitForChild("Chest"):WaitForChild("Remotes"):WaitForChild("Functions"):WaitForChild("KenEvent"):InvokeServer()
				end
			end) 
		end
	end
end)

spawn(function()
	pcall(function()
		game:GetService("RunService").Stepped:Connect(function()
			if Auto_Ghost_Ship or Auto_Hydra or Auto_Sea_King then
				for _, v in pairs(game.Players.LocalPlayer.Character:GetDescendants()) do
					if v:IsA("BasePart") then
						v.CanCollide = false    
					end
				end
			else
				for _, v in pairs(game.Players.LocalPlayer.Character:GetDescendants()) do
					if v:IsA("BasePart") then
						v.CanCollide = true   
						noclip:Destroy() 
					end
				end
			end
		end)
	end)
end)



function EquipWeapon(ToolSe)
	if game.Players.LocalPlayer.Backpack:FindFirstChild(ToolSe) then
		getgenv().tool = game.Players.LocalPlayer.Backpack:FindFirstChild(ToolSe)
		wait()
		game.Players.LocalPlayer.Character.Humanoid:EquipTool(tool)
	end
end

function Hop()
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
	Teleport()
end

function UseSkill(skill, CFrameMon)
    local remote = game:GetService("ReplicatedStorage").Chest.Remotes.Functions.SkillAction

    -- ส่งคำสั่ง "Up"
    remote:InvokeServer(TypeWeapon .. "_" .. WeaPon_Select .. "_" .. skill, { 
        Type = "Up", 
        MouseHit = CFrameMon * CFrame.Angles(0, 0, 0) 
    })
	game:GetService("VirtualInputManager"):SendKeyEvent(true,skill,false,game)
    -- รอเวลาเล็กน้อยก่อนส่งคำสั่ง "Down"
	task.wait()-- คุณสามารถปรับเวลาใน wait ได้ตามที่ต้องการ

    -- ส่งคำสั่ง "Down"
    remote:InvokeServer(TypeWeapon .. "_" .. WeaPon_Select .. "_" .. skill, { 
        Type = "Down", 
        MouseHit = CFrameMon * CFrame.Angles(0, 0, 0) 
    })
	game:GetService("VirtualInputManager"):SendKeyEvent(false,skill,false,game)
end



------------------------------------------------- Ui ----------------------------------------------------------
if game.PlaceId == 6381829480 then
	WorldCheck = 2
	MapPlaceId = "6381829480"
elseif game.PlaceId == 4520749081 then
	WorldCheck = 1
	MapPlaceId = "4520749081"
end

local RenUi = Update:AddWindow("RebornXer Hub","10039618734",Enum.KeyCode.RightControl)
local Main = RenUi:AddTab("Farm","6026568198")
    local Player = RenUi:AddTab("Player - TP","7044226690")
    local Misc = RenUi:AddTab("Misc","6034900727")
    local Setting = RenUi:AddTab("","")
    
    local S = RenUi:AddTabH("Top","14134158045")
	
	
	Main:AddSeperatorRight("Sea Chack")

	local SeaChack = Main:AddLabelRight("")

function SeaChackSent()
    -- ดึงข้อมูลจาก SKTimeLabel
    local TimeSea = game:GetService("Players").LocalPlayer.PlayerGui.MainGui.StarterFrame.LegacyPoseFrame.SecondSea.SKTimeLabel.Text

    -- ตรวจสอบเงื่อนไขการแสดงผลของภาพ HDImage และ SKImage
    local HDVisible = game:GetService("Players").LocalPlayer.PlayerGui.MainGui.StarterFrame.LegacyPoseFrame.SecondSea.HDImage.Visible
    local SKVisible = game:GetService("Players").LocalPlayer.PlayerGui.MainGui.StarterFrame.LegacyPoseFrame.SecondSea.SKImage.Visible

    -- ปรับข้อความใน SeaChack ตามเงื่อนไข
    if HDVisible == true and SKVisible == false then
        SeaChack:Set("Hydra       : " .. TimeSea)
	elseif SKVisible == true and HDVisible == false then
        SeaChack:Set("Sea King    : " .. TimeSea)
    end
end

-- เรียกใช้ฟังก์ชัน SeaChackSent ในลูปทุก ๆ interval ที่กำหนด
spawn(function()
    while task.wait() do
        pcall(SeaChackSent)
    end
end)

		 ShipChack = Main:AddLabelRight("")
  

             function ShipChackSent()		
						TimeShip = game:GetService("Players").LocalPlayer.PlayerGui.MainGui.StarterFrame.LegacyPoseFrame.SecondSea.GSTimeLabel.Text
						ShipChack:Set("Ghost Ship  : "..TimeShip)   
                end

         spawn(function()
        while task.wait() do
            pcall(function()
				ShipChackSent()
            end)
        end
         end)

    Main:AddSeperatorRight("Settings")
    
Setting:AddButtonLeft("Copy CFrame",function()
setclipboard(tostring(game.Players.LocalPlayer.Character.HumanoidRootPart.Position))
end)

 Main:AddSeperatorLeft("Info")
    Main:AddLabelLeft("Wecome To RebornXer Hub Script")
    Main:AddLabelLeft("Map : King Legazy")
    Date = os.date("%d".." ".."%B".." ".."%Y")
    Main:AddLabelLeft("Day : "..Date)
    Main:AddSeperatorLeft("Job ID")

	Main:AddTextboxLeft("job id ","...",true,function(s)
		Jobid = s
		end)
		
		Main:AddButtonLeft("Copy Job id",function()
		setclipboard(tostring(game.JobId))
		end)
					
			 Main:AddButtonLeft("Join Job",function(s)
			game:GetService("TeleportService"):TeleportToPlaceInstance(MapPlaceId, Jobid)
			end)
Main:AddToggleL("Spam Join Job",Spam_Join_Job,function(a)
	Spam_Join_Job = a
			end)

			spawn(function()
				while wait() do
					pcall(function()
						if Spam_Join_Job then
							game:GetService("TeleportService"):TeleportToPlaceInstance(MapPlaceId, Jobid)
						end
					end)
				end
			end)
				
 Main:AddSeperatorLeft("Main")

Main:AddToggleL("Auto Farm",Auto_Farm,function(a)
Auto_Farm = a
end)

function CheckQuest()
	local MyLevel = game.Players.LocalPlayer.PlayerStats.lvl.Value
      if MyLevel == 0 or MyLevel <= 80 then
	MonQuest = "Kill 4 Soldiers"
	PahtNPC = game:GetService("Workspace").AllNPC["Starter Island Quest"].CFrame
	  end
	end


 

	spawn(function()
		while task.wait(0) do
			pcall(function()
				if Auto_Farm then
					CheckQuest()
					local questBoard = game.Players.LocalPlayer.PlayerGui.Quest.QuestBoard
					if not questBoard.Visible == false then
						TP(PahtNPC)
						game:GetService("ReplicatedStorage").Chest.Remotes.Functions.Quest:InvokeServer("take", MonQuest)
					else
						local questText = questBoard.QuestCount.Text
						local Ms = string.sub(questText, 5, #questText)
						local monsters = game:GetService("Workspace").Monster
						if monsters.Mon:FindFirstChild(Ms) or monsters.Boss:FindFirstChild(Ms) then
							for _, v in pairs(monsters:GetDescendants()) do
								if v.Name == Ms and v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
									repeat
										wait()
										AutoHaki()
										game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame * MethodFarm
										EquipWeapon(_G.SelectWeapon)
										v.Humanoid.WalkSpeed = 0
										if _G.AutoSkill then
											UseSkill("Z")
											UseSkill("X")
											UseSkill("C")
											UseSkill("V")
										end
									until not v.Parent or v.Humanoid.Health <= 0 or not _G.AutoFarm or not questBoard.Visible == false
								end
							end
						end
					end
				end
			end)
		end
	end)
	
function TP(Pos)
	local NamePlayer = game.Players.LocalPlayer.Name
     local MainPlayer = game.workspace.PlayerCharacters:FindFirstChild(NamePlayer)
	 MainPlayer.HumanoidRootPart.CFrame = Pos
end

Main:AddSeperatorLeft("World Quest")

Main:AddToggleL("Auto Sea Two",Auto_Sea_Two,function(a)
    Auto_Sea_Two = a
end)

spawn(function()
    while wait() do
        pcall(function()
            if Auto_Sea_Two then
                
            end
    end)
end
end)

Main:AddToggleL("Auto Sea thi")

Main:AddSeperatorLeft("Sea Event")

Main:AddToggleL("Hop Mix",_G.SST.Hop_Mix,function(a)
	Hop_Mix = a
		_G.SST.Hop_Mix = Hop_Mix
	SS()
end)

spawn(function()
    while wait() do
        if Hop_Mix and Auto_Hydra and Auto_Sea_King and Auto_Ghost_Ship then
            pcall(function()
                if not game:GetService("Workspace").Island:FindFirstChild("Sea King Thunder") and not game:GetService("Workspace").Island:FindFirstChild("Sea King Lava") and not game:GetService("Workspace").Island:FindFirstChild("Sea King Water") and  not game:GetService("Workspace").Island:FindFirstChild("Legacy Island1") and not game:GetService("Workspace").Island:FindFirstChild("Legacy Island2") and not game:GetService("Workspace").Island:FindFirstChild("Legacy Island3") and not game:GetService("Workspace").Island:FindFirstChild("Legacy Island4") and not game:GetService("Workspace").GhostMonster:FindFirstChild("Ghost Ship") then
                    wait(8)
                    Hop()
                end
            end)
        end
    end
end)


Hydra = Main:AddLabelLeft("")
  

             function HydraSent()
				if game:GetService("Workspace").Island:FindFirstChild("Sea King Thunder") or game:GetService("Workspace").Island:FindFirstChild("Sea King Lava") or game:GetService("Workspace").Island:FindFirstChild("Sea King Water") then
              Hydra:Set("Hydra : ✔")   
                else
                    Hydra:Set("Hydra : ✖")    
                end
                end

         spawn(function()
        while task.wait() do
            pcall(function()
                HydraSent()
            end)
        end
         end)


Main:AddToggleL("Auto Hydra",_G.SST.Auto_Hydra,function(a)
    Auto_Hydra = a
	_G.SST.Auto_Hydra = Auto_Hydra
	SS()
end)

spawn(function()
    while task.wait(0) do
        if Auto_Hydra then
            pcall(function()
                -- ตรวจสอบ Hydra ว่าเกิดขึ้นหรือไม่
                local hydra = game:GetService("Workspace").SeaMonster:FindFirstChild("HydraSeaKing")
                if hydra then
                    -- ถ้า Hydra เกิดแล้ว ทำการเทเลพอร์ตไปที่ Hydra
                    repeat
                        task.wait(0) -- เพิ่มการหน่วงเวลาให้เหมาะสม
                        EquipWeapon(WeaPon_Select)
                        TP(hydra.HumanoidRootPart.CFrame * MethodFarm)
                        if Auto_Skill then
                            UseSkill("Z",hydra.HumanoidRootPart.CFrame)
							wait(0.1)
                            UseSkill("X",hydra.HumanoidRootPart.CFrame)
							wait(0.1)
                            UseSkill("C",hydra.HumanoidRootPart.CFrame)
							wait(0.1)
                            UseSkill("V",hydra.HumanoidRootPart.CFrame)
							wait(0.1)
                        end
                    until hydra.Humanoid.Health <= 0 or not Auto_Hydra or not game:GetService("Workspace").SeaMonster:FindFirstChild("HydraSeaKing")
                    
                    -- หาก Hydra ตายแล้ว, เทเลพอร์ตไปที่กล่อง
                    if hydra.Humanoid.Health <= 0 then
                        local lootBox = game:GetService("Workspace").SeaMonster:FindFirstChild("LootBox") -- สมมติว่าชื่อกล่องคือ LootBox
                        if lootBox then
                            TP(lootBox.CFrame)
                        end
                    end
                else
                    -- ถ้า Hydra ไม่เกิด แต่มีเกาะ Hydra, เทเลพอร์ตไปที่เกาะ
                    local seaKingTypes = {"Sea King Thunder", "Sea King Lava", "Sea King Water"}
                    for _, seaKingType in ipairs(seaKingTypes) do
                        local seaKing = game:GetService("Workspace").Island:FindFirstChild(seaKingType)
                        if seaKing then
                            TP(seaKing.HydraStand.CFrame)
                            break
                        end
                    end
                end
            end)
        end
    end
end)


Main:AddToggleL("Auto Hydra Hop",_G.SST.Auto_Hydra_Hop,function(a)
    Auto_Hydra_Hop = a
	_G.SST.Auto_Hydra_Hop = Auto_Hydra_Hop
	SS()
end)

spawn(function()
    while wait() do
        if Auto_Hydra and Auto_Hydra_Hop then
            pcall(function()
                if not game:GetService("Workspace").Island:FindFirstChild("Sea King Thunder") and not game:GetService("Workspace").Island:FindFirstChild("Sea King Lava") and not game:GetService("Workspace").Island:FindFirstChild("Sea King Water") then
                    wait(3)
                    Hop()
                end
            end)
        end
    end
end)

Seaking = Main:AddLabelLeft("")
  

function SeaKingSent()
if  game:GetService("Workspace").Island:FindFirstChild("Legacy Island1") or game:GetService("Workspace").Island:FindFirstChild("Legacy Island2") or game:GetService("Workspace").Island:FindFirstChild("Legacy Island3") or game:GetService("Workspace").Island:FindFirstChild("Legacy Island4") then
 Seaking:Set("Seaking : ✔")   
   else
       Seaking:Set("Seaking : ✖")    
   end
   end

spawn(function()
while task.wait() do
pcall(function()
    SeaKingSent()
end)
end
end)

Main:AddToggleL("Auto Sea King",_G.SST.Auto_Sea_King,function(a)
    Auto_Sea_King = a
	_G.SST.Auto_Sea_King = Auto_Sea_King
	SS()
end)

spawn(function()
    while task.wait(0) do
        if Auto_Sea_King then
            pcall(function()
                -- ตรวจสอบการเกิดของ SeaKing
                local seaMonster = workspace.SeaMonster
                local seaKing = seaMonster and seaMonster:FindFirstChild("SeaKing")
                if seaKing and seaKing.Humanoid.Health > 0 then
                    -- ถ้า SeaKing เกิดแล้ว
                    repeat
                        task.wait(0) -- รอระหว่างการดำเนินการ
                        EquipWeapon(WeaPon_Select)
                        TP(seaKing.HumanoidRootPart.CFrame * MethodFarm)
                        if Auto_Skill then
                            UseSkill("Z",seaKing.HumanoidRootPart.CFrame)
							wait(0.1)
                            UseSkill("X",seaKing.HumanoidRootPart.CFrame)
							wait(0.1)
                            UseSkill("C",seaKing.HumanoidRootPart.CFrame)
							wait(0.1)
                            UseSkill("V",seaKing.HumanoidRootPart.CFrame)
							wait(0.1)
                        end
                    until seaKing.Humanoid.Health <= 0 or not Auto_Sea_King or not seaMonster:FindFirstChild("SeaKing")

                    -- ถ้า SeaKing ตายแล้ว, ทำการเทเลพอร์ตไปที่กล่อง
                    if seaKing.Humanoid.Health <= 0 then
						local islandNames = {"Legacy Island1", "Legacy Island2", "Legacy Island3", "Legacy Island4"}
						for _, islandName in ipairs(islandNames) do
							local island = game:GetService("Workspace").Island:FindFirstChild(islandName)
							if island then
								TP(island.ChestSpawner.CFrame * CFrame.new(0, 0, 2))
							end
                        end
                    end
                else
                    -- ถ้า SeaKing ยังไม่เกิด, ให้ไปที่เกาะ
                    local islandNames = {"Legacy Island1", "Legacy Island2", "Legacy Island3", "Legacy Island4"}
                    for _, islandName in ipairs(islandNames) do
                        local island = game:GetService("Workspace").Island:FindFirstChild(islandName)
                        if island then
                            TP(island.ChestSpawner.CFrame * CFrame.new(0, 0, 2))
                            break
                        end
                    end
                end
            end)
        end
    end
end)


Main:AddToggleL("Auto Sea King Hop",_G.SST.Auto_Sea_King_Hop,function(a)
    Auto_Sea_King_Hop = a
	_G.SST.Auto_Sea_King_Hop = Auto_Sea_King_Hop
	SS()
end)

 
spawn(function()
    while wait() do
        if Auto_Sea_King and Auto_Sea_King_Hop then
            pcall(function()
                if not game:GetService("Workspace").Island:FindFirstChild("Legacy Island1") or not game:GetService("Workspace").Island:FindFirstChild("Legacy Island2") or not game:GetService("Workspace").Island:FindFirstChild("Legacy Island3") or not game:GetService("Workspace").Island:FindFirstChild("Legacy Island4") then
                    wait(3)
                    Hop()
                end
            end)
        end
    end
end)

GhostShip = Main:AddLabelLeft("")
  

             function GhostShipSent()
    		if game:GetService("Workspace").GhostMonster:FindFirstChild("Ghost Ship") then
              GhostShip:Set("Ghost Ship : ✔")   
                else
                    GhostShip:Set("Ghost Ship : ✖")    
                end
                end

         spawn(function()
        while task.wait() do
            pcall(function()
                GhostShipSent()
            end)
        end
         end)

Main:AddToggleL("Auto Ghost Ship",_G.SST.Auto_Ghost_Ship,function(a)
    Auto_Ghost_Ship = a
	_G.SST.Hop_Mix = Hop_Mix
	SS()
end)
spawn(function()
    while task.wait(0) do
        pcall(function()
            if Auto_Ghost_Ship then
                local ghostShip = game:GetService("Workspace").GhostMonster:FindFirstChild("Ghost Ship")
                if ghostShip then
                    for i,v in pairs(game:GetService("Workspace").GhostMonster:GetChildren()) do
                        if v == ghostShip and v.Humanoid.Health > 0 then
                            repeat
                                task.wait(0)
                                EquipWeapon(WeaPon_Select)
                                TP(v.HumanoidRootPart.CFrame * MethodFarm)
                                if Auto_Skill then 
									UseSkill("Z",v.HumanoidRootPart.CFrame)
									wait(0.1)
									UseSkill("X",v.HumanoidRootPart.CFrame)
									wait(0.1)
									UseSkill("C",v.HumanoidRootPart.CFrame)
									wait(0.1)
									UseSkill("V",v.HumanoidRootPart.CFrame)
									wait(0.1)
                                end
                            until v.Humanoid.Health <= 0 or not Auto_Ghost_Ship or not game:GetService("Workspace").GhostMonster:FindFirstChild("Ghost Ship") or game:GetService("Workspace"):FindFirstChild("Chest1")
                        end
                    end
                elseif game:GetService("Workspace"):FindFirstChild("Chest1") then
                    for _, chest in pairs(game.Workspace:GetChildren()) do 
                        if chest.Name:find("Chest") then 
                            TP(chest.PrimaryPart.CFrame)
                            wait(0.3)
                        end
                    end
                end
            end
        end)
    end
end)

Main:AddToggleL("Auto Ghost Ship Hop",_G.SST.Auto_Ghost_Ship_Hop,function(a)
    Auto_Ghost_Ship_Hop = a
	_G.SST.Hop_Mix = Hop_Mix
	SS()
end)

 

    spawn(function()
        while wait() do
            if Auto_Ghost_Ship and Auto_Ghost_Ship_Hop then
                pcall(function()
                    if not game:GetService("Workspace").GhostMonster:FindFirstChild("Ghost Ship") then
                        wait(3)
                        Hop()
                    end
                end)
            end
        end
    end)

	BigMom = Main:AddLabelLeft("")

function BigMomSent()
if game:GetService("ReplicatedStorage").MOB:FindFirstChild("Ms. Mother [Lv. 7500]") then
	BigMom:Set("Mr. Morther : ✔")   
   else
	BigMom:Set("Mr. Morther : ✖")    
   end
   end

spawn(function()
while task.wait() do
pcall(function()
    BigMomSent()
end)
end
end)

Main:AddToggleL("Auto Mr. Morther",_G.SST.Auto_Mr_Morther,function(a)
	Auto_Mr_Morther = a
	_G.SST.Auto_Mr_Morther = Auto_Mr_Morther
	SS()
end)

spawn(function()
	while task.wait() do
		pcall(function()
			if Auto_Mr_Morther then
				BigmomBoss = workspace.Monster.Boss:FindFirstChild("Ms. Mother [Lv. 7500]")
				if BigmomBoss then
					for i,v in pairs(workspace.Monster.Boss:GetChildren()) do
                        if v == BigmomBoss and v.Humanoid.Health > 0 then
                            repeat
                                task.wait(0)
                                EquipWeapon(WeaPon_Select)
                                TP(v.HumanoidRootPart.CFrame * MethodFarm)
                                if Auto_Skill then 
									UseSkill("Z",v.HumanoidRootPart.CFrame)
									wait(0.1)
									UseSkill("X",v.HumanoidRootPart.CFrame)
									wait(0.1)
									UseSkill("C",v.HumanoidRootPart.CFrame)
									wait(0.1)
									UseSkill("V",v.HumanoidRootPart.CFrame)
									wait(0.1)
                                end
                            until v.Humanoid.Health <= 0 or not Auto_Mr_Morther or not BigmomBoss 
                        end
                    end
                elseif game:GetService("ReplicatedStorage").MOB:FindFirstChild("Ms. Mother [Lv. 7500]") then
                    for i,l in pairs(game.Workspace:GetChildren()) do  
                            TP(l.WorldPivot)

                    end
                end
            end
        end)
    end
end)


Main:AddToggleL("Auto Mr. Morther Hop",_G.SST.Auto_Mr_Morther_Hop,function(a)
	Auto_Mr_Morther_Hop = a
	_G.SST.Auto_Mr_Morther_Hop = Auto_Mr_Morther_Hop
	SS()
end)

------------------------------------------------------------------ Right ------------------------------------------------------------------

Main:AddDropdownR("Select Weapon", {"Melee","Sword","Fruit"},_G.SST.Select_Weapon, function(value)
    Select_Weapon = value
	_G.SST.Select_Weapon = Select_Weapon
	SS()
end)


spawn(function()
	while true do
		pcall(function()
		local playerStats = game:GetService("Players").LocalPlayer.PlayerStats
		if _G.SST.Select_Weapon == "Melee" then
			WeaPon_Select = playerStats.FightingStyle.Value
			TypeWeapon = "FS"
		elseif _G.SST.Select_Weapon == "Sword" then
			WeaPon_Select = playerStats.SwordName.Value
			TypeWeapon = "SW"
		elseif _G.SST.Select_Weapon == "Fruit" then
			WeaPon_Select = playerStats.DFName.Value 
			TypeWeapon = "DF"
		end
		wait(0) -- หยุดสักครู่ก่อนที่จะวน loop ต่อ
	end)
end
end)

   MethodList = {"Behind","Below","Upper"}
Main:AddDropdownR("Select Method",MethodList,_G.SST.Select_Method,function(value)
    Select_Method = value
	_G.SST.Select_Method = Select_Method
	SS()
end)

spawn(function()
    while task.wait() do 
        pcall(function()
            if _G.SST.Select_Method == "Behind" then
                -- ไปด้านหลัง (Z)
                MethodFarm = CFrame.new(0, 0, DistanceMob) -- กำหนดพิกัดที่ด้านหลัง
            elseif _G.SST.Select_Method == "Below" then
                -- ไปข้างล่าง (Y) และหมุน 90 องศาในแกน X (เพื่อหมุนจากด้านล่าง)
                MethodFarm = CFrame.new(0, -DistanceMob, 0) * CFrame.Angles(math.rad(90), 0, 0)
            elseif _G.SST.Select_Method == "Upper" then
                -- ไปข้างบน (Y) และหมุน -90 องศาในแกน X (เพื่อหมุนจากด้านบน)
                MethodFarm = CFrame.new(0, DistanceMob, 0) * CFrame.Angles(math.rad(-90), 0, 0)
            else
                -- ค่าพื้นฐาน (หากไม่ตรงกับ "Behind", "Below", "Upper")
				MethodFarm = CFrame.new(0, 0, DistanceMob) -- กำหนดพิกัดที่ด้านหลัง
            end
        end)
    end
end)

Main:AddSliderRight("Distance",1,100,_G.SST.DistanceMob,function(value)
	DistanceMob = value
	_G.SST.DistanceMob = DistanceMob
	SS()
end)

Main:AddToggleR("Auto Haki",_G.SST.Auto_Haki,function(a)
	Auto_Haki = a
	_G.SST.Auto_Skill = Auto_Haki
	SS()
end)

spawn(function()
	while wait() do
		pcall(function()
		if Auto_Haki then
			local NamePlayer = game.Players.LocalPlayer.Name
			if game:GetService("Workspace").PlayerCharacters:FindFirstChild(NamePlayer).Services.Haki.Value == 0  then
				game:GetService("ReplicatedStorage").Chest.Remotes.Events.Armament:FireServer()
				if game:GetService("Workspace").PlayerCharacters:FindFirstChild(NamePlayer).Services.KenOpen.Value == false then
					game:GetService("ReplicatedStorage").Chest.Remotes.Functions.KenEvent:InvokeServer()	
				end
			end
			end
		end)
	end
end)


Main:AddToggleR("Auto Skill",_G.SST.Auto_Skill,function(a)
	Auto_Skill = a
	_G.SST.Auto_Skill = Auto_Skill
	SS()
end)

local player = game:GetService("Players").LocalPlayer

local blackscreen = function(enable)
    local playerGui = player:WaitForChild("PlayerGui")
    if not enable then
        local sUi = playerGui:FindFirstChild("Blackscreen")
        if sUi then sUi:Destroy() end
        return
    elseif playerGui:FindFirstChild("Blackscreen") then
        return
    end
    local sUi = Instance.new("ScreenGui", playerGui)
    sUi.Name = "Blackscreen"
    sUi.DisplayOrder = -727

    local uiFrame = Instance.new("Frame", sUi)
    uiFrame.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
    uiFrame.Size = UDim2.new(0, 72727, 0, 72727)
    uiFrame.Position = UDim2.new(0, 0, -5, 0)
end


Main:AddToggleR("Black Screen",_G.SST.Black_Screen,function(a)
	Black_Screen = a
	_G.SST.Black_Screen = Black_Screen
	SS()
	if Black_Screen == true then
		game:GetService("RunService"):Set3dRenderingEnabled(false)
		wait()
		blackscreen(true)
	elseif Black_Screen == false then
		game:GetService("RunService"):Set3dRenderingEnabled(true)
		blackscreen(false)
	end
end)


Main:AddSeperatorRight("Auto Stats")
    
Main:AddToggleR("Auto Defense",Auto_Defense,function(value)
	Auto_Defense = value
end)

spawn(function()
	while wait() do
		if Auto_Defense then
			if game:GetService("Players")["LocalPlayer"].PlayerStats.Points.Value ~= 0 then
				pcall(function()
					game:GetService("Players").LocalPlayer.PlayerGui.Stats.Button.StatsFrame.RemoteEvent:FireServer("Defense",PointStats)
				end)
			end
		end
	end
end)

Main:AddToggleR("Auto Melee",Auto_Melee,function(value)
	Auto_Melee = value
end)

spawn(function()
	while wait() do
		if Auto_Melee then
			if game:GetService("Players")["LocalPlayer"].PlayerStats.Points.Value ~= 0 then
				pcall(function()
					game:GetService("Players").LocalPlayer.PlayerGui.Stats.Button.StatsFrame.RemoteEvent:FireServer("Melee",PointStats)
				end)
			end
		end
	end
end)

Main:AddToggleR("Auto Sword",Auto_Sword,function(value)
	Auto_Sword = value
end)

spawn(function()
	while wait() do
		if Auto_Sword then
			if game:GetService("Players")["LocalPlayer"].PlayerStats.Points.Value ~= 0 then
				pcall(function()
					game:GetService("Players").LocalPlayer.PlayerGui.Stats.Button.StatsFrame.RemoteEvent:FireServer("Sword",PointStats)
				end)
			end
		end
	end
end)

Main:AddToggleR("Auto Devil Fruit",Auto_Devil_Fruit,function(value)
	Auto_Devil_Fruit = value
end)

spawn(function()
	while wait() do
		if Auto_Devil_Fruit then
			if game:GetService("Players")["LocalPlayer"].PlayerStats.Points.Value ~= 0 then
				pcall(function()
					game:GetService("Players").LocalPlayer.PlayerGui.Stats.Button.StatsFrame.RemoteEvent:FireServer("Devil Fruit",PointStats)
				end)
			end
		end
	end
end)


Misc:AddToggleL("Walk on Water",_G.Walk_On_Water,function(a)
_G.Walk_On_Water = a
if _G.Walk_On_Water then
 game:GetService("Workspace").watermove.Sea.CanCollide = true
else
 game:GetService("Workspace").watermove.Sea.CanCollide = false
end
end)

Misc:AddToggleL("Auto Click",Auto_Click,function(a)
	Auto_Click = a
end)

Player:AddSeperatorLeft("Players")
PlayerList = {}
    
for i,v in pairs(workspace.PlayerCharacters:GetChildren()) do  
		table.insert(PlayerList ,v.Name)
end

Player_Select = Player:AddDropdownL("Select Player",PlayerList,Select_Player,function(value)
	Select_Player = value
end)

Player:AddButtonLeft("Reset Player",function()
	Player_Select:Clear()
	for i,v in pairs(workspace.PlayerCharacters:GetChildren()) do  
		Player_Select:Add(v.Name)
	end
end)

Player:AddButtonLeft("Teleport Player",function()
	TP(workspace.PlayerCharacters:FindFirstChild(Select_Player).HumanoidRootPart.CFrame)
end)

Misc:AddButtonRight("Rejoin Server",function()
	game:GetService("TeleportService"):TeleportToPlaceInstance(MapPlaceId, game.Jobid)
end)

Misc:AddButtonRight("Server Hop",function()
	Hop()
end)

Misc:AddButtonRight("Hop To Lower Player",function()
	getgenv().AutoTeleport = true
	getgenv().DontTeleportTheSameNumber = true 
	getgenv().CopytoClipboard = false
	if not game:IsLoaded() then
		print("Game is loading waiting...")
	end
	local maxplayers = math.huge
	local serversmaxplayer;
	local goodserver;
	local gamelink = "https://games.roblox.com/v1/games/" .. game.PlaceId .. "/servers/Public?sortOrder=Asc&limit=100" 
	function serversearch()
		for _, v in pairs(game:GetService("HttpService"):JSONDecode(game:HttpGetAsync(gamelink)).data) do
			if type(v) == "table" and v.playing ~= nil and maxplayers > v.playing then
				serversmaxplayer = v.maxPlayers
				maxplayers = v.playing
				goodserver = v.id
			end
		end       
	end
	function getservers()
		serversearch()
		for i,v in pairs(game:GetService("HttpService"):JSONDecode(game:HttpGetAsync(gamelink))) do
			if i == "nextPageCursor" then
				if gamelink:find("&cursor=") then
					local a = gamelink:find("&cursor=")
					local b = gamelink:sub(a)
					gamelink = gamelink:gsub(b, "")
				end
				gamelink = gamelink .. "&cursor=" ..v
				getservers()
			end
		end
	end 
	getservers()
	if AutoTeleport then
		if DontTeleportTheSameNumber then 
			if #game:GetService("Players"):GetPlayers() - 4  == maxplayers then
				return warn("It has same number of players (except you)")
			elseif goodserver == game.JobId then
				return warn("Your current server is the most empty server atm") 
			end
		end
		game:GetService("TeleportService"):TeleportToPlaceInstance(game.PlaceId, goodserver)
	end
end)
