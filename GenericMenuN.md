Here's a comprehensive documentation for your `GenericMenuN` in GitHub Markdown format, incorporating all the public methods with descriptions and examples from your code:

# GenericMenuN for Unity3D

## Overview
`GenericMenuN` is an enhanced version of the standard `GenericMenu` in Unity3D, designed to simplify navigation and menu management. This script is intended for use in **UnityEditor** and provides users with a more intuitive and convenient interface for interacting with menus.

## Key Features

- **Hotkeys**: Supports hotkeys for quick access to commands. Users can customize their own key combinations to optimize their workflow.
- **Easy Navigation**: Navigate through menus easily using keyboard arrow keys, as well as WASD keys and numbers.
- **Customizability**: Ability to add custom functionality and define unique hotkeys for different commands.
- **Grouping**: Organize menu items into logical groups with scoped sections.
- **History & Favorites**: Track recently used items and mark favorites for quick access.
- **Coloring**: Customize menu item colors for better visual organization.

## Installation
1. Copy the `GenericMenuN` script into your Unity project folder.
2. Customize hotkeys and commands as desired.
3. Run the script in **UnityEditor** and start using it to simplify navigation.

## First Steps
```csharp
using Dincrid;
```

## Basic Usage

### Creating a Menu
```csharp
GenericMenuN menu = new GenericMenuN("Main Menu");
```

### Hotkeys Configuration
```csharp
GenericMenuN menu = new GenericMenuN("Main Menu");
menu.UseDefault09Hotkeys = false; // Disable default 1-9 hotkeys
```

### Icons
Use Unity's built-in icons:
```csharp
Texture icon = EditorGUIUtility.IconContent("d_SceneAsset Icon").image;
```

## API Reference

### Adding Menu Items

#### Basic Item
```csharp
menu.AddItem("File/Save", () => Debug.Log("Saved!"));
```

#### Item with Hotkey
```csharp
menu.AddItem("[F]File/[S]Save", () => Debug.Log("Saved!"));
```

#### Item with Icon and Tooltip
```csharp
Texture icon = EditorGUIUtility.IconContent("d_SaveAs Icon").image;
menu.AddItem("File/Save", () => {}, "Saves the current scene", icon);
```

#### Item with Conditional Checkmark
```csharp
menu.AddItem("View/Grid", () => {}, _checkMark: () => showGrid);
```

### Grouping Items

#### Group Scope (Recommended)
```csharp
using (menu.GroupScope("Edit"))
{
    menu.AddItem("Undo", () => {});
    menu.AddItem("Redo", () => {});
}
```

#### Manual Grouping
```csharp
menu.StartGroup("Edit");
menu.AddItem("Undo", () => {});
menu.AddItem("Redo", () => {});
menu.EndGroup();
```

### Coloring

#### Set Default Color
```csharp
GenericMenuN.SetDefaultColor(Color.red); // All new items will be red
```

#### Color Scope
```csharp
using (new GenericMenuN.ItemColorScope(Color.blue))
{
    menu.AddItem("Blue Item", () => {});
    // More blue items...
}
// Color returns to previous
```

### History & Favorites

#### Add History Tab
```csharp
menu.AddHistoryTab("[H]History", 5); // Shows last 5 used items
```

#### Add Favorite Tab
```csharp
menu.AddFavoriteTab("[F]Favorites");
// Right-click any item to add to favorites
```

### Advanced Features

#### Separators
```csharp
menu.AddSeparator(); // Adds at current position
menu.AddSeparator("Edit/"); // Adds in specific path
```

#### Showing the Menu
```csharp
menu.Show(); // Shows with default behavior
menu.Show(GenericMenuN.AppendType.addToNextLevel); // Multi-level menu
```

## Complete Example

```csharp
using UnityEngine;
using UnityEditor;
using Dincrid;

public class MenuExample
{
    [MenuItem("Tools/Show Custom Menu")]
    public static void ShowMenu()
    {
        GenericMenuN menu = new GenericMenuN("Example Menu", searcherEnabled: true);
        
        // Set default color
        GenericMenuN.SetDefaultColor(new Color(0.2f, 0.5f, 0.8f));
        
        // File group
        using (menu.GroupScope("[F]File"))
        {
            Texture saveIcon = EditorGUIUtility.IconContent("d_SaveAs Icon").image;
            menu.AddItem("[S]Save", () => Debug.Log("Saved"), "Save current scene", saveIcon);
            
            menu.AddSeparator();
            
            using (new GenericMenuN.ItemColorScope(Color.red))
            {
                menu.AddItem("[Q]Quit", () => EditorApplication.ExitPlaymode());
            }
        }
        
        // Edit group
        using (menu.GroupScope("[E]Edit"))
        {
            menu.AddItem("[U]Undo", () => Undo.PerformUndo());
            menu.AddItem("[R]Redo", () => Undo.PerformRedo());
        }
        
        // Add history and favorites
        menu.AddHistoryTab();
        menu.AddFavoriteTab();
        
        // Show the menu
        menu.Show(GenericMenuN.AppendType.addToNextLevel);
    }
}
```

