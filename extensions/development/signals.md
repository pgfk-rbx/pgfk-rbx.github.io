---
sidebar_position: 1
parent: Developing Extensions
---

# **What is the Signals module?**

The Signals module, located in `ReplicatedStorage.Shared.Signals`, contains a list of signals that are useful for extension development.

---

## **Object Signals**

These signals are used when the loaders are loaded/unloaded.

### **V5**

- Loaded: (Path: Folder, Orphaned: Boolean)
- Unloaded: (None)

### **V6**

- Loaded: (Path: Folder, Orphaned: Boolean)
- Unloaded: (None)

---

## **Extension Signals**

These signals are used when extensions are loaded.

- Loaded: (Extension)