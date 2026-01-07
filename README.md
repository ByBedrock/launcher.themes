# 🎨 ByBedrock Themes

<div align="center">

**Theme collection for ByBedrock Launcher customization**

[![Version](https://img.shields.io/badge/version-1.0.0-blue?style=flat-square)](https://github.com/ByBedrock/ThemesSource)
[![Themes](https://img.shields.io/badge/themes-5-blueviolet?style=flat-square)](https://github.com/ByBedrock/ThemesSource/releases)
[![Format](https://img.shields.io/badge/format-JSON-yellow?style=flat-square)](https://www.json.org/)

**[🇷🇺 Русская версия](README.ru.md)**

</div>

---

## 🆕 What's New

- **Glass effects** — semi-transparent elements with blur
- **Glow effects** — accent element illumination
- **Gradient buttons** — gradient fills for primary actions
- **Micro-animations** — smooth hover/click transitions
- **Updated palette** — modern color schemes

---

## 🌈 Available Themes

| Theme | Description | Style |
|-------|-------------|-------|
| **DefaultTheme** | Standard theme with purple gradients | Dark |
| **NanoDark** | Ultra-dark with custom icons | Dark OLED |
| **NanoLight** | Light theme for daytime use | Light |
| **MinecraftTheme** | Minecraft-styled design | Dark Green |
| **NeonTheme** | Cyberpunk with neon glow | Dark Neon |

---

## 📁 Theme Structure

```
MyTheme/
├── theme.manifest.json    # Only required file
├── preview.png            # Theme preview (recommended)
├── background.png         # Background image (optional)
├── banner.png             # Banner image (optional)
├── icon_home.png          # Custom icons (optional)
├── icon_profiles.png
├── icon_versions.png
└── icon_settings.png
```

---

## 📄 theme.manifest.json — Full Specification

### Minimal Manifest

```json
{
    "name": "MyTheme",
    "version": "1.0.0",
    "author": "Your Name",
    "description": "Theme description",
    "variables": {
        "primaryColor": "#818CF8",
        "secondaryColor": "#A78BFA"
    }
}
```

### Complete Manifest with All Options

```json
{
    "name": "MyAwesomeTheme",
    "version": "1.0.0",
    "author": "Your Name",
    "description": "My awesome theme with glass effects",
    "compatibility": "1.0.0",
    "preview": "preview.png",
    "variables": {
        "primaryColor": "#818CF8",
        "secondaryColor": "#A78BFA",
        "accentColor": "#34D399",
        "backgroundColor": "#0A0A0F",
        "surfaceColor": "#12121A",
        "cardColor": "#1A1A24",
        "textColor": "#F8FAFC",
        "textSecondaryColor": "#94A3B8",
        "borderColor": "#2A2A3A",
        "errorColor": "#F87171",
        "successColor": "#4ADE80",
        "warningColor": "#FBBF24",
        "glassColor": "#15FFFFFF",
        "glassBorderColor": "#25FFFFFF",
        "glowColor": "#40818CF8",
        "fontFamily": "Inter",
        "borderRadius": 16,
        "animationDuration": 0.2,
        "backgroundImage": "background.png",
        "bannerImage": "banner.png",
        "iconHome": "icon_home.png",
        "iconProfiles": "icon_profiles.png",
        "iconVersions": "icon_versions.png",
        "iconSettings": "icon_settings.png",
        "emojiHome": "🏠",
        "emojiProfiles": "👥",
        "emojiVersions": "📦",
        "emojiModules": "🧩",
        "emojiThemes": "🎨",
        "emojiSettings": "⚙️"
    }
}
```

---

## 🎨 Variable Reference

### Primary Colors

| Variable | Description | Example |
|----------|-------------|---------|
| `primaryColor` | Main accent color (buttons, links) | `#818CF8` |
| `secondaryColor` | Secondary color for gradients | `#A78BFA` |
| `accentColor` | Success/active elements color | `#34D399` |

### Background Colors

| Variable | Description | Example |
|----------|-------------|---------|
| `backgroundColor` | Main app background | `#0A0A0F` |
| `surfaceColor` | Sidebar and sections background | `#12121A` |
| `cardColor` | Cards and panels background | `#1A1A24` |

### Text Colors

| Variable | Description | Example |
|----------|-------------|---------|
| `textColor` | Primary text color | `#F8FAFC` |
| `textSecondaryColor` | Secondary text (labels) | `#94A3B8` |

### Status Colors

| Variable | Description | Example |
|----------|-------------|---------|
| `errorColor` | Errors and critical warnings | `#F87171` |
| `successColor` | Successful operations | `#4ADE80` |
| `warningColor` | Warnings | `#FBBF24` |

### Glass and Glow Effects

| Variable | Description | Example |
|----------|-------------|---------|
| `glassColor` | Semi-transparent glass background | `#15FFFFFF` |
| `glassBorderColor` | Glass element borders | `#25FFFFFF` |
| `glowColor` | Button glow color | `#40818CF8` |

### Other Settings

| Variable | Description | Example |
|----------|-------------|---------|
| `borderColor` | Border color | `#2A2A3A` |
| `fontFamily` | Font family | `Inter` |
| `borderRadius` | Corner radius (px) | `16` |
| `animationDuration` | Animation duration (sec) | `0.2` |

---

## 🆕 Creating a New Theme

### Step 1: Create a Folder

```bash
mkdir MyTheme
cd MyTheme
```

### Step 2: Create theme.manifest.json

```json
{
    "name": "MyTheme",
    "version": "1.0.0",
    "author": "Your Name",
    "description": "My first theme",
    "compatibility": "1.0.0",
    "variables": {
        "primaryColor": "#FF6B6B",
        "secondaryColor": "#4ECDC4",
        "accentColor": "#45B7D1",
        "backgroundColor": "#0D1117",
        "surfaceColor": "#161B22",
        "cardColor": "#21262D",
        "textColor": "#F0F6FC",
        "textSecondaryColor": "#8B949E",
        "borderColor": "#30363D",
        "errorColor": "#F85149",
        "successColor": "#3FB950",
        "warningColor": "#D29922",
        "glassColor": "#15FFFFFF",
        "glassBorderColor": "#25FFFFFF",
        "glowColor": "#40FF6B6B",
        "borderRadius": 12,
        "animationDuration": 0.2
    }
}
```

### Step 3: Add Preview (Recommended)

Create `preview.png` at 400x300 pixels with a screenshot of your theme.

### Step 4: Install and Test

```
1. Copy folder to: %APPDATA%\ByBedrockLauncher\Themes\
2. Restart the launcher
3. Open "Themes" tab
4. Select your theme
```

---

## 💡 Color Scheme Examples

### GitHub Dark

```json
{
    "primaryColor": "#238636",
    "secondaryColor": "#1F6FEB",
    "backgroundColor": "#0D1117",
    "surfaceColor": "#161B22",
    "cardColor": "#21262D",
    "textColor": "#F0F6FC",
    "borderColor": "#30363D",
    "glassColor": "#10238636",
    "glowColor": "#40238636"
}
```

### Ocean Blue

```json
{
    "primaryColor": "#0EA5E9",
    "secondaryColor": "#06B6D4",
    "backgroundColor": "#0C1222",
    "surfaceColor": "#111827",
    "cardColor": "#1F2937",
    "textColor": "#F9FAFB",
    "borderColor": "#374151",
    "glassColor": "#150EA5E9",
    "glowColor": "#400EA5E9"
}
```

### Rose Gold

```json
{
    "primaryColor": "#F43F5E",
    "secondaryColor": "#EC4899",
    "backgroundColor": "#18181B",
    "surfaceColor": "#27272A",
    "cardColor": "#3F3F46",
    "textColor": "#FAFAFA",
    "borderColor": "#52525B",
    "glassColor": "#15F43F5E",
    "glowColor": "#40F43F5E"
}
```

### Forest Green

```json
{
    "primaryColor": "#22C55E",
    "secondaryColor": "#16A34A",
    "backgroundColor": "#052E16",
    "surfaceColor": "#14532D",
    "cardColor": "#166534",
    "textColor": "#F0FDF4",
    "borderColor": "#15803D",
    "glassColor": "#1522C55E",
    "glowColor": "#4022C55E"
}
```

---

## 🖼️ Image Requirements

| File | Size | Format | Description |
|------|------|--------|-------------|
| `preview.png` | 400x300 | PNG | Preview in theme list |
| `background.png` | 1920x1080+ | PNG | App background |
| `banner.png` | 1920x300 | PNG | Home banner |
| `icon_*.png` | 24x24 | PNG + Alpha | Navigation icons |

---

## ✅ Quality Theme Checklist

- [ ] Sufficient text contrast (minimum 4.5:1)
- [ ] All required colors defined
- [ ] `preview.png` included
- [ ] Theme tested in all sections
- [ ] No overly bright/blinding colors
- [ ] Glass effects don't affect readability
- [ ] Glow intensity is balanced

---

## 📦 Installing from Releases

1. Download `.zip` from [Releases](https://github.com/ByBedrock/ThemesSource/releases/latest)
2. Extract to `%APPDATA%\ByBedrockLauncher\Themes\`
3. Restart the launcher
4. Select theme in "Themes" tab

---

## 🤝 Contributing Your Theme

1. Fork this repository
2. Create folder `YourThemeName/`
3. Add `theme.manifest.json`
4. Add `preview.png`
5. Create Pull Request

---

<div align="center">

**Made with 🎨 by ByBedrock Team**

[🚀 Launcher](https://github.com/ByBedrock/Launcher) • [🧩 Modules](https://github.com/ByBedrock/ModulesSource) • [🎨 Themes](https://github.com/ByBedrock/ThemesSource)

</div>
