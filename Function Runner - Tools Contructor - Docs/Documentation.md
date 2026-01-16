# Attention:
Use online documentation (from Git-Hub) as it might contain most updated info with examples and GIFs:
https://github.com/Dincrid/Documentations/blob/main/Function%20Runner%20-%20Tools%20Contructor%20-%20Docs/Documentation.md

# Function Runner (Tools Constructor) - User Guide
**Version:** 1.0  
**Product:** Function Runner | Tools Constructor  
**Category:** Unity Editor Extension  
**Author:** Dincrid Games


#  ⚡️ Quick start 

### Note Tool:
1. Go to **Tools → Dincrid → Function Runner** in the main menu  
or press **Alt + R**

2. Click on Search input field or Press **Tab** to start search
3. Find your first method (Example: "TheNote" in Static Methods ) 
4. Add it by pressing **[+]** button or hit **Enter**
5. (Optional) Assign parameters for method (Example: The Note / The Object)
6. Run it by pressing on the function

### Bookmark Tool:
 1. Open Tool: [Alt] + [R] (Tools>Dincrid Games>Function Runner)
 2. Hit [Tab] - Search
 3. Search for "TheBookMark" in [Static Methods]
 4. Hit Enter to Add method
 5. Copy added method several times with: [Ctrl+D] x5
 6. **Done!**. Bookmarks tool completed. 
 Assign the web path like: "www.Google.com" or local: "C:/SomeFolder" or "C:/SomeFolder/SomeFile.txt". Click on big button with method name to jump into the given path
### More Info:
 ... for more info and examples open demo scene. Find "ReadMe" game object. Expand Childs > and follow tutorial guide.
 Create step by step 3 tools withing 5-10 minutes:
 1. **Bookmark Tool** (Allows to save your web-site or local drive paths and open them) 
 2. **Notes Tool** ( Notes with messages, object pinging, urgency)
 3. **2D World Builder** ( Handles Managing and Drawing 2D-Cubes in 2D-World with different brushes, with different sizes, methods, fillers, generators)
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

## 🎥 3. Videos

Overview:
https://youtu.be/ve9zq-dZSRE

How to use:
https://youtu.be/dzPJ5AL1xsQ

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

## 🌈 6. Parameters Support

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
## 💡 10. Tutorials

