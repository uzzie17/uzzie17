local key = loadstring(game:HttpGet("https://pastebin.com/raw/cuC1tCvq"))()
local hwid = game:GetService("RbxAnalyticsService"):GetClientId()
for i,v in pairs(key) do 
    if v == hwid then
         getgenv().autofarm = false
         
         if autofarm == true then
             print("working")
            end
         
         spawn(function()
    while autofarm == true do
    local args = {
    [1] = "BlowBubble"
}

game:GetService("ReplicatedStorage").NetworkRemoteEvent:FireServer(unpack(args))
wait()
end
end)

spawn(function()
    while autofarm == true do
    local args = {
    [1] = "SellBubble",
    [2] = "Sell"
}

game:GetService("ReplicatedStorage").NetworkRemoteEvent:FireServer(unpack(args))
wait()
end    
end)
         else
             game.Players.localPlayer:Kick("not whitlisted")
   
    end 
      end
    

setclipboard(game:GetService("RbxAnalyticsService"):GetClientId())
    
