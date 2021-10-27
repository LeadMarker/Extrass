local Noti = {}
local TweenService = game:GetService("TweenService")
local YOffset = -20
local NewSet = -20


pcall(function()
    if game.CoreGui:FindFirstChild("Notilib") then
        game.CoreGui:FindFirstChild("Notilib"):Destroy()
    end
end)

local Notilib = Instance.new("ScreenGui")
Notilib.Name = "Notilib"
Notilib.Parent = game.CoreGui

color = Color3.fromRGB(0, 123, 255)

function Noti.Notify(title, text, waitT, accent)
    local NAccent = accent or color

    waitT = waitT or 5
    local Main = Instance.new("Frame")
    Main.Name = "Main"
    Main.Parent = Notilib
    Main.BackgroundColor3 = Color3.fromRGB(25, 25, 25)
    Main.BorderSizePixel = 0
    Main.Position = UDim2.new(-0.1, -75, 0.95, -20)
    Main.Size = UDim2.new(0, 150, 0, 40)

    local Side = Instance.new("Frame")
    Side.Name = "Side"
    Side.Parent = Main
    Side.BackgroundColor3 = NAccent
    Side.BorderSizePixel = 0
    Side.Size = UDim2.new(0, 3, 0, 40)

    local Notification = Instance.new("TextLabel")
    Notification.Name = "Notification"
    Notification.Parent = Side
    Notification.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    Notification.BackgroundTransparency = 1.000
    Notification.BorderSizePixel = 0
    Notification.Position = UDim2.new(3.33333325, 0, 0.119999997, 0)
    Notification.Size = UDim2.new(0, 140, 0, 10)
    Notification.Font = Enum.Font.Gotham
    Notification.Text = title or "Notification"
    Notification.TextColor3 = Color3.fromRGB(255, 255, 255)
    Notification.TextSize = 14.000
    Notification.TextXAlignment = Enum.TextXAlignment.Left

    local Text = Instance.new("TextLabel")
    Text.Name = "Text"
    Text.Parent = Side
    Text.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
    Text.BackgroundTransparency = 1.000
    Text.BorderSizePixel = 0
    Text.Position = UDim2.new(3.33333325, 0, 0.574999988, 0)
    Text.Size = UDim2.new(0, 135, 0, 10)
    Text.Font = Enum.Font.Gotham
    Text.Text = text or "This is the discription"
    Text.TextColor3 = Color3.fromRGB(255, 255, 255)
    Text.TextSize = 10.000
    Text.TextXAlignment = Enum.TextXAlignment.Left
    Text.AutomaticSize = Enum.AutomaticSize.X
    Text.TextTransparency = 1

    NewSet = NewSet -20

    local function amdone(lol)
        if lol then 
            Main:Destroy()
        end
    end

    local function finish(tween)
        if tween then 
            Text.TextTransparency = 0
            wait(waitT)
            Main:TweenPosition(UDim2.new(-10.0214723852, 0, 0.900481522, NewSet), Enum.EasingDirection.In, Enum.EasingStyle.Quart, 1, false,amdone)
        end
    end

    wait(1)

    Main:TweenSize(UDim2.new(0, Text.AbsoluteSize.X + 20, 0, 40), Enum.EasingDirection.In, Enum.EasingStyle.Quart, 0.3, false)
    Main:TweenPosition(UDim2.new(0.06, -75, 0.95, YOffset), Enum.EasingDirection.In, Enum.EasingStyle.Quart, 0.3, false, finish)


    YOffset = YOffset - 45

    wait(0.2)
end

return Noti