```

Read ME! Expand Childs For more info:
	Video Tutorials:
		There is should be a link on you-tube (TBD)
	Creating: [BookMarks]
		0. [Alt + R] to open tool. Or: MainMenu/Tools/Dincrid Games/Function Runner
		1. Press [Tab] for Search
		2. Search for: "gotolink" in Static Methods.
			Change search type by clicking on it. Or: [Alt]+[A] or [Alt]+[D]
		3. [Tab] to exit search
		4. Put some Web-Site (like Google.com) or Local Drive path like (C:/SomeFolder)
			4.1 Or even the document like: C:/SomeFolder/SomeFile.txt
		5. Press on Wide button with function name to activate the function
		6. Result: Opened Web-Site or Local Drive Path or File
	Creating: [Notes Manager]
		1. [Alt + R] to open tool. Or: MainMenu/Tools/Dincrid Games/Function Runner
		 Changing/Creating Page ( > Expand )
			Change active page to another by click on Page name at the top.
			Green Dots are showing functions Count. No dots: Empty Page
			Choose another Page
			After selecting page for Example "Page2", rename it by Pressing [F2]
		2. [Tab] to Search. Search for: "TheNote" In Static methods. "TheNote" methods should be appeared.
			Change search type by clicking on it. Or: [Alt]+[A] or [Alt]+[D]
		3. Add "TheNote" method.
		4. Press [Tab] to end search
		5. [Ctrl + D] to Duplicate method.
		5.5 Hold: [Ctrl + Alt] to make field names visible
		6. Add any object as "An Object" parameter. (some object in scene or project)
		7. Add some Note to field below: Like: "Need to Fix it"
		8. Press on Wide button with function name to activate the function 
		9. Result: It will Ping and Select object. And log in console the message you put as a Note
	Creating: [2D World Creator]
		0. [Alt + R] to open tool. Or: MainMenu/Tools/Dincrid Games/Function Runner
		Changing/Creating Page ( > Expand )
			Change active page to another by click on Page name at the top.
			Green Dots are showing functions Count. No dots: Empty Page
			Choose another Page
			After selecting page for Example "Page2", rename it by Pressing [F2]
		1. Press [Tab] to Search
		2. Go to [Classes] search type
		3. Search for class name "BlockManager"
			You can learn about BlockManager in BlockManager.cs file
		4. Add it. Allow to add all methods of class.
			-Only public methods will be added
		5. To see which parameter is doing: press [Alt + Shift]
			-To see the logic of the method: Right Click to Any method and choose: Go To Defenition
		7. Using "Fill" Method. Set X,Y to 20. Press Fill button
			Find "Fill" Method
			Set Parameters:  X:20 Y: 20 
			Hold: [Alt] + [Shift] to see parameters Names
			Set Parameter: Type:  Ground/Sand or Water
			Click [Fill] button. Allow to Find and Execute target for the first time
			Result: 20 x 20 water blocks created.
			You can select different BlockManager layers and Fill them as well
				BlockManagers are located at the end of the scene
		8. Using "Drawing" Methods
			1. Before Draw: you might want to activate drawing cursor with "ActivateCursor" method:
				Find "ActivateCursor" method (should be the last in list)
				Set parameter value to "true".
				Select BlockManager you want  to Run Method
				Run Method
			1.1 Draw methods have to be used with Keyboard Shortcuts in scene view.
			[Space] + [1] - Runs 1st method in current page.
			[Space] + [2] - Runs 2nd method etc..
			If you want to change [Space]  (most likely in 2021 version: Unity shows Overlay Menu...)
				Go to settings and put another key like "B" or "V" in ShortCuts.
				Notice: Alt + [1-9] is Already taken by Pages. 
				Notice: Ctrl + [1-9] is taken by Unity3d
			2. [Draw] Method:
				[Draw] method is 2nd method in the page
					(by default if you haven't move it and created in new page)
					If it's not then: Move it by drag and drop to 2nd place
					Or use appropriate Hotkey from 1-9
				Select any BlockManager.
				Press [Space]+[2] in scene view to draw with it
				Result: Chosen type of block created at the mouse cursor in scene view
				Optional: ExecutePerFrame
					Open Function Runner [Alt]+[R]
					Right Click on [Draw] function.
					 Go to Properties>Execute Per Frame
					Now you can Press and Hold [Space]+[2] to Draw
			3. [DrawLine] Method:
				Do the same thing just before with [Draw] method except Execution Per Frame
				To Draw the line you need to specify 2 points with cursor.
				I haven't made any specific indicators for it at this moment
				So press [Space]+[4] to specify PointA
				And press again [Space]+[4] to specify PointB
				Don't forget to choose Type(Ground) and Radius (0 is fine)
				Result: Line Drawned with selected Type and Radius
		9. Other methods:
			Try other methods as well
			All Methods got Descriptions
			[RightClick] on any method and Choose [GoToDefenition] for more info 
	- Hints
		Navingation Can be done with [Alt]+[WASD] in Search or in Regular Mode
			In Regular Mode:
				[Alt] + [A] / [D] - Change Pages
				[Alt] + [S] / [W] - Navigate though Methods
					With + [Shift] - Methods Will be selected
					With + [Shift] + [Ctrl] - Methods will be moved
			In Search Mode: 
				[Alt] + [A] / [D] - Change search type
					+ [Shift] to add type to search instead of switch
				[Alt] + [S] / [W] - Navigate though search results
		Zoom: [Ctrl] + [Mouse Wheel]. or: [Ctrl] + [+] / [-]
		Rename:
			[F2] - Rename Page
			[Ctrl] + [F2] - Rename Function
		More hints Coming soon...


```
---

## 🧠 11. Best Practices

- Keep reusable methods in a dedicated Utility class for clarity.  
- Use clear names for pages ("Scene Tools", "UI Setup", "Testing").  
- Keep public methods in single class so they can be shared / added with ease

---

## ⚡ 12. Performance Analyzer (optional module)

**Performance Analyzer:**  
Measure the execution time of any selected method to identify slow operations and optimize custom tools.  
Activate it from the context menu of methods and view average time that taken to execute method.

---

## 🤝 13. Team Usage and Sharing
Create a class with a lot of usefull public methods. Share it with your team.
Now team will be able to add whole class as methods or tool in Function Runner  


---

## 🔧 14. Compatibility

- Unity 2021.3 LTS and higher  
- Windows and macOS  
- Editor-only extension (not for runtime). But you can use runtime methods
- Works with Built-in, URP, and HDRP pipelines  
- No third-party dependencies

---

## 📜 15. License and Support

- **License Type:** Standard Unity Asset Store EULA  
- **Support:** dincrid@gmail.com  
- **Documentation URL:** [Git-Hub Link](https://github.com/Dincrid/Documentations/blob/main/Function%20Runner%20-%20Tools%20Contructor%20-%20Docs/Documentation.md)

---

## 🧩 16. Changelog

**v1.0 – Initial release:** Initial commit

---
