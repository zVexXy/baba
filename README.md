local player = game.Players.LocalPlayer

local gui = Instance.new("ScreenGui")
gui.Parent = player:WaitForChild("PlayerGui")

local frame = Instance.new("Frame")
frame.Size = UDim2.new(0, 200, 0, 60)
frame.AnchorPoint = Vector2.new(0.5, 0.5)
frame.Position = UDim2.new(0.5, 0, 0.5, 0)
frame.BackgroundColor3 = Color3.fromRGB(40,40,40)
frame.BorderSizePixel = 2
frame.Active = true
frame.Draggable = true
frame.Parent = gui

local btnSurvivor = Instance.new("TextButton")
btnSurvivor.Size = UDim2.new(0.5, -6, 1, -12)
btnSurvivor.Position = UDim2.new(0, 6, 0, 6)
btnSurvivor.Text = "Sobrevivente"
btnSurvivor.TextScaled = true
btnSurvivor.BackgroundColor3 = Color3.fromRGB(40,180,40)
btnSurvivor.Parent = frame

local btnHunter = Instance.new("TextButton")
btnHunter.Size = UDim2.new(0.5, -6, 1, -12)
btnHunter.Position = UDim2.new(0.5, 6, 0, 6)
btnHunter.Text = "Caçador"
btnHunter.TextScaled = true
btnHunter.BackgroundColor3 = Color3.fromRGB(180,40,40)
btnHunter.Parent = frame

local modo = nil

btnSurvivor.MouseButton1Click:Connect(function()
    modo = "sobrevivente"
    btnSurvivor.BackgroundColor3 = Color3.fromRGB(80,220,80)
    btnHunter.BackgroundColor3 = Color3.fromRGB(180,40,40)
    print("Modo Sobrevivente ativado")
    -- coloque aqui o que o sobrevivente faz
end)

btnHunter.MouseButton1Click:Connect(function()
    modo = "caçador"
    btnHunter.BackgroundColor3 = Color3.fromRGB(220,80,80)
    btnSurvivor.BackgroundColor3 = Color3.fromRGB(40,180,40)
    print("Modo Caçador ativado")
    -- coloque aqui o que o caçador faz
end)
