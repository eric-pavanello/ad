local function safeLoad(url)
    local success, errorMsg = pcall(function()
        loadstring(game:HttpGet(url))()
    end)
    
    if success then
        print("Script executado com sucesso!")
    else
        warn("Erro ao executar o script: " .. errorMsg)
    end
end

local gameId = game.PlaceId

if gameId == 2753915549 or gameId == 4442272183 or gameId == 7449423635 then
    -- Blox Fruits
    print("Detectado Blox Fruits, executando script...")
    safeLoad("https://raw.githubusercontent.com/Tsuo7/TsuoHub/main/TsuoHubOld")
elseif gameId == 10260193230 then
    -- Meme Sea
    print("Detectado Meme Sea, executando script...")
    safeLoad("https://raw.githubusercontent.com/Tsuo7/TsuoHub/main/memesea")
else
    print("Jogo não reconhecido. Nenhum script foi executado.")
end
