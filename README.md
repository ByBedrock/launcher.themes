# 🎨 ByBedrock Themes

<div align="center">

**Theme collection for customizing ByBedrock Launcher**

[![Auto Build](https://img.shields.io/badge/build-automated-success?style=flat-square)](https://github.com/ByBedrock/ThemesSource)
[![Themes](https://img.shields.io/badge/themes-6-blueviolet?style=flat-square)](https://github.com/ByBedrock/ThemesSource/releases)
[![JSON](https://img.shields.io/badge/format-JSON-yellow?style=flat-square)](https://www.json.org/)

**[🇷🇺 Русская версия](README.ru.md)**

</div>

---

## 🎭 Description

This repository contains theme sources for ByBedrock Launcher. Themes allow you to fully customize the launcher's appearance — from color schemes to background images.

---

## 🌈 Available Themes

### 🌑 DefaultTheme
**Classic Dark Theme**
- Minimalist design
- Dark color scheme
- Excellent readability
- Perfect for extended use

### ☀️ NanoLight
**Light Theme**
- Clean light interface
- Contrasting accents
- Ideal for daytime use
- Pleasant pastel tones

### 🌙 NanoDark
**Modern Dark Theme**
- Deep black background
- Bright accent colors
- Reduces eye strain
- OLED-friendly design

### 🟩 MinecraftTheme
**Minecraft-styled**
- In-game colors
- Pixel font
- Familiar UI elements
- Nostalgic style

### 💜 NeonTheme
**Bright Neon Theme**
- Fluorescent accents
- Futuristic design
- High contrast
- Wow effect

---

## 📁 Theme Structure

Each theme consists of:

```
ThemeName/
├── theme.manifest.json    # Theme metadata
├── colors.json            # Color palette
├── Background.png         # (Optional) Background image
├── Icon.png               # (Optional) Theme icon
└── Banner.png             # (Optional) Theme banner
```

### 📄 theme.manifest.json

Main metadata file:

```json
{
  "name": "MyAwesomeTheme",
  "version": "1.0.0",
  "author": "Your Name",
  "description": "Your theme description",
  "accentColor": "#FF6B6B",
  "isDark": true,
  "assets": {
    "background": "Background.png",
    "icon": "Icon.png",
    "banner": "Banner.png"
  }
}
```

### 🎨 colors.json

Defines the color scheme:

```json
{
  "primary": "#1E1E1E",
  "secondary": "#2D2D2D",
  "accent": "#FF6B6B",
  "text": "#FFFFFF",
  "textSecondary": "#B0B0B0",
  "success": "#4CAF50",
  "warning": "#FFC107",
  "error": "#F44336",
  "background": "#121212",
  "surface": "#1E1E1E",
  "border": "#333333"
}
```

---

## 🆕 Creating a New Theme

### Step 1: Create Structure

```bash
mkdir MyTheme
cd MyTheme
```

### Step 2: Create Manifest

`theme.manifest.json`:
```json
{
  "name": "MyTheme",
  "version": "1.0.0",
  "author": "Your Name",
  "description": "My awesome theme!",
  "accentColor": "#00FF00",
  "isDark": true
}
```

### Step 3: Define Colors

`colors.json`:
```json
{
  "primary": "#000000",
  "secondary": "#111111",
  "accent": "#00FF00",
  "text": "#FFFFFF",
  "background": "#000000"
}
```

### Step 4: Add Assets (optional)

- `Background.png` — background image (recommended 1920x1080)
- `Icon.png` — theme icon (recommended 256x256)
- `Banner.png` — theme banner (recommended 1920x200)

### Step 5: Test

1. Copy theme folder to `%APPDATA%\ByBedrockLauncher\Themes\`
2. Restart launcher
3. Select your theme in settings

### Step 6: Share!

Create a Pull Request and add your theme to the collection!

---

## 🎨 Color Guide

### Main Colors

- **primary** — main background color for containers
- **secondary** — secondary color for dividers
- **accent** — accent color for buttons and highlights
- **background** — main application background color
- **surface** — surface color (cards, panels)

### Text Colors

- **text** — main text color
- **textSecondary** — secondary text color (captions, metadata)

### Status Colors

- **success** — for successful operations (green)
- **warning** — for warnings (yellow/orange)
- **error** — for errors (red)

### Additional

- **border** — border and frame color

---

## 🖼️ Image Requirements

### Background.png
- **Resolution:** 1920x1080 or higher
- **Format:** PNG with alpha channel
- **File Size:** Up to 5 MB
- **Recommendations:** Use blur or gradients for better text readability

### Icon.png
- **Resolution:** 256x256
- **Format:** PNG with alpha channel
- **File Size:** Up to 500 KB
- **Recommendations:** Simple, recognizable design

### Banner.png
- **Resolution:** 1920x200
- **Format:** PNG
- **File Size:** Up to 2 MB
- **Recommendations:** Horizontal composition

---

## 🔄 Automatic Build

Themes are automatically built via GitHub Actions:

1. On every push to `main`
2. All themes are packaged into `.zip` archives
3. Published to [GitHub Releases](https://github.com/ByBedrock/ThemesSource/releases)
4. Launcher automatically fetches updates

---

## 📦 Manual Theme Installation

1. Download theme from [Releases](https://github.com/ByBedrock/ThemesSource/releases/latest)
2. Extract archive
3. Copy theme folder to `%APPDATA%\ByBedrockLauncher\Themes\`
4. Restart launcher
5. Select theme in settings

---

## 🎓 Best Practices

### ✅ Do

- Use meaningful color names
- Test theme at different resolutions
- Ensure sufficient text contrast
- Optimize images
- Specify accurate version

### ❌ Don't

- Don't use overly bright backgrounds
- Avoid low contrast
- Don't upload huge images
- Don't copy others' themes without credit

---

## 🌟 Inspiration Examples

### Color Schemes

- [Coolors](https://coolors.co/) — palette generator
- [Adobe Color](https://color.adobe.com/) — color picker
- [Material Design Colors](https://materialui.co/colors) — Material palettes

### Design

- [Dribbble](https://dribbble.com/) — design concepts
- [Behance](https://www.behance.net/) — designer portfolios
- [UI Design Daily](https://www.uidesigndaily.com/) — daily UI

---

## 🤝 Contributing

Want to add your theme?

1. 🍴 Fork this repository
2. 🎨 Create a folder for your theme
3. 📝 Add `theme.manifest.json` and `colors.json`
4. 🖼️ (Optional) Add images
5. ✅ Test the theme
6. 📤 Create a Pull Request

---

## 🐛 Report an Issue

Found a bug or have a theme idea?

- [🐛 Create Issue](https://github.com/ByBedrock/ThemesSource/issues)
- [💬 Discuss in Discussions](https://github.com/ByBedrock/ThemesSource/discussions)

---

## 📄 License

All themes are distributed under the MIT License.

---

<div align="center">

**Created with 🎨 by ByBedrock Team**

[🚀 Launcher](https://github.com/ByBedrock/Launcher) • [🧩 Modules](https://github.com/ByBedrock/ModulesSource) • [🎨 Themes](https://github.com/ByBedrock/ThemesSource)

</div>
