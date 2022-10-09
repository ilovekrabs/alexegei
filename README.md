# This repo is for my crazy lua experiments/scripts/ui libraries

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
#### in the end the whole thing should look like this
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
