local Players = game:GetService("Players")
local LP = Players.LocalPlayer

local RS = game:GetService("RunService")

_G.carry = true
while _G.carry == true do
    for _, plr in pairs(Players:GetPlayers()) do
        if plr ~= LP then
            local LPChar = LP.Character
            local plrChar = plr.Character
            if plrChar and LPChar then
                local args = {
                    [1] = LPChar,
                    [2] = plrChar
                }

                game:GetService("ReplicatedStorage").ActionEvents.PickBaby:FireServer(unpack(args))
                
                RS.Heartbeat:Wait()
                
                if plrChar and LPChar then
                    local args = {
                        [1] = LPChar,
                        [2] = plrChar
                    }

                    game:GetService("ReplicatedStorage").ActionEvents.DropBaby:FireServer(unpack(args))
                end
            end
        end
    end
    RS.Heartbeat:Wait()
end
