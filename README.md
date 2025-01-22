# Delta
-- Chargement de la bibliothèque Delta Executor
local Delta = loadstring(game:HttpGet("https://raw.githubusercontent.com/DeltaExecutor/UI-Library/main/Library.lua"))()

-- Création de la fenêtre principale
local Window = Delta:Window("Cheat Interface", "Cheat Hub", Enum.KeyCode.RightControl)

-- Onglet "Game"
local GameTab = Window:Tab("Game")

GameTab:Section("Jeux disponibles")
GameTab:Button("Brookhaven", function()
    loadBrookhavenScripts()
end)

GameTab:Button("Blox Fruits", function()
    loadBloxFruitScripts()
end)

GameTab:Button("Murder Mystery 2", function()
    loadMM2Scripts()
end)

-- Onglet "+"
local PlusTab = Window:Tab("+")

PlusTab:Section("Cheat Hubs")
PlusTab:Button("RedzHub", function()
    print("RedzHub chargé")
end)

PlusTab:Button("R4D", function()
    print("R4D chargé")
end)

PlusTab:Button("Infiniyel", function()
    print("Infiniyel chargé")
end)

-- Onglet "Serius" (Brookhaven)
local SeriusTab = Window:Tab("Serius")

SeriusTab:Section("Pass Brookhaven")
SeriusTab:Button("Débloquer tous les Pass", function()
    print("Tous les Pass débloqués pour Brookhaven")
    -- Code pour débloquer les Pass
end)

-- Onglet "Troll" (Brookhaven)
local TrollTab = Window:Tab("Troll")

TrollTab:Section("Troll Options")
TrollTab:Button("Activer un troll", function()
    print("Troll activé")
    -- Ajouter ici les trolls
end)

-- Onglet "Indice" (MM2)
local IndiceTab = Window:Tab("Indice")

IndiceTab:Section("Infos MM2")
IndiceTab:Button("Afficher Murder/Serif", function()
    print("Murder : Player1, Serif : Player2")
    -- Code pour afficher les infos Murder/Serif
end)

IndiceTab:Button("Activer ESP", function()
    print("ESP activé")
    -- Code pour ESP (murder, serif, innocents)
end)

-- Onglet "MM2 Sup"
local MM2SupTab = Window:Tab("MM2 Sup")

MM2SupTab:Section("Rôles et Maps")
MM2SupTab:Button("100% Murder", function()
    print("Prochain rôle : Murder")
    -- Code pour 100% Murder
end)

MM2SupTab:Button("100% Serif", function()
    print("Prochain rôle : Serif")
    -- Code pour 100% Serif
end)

MM2SupTab:Textbox("Nom de la Map", "Entrez le nom ici", true, function(value)
    print("Map sélectionnée : " .. value)
    -- Sauvegarder le nom de la map sélectionnée
end)

MM2SupTab:Button("Confirmer la Map", function()
    print("Map confirmée")
    -- Code pour confirmer la map
end)

-- Onglet "Woaw" (Blox Fruits)
local WoawTab = Window:Tab("Woaw")

WoawTab:Section("Options Blox Fruits")
WoawTab:Dropdown("Choisissez un Fruit", {
    "Bomb",
    "Flame",
    "Ice",
    "Light",
    "Dark",
    "String",
    "Quake",
    "Buddha",
    "Phoenix",
    "Dragon",
    "Kitsune" -- Fruit ajouté
}, function(selectedFruit)
    print("Fruit sélectionné : " .. selectedFruit)
    -- Code pour donner le fruit
end)

WoawTab:Button("Farm Argent", function()
    print("Farming Argent...")
    -- Code pour farm argent
end)

WoawTab:Dropdown("Auto Farm", {"Melee", "Sword", "Fruit"}, function(farmType)
    print("Farming : " .. farmType)
    -- Code pour Auto Farm
end)

WoawTab:Textbox("Numéro de la Sea", "Entrez le numéro ici", true, function(value)
    print("Sea sélectionnée : " .. value)
    -- Vérifier si la Sea existe et TP
end)

WoawTab:Button("TP vers Sea", function()
    print("Téléportation vers la Sea")
    -- Code pour TP vers la Sea
end)

-- === Fonctions de chargement des scripts ===
function loadBrookhavenScripts()
    print("Scripts Brookhaven chargés")
    -- Ajouter le code Brookhaven ici
end

function loadBloxFruitScripts()
    print("Scripts Blox Fruits chargés")
    -- Ajouter le code Blox Fruits ici
end

function loadMM2Scripts()
    print("Scripts Murder Mystery 2 chargés")
    -- Ajouter le code MM2 ici
end