## Hotkey Reference
- **WASD/Arrows**: Navigate menu items
- **1-9**: Select corresponding numbered item (when enabled)
- **Enter/Space**: Confirm selection
- **Right-click**: On items to add to favorites
- **Shift+Right-click**: Alternative actions
- **Escape**: Close current menu level

## Icons
Use Unity's built-in icons:
- [Unity Editor Icons List 1](https://github.com/halak/unity-editor-icons)
- [Unity Editor Icons List 2](https://github.com/ErnSur/unity-editor-icons)
- [Icon Browser Tool](https://github.com/GilpStudio/unity-internal-icon-browser)

## Best Practices
1. Use `GroupScope` for better code organization
2. Assign hotkeys to frequently used items
3. Use colors sparingly for important items
4. Leverage history and favorites for productivity
5. Keep menu hierarchies shallow (2-3 levels max)

## Troubleshooting
- **Hotkeys not working**: Ensure `UseDefault09Hotkeys` is true (default)
- **Items not appearing**: Check your grouping scopes are properly closed
- **Performance issues**: Avoid extremely deep menu hierarchies











Here's how you can document the `AppendType` enum in detail with an expandable section in your GitHub Markdown:

# GenericMenuN for Unity3D

## Menu Layering System

`GenericMenuN` features an advanced layering system that allows for complex menu hierarchies. This is controlled through the `AppendType` enum when showing menus.

<details>
<summary><b>📚 AppendType Detailed Explanation (Click to expand)</b></summary>

### `AppendType` Enum Values

#### `closeAllOtherMenus` (Default Behavior)
```csharp
menu.Show(GenericMenuN.AppendType.closeAllOtherMenus);
```
- **Behavior**: Closes all existing menu windows before opening the new one
- **Use Case**: When you want a clean slate (like Unity's default GenericMenu)
- **Visualization**:
  ```
  [Main Window] → [New Menu]  // Old menus are closed
  ```

#### `addToSameLevel`
```csharp
menu.Show(GenericMenuN.AppendType.addToSameLevel);
```
- **Behavior**:
  - Keeps existing menus at the same level
  - Opens new menu at current level
  - Closing higher levels when focusing lower ones
- **Use Case**: Creating alternative options at the same depth
- **Visualization**:
  ```
  [Main Window] → [Menu A]
                → [Menu B]  // Both at same level
  ```

#### `addToNextLevel`
```csharp
menu.Show(GenericMenuN.AppendType.addToNextLevel);
```
- **Behavior**:
  - Opens menu at next depth level (+1)
  - Maintains parent-child relationship
  - Auto-closes when parent loses focus
- **Use Case**: Creating drill-down menus
- **Visualization**:
  ```
  [Main Window] → [Menu 1] → [Submenu 1.1]
                            → [Submenu 1.2]
  ```

### Key Behaviors
1. **Focus Changes**:
   - Focusing a level 2 window closes all level 3+ windows
   - Focusing a non-menu window (level -1) closes all menus (unless Shift is held)

2. **Keyboard Navigation**:
   ```mermaid
   graph LR
   A[Level 0] --> B[Level 1]
   B --> C[Level 2]
   C --> D[Level 3]
   ```
   - Pressing ←/Backspace closes current level
   - Pressing →/Enter opens submenus

3. **Modifier Keys**:
   - **Shift**: Maintains menu stack when clicking outside
   - **Ctrl**: Special behaviors (context-dependent)

### Example Scenarios

**Scenario 1: Simple Menu**
```csharp
var menu = new GenericMenuN("Main");
menu.Show(); // Defaults to closeAllOtherMenus
```

**Scenario 2: Multi-level Dashboard**
```csharp
mainMenu.Show(GenericMenuN.AppendType.closeAllOtherMenus);
// Later...
subMenu.Show(GenericMenuN.AppendType.addToNextLevel);
```

**Scenario 3: Alternative Views**
```csharp
view1Menu.Show(GenericMenuN.AppendType.addToSameLevel);
// User switches to:
view2Menu.Show(GenericMenuN.AppendType.addToSameLevel);
```

### Best Practices
1. Use `addToNextLevel` for hierarchical data
2. Use `addToSameLevel` for alternative views
3. Default to `closeAllOtherMenus` for root menus
4. Limit depth to 3-4 levels for usability
</details>

## Basic Usage Example
```csharp
// Simple menu with submenus
var mainMenu = new GenericMenuN("Main Menu");
mainMenu.AddItem("File/New", () => {});
mainMenu.Show(GenericMenuN.AppendType.addToNextLevel);
```

This expandable section provides comprehensive documentation while keeping the main documentation clean. The Mermaid diagram and visualization examples help users understand the layering concept visually.
