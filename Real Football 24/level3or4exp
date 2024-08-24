--[[
    RF24 Anticheat Bypass
    Supported Executors: Solara, Celery, Feather
    Discord: lerisaaa
]]

local repst             = game:GetService("ReplicatedStorage")
local nw                = repst:WaitForChild("network")
local sh                = nw:WaitForChild("Shared")
local revents           = sh:GetChildren()
local revent

local cnns = {}

for _, i in ipairs(revents) do
    if i:IsA("RemoteEvent") then
        revent = i
        break
    end
end

if revent then
    if revent.OnServerEvent then
        for _, cnn in ipairs(getconnections(revent.OnServerEvent)) do
            table.insert(cnns, cnn)
            cnn:Disable()
        end
    end
end
