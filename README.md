# 
local ScreenGui = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local Title = Instance.new("TextLabel")
local ImageLabel = Instance.new("ImageLabel")
local PasswordBox = Instance.new("TextBox")
local SubmitButton = Instance.new("TextButton")
local UICorner = Instance.new("UICorner")
local UIStroke = Instance.new("UIStroke")
local UIListLayout = Instance.new("UIListLayout")

local CorrectPassword = "syntax"
local isAuthenticated = false

if game.Players.LocalPlayer:FindFirstChild("PlayerGui"):FindFirstChild("TubersGui") then
	game.Players.LocalPlayer:FindFirstChild("PlayerGui"):FindFirstChild("TubersGui"):Destroy()
end

ScreenGui.Name = "TubersGui"
ScreenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")

Frame.Parent = ScreenGui
Frame.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
Frame.Size = UDim2.new(0, 700, 0, 3000) 
Frame.Position = UDim2.new(0.5, -225, 0.5, -325)
Frame.BorderSizePixel = 0
Frame.Active = true
Frame.Draggable = true



Title.Parent = Frame
Title.Text = "as00kidd v.5  login"
Title.TextColor3 = Color3.fromRGB(255, 255, 255)
Title.BackgroundTransparency = 1
Title.Size = UDim2.new(1, 0, 0, 50)
Title.Position = UDim2.new(0, 0, 0, 10)
Title.Font = Enum.Font.SourceSansBold
Title.TextSize = 26
Title.TextScaled = true
Title.TextWrapped = true

ImageLabel.Parent = Frame
ImageLabel.Size = UDim2.new(0.55, 0, 0.25, 0)
ImageLabel.Position = UDim2.new(0.1, 0, 0.1, 0)
ImageLabel.BackgroundTransparency = 1
ImageLabel.Image = "rbxassetid://88053756652813"

PasswordBox.Parent = Frame
PasswordBox.Size = UDim2.new(0.8, 0, 0, 45)
PasswordBox.Position = UDim2.new(0.1, 0, 0.4, 0)
PasswordBox.PlaceholderText = "Enter Password now loololololooloolol"
PasswordBox.TextColor3 = Color3.fromRGB(204, 0, 255)
PasswordBox.BackgroundColor3 = Color3.fromRGB(50, 50, 50)
PasswordBox.TextScaled = true
PasswordBox.ClearTextOnFocus = false

SubmitButton.Parent = Frame
SubmitButton.Size = UDim2.new(0.8, 0, 0, 45)
SubmitButton.Position = UDim2.new(0.1, 0, 0.5, 0)
SubmitButton.BackgroundColor3 = Color3.fromRGB(200, 0, 0)
SubmitButton.Text = "Submit"
SubmitButton.TextSize = 18
SubmitButton.TextColor3 = Color3.fromRGB(230, 230, 230)

UIListLayout.Parent = Frame
UIListLayout.SortOrder = Enum.SortOrder.LayoutOrder
UIListLayout.Padding = UDim.new(0, 10)
UIListLayout.HorizontalAlignment = Enum.HorizontalAlignment.Center

local function createButton(name, callback)
	if not isAuthenticated then return end

	local Button = Instance.new("TextButton")
	Button.Parent = Frame
	Button.Size = UDim2.new(0.8, 0, 0, 50)
	Button.BackgroundColor3 = Color3.fromRGB(200, 0, 0)
	Button.Text = name
	Button.TextSize = 18
	Button.TextColor3 = Color3.fromRGB(230, 230, 230)
	Button.MouseButton1Click:Connect(callback)
end

