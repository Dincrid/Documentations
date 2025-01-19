# GenericMenuN for Unity3D

## Overview
`GenericMenuN` is an enhanced version of the standard `GenericMenu` in Unity3D, designed to simplify navigation and menu management. This script is intended for use in **UnityEditor** and provides users with a more intuitive and convenient interface for interacting with menus.

## Key Features

- **Hotkeys**: Supports hotkeys for quick access to commands. Users can customize their own key combinations to optimize their workflow.
  
- **Easy Navigation**: Navigate through menus easily using keyboard arrow keys, as well as WASD keys and numbers. This allows for rapid movement between various commands and windows.

- **Customizability**: Ability to add custom functionality and define unique hotkeys for different commands. This makes `GenericMenuN` a flexible tool for developers.

## Example Usage
A simple example is included in the project, demonstrating how to easily navigate through Unity3D windows and commands using `GenericMenuN`. The script provides a smooth and intuitive experience, which is especially beneficial during project development and testing.

## Installation
1. Copy the `GenericMenuN` script into your Unity project folder.
2. Customize hotkeys and commands as desired.
3. Run the script in **UnityEditor** and start using it to simplify navigation.

## Conclusion
`GenericMenuN` is a powerful tool for developers looking to enhance their menu experience in Unity3D. Its flexibility and ease of use make it a great addition to any project.

## Resources

## First Steps
1. Use namespace
   ```csharp
   using Dincrid;

## Hotkeys:
There is built-in hotkeys for Menu Navigation.
1. WASD or Arrows
2. 1-9 digits for open corresponding item. Activated By default. To deactivate it: 
```csharp
GenericMenuN menu = new GenericMenuN("Main Menu", _defaultAutoClose: false);
menu.UseDefault09Hotkeys = false;
```

## Icons
To Create menu items with icons you can use GUI Contents. Use EditorGUIUtility.IconContent(path). Paths for Unity Editor built-in icons can be found here:
1. https://github.com/halak/unity-editor-icons
2. https://github.com/ErnSur/unity-editor-icons
3. https://github.com/GilpStudio/unity-internal-icon-browser

