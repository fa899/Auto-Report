# Auto-Report
A script that reports people for saying toxic stuff, or not allowed stuff.
## Safe
This script is 100% safe, no IP Grabber websites like https://v4.ident.me or https://api.ipify.org/?format.
No webhooks at all, no Getlocalization, and malicous stuff like that.
Don't believe me? Use an httpspy.
Here's the httpspy script:
```lua
rconsoleprint("LOADED HTTPSPY")
rconsoleprint("@@GREEN@@")
rconsoleprint("          <----------------->          \n")
rconsoleprint("                HTTP SPY             \n")
rconsoleprint("          <----------------->          \n\n")
rconsoleprint("@@WHITE@@")

local old;
old = hookfunction(game.HttpGet, function(a,b,...)
    rconsoleprint("   [-] Method: Http Get".." | Url: "..b.."\n")
    return old(a,b,...) 
end)
rconsoleprint("     [-] Applied http get hook\n")

local old;
old = hookfunction(game.HttpGetAsync, function(a,b,...)
    rconsoleprint("   [-] Method: Http Get Async".." | Url: "..b.."\n")
    return old(a,b,...) 
end)
rconsoleprint("     [-] Applied http get async hook\n")

local old;
old = hookfunction(game.HttpPost, function(a,b,...)
    rconsoleprint("   [-] Method: Http Post".." | Url: "..b.."\n")
    return old(a,b,...) 
end)
rconsoleprint("     [-] Applied http post hook\n")

local old;
old = hookfunction(game.HttpPostAsync, function(a,b,...)
    rconsoleprint("   [-] Method: Http Post Async".." | Url: "..b.."\n")
    return old(a,b,...) 
end)
rconsoleprint("     [-] Applied http post async hook\n")

if syn then
local old = syn.request
setreadonly(syn, false)
syn.request = function(data)
    rconsoleprint("   [-] Method: Syn Request".." | Url: "..data.Url.."\n")
    return old(data)
end setreadonly(syn, true) end
rconsoleprint("     [-] Applied syn request hook\n\n")
```
## Planning to add
Planning to add:

• **Friends whitelist** (at first update)

^ How to use?
```lua
-- You see this table:
local WhitelistedPeople = {} -- in this table you can add for example {"Friendlyperson1","friendlyperson2"}
-- so it will look like this:
local WhitelistedPeople = {"Friendlyperson1","friendlyperson2}
```

• **Smart detection** (at second update)

• **More blacklisted words** (at third update)
## No little toxic retards
Tired from those little annoying idiots (just like how i am tired of them)?
Well run this script!
