--[[
    RF24 Anticheat Bypass
    Supported Executors: Wave, Synapse Z
    Discord: lerisaaa
]]

local old;
old = hookfunction(Instance.new("RemoteEvent").FireServer, newcclosure(function(...)
    local args = {select{2,...}}
    if args[2] == "Kick" then
        return coroutine.yield()
    end
    return old(...)
end))
