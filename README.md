# This repo is for my crazy lua experiments/scripts/ui libraries
## My New Library

### loadstring
```lua
loadstring(game:HttpGet('https://raw.githubusercontent.com/ilovekrabs/alexegei/ong/mynewlib'))()
```

### How to use

#### First you have to get the loadstring and set it as a local
```lua
local MyUILibrary = loadstring(game:HttpGet("https://raw.githubusercontent.com/ilovekrabs/alexegei/ong/mynewlib"))()
```

#### After that you can call this function to create the library
```lua
local Main = MyUILibrary:New({
  Title = "My New Library", --: Title of the UI LIbrary
  Size = UDim2.fromOffset(450,350) --: Size of the UI LIbrary
})
```

#### Now to load a tab all you have to do is this
```lua
local Tab = Main:Tab({
  Title = "Tab", --: Title of the Tab
  Icon = "rbxassetid://11356040586" --: Icon of the Tab
})
```

#### Here are all of elements that you can use

##### Button
```lua
local Button = Tab:Button({
  Title = "Button",
  Callback = function()
    print("cum chugging monkeys uwu")
    
    Button:SetText("sus")
    Button:SetCallback(function()
      print("callback has been changed")
    end)
  end
})
```

##### Toggle
```lua
local Toggle = Tab:Toggle({
  Title = "Toggle",
  Callback = function(v)
    print(v)
  end
})
```

##### Label
```lua
local Label = Tab:Label({
  Message = "I love labels."
})

wait(3)

label:SetText("That was a lie!")
```

##### Github Inspired Labels
```lua
local Info = Tab:Info({
  Message = "This UI Library was created by rizz god#5961 and random#0915."
})

local Warning = Tab:Warning({
  Message = "Dont agro bees or you're gonna' get stung!"
})

local Error = Tab:Error({
  Message = "Something bad happened."
})

wait(3)
Info:SetText("This is a Info Label.")
Warning:SetText("This is a Warning Label.")
Error:SetText("This is a Error Label.")
```

##### Slider
```lua
local Slider = Tab:Slider({
  Title = "Slider",
	Min = 0,
	Max = 100,
	Default = 50,
  Callback = function(v)
    print(v)
  end
})
```

#### Dropdown
- Currently unavailable since im bad at coding xD

## Notification Library

### loadstring
```lua
loadstring(game:HttpGet('https://raw.githubusercontent.com/ilovekrabs/alexegei/ong/notificationlib.lua'))()
```

### How to use

#### First you have to set it as a local, like this
```lua
local notify = loadstring(game:HttpGet("https://raw.githubusercontent.com/ilovekrabs/alexegei/ong/notificationlib.lua"))()
```

#### After that you call this function which is just credits, since i need to credit myself somehow
```lua
local credits = notify:made_by_rizz_god_5961()
```

#### And last but not least you just have to call this function
```lua
credits:notify("Hello!", "I'm an description.", 10, "Lime") -- Color variations can be Blue, Purple, Pink, Red, Orange, Yellow, Lime, Cyan
```
#### In the end the whole thing should look like this
```lua
local notify = loadstring(game:HttpGet("https://raw.githubusercontent.com/ilovekrabs/alexegei/ong/notificationlib.lua"))()

local credits = notify:made_by_rizz_god_5961()

credits:notify("Hello!", "I'm an description.", 10, "Lime") -- Color variations can be Blue, Purple, Pink, Red, Orange, Yellow, Lime, Cyan
```

#### To add more notifications in 1 execution you just have to copy and paste it like this
```lua
credits:notify("Hello!", "I'm an description.", 10, "Lime")
credits:notify("Hello!", "I'm an description.", 10, "Blue")
credits:notify("Hello!", "I'm an description.", 10, "Purple")
credits:notify("Hello!", "I'm an description.", 10, "Pink")
```

## Utilities
### loadstring
```lua
loadstring(game:HttpGet('https://raw.githubusercontent.com/ilovekrabs/alexegei/ong/Utilities'))()
```

### How to use

#### First you have to get the loadstring and set it as a local
```lua
local Utilities = loadstring(game:HttpGet("https://raw.githubusercontent.com/ilovekrabs/alexegei/ong/Utilities"))()
```

#### After that you can call this function to replace the function "for index, value in pairs()" so it's easier to write and read
```lua
local customTable = {
    ["cool index"] = "cool value",
    ["cooler index"] = "cooler value"
}

Utilities:P{
    Table = customTable, --: You can replace this with a table that isnt a local table, like this "{ ["index"] = "value" }"
    Callback = function(index, value)
        print(index, value) 
    end
}
```

#### You can also call this function that teleports you to specific places
##### You can use the Type "PLR"
```lua
Utilities:Teleport{
    Type = "PLR",
    Object = CFrame.new(0, 0, 0) --: This is the object CFrame, if you wanted to teleport to a certain player just type "game.Players["Certain Player Username"].Character.PrimaryPart" without the quotes ""
}
```

##### You can also use the Type "CF"
```lua
Utilities:Teleport{
    Type = "CF",
    Object = game.Workspace.CertainPartOrSomethingLikeThat, --: This is the object that gets teleported to the Target
    Target = game.Workspace.AnotherCertainPartLol --: This is the target
}
```
