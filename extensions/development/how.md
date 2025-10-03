---
sidebar_position: 3
parent: Developing Extensions
---

# **How do I make one?**
**All extension module names must start with "pgfk"**. For example, "Extension1" would not be valid, while "pgfkExtension1" would! This does not apply to `Extension.Data.Name`.

- You can get started by creating a ModuleScript in any of the places mentioned above and using the code at the bottom of this page!
- You can also join the discord server for community-made extensions!

# **Template**
```lua
-- holds the extension table itself
local Extension = {
    Data = {},
    Lifecycle = {}
}

-- name of the extension
Extension.Data.Name = "extension 1"

-- creator of the extension
Extension.Data.Creator = "creator 1"

-- order to be ran (priority 1 runs before priority 2, etc)
Extension.Data.Order = 3

-- this runs first
function Extension.Lifecycle.Init()
    print("extension 1 init")
end

-- this runs after every "Init" function has been called
function Extension.Lifecycle.Start()
    print("extension 1 start")
end

return Extension
```

---

[Back](/extensions/extensions.html){: .btn }