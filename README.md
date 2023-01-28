# -MaskouuHub
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/MaSKaThGod/-MaskouuHub/main/Maskouu.lua"))()

local window = Library.new("Window") 

window:LockScreenBoundaries(true) 

local tab = window:Tab("Tab") 

local section = tab:Section("Section") 

local title = section:Title("Title") 
title:ChangeText("Title") 

local label = section:Label("Label") 
label:ChangeText("Label") 

local toggle = section:Toggle("Toggle", function(bool)
   print("Toggle is: "..tostring(bool))
end) -- Args(<String> Name, <Function> Callback)
toggle:Set(false) 

section:Button("Button", function()
   print("Pressed button!")
end) 

local dropdown = section:Dropdown("Dropdown") -- Args(<String> Name)
dropdown:ChangeText("Dropdown") -- Args(<String> NewText)
dropdown:Toggle("Toggle") 

section:Slider("Slider", function(val)
   print("Slider Value is: "..val)
end) 

local searchBar = section:SearchBar("Search...") -- Args(<String> PlaceholderText)
searchBar:Toggle("Toggle") 

section:Keybind("Keybind", function()
   print("Keybind pressed!")
end) 

section:TextBox("Textbox", function(txt)
   print("Textbox string is: "..txt)
end) 

section:ColorWheel("ColorWheel", function(color)
   print("ColorWheel color is: "..tostring(color))
end) 
