Search in ‘esx_policejob/client/main.lua’ for

``lua
elseif action == 'handcuff' then

TriggerServerEvent('esx_policejob:handcuff', GetPlayerServerId(closestPlayer))


Replace it with:

elseif action == 'handcuff' then

TriggerServerEvent('esx_cuffanimation:startArrest',

GetPlayerServerId(closestPlayer))

Citizen.Wait(3100)

TriggerServerEvent('esx_policejob:handcuff',

GetPlayerServerId(closestPlayer))``
