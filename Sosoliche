local RunService = game:GetService("RunService")
local player = game.Players.LocalPlayer

-- Ждём загрузку персонажа
player.CharacterAdded:Connect(function(char)
	local humanoidRootPart = char:WaitForChild("HumanoidRootPart")

	-- Крутится постоянно
	RunService.RenderStepped:Connect(function()
		if humanoidRootPart then
			local rot = humanoidRootPart.Orientation
			humanoidRootPart.Orientation = Vector3.new(rot.X, rot.Y + 2, rot.Z)
		end
	end)
end)

-- Если персонаж уже загружен
if player.Character then
	player.Character:Destroy() -- Принудительно перезагрузим
end