SubmitButton.MouseButton1Click:Connect(function()
	if PasswordBox.Text == CorrectPassword then
		isAuthenticated = true
		PasswordBox:Destroy()
		SubmitButton:Destroy()
		Title.Text = "u00pkid6 reborn"

		createButton("Skybox", function()
			local skybox = Instance.new("Sky")
			local skyId = "rbxassetid://118693644365208"
			skybox.SkyboxBk = skyId
			skybox.SkyboxDn = skyId
			skybox.SkyboxFt = skyId
			skybox.SkyboxLf = skyId
			skybox.SkyboxRt = skyId
			skybox.SkyboxUp = skyId
			skybox.Parent = game.Lighting
		end)



		createButton("as00kidd music", function()
			local sound = Instance.new("Sound")
			sound.SoundId = "rbxassetid://89410458182135"
			sound.Volume = 2
			sound.Looped = true
			sound.Parent = game.Workspace
			sound:Play()
		end)






		createButton("Jumpscare", function()
			for _, player in pairs(game.Players:GetPlayers()) do
				if player and player:FindFirstChild("PlayerGui") then
					local jumpscareGUI = Instance.new("ScreenGui", player.PlayerGui)
					local image = Instance.new("ImageLabel", jumpscareGUI)
					image.Size = UDim2.new(1, 0, 1, 0)
					image.Image = "rbxassetid://88053756652813"
					local jumpscareSound = Instance.new("Sound", workspace)
					jumpscareSound.SoundId = "rbxassetid://6129291390"
					jumpscareSound.Volume = 66
					jumpscareSound:Play()
					wait(8)
					jumpscareSound:Destroy()
					jumpscareGUI:Destroy()
				end
			end
		end)



		-- ✅ NEW BUTTON: Display Message ✅
		createButton("hint 1", function()
			local m = Instance.new("Hint", game.Workspace)
			m.Text = "as00kidd has killed your game"
			wait(2222222222222222222222222222222222222222222222222222) -- Show message for 3 seconds

		end)

		-- ✅ NEW BUTTON: Display Message ✅
		createButton("hint 2", function()
			local m = Instance.new("Hint", game.Workspace)
			m.Text = "as00kidd is better"
			wait(2222222222222222222222222222222222222222222222222222) -- Show message for 3 seconds

		end)

		createButton("hint 3", function()
			local m = Instance.new("Hint", game.Workspace)
			m.Text = "as00kidd has hacked the game  🙏discord.gg/6DpfFMS9 🙏"
			wait(2222222222222222222222222222222222222222222222222222) -- Show message for 3 seconds

		end)



		-- ✅ NEW BUTTON: Display Message ✅
		createButton("m", function()
			local m = Instance.new("Message")
			m.Parent = game.Workspace
			m.Text = "leave before as00kidd hacks you"
			wait(5) -- Message stays for 5 seconds
			m:Destroy()
		end)

		-- ✅ NEW BUTTON: Display Message ✅
		createButton("m", function()
			local m = Instance.new("Message")
			m.Parent = game.Workspace
			m.Text = "your game got noobed"
			wait(5) -- Message stays for 5 seconds
			m:Destroy()
		end)

		-- ✅ NEW BUTTON: Display Message ✅
		createButton("m", function()
			local m = Instance.new("Message")
			m.Parent = game.Workspace
			m.Text = "you think you can escape yall islam"
			wait(5) -- Message stays for 5 seconds
			m:Destroy()
		end)


		createButton("m", function()
			local m = Instance.new("Message")
			m.Parent = game.Workspace
			m.Text = "as00kid fucked the game LOLLLLL"
			wait(5) -- Message stays for 5 seconds
			m:Destroy()
		end)


		createButton("m", function()
			local m = Instance.new("Message")
			m.Parent = game.Workspace
			m.Text = "WE LOVE YOU GEORGE"
			wait(5) -- Message stays for 5 seconds
			m:Destroy()
		end)




		createButton("Decal Spam", function()
			local textureId = "rbxassetid://115264561439206"
			for _, part in pairs(workspace:GetDescendants()) do
				if part:IsA("BasePart") then
					for _, existing in pairs(part:GetChildren()) do
						if existing:IsA("Texture") or existing:IsA("Decal") then
							existing:Destroy()
						end
					end

					local faces = {Enum.NormalId.Front, Enum.NormalId.Back, Enum.NormalId.Left, Enum.NormalId.Right, Enum.NormalId.Top, Enum.NormalId.Bottom}
					for _, face in pairs(faces) do
						local texture = Instance.new("Texture")
						texture.Texture = textureId
						texture.StudsPerTileU = 10
						texture.StudsPerTileV = 10
						texture.Face = face
						texture.Parent = part
					end
				end
			end
		end)




		createButton("Decal Spam", function()
			local textureId = "rbxassetid://118693644365208"
			for _, part in pairs(workspace:GetDescendants()) do
				if part:IsA("BasePart") then
					for _, existing in pairs(part:GetChildren()) do
						if existing:IsA("Texture") or existing:IsA("Decal") then
							existing:Destroy()
						end
					end

					local faces = {Enum.NormalId.Front, Enum.NormalId.Back, Enum.NormalId.Left, Enum.NormalId.Right, Enum.NormalId.Top, Enum.NormalId.Bottom}
					for _, face in pairs(faces) do
						local texture = Instance.new("Texture")
						texture.Texture = textureId
						texture.StudsPerTileU = 10
						texture.StudsPerTileV = 10
						texture.Face = face
						texture.Parent = part
					end
				end
			end
		end)




		createButton("Particle spam", function()
			for _, player in pairs(game.Players:GetPlayers()) do
				if player.Character then  -- Ensure the player has a character
					local parts = {"Head", "Torso", "Left Arm", "Right Arm", "Left Leg", "Right Leg"}  -- List of parts
					for _, partName in ipairs(parts) do
						local part = player.Character:FindFirstChild(partName)
						if part then
							for i = 1, 5 do  -- Create multiple ParticleEmitters per part
								local emit = Instance.new("ParticleEmitter")
								emit.Parent = part
								emit.Texture = "http://www.roblox.com/asset/?id=108644129095827"
								emit.VelocitySpread = 100000
								emit.Rate = emit.Rate * 6  -- Increase particle emission rate
							end
						end
					end
				end
			end
		end)






		createButton("WE LOVE YOU GEORGE", function()
			local spamText = "WE LOVE YOU GEORGE" -- The text you want to display

			-- Loop through all the parts in the workspace
			for _, part in ipairs(workspace:GetDescendants()) do
				if part:IsA("BasePart") then
					-- Remove existing SurfaceGuis to prevent stacking
					for _, existing in ipairs(part:GetChildren()) do
						if existing:IsA("SurfaceGui") then
							existing:Destroy()
						end
					end

					-- Apply text on all faces of each part
					local faces = {
						Enum.NormalId.Front, Enum.NormalId.Back,
						Enum.NormalId.Left, Enum.NormalId.Right,
						Enum.NormalId.Top, Enum.NormalId.Bottom
					}

					-- Loop through the faces and apply text on each
					for _, face in ipairs(faces) do
						-- Create a new SurfaceGui for each face
						local surfaceGui = Instance.new("SurfaceGui")
						surfaceGui.Adornee = part
						surfaceGui.Face = face
						surfaceGui.Parent = part

						-- Create a TextLabel inside the SurfaceGui to display the text
						local textLabel = Instance.new("TextLabel")
						textLabel.Size = UDim2.new(1, 0, 1, 0) -- Make it cover the entire face of the part
						textLabel.Text = spamText
						textLabel.TextColor3 = Color3.fromRGB(255, 157, 0) -- Red text (you can change the color)
						textLabel.TextScaled = true -- Ensure the text scales to fit the face
						textLabel.BackgroundTransparency = 1 -- Make the background transparent
						textLabel.Parent = surfaceGui
					end
				end
			end

			print("Text spam applied to the entire map!")
		end)


		createButton("game killer", function()
			for i = 1, 1665 do
				local part = Instance.new("Part")
				part.Size = Vector3.new(3, 3, 3)
				part.Position = Vector3.new(math.random(-50, 50), math.random(10, 100), math.random(-50, 50))
				part.Color = Color3.fromRGB(math.random(0, 255), math.random(0, 255), math.random(0, 255))
				part.Material = Enum.Material.Rubber
				part.Parent = game.Workspace
				part.Anchored = false
			end
		end)



	else
		Title.Text = "Wrong Password goofy kid"
		wait(1.5)
		Title.Text = "as00kidd v.5 login "
	end 
end) game.StarterGui:SetCore("SendNotification", {
	Title = "as00kidd v.5 ";
	Text = "Script made by as00kidd"; -- what the text says (ofc)
	Duration = 10;
})
