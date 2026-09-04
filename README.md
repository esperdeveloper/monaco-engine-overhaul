<div align="center">

<img src="https://raw.githubusercontent.com/microsoft/vscode/main/resources/win32/code_150x150.png" alt="VS Code Logo" width="100" style="filter: drop-shadow(0px 0px 15px #C6FF00);"/>

# ⚡ MONACO ENGINE OVERHAUL

*An uncompromising, high-contrast UI modification for Visual Studio Code.*

<br>

<img src="https://img.shields.io/badge/Editor-VS_Code-1E1E1E?style=for-the-badge&logo=visualstudiocode&logoColor=007ACC" alt="VS Code">
<img src="https://img.shields.io/badge/Palette-Chartreuse_Neon-C6FF00?style=for-the-badge&logoColor=black" alt="Theme Palette">
<img src="https://img.shields.io/badge/Engine-Custom_CSS-311B92?style=for-the-badge&logo=css3&logoColor=white" alt="Custom CSS">

<br><br>

<!-- Replace this image source with your actual screenshot -->
<img src="https://via.placeholder.com/1000x500/1E1E1E/C6FF00?text=+Visual+Studio+Code+Screenshot+Placeholder+" width="100%"/>

</div>

<br>

## 🧠 The Concept

This configuration bypasses the standard Visual Studio Code theme engine. It utilizes custom DOM manipulation and CSS overrides to build a cohesive, cyberpunk-inspired workspace. The focus is on extreme contrast, floating structural elements, and pure neon accents.

<br>

## ✨ Core Features

* 🎨 **Custom SVG Iconography:** Replaces default system menus and titlebar icons with gradient-masked vector graphics.
* 🟢 **Chartreuse Neon Engine:** Injects a `#C6FF00` linear gradient and multi-layered `box-shadow` glow to active workspace tabs.
* 💊 **Floating Tab Architecture:** Alters native margin structures to isolate editor tabs into distinct, floating visual components.
* 🔴 **Crimson Action States:** Upgrades close buttons with frosted borders and modern red gradients for precise visual feedback.
* 🗄️ **Menubar Overrides:** Bypasses native OS menus to render dark-mode HTML/CSS dropdowns with custom hover tracking.

<br>

## 📂 Architecture

```text
monaco-engine-overhaul/
├── css/
│   └── VisualStudioCode.css
├── js/
│   └── custom.js
└── settings.json
```

<br>

## 🚀 Deployment Integration

To inject this UI into your local editor, you must utilize the Custom CSS and JS Loader to override the application's default styling.

**1. Install the Injector**
Install the [Custom CSS and JS Loader](https://marketplace.visualstudio.com/items?itemName=be5invis.vscode-custom-css) extension from the VS Code Marketplace.

**2. Link the Environment**
Clone this repository to a stable directory on your machine. Open your VS Code `settings.json` file and map the explicit local paths:

```json
"vscode_custom_css.imports": [
    "file:///C:/absolute/path/to/monaco-engine-overhaul/css/VisualStudioCode.css",
    "file:///C:/absolute/path/to/monaco-engine-overhaul/js/custom.js"
]
```
*(Note: macOS and Linux users must adjust the `file:///` protocol path syntax accordingly).*

**3. Initialize**
Open the VS Code Command Palette (`Ctrl + Shift + P`) and execute:
> `> Reload Custom CSS and JS`

<br>

***

> ⚠️ **Maintenance Note:** Routine Visual Studio Code application updates will occasionally overwrite the injected CSS loader. If your UI reverts to the factory default, simply re-run the `Reload Custom CSS and JS` command to restore the custom environment.
