# Function Runner (Tools Constructor)
 *Function Runner is the second and working name*

## User Guide

**Version:** 1.0  
**Product:** Function Runner | Tools Constructor  
**Category:** Unity Editor Extension  
**Author:** Dincrid Games

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
4. Restart Unity (optional) to ensure all menu items are initialized.

---

## 🌈 3. Opening the Tool Window

Go to **Tools → Dincrid → Tools Constructor** in the main menu  
or press the default hotkey:
**Alt + R**





You can dock the window anywhere in the Unity Editor layout.

---

## 🧩 4. Main Interface Elements

| Element | Description |
|----------|--------------|
| **Toolbar** | Page selector, quick controls, and search bar |
| **Methods List** | Contains added functions (methods or menu items) |
| **Parameters Panel** | Displays editable fields for method arguments |
| **Execution Buttons** | Run ▶, Pin 📌, or Delete ❌ selected method |
| **Groups/Pages** | Logical sets of methods that act as complete tools |

---

## ⚙️ 5. Adding Methods

1. Click **Add Method** (top-left button).  
2. Select a class and method from your project assembly.  
   - Static and non-static methods are supported.  
3. If the method has parameters, the parameter editor will appear automatically.  
4. Click **Apply** to save it in the current group.  

You can also drag and reorder methods intuitively within the list.

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

1. Click the ▶ button in the window.  
2. Use the mouse context menu in the list.  
3. Assign a hotkey combo (see below).

**Smart Execution:** the tool remembers the last non-static target and automatically reuses it until you change selection.

---

## ⌨️ 8. Hotkeys and Global Shortcuts

Tools Constructor supports both local and global shortcuts.

| Shortcut | Action |
|-----------|---------|
| **Space + [1–10]** | Execute the corresponding method even if the tool window is closed |
| **Alt + [1–10]** | Switch between pages or groups |


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
- Save layouts! Tools Constructor remembers your setup per project.

---

## ⚡ 11. Performance Analyzer (optional module)

**Performance Analyzer:**  
Measure the execution time of any selected method to identify slow operations and optimize custom tools.  
Activate it from the context menu and view average runtime in the console or panel.

---

## 🤝 12. Team Usage and Sharing

All methods can be added from a shared class.  
Commit the Scriptable Object file in Assets/Dincrid Games/res   in version control to make tools available to the whole team.

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

### ✅ Tip

Add sections **Screenshots**, **Quick Start**, and **FAQ** to your PDF version.  
They are optional for Asset Store but make documentation look complete and professional.