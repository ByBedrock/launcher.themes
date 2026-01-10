# 🎨 ByBedrock Themes v1.1

<div align="center">

**Коллекция тем для кастомизации ByBedrock Launcher**

[![Version](https://img.shields.io/badge/version-1.1.1-blue?style=flat-square)](https://github.com/ByBedrock/ThemesSource)
[![Themes](https://img.shields.io/badge/themes-5-blueviolet?style=flat-square)](https://github.com/ByBedrock/ThemesSource/releases)
[![Format](https://img.shields.io/badge/format-JSON-yellow?style=flat-square)](https://www.json.org/)

**[🇬🇧 English version](README.md)**

</div>

---

## ✨ Возможности движка

| Фича | Описание |
|------|----------|
| 🎨 **Glass/Glow эффекты** | Современные полупрозрачные стили с размытием |
| 💉 **Dynamic XAML Injection** | Полная кастомизация UI через `styles.axaml` |
| 📁 **Assets Folder** | Автоматическая регистрация всех файлов из `Assets/` |
| 🔄 **Hot-Reload** | Мгновенное обновление при сохранении файлов (без перезапуска!) |
| 🔧 **Расширяемые переменные** | Любые пользовательские токены в JSON |
| 🖼️ **Универсальные иконки** | Поддержка Fluent Icons, SVG path, PNG и emoji в одном поле |

---

## 🌈 Встроенные темы

| Тема | Описание | Стиль |
|------|----------|-------|
| **DefaultTheme** | Стандартная тема с фиолетовыми градиентами | Dark |
| **NanoDark** | Ультра-тёмная OLED тема с кастомным фоном | Dark OLED |
| **NanoLight** | Светлая для дневного использования | Light |
| **MinecraftTheme** | Стилизация под Minecraft | Dark Green |
| **NeonTheme** | Киберпанк с неоновым свечением | Dark Neon |

---

## 📁 Структура папки темы

```
MyTheme/
├── theme.manifest.json    # ⚠️ ОБЯЗАТЕЛЬНЫЙ манифест
├── styles.axaml           # Кастомные стили Avalonia (опционально)
├── preview.png            # Превью 400x300 (рекомендуется)
├── background.png         # Фон приложения (опционально)
├── banner.png             # Баннер на главной (опционально)
└── Assets/                # Папка для любых ресурсов
    ├── my_icon.png
    └── custom_font.ttf
```

> **💡 Совет:** Все файлы в `Assets/` автоматически регистрируются как `{DynamicResource ThemeAsset_filename_ext}`.  
> Например: `Assets/my_icon.png` → `{DynamicResource ThemeAsset_my_icon_png}`

---

## 📄 theme.manifest.json

### Минимальный манифест

```json
{
    "name": "MyTheme",
    "version": "1.0.0",
    "author": "Your Name",
    "description": "Описание темы",
    "compatibility": "1.1.0",
    "variables": {
        "primaryColor": "#818CF8",
        "secondaryColor": "#A78BFA"
    }
}
```

### Полный манифест со всеми опциями

```json
{
    "name": "MyAwesomeTheme",
    "version": "1.1.0",
    "author": "Your Name",
    "description": "Моя крутая тема с кастомным дизайном",
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
        "settings": "fluent:Settings"
    }
}
```

---

## 🎨 Описание всех переменных

### Основные цвета

| Переменная | Описание | Формат | Пример |
|------------|----------|--------|--------|
| `primaryColor` | Основной акцент (кнопки, ссылки, активные элементы) | HEX | `#818CF8` |
| `secondaryColor` | Вторичный цвет (градиенты, hover-состояния) | HEX | `#A78BFA` |
| `accentColor` | Дополнительный акцент (успех, активация) | HEX | `#34D399` |

### Фоновые цвета

| Переменная | Описание | Формат | Пример |
|------------|----------|--------|--------|
| `backgroundColor` | Основной фон приложения | HEX | `#0A0A0F` |
| `surfaceColor` | Фон sidebar, секций, панелей | HEX | `#12121A` |
| `cardColor` | Фон карточек, диалогов, popup'ов | HEX | `#1A1A24` |

### Текст

| Переменная | Описание | Формат | Пример |
|------------|----------|--------|--------|
| `textColor` | Основной цвет текста | HEX | `#F8FAFC` |
| `textSecondaryColor` | Вторичный текст (подписи, мета) | HEX | `#94A3B8` |

### Статусы

| Переменная | Описание | Формат | Пример |
|------------|----------|--------|--------|
| `errorColor` | Ошибки, критические предупреждения | HEX | `#F87171` |
| `successColor` | Успешные операции | HEX | `#4ADE80` |
| `warningColor` | Предупреждения | HEX | `#FBBF24` |

### Glass/Glow эффекты

| Переменная | Описание | Формат | Пример |
|------------|----------|--------|--------|
| `glassColor` | Полупрозрачный фон glass-элементов | HEX с Alpha | `#15FFFFFF` |
| `glassBorderColor` | Граница glass-элементов | HEX с Alpha | `#25FFFFFF` |
| `glowColor` | Цвет свечения кнопок | HEX с Alpha | `#40818CF8` |

> **💡 HEX с Alpha:** Формат `#AARRGGBB`, где `AA` — прозрачность (00-FF).  
> Пример: `#40818CF8` = 40 (25% непрозрачность) + 818CF8 (цвет)

### Шрифты

| Переменная | Описание | Тип | По умолчанию |
|------------|----------|-----|--------------|
| `fontFamily` | Шрифт | String | `Inter` |
| `fontSize` | Базовый размер шрифта (px) | Number | `14` |
| `fontSizeSmall` | Маленький текст (px) | Number | `12` |
| `fontSizeLarge` | Большой текст (px) | Number | `18` |
| `fontSizeTitle` | Заголовки (px) | Number | `24` |

### Скругления (Corner Radius)

| Переменная | Описание | Тип | По умолчанию |
|------------|----------|-----|--------------|
| `borderRadius` | Общее скругление (px) | Number | `12` |
| `buttonRadius` | Скругление кнопок (px) | Number | `12` |
| `cardRadius` | Скругление карточек (px) | Number | `16` |
| `inputRadius` | Скругление полей ввода (px) | Number | `10` |

### Тени (Shadows)

| Переменная | Описание | Тип | По умолчанию |
|------------|----------|-----|--------------|
| `shadowColor` | Цвет тени | HEX с Alpha | `#20000000` |
| `shadowBlur` | Размытие тени (px) | Number | `24` |
| `shadowOffsetY` | Смещение тени по Y (px) | Number | `8` |

### Анимации

| Переменная | Описание | Тип | По умолчанию |
|------------|----------|-----|--------------|
| `animationDuration` | Длительность анимаций (сек) | Number | `0.3` |
| `hoverScale` | Масштаб при наведении | Number | `1.02` |
| `pressedScale` | Масштаб при нажатии | Number | `0.98` |

### Padding (отступы внутри элементов)

| Переменная | Описание | Тип | По умолчанию |
|------------|----------|-----|--------------|
| `buttonPadding` | Отступы кнопок | String | `"20,12"` |
| `cardPadding` | Отступы карточек | String | `"20"` |
| `inputPadding` | Отступы полей ввода | String | `"14,12"` |

### Навигация (Navbar)

| Переменная | Описание | Тип | По умолчанию |
|------------|----------|-----|--------------|
| `navbarColor` | Цвет кнопок навигации | HEX | — |
| `navbarActiveColor` | Цвет активной кнопки | HEX | — |
| `navbarHoverColor` | Цвет при наведении | HEX | — |

### Скроллбар

| Переменная | Описание | Тип | По умолчанию |
|------------|----------|-----|--------------|
| `scrollbarColor` | Цвет скроллбара | HEX | — |
| `scrollbarWidth` | Ширина скроллбара (px) | Number | `8` |

### Размеры интерфейса

| Переменная | Описание | Тип | По умолчанию |
|------------|----------|-----|--------------|
| `opacity` | Общая прозрачность (0-1) | Number | `1.0` |
| `blurStrength` | Сила размытия | Number | `0` |
| `headerHeight` | Высота заголовка (px) | Number | `64` |
| `sidebarWidth` | Ширина sidebar (px) | Number | `240` |

### Изображения

| Переменная | Описание | Формат |
|------------|----------|--------|
| `backgroundImage` | Фоновое изображение приложения | Путь к файлу |
| `bannerImage` | Баннер на главной странице | Путь к файлу |

---

## 🖼️ Универсальная система иконок

Начиная с версии 1.1.1 используется **единое поле** для каждой иконки. Движок автоматически определяет тип по содержимому строки.

### Поддерживаемые форматы

| Тип | Синтаксис | Пример | Приоритет |
|-----|-----------|--------|-----------|
| **Fluent Icon** | `fluent:IconName` или `fluent:IconName:Filled` | `"fluent:Home"` | ⭐ Рекомендуется |
| **SVG файл** | Путь с расширением `.svg` | `"icons/home.svg"` | Для кастомных SVG |
| **PNG/JPG** | Путь с расширением `.png/.jpg/.ico` | `"icons/home.png"` | Для растровых иконок |
| **SVG Path** | `M...` (начинается с M или F) | `"M12,2L2,7..."` | Для inline SVG |
| **Emoji** | Любой символ Unicode | `"🏠"` | Для фана |

### Список полей иконок

```json
"variables": {
    "home": "...",      // Главная страница
    "profiles": "...",  // Профили
    "versions": "...",  // Версии
    "servers": "...",   // Серверы
    "themes": "...",    // Темы
    "settings": "..."   // Настройки
}
```

### Примеры использования

**Fluent Icons (рекомендуется):**
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

**Fluent Icons залитый стиль (Filled):**
```json
"variables": {
    "home": "fluent:Home:Filled",
    "profiles": "fluent:People:Filled",
    "settings": "fluent:Settings:Filled"
}
```

**PNG иконки:**
```json
"variables": {
    "home": "icons/home.png",
    "profiles": "icons/profiles.png",
    "settings": "icons/settings.png"
}
```

**SVG файлы (рекомендуется для кастомных иконок):**
```json
"variables": {
    "home": "icons/home.svg",
    "profiles": "icons/profiles.svg",
    "settings": "icons/settings.svg"
}
```

> **💡 Совет:** SVG файлы масштабируются без потери качества и поддерживают любой цвет через `Foreground`.

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

**SVG Path (inline, для продвинутых):**
```json
"variables": {
    "home": "M10,20V14H14V20H19V12H22L12,3L2,12H5V20H10Z"
}
```

### 🔍 Где найти Fluent Icons?

| Ресурс | Ссылка | Описание |
|--------|--------|----------|
| **Fluent Icons Gallery** | [fluenticons.co](https://fluenticons.co/) | Официальный каталог с поиском |
| **GitHub Repo** | [microsoft/fluentui-system-icons](https://github.com/microsoft/fluentui-system-icons) | Исходники и полный список |
| **Figma Community** | [Fluent UI Icons](https://www.figma.com/community/file/836835755999442291) | Для дизайнеров |

> **⚠️ Важно:** Используйте имя иконки в **PascalCase** без префикса.  
> Правильно: `fluent:Home`, `fluent:People`, `fluent:Settings`  
> Неправильно: `fluent:home`, `fluent:ic_fluent_home_24_regular`

---

## 🖼️ Требования к изображениям

| Файл | Размер | Формат | Описание |
|------|--------|--------|----------|
| `preview.png` | 400×300 px | PNG | Превью в списке тем |
| `background.png` | 1920×1080+ px | PNG/JPG | Фоновое изображение |
| `banner.png` | 1920×300 px | PNG | Баннер на главной |
| Иконки (если PNG) | 24×24 px | PNG + Alpha | Иконки навигации |

> **💡 Совет:** Для фона используйте изображения с темными краями или добавьте виньетку для лучшей читаемости текста.

---

## 🛠️ Полная кастомизация через XAML

Вы можете переопределить дизайн **ЛЮБОГО** UI компонента через XAML! Это даёт максимальную гибкость.

> **📚 Полный пример:** Смотрите [`DevTheme/styles.axaml`](DevTheme/styles.axaml) — там есть все селекторы с комментариями!

### Автоматическая загрузка
Создайте файл `styles.axaml` в папке темы — он загрузится автоматически.

### Множество файлов стилей
```json
"resources": {
    "styles": ["Styles/Buttons.axaml", "Styles/Cards.axaml", "Styles/Navigation.axaml"]
}
```

---

### 📋 Все доступные CSS-селекторы

#### Кнопки

| Селектор | Описание |
|----------|----------|
| `Button.primary` | Основная кнопка (градиент) |
| `Button.primary:pointerover` | При наведении |
| `Button.primary:pressed` | При нажатии |
| `Button.primary:disabled` | Отключённая |
| `Button.primary.large` | Большая кнопка |
| `Button.secondary` | Вторичная кнопка |
| `Button.ghost` | Прозрачная кнопка |
| `Button.danger` | Кнопка опасного действия |
| `Button.icon` | Кнопка-иконка |
| `Button.gradient` | Градиентная кнопка |
| `Button.navbutton` | Кнопка навигации |
| `Button.navbutton.active` | Активная кнопка навигации |
| `Button.navbutton.selected` | Выбранная кнопка навигации |

#### Карточки и контейнеры

| Селектор | Описание |
|----------|----------|
| `Border.card` | Стандартная карточка |
| `Border.card:pointerover` | Карточка при наведении |
| `Border.glass` | Стеклянный контейнер |
| `Border.hero` | Hero-секция с градиентом |
| `Border.stat-card` | Карточка статистики |

#### Поля ввода

| Селектор | Описание |
|----------|----------|
| `TextBox.themed` | Стилизованное поле ввода |
| `TextBox.themed:focus` | При фокусе |
| `ComboBox` | Выпадающий список |
| `CheckBox` | Чекбокс |
| `Slider` | Слайдер |

#### Списки

| Селектор | Описание |
|----------|----------|
| `ListBox` | Список |
| `ListBoxItem` | Элемент списка |
| `ListBoxItem:selected` | Выбранный элемент |

#### Другое

| Селектор | Описание |
|----------|----------|
| `Window` | Главное окно |
| `ProgressBar` | Прогресс-бар |
| `ToolTip` | Подсказка |
| `ScrollViewer` | Область прокрутки |

---

### 🎨 Примеры кастомизации

#### Полностью кастомные кнопки

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

#### Карточки с неоновым свечением

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

#### Кастомная навигация

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

#### Стилизованные поля ввода

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

### 📚 Все доступные ресурсы темы

#### Цвета (Color)

| Ресурс | Описание |
|--------|----------|
| `ThemePrimaryColor` | Основной цвет |
| `ThemeSecondaryColor` | Вторичный цвет |
| `ThemeAccentColor` | Акцентный цвет |
| `ThemeBackgroundColor` | Цвет фона |
| `ThemeSurfaceColor` | Цвет поверхности |
| `ThemeCardColor` | Цвет карточек |
| `ThemeTextColor` | Цвет текста |
| `ThemeTextSecondaryColor` | Вторичный текст |
| `ThemeBorderColor` | Цвет границ |
| `ThemeErrorColor` | Цвет ошибок |
| `ThemeSuccessColor` | Цвет успеха |
| `ThemeWarningColor` | Цвет предупреждений |
| `ThemeGlassColor` | Цвет стекла |
| `ThemeGlassBorderColor` | Граница стекла |
| `ThemeGlowColor` | Цвет свечения |
| `ThemeShadowColor` | Цвет тени |
| `ThemeNavbarColor` | Цвет навбара |
| `ThemeNavbarActiveColor` | Активный навбар |
| `ThemeNavbarHoverColor` | Hover навбара |
| `ThemeScrollbarColor` | Цвет скроллбара |

#### Кисти (SolidColorBrush)

Для каждого цвета есть соответствующая кисть с суффиксом `Brush`:
`ThemePrimaryBrush`, `ThemeSecondaryBrush`, `ThemeBackgroundBrush`, и т.д.

#### Специальные кисти

| Ресурс | Тип | Описание |
|--------|-----|----------|
| `ThemeGradientBrush` | LinearGradientBrush | Градиент primary→secondary |

#### Размеры

| Ресурс | Тип | Описание |
|--------|-----|----------|
| `ThemeBorderRadius` | CornerRadius | Общее скругление |
| `ThemeButtonRadius` | CornerRadius | Скругление кнопок |
| `ThemeCardRadius` | CornerRadius | Скругление карточек |
| `ThemeInputRadius` | CornerRadius | Скругление инпутов |
| `ThemeButtonPadding` | Thickness | Отступы кнопок |
| `ThemeCardPadding` | Thickness | Отступы карточек |
| `ThemeInputPadding` | Thickness | Отступы инпутов |
| `ThemeFontSize` | Double | Базовый размер шрифта |
| `ThemeFontSizeSmall` | Double | Маленький шрифт |
| `ThemeFontSizeLarge` | Double | Большой шрифт |
| `ThemeFontSizeTitle` | Double | Размер заголовков |
| `ThemeHeaderHeight` | Double | Высота заголовка |
| `ThemeSidebarWidth` | Double | Ширина сайдбара |
| `ThemeScrollbarWidth` | Double | Ширина скроллбара |

#### Эффекты

| Ресурс | Тип | Описание |
|--------|-----|----------|
| `ThemeOpacity` | Double | Прозрачность |
| `ThemeBlur` | Double | Сила размытия |
| `ThemeHoverScale` | Double | Масштаб при наведении |
| `ThemePressedScale` | Double | Масштаб при нажатии |
| `ThemeShadowBlur` | Double | Размытие тени |
| `ThemeShadowOffsetY` | Double | Смещение тени |
| `ThemeAnimationDuration` | TimeSpan | Длительность анимаций |

#### Изображения

| Ресурс | Тип | Описание |
|--------|-----|----------|
| `ThemeBackgroundImage` | Bitmap | Фоновое изображение |
| `ThemeBannerImage` | Bitmap | Баннер |
| `ThemeAsset_*` | Bitmap | Файлы из Assets/ |

#### Иконки

| Ресурс | Тип | Описание |
|--------|-----|----------|
| `ThemeIconHome` | Geometry/Bitmap/String | Иконка главной |
| `ThemeIconProfiles` | Geometry/Bitmap/String | Иконка профилей |
| `ThemeIconVersions` | Geometry/Bitmap/String | Иконка версий |
| `ThemeIconServers` | Geometry/Bitmap/String | Иконка серверов |
| `ThemeIconThemes` | Geometry/Bitmap/String | Иконка тем |
| `ThemeIconSettings` | Geometry/Bitmap/String | Иконка настроек |

---

### 🔥 Кастомные переменные

Любые поля в `variables`, которые не являются встроенными, автоматически становятся ресурсами!

```json
"variables": {
    "myCustomColor": "#FF00FF",
    "myCustomSize": 42,
    "myCustomText": "Hello"
}
```

Становятся доступны как:
- `Theme_myCustomColorColor` (Color)
- `Theme_myCustomColorBrush` (SolidColorBrush) 
- `Theme_myCustomSize` (Double)
- `Theme_myCustomText` (String)

---

## 🆕 Создание новой темы

### Шаг 1: Создайте папку

```powershell
# Windows PowerShell
mkdir MyTheme
cd MyTheme
```

### Шаг 2: Создайте theme.manifest.json

```json
{
    "name": "MyTheme",
    "version": "1.0.0",
    "author": "Your Name",
    "description": "Моя первая тема",
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

### Шаг 3: Добавьте превью

Создайте скриншот размером **400×300 px** и сохраните как `preview.png`.

### Шаг 4: Установите и протестируйте

```
1. Скопируйте папку в: %APPDATA%\ByBedrockLauncher\Themes\
2. Перезапустите лаунчер
3. Откройте вкладку "Темы"
4. Выберите вашу тему
```

---

## 💡 Готовые цветовые схемы

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
    "glowColor": "#40238636"
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
    "glowColor": "#400EA5E9"
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
    "glowColor": "#40F43F5E"
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
    "glowColor": "#4022C55E"
}
```

### ☀️ Light Theme (базовая)

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
    "glowColor": "#306366F1"
}
```

---

## ✅ Чек-лист качественной темы

- [ ] ✨ Достаточный контраст текста (минимум 4.5:1 по WCAG)
- [ ] 🎨 Все обязательные цвета заданы
- [ ] 🖼️ `preview.png` присутствует (400×300)
- [ ] 🧪 Тема протестирована во всех разделах лаунчера
- [ ] 👀 Нет слишком ярких/слепящих цветов
- [ ] 📖 Glass-эффекты не мешают читаемости
- [ ] 💫 Glow не слишком интенсивный
- [ ] 📱 UI элементы читаемы на разных разрешениях

> **🔗 Проверка контраста:** [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/)

---

## 📦 Установка из релизов

1. Скачайте `.zip` из [Releases](https://github.com/ByBedrock/ThemesSource/releases/latest)
2. Распакуйте в `%APPDATA%\ByBedrockLauncher\Themes\`
3. Перезапустите лаунчер
4. Выберите тему во вкладке "Темы"

---

## 🤝 Как добавить свою тему в репозиторий

1. **Fork** этого репозитория
2. Создайте папку `YourThemeName/`
3. Добавьте `theme.manifest.json` (обязательно)
4. Добавьте `preview.png` (рекомендуется)
5. Создайте **Pull Request**

---

## 🔧 Миграция с v1.0

1. Обновите `compatibility` на `1.1.0`
2. **Удалите** устаревшие поля `iconHome`, `iconProfiles`, `iconVersions`, `iconSettings`
3. Добавьте новые унифицированные поля иконок: `home`, `profiles`, `versions`, `servers`, `themes`, `settings`
4. По желанию перенесите картинки в папку `Assets/`
5. Используйте `styles.axaml` для расширенной кастомизации UI

---

## ❓ FAQ

**Q: Моя тема не отображается в лаунчере**  
A: Проверьте, что `theme.manifest.json` валидный JSON и находится в корне папки темы.

**Q: Иконки не отображаются**  
A: Убедитесь, что используете правильный синтаксис (`fluent:Home`, а не `Home` или `fluent:home`).

**Q: Hot-Reload не работает**  
A: Hot-Reload срабатывает с задержкой ~500мс. Убедитесь, что файл сохранён полностью.

**Q: Glass-эффекты не видны**  
A: Установите `opacity` меньше 1.0 и/или `blurStrength` больше 0.

---

<div align="center">

**Создано с 🎨 командой ByBedrock**

[🚀 Launcher](https://t.me/bybedrock_launcher) • [🎨 Themes](https://github.com/ByBedrock/ThemesSource)

</div>
