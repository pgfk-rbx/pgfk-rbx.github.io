---
layout: page
title: Extensions
permalink: /extensions
nav_order: 999
---

# **Extensions**

---

## **What are they?**

pgfk has "extensions", which are addons that extend the functionality of pgfk in ways such as:

- adding new Loaders
- adding new functionality

---

## **Where do they go?**

- Client extensions are only ran on the client, and they go in **ReplicatedStorage/Extensions/Client**.
- Shared extensions run on both the client *and* server, allowing for different functionality on **both** runtimes while only using one extension, and they go in **ReplicatedStorage/Extensions/Shared**.
- Server extensions are only ran on the server, and they go in **ServerScriptService/Extensions**.

---

## **How do I make one?**

{: .warning }
**All extension module names must start with "pgfk"**. For example, "Extension1" would not be valid, while "pgfkExtension1" would! This does not apply to `Extension.Data.Name`.

You can get started by creating a ModuleScript in any of the places mentioned above and pasting the code below into it:

```lua
local Extension = {
    Data = {},
    Lifecycle = {}
} --// Holds the extension table itself

Extension.Data.Name = "extension 1" --// Name of the extension.
Extension.Data.Creator = "creator 1" --// Creator of the extension.

Extension.Data.Order = 3 --// Order to be ran (priority 1 runs before priority 2, etc).

function Extension.Lifecycle.Init() --// This runs first.
    print("extension 1 init")
end

function Extension.Lifecycle.Start() --// This runs after every "Init" function has been called.
    print("extension 1 start")
end

return Extension
```

You can also join the discord server for community-made extensions!