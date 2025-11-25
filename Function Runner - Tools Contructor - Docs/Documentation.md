# Attention:
Use online documentation as it might contain most updated info with examples and GIFs:
https://github.com/Dincrid/Documentations/blob/main/Function%20Runner%20-%20Tools%20Contructor%20-%20Docs/Documentation.md

# Function Runner (Tools Constructor) - User Guide
**Version:** 1.0  
**Product:** Function Runner | Tools Constructor  
**Category:** Unity Editor Extension  
**Author:** Dincrid Games


#  ⚡️ Quick start 
 Open demo scene. Find "ReadMe" game object. Expand Childs > and follow tutorial guide.
 Create step by step 3 tools withing 5-10 minutes:
 1. **Bookmark Tool** (Allows to save your web-site or local drive paths and open them) 
 2. **Notes Tool** ( Notes with messages, object pinging, urgency)
 3. **2D World Builder** ( Handles Managing and Drawing 2D-Cubes in 2D-World with different brushes, with different sizes, methods, fillers, generators)
 ## OR:
 1. Open Tool: [Alt] + [R] (Tools>Dincrid Games>Function Runner)
 2. Hit [Tab] - Search
 3. Search for "TheBookMark" in [Static Methods]
 4. Hit Enter to Add method
 5. Copy added method several times with: [Ctrl+D] x5
 6. **Done!**. Bookmarks tool completed. 
 Assign the web path like: "www.Google.com" or local: "C:/SomeFolder" or "C:/SomeFolder/SomeFile.txt". Click on big button with method name to jump into the given path

*This is lazy start. I highly recommend to check Example scebe in Example Folder*

---

## 🧭 1. Overview

**Tools Constructor** is a Unity Editor Extension that lets you create and run custom methods and functions directly from the Unity Editor.  
You can add methods from any C# class, pass parameters of different types, trigger menu items, and organize everything into reusable tools with hotkeys.  
No need to write separate Editor scripts or custom UI windows — simply use your existing functions as powerful tools.

---

## ⚙️ 2. Installation

1. Import the package into your project via **Unity Package Manager** or **Assets → Import Package**.  
2. After import, Unity will create a folder:
Assets/Dincrid Games/Function Runner/

3. Inside you’ll find:
- `Editor/ToolsConstructor` – main script files and editor window  
- `Examples/` – sample methods and demo scene  
- `Documentation/` – this user guide  
---

## 🌈 3. Opening the Tool Window

Go to **Tools → Dincrid → Function Runner** in the main menu  
or press the default hotkey:
**Alt + R**

---

## 🧩 4. Main Interface Elements

| Element | Description |
|----------|--------------|
| **Page Button** | Shows name of current page. Open **Page Selector** by pressing on it|
| **Page Selector** | Window for Choosing / Managing / Renaming pages |
| **Functions List** | Contains added functions (methods or menu items) with  |
| **Function** | Contain Icon, Target (for non-static), Run Button ▶, Parameters  (for parameter functions) |
| **Parameters Panel** | Displays editable fields for method arguments. [Ctrl] + [Alt]: Show Names |
| **Search Panel** | Search by method name or class name. Choose search type |

---

## 🔎 5. Search and Add Methods:
Press [Tab]
You can search by:
1. Menu Item name
2. Static Method Name: 
*have to be public method in public class* 
3. Non Static-Method Name: 
*have to be public method in public class*
4. Class name: 
*This type of search will add public child methods of this class. Class have to be derieved from UnityObject. Like: Scriptable Object or MonoBehaviour etc..*


Use [Alt] + [WASD] to navigate through search results and search type
[Enter] - Add
[Ctrl] + [Enter] - Run
[Ctrl] + [Alt] + [Enter] - Add, allow copies
[Ctrl] + [Alt] + [Shift] + [Enter] - Go To Definition

---

## 🌈 6. Parameter Support

Parameter system supports the following types:

- **Primitive:** int, float, bool, string  
- **Structs:** Color, Vector2, Vector3, Rect, Quaternion  
- **Classes and Unity Objects:** ScriptableObject, MonoBehaviour, GameObject, Material, Texture, Component  
- **Collections:** array or List of any supported type  
- **Enums:** shown as dropdowns  

Parameter values are serialized and saved with the project, so you can reuse them later without re-entering data.

---

## 📜 7. Executing Methods

You can run methods in three ways:

1. Click the button with function name 
2. Select Method with arrows and Ctrl + Space
   Multiple methods selection with [Shift] and execution with [Ctrl]+[Space] also allowed
3. Use shortcuts : [Space] + [1] / [2] / [3] etc..
   [Space] + [`] - Execute last functions (Repeat last action)
**Smart Execution:** the tool remembers the last non-static target and automatically reuses it until you change selection.

---

## ⌨️ 8. Hotkeys and Global Shortcuts
Function Runner contains a lot of usefull shortcuts. With this amount of shortcuts you can use tool without a single click just with a left hand.
All shortcuts can be found in Shortcuts window, by clicking help button at the right bottom corner 
Tools Constructor supports both local and global shortcuts.

| Shortcut | Action |
|-----------|---------|
| **Space + [1–10]** | Execute the corresponding method even if the tool window is closed |
| **Alt + [1–10]** | Switch between pages or groups |

These Shortcuts can be changed in settings panel in [Shortcuts] area
Global shortcuts work everywhere in the Unity Editor.


---

## 🗂️ 9. Groups (Pages)

- Each group acts as an independent "tool set".  
- Create groups by pressing on the page name then **+ Page** button.
- Rename by pressing F2 or MMB.
- Reorder with drag and drop.  
- By default change page with: Alt + 1 | Alt + 2 etc... 

This feature allows you to organize methods by task or project team.

---

## 🧠 10. Best Practices

- Keep reusable methods in a dedicated Utility class for clarity.  
- Use clear names for pages ("Scene Tools", "UI Setup", "Testing").  
- Keep public methods in single class so they can be shared / added with ease

---

## ⚡ 11. Performance Analyzer (optional module)

**Performance Analyzer:**  
Measure the execution time of any selected method to identify slow operations and optimize custom tools.  
Activate it from the context menu of methods and view average time that taken to execute method.

---

## 🤝 12. Team Usage and Sharing
Create a class with a lot of usefull public methods. Share it with your team.
Now team will be able to add whole class as methods or tool in Function Runner  


---

## 🔧 13. Compatibility

- Unity 2021.3 LTS and higher  
- Windows and macOS  
- Editor-only extension (not for runtime). But you can use runtime methods
- Works with Built-in, URP, and HDRP pipelines  
- No third-party dependencies

---

## 📜 14. License and Support

- **License Type:** Standard Unity Asset Store EULA  
- **Support:** dincrid@gmail.com  
- **Documentation URL:** [Git-Hub Link](https://github.com/Dincrid/Documentations/blob/main/Function%20Runner%20-%20Tools%20Contructor%20-%20Docs/Documentation.md)

---

## 🧩 15. Changelog

**v1.0 – Initial release:** core method execution, groups, parameters, global hotkeys, performance analyzer.

---
