_G.Thedarklord = true -- Variável global para controle

while wait() do
    if not _G.Thedarklord then
        return -- Finaliza o loop se Thedarklord for falso
    end

    if _G.Thedarklord then
        -- Obtém o serviço ReplicatedStorage e o evento remoto
        local Event = game:GetService("ReplicatedStorage").Remotes.DoubleReg
        
        -- Dispara o evento remoto 3 vezes
        for i = 1, 3 do
            Event:FireServer()
        end
    end
end
