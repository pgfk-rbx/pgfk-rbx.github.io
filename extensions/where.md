---
sidebar_position: 2
parent: Extensions
---

# **Where do they go?**

- Client extensions are **only** ran on the client, and they go in **ReplicatedStorage/Extensions/Client**.
- Shared extensions run on **both** the client *and* server, allowing for different functionality on **both** runtimes while only using one extension, and they go in **ReplicatedStorage/Extensions/Shared**.
- Server extensions are **only** ran on the server, and they go in **ServerScriptService/Extensions**.

---

[Back](/extensions/extensions.html){: .btn }