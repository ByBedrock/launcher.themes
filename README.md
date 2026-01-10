# 🎨 ByBedrock Themes v1.1

<div align="center">

**Theme collection for ByBedrock Launcher customization**

[![Version](https://img.shields.io/badge/version-1.1.1-blue?style=flat-square)](https://github.com/ByBedrock/ThemesSource)
[![Themes](https://img.shields.io/badge/themes-5-blueviolet?style=flat-square)](https://github.com/ByBedrock/ThemesSource/releases)
[![Format](https://img.shields.io/badge/format-JSON-yellow?style=flat-square)](https://www.json.org/)

**[🇷🇺 Русская версия](README.ru.md)**

</div>

---

## ✨ Engine Features

| Feature | Description |
|---------|-------------|
| 🎨 **Glass/Glow Effects** | Modern semi-transparent styles with blur |
| 💉 **Dynamic XAML Injection** | Full UI customization via `styles.axaml` |
| 📁 **Assets Folder** | Auto-registration of all files in `Assets/` |
| 🔄 **Hot-Reload** | Instant updates on file save (no restart needed!) |
| 🔧 **Extensible Variables** | Any custom tokens in JSON |
| 🖼️ **Universal Icons** | Fluent Icons, SVG path, PNG and emoji in a single field |

---

## 🌈 Built-in Themes

| Theme | Description | Style |
|-------|-------------|-------|
| **DefaultTheme** | Standard theme with purple gradients | Dark |
| **NanoDark** | Ultra-dark OLED theme with custom background | Dark OLED |
| **NanoLight** | Light theme for daytime use | Light |
| **MinecraftTheme** | Minecraft-styled design | Dark Green |
| **NeonTheme** | Cyberpunk with neon glow | Dark Neon |

---

## 📁 Theme Folder Structure

```
MyTheme/
├── theme.manifest.json    # ⚠️ REQUIRED manifest
├── styles.axaml           # Custom Avalonia styles (optional)
├── preview.png            # Preview 400x300 (recommended)
├── background.png         # App background (optional)
├── banner.png             # Home banner (optional)
└── Assets/                # Folder for any resources
    ├── my_icon.png
    └── custom_font.ttf
```

> **💡 Tip:** All files in `Assets/` are auto-registered as `{DynamicResource ThemeAsset_filename_ext}`.  
> Example: `Assets/my_icon.png` → `{DynamicResource ThemeAsset_my_icon_png}`

---

## 📄 theme.manifest.json

### Minimal Manifest

```json
{
    "name": "MyTheme",
    "version": "1.0.0",
    "author": "Your Name",
    "description": "Theme description",
    "compatibility": "1.1.0",
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
    "version": "1.1.0",
    "author": "Your Name",
    "description": "My awesome theme with custom design",
    "compatibility": "1.1.0",
    "preview": "preview.png",
    "resources": {
        "styles": ["styles.axaml", "Styles/Buttons.axaml"]
    },
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
        "opacity": 0.85,
        "blurStrength": 12,
        "animationDuration": 0.2,
        "headerHeight": 64,
        "sidebarWidth": 240,
        "backgroundImage": "background.png",
        "bannerImage": "banner.png",
        "home": "fluent:Home",
        "profiles": "fluent:People",
        "versions": "fluent:Box",
        "servers": "fluent:Globe",
        "themes": "fluent:Color",
        "settings": "fluent:Settings",
        "navbarColor": "#1A1A24",
        "navbarActiveColor": "#818CF8",
        "navbarHoverColor": "#15FFFFFF"
    }
}
```

---

## 🎨 Variable Reference

### Primary Colors

| Variable | Description | Format | Example |
|----------|-------------|--------|---------|
| `primaryColor` | Main accent (buttons, links, active elements) | HEX | `#818CF8` |
| `secondaryColor` | Secondary color (gradients, hover states) | HEX | `#A78BFA` |
| `accentColor` | Additional accent (success, activation) | HEX | `#34D399` |

### Background Colors

| Variable | Description | Format | Example |
|----------|-------------|--------|---------|
| `backgroundColor` | Main app background | HEX | `#0A0A0F` |
| `surfaceColor` | Sidebar, sections, panels background | HEX | `#12121A` |
| `cardColor` | Cards, dialogs, popups background | HEX | `#1A1A24` |

### Text

| Variable | Description | Format | Example |
|----------|-------------|--------|---------|
| `textColor` | Primary text color | HEX | `#F8FAFC` |
| `textSecondaryColor` | Secondary text (labels, meta) | HEX | `#94A3B8` |

### Status Colors

| Variable | Description | Format | Example |
|----------|-------------|--------|---------|
| `errorColor` | Errors, critical warnings | HEX | `#F87171` |
| `successColor` | Successful operations | HEX | `#4ADE80` |
| `warningColor` | Warnings | HEX | `#FBBF24` |

### Glass/Glow Effects

| Variable | Description | Format | Example |
|----------|-------------|--------|---------|
| `glassColor` | Semi-transparent glass background | HEX with Alpha | `#15FFFFFF` |
| `glassBorderColor` | Glass element borders | HEX with Alpha | `#25FFFFFF` |
| `glowColor` | Button glow color | HEX with Alpha | `#40818CF8` |

> **💡 HEX with Alpha:** Format `#AARRGGBB`, where `AA` is opacity (00-FF).  
> Example: `#40818CF8` = 40 (25% opacity) + 818CF8 (color)

### Fonts

| Variable | Description | Type | Default |
|----------|-------------|------|---------|
| `fontFamily` | Font family | String | `Inter` |
| `fontSize` | Base font size (px) | Number | `14` |
| `fontSizeSmall` | Small text (px) | Number | `12` |
| `fontSizeLarge` | Large text (px) | Number | `18` |
| `fontSizeTitle` | Titles (px) | Number | `24` |

### Corner Radius

| Variable | Description | Type | Default |
|----------|-------------|------|---------|
| `borderRadius` | General corner radius (px) | Number | `12` |
| `buttonRadius` | Button corner radius (px) | Number | `12` |
| `cardRadius` | Card corner radius (px) | Number | `16` |
| `inputRadius` | Input field corner radius (px) | Number | `10` |

### Shadows

| Variable | Description | Type | Default |
|----------|-------------|------|---------|
| `shadowColor` | Shadow color | HEX with Alpha | `#20000000` |
| `shadowBlur` | Shadow blur (px) | Number | `24` |
| `shadowOffsetY` | Shadow Y offset (px) | Number | `8` |

### Animations

| Variable | Description | Type | Default |
|----------|-------------|------|---------|
| `animationDuration` | Animation duration (sec) | Number | `0.3` |
| `hoverScale` | Scale on hover | Number | `1.02` |
| `pressedScale` | Scale on press | Number | `0.98` |

### Padding

| Variable | Description | Type | Default |
|----------|-------------|------|---------|
| `buttonPadding` | Button padding | String | `"20,12"` |
| `cardPadding` | Card padding | String | `"20"` |
| `inputPadding` | Input field padding | String | `"14,12"` |

### Navigation (Navbar)

| Variable | Description | Type | Default |
|----------|-------------|------|---------|
| `navbarColor` | Navigation button color | HEX | — |
| `navbarActiveColor` | Active button color | HEX | — |
| `navbarHoverColor` | Hover color | HEX | — |

### Scrollbar

| Variable | Description | Type | Default |
|----------|-------------|------|---------|
| `scrollbarColor` | Scrollbar color | HEX | — |
| `scrollbarWidth` | Scrollbar width (px) | Number | `8` |

### Interface Dimensions

| Variable | Description | Type | Default |
|----------|-------------|------|---------|
| `opacity` | Overall opacity (0-1) | Number | `1.0` |
| `blurStrength` | Blur strength | Number | `0` |
| `headerHeight` | Header height (px) | Number | `64` |
| `sidebarWidth` | Sidebar width (px) | Number | `240` |

### Images

| Variable | Description | Format |
|----------|-------------|--------|
| `backgroundImage` | App background image | File path |
| `bannerImage` | Home page banner | File path |

---

## 🖼️ Universal Icon System

Starting from version 1.1.1, a **single field** is used for each icon. The engine automatically detects the type based on string content.

### Supported Formats

| Type | Syntax | Example | Priority |
|------|--------|---------|----------|
| **Fluent Icon** | `fluent:IconName` or `fluent:IconName:Filled` | `"fluent:Home"` | ⭐ Recommended |
| **SVG File** | Path with `.svg` extension | `"icons/home.svg"` | For custom SVG |
| **PNG/JPG** | Path with `.png/.jpg/.ico` extension | `"icons/home.png"` | For raster icons |
| **SVG Path** | `M...` (starts with M or F) | `"M12,2L2,7..."` | For inline SVG |
| **Emoji** | Any Unicode character | `"🏠"` | For fun |

### Icon Field List

```json
"variables": {
    "home": "...",      // Home page
    "profiles": "...",  // Profiles
    "versions": "...",  // Versions
    "servers": "...",   // Servers
    "themes": "...",    // Themes
    "settings": "..."   // Settings
}
```

### Usage Examples

**Fluent Icons (recommended):**
```json
"variables": {
    "home": "fluent:Home",
    "profiles": "fluent:People",
    "versions": "fluent:Box",
    "servers": "fluent:Globe",
    "themes": "fluent:Color",
    "settings": "fluent:Settings"
}
```

**Fluent Icons filled style:**
```json
"variables": {
    "home": "fluent:Home:Filled",
    "profiles": "fluent:People:Filled",
    "settings": "fluent:Settings:Filled"
}
```

**PNG icons:**
```json
"variables": {
    "home": "icons/home.png",
    "profiles": "icons/profiles.png",
    "settings": "icons/settings.png"
}
```

**SVG files (recommended for custom icons):**
```json
"variables": {
    "home": "icons/home.svg",
    "profiles": "icons/profiles.svg",
    "settings": "icons/settings.svg"
}
```

> **💡 Tip:** SVG files scale without quality loss and support any color via `Foreground`.

**Emoji:**
```json
"variables": {
    "home": "🏠",
    "profiles": "👥",
    "versions": "📦",
    "servers": "🌍",
    "themes": "🎨",
    "settings": "⚙️"
}
```

**SVG Path (inline, advanced):**
```json
"variables": {
    "home": "M10,20V14H14V20H19V12H22L12,3L2,12H5V20H10Z"
}
```

### 🔍 Where to Find Fluent Icons?

| Resource | Link | Description |
|----------|------|-------------|
| **Fluent Icons Gallery** | [fluenticons.co](https://fluenticons.co/) | Official catalog with search |
| **GitHub Repo** | [microsoft/fluentui-system-icons](https://github.com/microsoft/fluentui-system-icons) | Source and full list |
| **Figma Community** | [Fluent UI Icons](https://www.figma.com/community/file/836835755999442291) | For designers |

> **⚠️ Important:** Use icon name in **PascalCase** without prefix.  
> Correct: `fluent:Home`, `fluent:People`, `fluent:Settings`  
> Incorrect: `fluent:home`, `fluent:ic_fluent_home_24_regular`

---

## 🖼️ Image Requirements

| File | Size | Format | Description |
|------|------|--------|-------------|
| `preview.png` | 400×300 px | PNG | Preview in theme list |
| `background.png` | 1920×1080+ px | PNG/JPG | Background image |
| `banner.png` | 1920×300 px | PNG | Home banner |
| Icons (if PNG) | 24×24 px | PNG + Alpha | Navigation icons |

> **💡 Tip:** For backgrounds, use images with dark edges or add a vignette for better text readability.

---

## 🛠️ Full XAML Customization

You can override the design of **ANY** UI component via XAML! This gives maximum flexibility.

> **📚 Full Example:** See [`DevTheme/styles.axaml`](DevTheme/styles.axaml) — contains all selectors with comments!

### Automatic Loading
Create a `styles.axaml` file in the theme folder — it will load automatically.

### Multiple Style Files
```json
"resources": {
    "styles": ["Styles/Buttons.axaml", "Styles/Cards.axaml", "Styles/Navigation.axaml"]
}
```

---

### 📋 All Available CSS Selectors

#### Buttons

| Selector | Description |
|----------|-------------|
| `Button.primary` | Primary button (gradient) |
| `Button.primary:pointerover` | On hover |
| `Button.primary:pressed` | On press |
| `Button.primary:disabled` | Disabled |
| `Button.primary.large` | Large button |
| `Button.secondary` | Secondary button |
| `Button.ghost` | Transparent button |
| `Button.danger` | Danger action button |
| `Button.icon` | Icon button |
| `Button.gradient` | Gradient button |
| `Button.navbutton` | Navigation button |
| `Button.navbutton.active` | Active navigation button |
| `Button.navbutton.selected` | Selected navigation button |

#### Cards and Containers

| Selector | Description |
|----------|-------------|
| `Border.card` | Standard card |
| `Border.card:pointerover` | Card on hover |
| `Border.glass` | Glass container |
| `Border.hero` | Hero section with gradient |
| `Border.stat-card` | Statistics card |

#### Input Fields

| Selector | Description |
|----------|-------------|
| `TextBox.themed` | Styled input field |
| `TextBox.themed:focus` | On focus |
| `ComboBox` | Dropdown |
| `CheckBox` | Checkbox |
| `Slider` | Slider |

#### Lists

| Selector | Description |
|----------|-------------|
| `ListBox` | List |
| `ListBoxItem` | List item |
| `ListBoxItem:selected` | Selected item |

#### Other

| Selector | Description |
|----------|-------------|
| `Window` | Main window |
| `ProgressBar` | Progress bar |
| `ToolTip` | Tooltip |
| `ScrollViewer` | Scroll area |

---

### 🎨 Customization Examples

#### Fully Custom Buttons

```xml
<Styles xmlns="https://github.com/avaloniaui"
        xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml">
    
    <Style Selector="Button.primary">
        <Setter Property="Background" Value="{DynamicResource ThemePrimaryBrush}"/>
        <Setter Property="Foreground" Value="White"/>
        <Setter Property="CornerRadius" Value="{DynamicResource ThemeButtonRadius}"/>
        <Setter Property="Padding" Value="{DynamicResource ThemeButtonPadding}"/>
        <Setter Property="FontWeight" Value="SemiBold"/>
        <Setter Property="BorderThickness" Value="0"/>
        <Setter Property="Cursor" Value="Hand"/>
    </Style>
    
    <Style Selector="Button.primary:pointerover">
        <Setter Property="Background" Value="{DynamicResource ThemeSecondaryBrush}"/>
        <Setter Property="RenderTransform" Value="scale(1.02)"/>
    </Style>
    
    <Style Selector="Button.primary:pressed">
        <Setter Property="RenderTransform" Value="scale(0.98)"/>
        <Setter Property="Opacity" Value="0.9"/>
    </Style>
    
</Styles>
```

#### Cards with Neon Glow

```xml
<Style Selector="Border.card">
    <Setter Property="Background" Value="{DynamicResource ThemeCardBrush}"/>
    <Setter Property="CornerRadius" Value="{DynamicResource ThemeCardRadius}"/>
    <Setter Property="BorderThickness" Value="1"/>
    <Setter Property="BorderBrush" Value="{DynamicResource ThemeBorderBrush}"/>
    <Setter Property="BoxShadow" Value="0 0 20 0 #40FF00FF"/>
</Style>

<Style Selector="Border.card:pointerover">
    <Setter Property="BorderBrush" Value="{DynamicResource ThemePrimaryBrush}"/>
    <Setter Property="BoxShadow" Value="0 0 30 0 #60FF00FF"/>
    <Setter Property="RenderTransform" Value="translateY(-4px)"/>
</Style>
```

#### Custom Navigation

```xml
<Style Selector="Button.navbutton">
    <Setter Property="Background" Value="Transparent"/>
    <Setter Property="Foreground" Value="{DynamicResource ThemeTextSecondaryBrush}"/>
    <Setter Property="Padding" Value="16,12"/>
    <Setter Property="CornerRadius" Value="12"/>
</Style>

<Style Selector="Button.navbutton.selected">
    <Setter Property="Background">
        <LinearGradientBrush StartPoint="0%,0%" EndPoint="100%,100%">
            <GradientStop Color="#FF00FF" Offset="0"/>
            <GradientStop Color="#00FFFF" Offset="1"/>
        </LinearGradientBrush>
    </Setter>
    <Setter Property="Foreground" Value="White"/>
</Style>
```

#### Styled Input Fields

```xml
<Style Selector="TextBox.themed">
    <Setter Property="Background" Value="{DynamicResource ThemeSurfaceBrush}"/>
    <Setter Property="Foreground" Value="{DynamicResource ThemeTextBrush}"/>
    <Setter Property="BorderBrush" Value="{DynamicResource ThemeBorderBrush}"/>
    <Setter Property="CornerRadius" Value="{DynamicResource ThemeInputRadius}"/>
    <Setter Property="Padding" Value="{DynamicResource ThemeInputPadding}"/>
</Style>

<Style Selector="TextBox.themed:focus">
    <Setter Property="BorderBrush" Value="{DynamicResource ThemePrimaryBrush}"/>
    <Setter Property="BoxShadow" Value="0 0 10 0 #40818CF8"/>
</Style>
```

---

### 📚 All Available Theme Resources

#### Colors (Color)

| Resource | Description |
|----------|-------------|
| `ThemePrimaryColor` | Primary color |
| `ThemeSecondaryColor` | Secondary color |
| `ThemeAccentColor` | Accent color |
| `ThemeBackgroundColor` | Background color |
| `ThemeSurfaceColor` | Surface color |
| `ThemeCardColor` | Card color |
| `ThemeTextColor` | Text color |
| `ThemeTextSecondaryColor` | Secondary text |
| `ThemeBorderColor` | Border color |
| `ThemeErrorColor` | Error color |
| `ThemeSuccessColor` | Success color |
| `ThemeWarningColor` | Warning color |
| `ThemeGlassColor` | Glass color |
| `ThemeGlassBorderColor` | Glass border |
| `ThemeGlowColor` | Glow color |
| `ThemeShadowColor` | Shadow color |
| `ThemeNavbarColor` | Navbar color |
| `ThemeNavbarActiveColor` | Active navbar |
| `ThemeNavbarHoverColor` | Navbar hover |
| `ThemeScrollbarColor` | Scrollbar color |

#### Brushes (SolidColorBrush)

For each color, there's a corresponding brush with `Brush` suffix:
`ThemePrimaryBrush`, `ThemeSecondaryBrush`, `ThemeBackgroundBrush`, etc.

#### Special Brushes

| Resource | Type | Description |
|----------|------|-------------|
| `ThemeGradientBrush` | LinearGradientBrush | Gradient primary→secondary |

#### Dimensions

| Resource | Type | Description |
|----------|------|-------------|
| `ThemeBorderRadius` | CornerRadius | General corner radius |
| `ThemeButtonRadius` | CornerRadius | Button corner radius |
| `ThemeCardRadius` | CornerRadius | Card corner radius |
| `ThemeInputRadius` | CornerRadius | Input corner radius |
| `ThemeButtonPadding` | Thickness | Button padding |
| `ThemeCardPadding` | Thickness | Card padding |
| `ThemeInputPadding` | Thickness | Input padding |
| `ThemeFontSize` | Double | Base font size |
| `ThemeFontSizeSmall` | Double | Small font |
| `ThemeFontSizeLarge` | Double | Large font |
| `ThemeFontSizeTitle` | Double | Title font size |
| `ThemeHeaderHeight` | Double | Header height |
| `ThemeSidebarWidth` | Double | Sidebar width |
| `ThemeScrollbarWidth` | Double | Scrollbar width |

#### Effects

| Resource | Type | Description |
|----------|------|-------------|
| `ThemeOpacity` | Double | Opacity |
| `ThemeBlur` | Double | Blur strength |
| `ThemeHoverScale` | Double | Hover scale |
| `ThemePressedScale` | Double | Pressed scale |
| `ThemeShadowBlur` | Double | Shadow blur |
| `ThemeShadowOffsetY` | Double | Shadow offset |
| `ThemeAnimationDuration` | TimeSpan | Animation duration |

#### Images

| Resource | Type | Description |
|----------|------|-------------|
| `ThemeBackgroundImage` | Bitmap | Background image |
| `ThemeBannerImage` | Bitmap | Banner |
| `ThemeAsset_*` | Bitmap | Files from Assets/ |

#### Icons

| Resource | Type | Description |
|----------|------|-------------|
| `ThemeIconHome` | Geometry/Bitmap/String | Home icon |
| `ThemeIconProfiles` | Geometry/Bitmap/String | Profiles icon |
| `ThemeIconVersions` | Geometry/Bitmap/String | Versions icon |
| `ThemeIconServers` | Geometry/Bitmap/String | Servers icon |
| `ThemeIconThemes` | Geometry/Bitmap/String | Themes icon |
| `ThemeIconSettings` | Geometry/Bitmap/String | Settings icon |

---

### 🔥 Custom Variables

Any fields in `variables` that are not built-in automatically become resources!

```json
"variables": {
    "myCustomColor": "#FF00FF",
    "myCustomSize": 42,
    "myCustomText": "Hello"
}
```

Become available as:
- `Theme_myCustomColorColor` (Color)
- `Theme_myCustomColorBrush` (SolidColorBrush) 
- `Theme_myCustomSize` (Double)
- `Theme_myCustomText` (String)

---

## 🆕 Creating a New Theme

### Step 1: Create a Folder

```powershell
# Windows PowerShell
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
    "compatibility": "1.1.0",
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
        "animationDuration": 0.2,
        "home": "fluent:Home",
        "profiles": "fluent:People",
        "versions": "fluent:Box",
        "servers": "fluent:Globe",
        "themes": "fluent:Color",
        "settings": "fluent:Settings"
    }
}
```

### Step 3: Add Preview

Create a screenshot at **400×300 px** and save as `preview.png`.

### Step 4: Install and Test

```
1. Copy folder to: %APPDATA%\ByBedrockLauncher\Themes\
2. Restart the launcher
3. Open "Themes" tab
4. Select your theme
```

---

## 💡 Ready-Made Color Schemes

### 🐙 GitHub Dark

```json
{
    "primaryColor": "#238636",
    "secondaryColor": "#1F6FEB",
    "backgroundColor": "#0D1117",
    "surfaceColor": "#161B22",
    "cardColor": "#21262D",
    "textColor": "#F0F6FC",
    "textSecondaryColor": "#8B949E",
    "borderColor": "#30363D",
    "glassColor": "#10238636",
    "glowColor": "#40238636",
    "navbarColor": "#21262D",
    "navbarActiveColor": "#238636",
    "navbarHoverColor": "#15238636"
}
```

### 🌊 Ocean Blue

```json
{
    "primaryColor": "#0EA5E9",
    "secondaryColor": "#06B6D4",
    "backgroundColor": "#0C1222",
    "surfaceColor": "#111827",
    "cardColor": "#1F2937",
    "textColor": "#F9FAFB",
    "textSecondaryColor": "#9CA3AF",
    "borderColor": "#374151",
    "glassColor": "#150EA5E9",
    "glowColor": "#400EA5E9",
    "navbarColor": "#1F2937",
    "navbarActiveColor": "#0EA5E9",
    "navbarHoverColor": "#150EA5E9"
}
```

### 🌹 Rose Gold

```json
{
    "primaryColor": "#F43F5E",
    "secondaryColor": "#EC4899",
    "backgroundColor": "#18181B",
    "surfaceColor": "#27272A",
    "cardColor": "#3F3F46",
    "textColor": "#FAFAFA",
    "textSecondaryColor": "#A1A1AA",
    "borderColor": "#52525B",
    "glassColor": "#15F43F5E",
    "glowColor": "#40F43F5E",
    "navbarColor": "#3F3F46",
    "navbarActiveColor": "#F43F5E",
    "navbarHoverColor": "#15F43F5E"
}
```

### 🌲 Forest Green

```json
{
    "primaryColor": "#22C55E",
    "secondaryColor": "#16A34A",
    "backgroundColor": "#052E16",
    "surfaceColor": "#14532D",
    "cardColor": "#166534",
    "textColor": "#F0FDF4",
    "textSecondaryColor": "#86EFAC",
    "borderColor": "#15803D",
    "glassColor": "#1522C55E",
    "glowColor": "#4022C55E",
    "navbarColor": "#166534",
    "navbarActiveColor": "#22C55E",
    "navbarHoverColor": "#1522C55E"
}
```

### ☀️ Light Theme (base)

```json
{
    "primaryColor": "#6366F1",
    "secondaryColor": "#8B5CF6",
    "backgroundColor": "#F8FAFC",
    "surfaceColor": "#FFFFFF",
    "cardColor": "#FFFFFF",
    "textColor": "#0F172A",
    "textSecondaryColor": "#64748B",
    "borderColor": "#E2E8F0",
    "glassColor": "#40FFFFFF",
    "glassBorderColor": "#20000000",
    "glowColor": "#306366F1",
    "navbarColor": "#FFFFFF",
    "navbarActiveColor": "#6366F1",
    "navbarHoverColor": "#106366F1"
}
```

---

## ✅ Quality Theme Checklist

- [ ] ✨ Sufficient text contrast (minimum 4.5:1 per WCAG)
- [ ] 🎨 All required colors defined
- [ ] 🖼️ `preview.png` included (400×300)
- [ ] 🧪 Theme tested in all launcher sections
- [ ] 👀 No overly bright/blinding colors
- [ ] 📖 Glass effects don't affect readability
- [ ] 💫 Glow intensity is balanced
- [ ] 📱 UI elements readable at different resolutions

> **🔗 Contrast Checker:** [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/)

---

## 📦 Installing from Releases

1. Download `.zip` from [Releases](https://github.com/ByBedrock/ThemesSource/releases/latest)
2. Extract to `%APPDATA%\ByBedrockLauncher\Themes\`
3. Restart the launcher
4. Select theme in "Themes" tab

---

## 🤝 Contributing Your Theme

1. **Fork** this repository
2. Create folder `YourThemeName/`
3. Add `theme.manifest.json` (required)
4. Add `preview.png` (recommended)
5. Create **Pull Request**

---

## 🔧 Migrating from v1.0

1. Update `compatibility` to `1.1.0`
2. **Remove** deprecated fields `iconHome`, `iconProfiles`, `iconVersions`, `iconSettings`
3. Add new unified icon fields: `home`, `profiles`, `versions`, `servers`, `themes`, `settings`
4. Optionally move images to `Assets/` folder
5. Use `styles.axaml` for advanced UI customization

---

## ❓ FAQ

**Q: My theme doesn't show up in the launcher**  
A: Check that `theme.manifest.json` is valid JSON and located in the theme folder root.

**Q: Icons aren't displaying**  
A: Make sure you're using correct syntax (`fluent:Home`, not `Home` or `fluent:home`).

**Q: Hot-Reload isn't working**  
A: Hot-Reload triggers with ~500ms delay. Make sure the file is fully saved.

**Q: Glass effects aren't visible**  
A: Set `opacity` less than 1.0 and/or `blurStrength` greater than 0.

---

<div align="center">

**Made with 🎨 by ByBedrock Team**

[🚀 Launcher](https://t.me/bybedrock_launcher) • [🎨 Themes](https://github.com/ByBedrock/ThemesSource)

</div>
