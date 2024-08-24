--[[
    MPS 4 A-Side Anticheat Bypass
    Supported Executors: Wave, Synapse Z
    Discord: lerisaaa
]]

local sizes = {}

local plr               = game:GetService("Players")
local char              = plr.Character
local lleg              = char:WaitForChild('Left Leg')
local rleg              = char:WaitForChild('Right Leg')
local larm              = char:WaitForChild('Left Arm')
local rarm              = char:WaitForChild('Right Arm')

local lcl1              = lleg:Clone()
local lcl2              = rleg:Clone()
local acl1              = larm:Clone()
local acl2              = rarm:Clone()

lcl1.Name = 'FakeLeg1'
lcl2.Name = 'FakeLeg2'
acl1.Name = 'FakeArm1'
acl2.Name = 'FakeArm2'

lcl1.Parent = char
lcl2.Parent = char
acl1.Parent = char
acl2.Parent = char

for _, i in ipairs(char:GetChildren()) do
    if i.ClassName == "Part" then
        sizes[i.Name] = i.Size
    end 
end

local old;
old = hookmetamethod(game, "__index", newcclosure(function(self, p)
    if p == "Size" and self.Parent == char then
        return Sizes[self.Name]
    end
    return old(self,p)
end))
