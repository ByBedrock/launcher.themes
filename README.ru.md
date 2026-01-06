# 🎨 ByBedrock Themes v2.0

<div align="center">

**Коллекция тем для кастомизации ByBedrock Launcher**

[![Version](https://img.shields.io/badge/version-2.0.0-blue?style=flat-square)](https://github.com/ByBedrock/ThemesSource)
[![Themes](https://img.shields.io/badge/themes-5-blueviolet?style=flat-square)](https://github.com/ByBedrock/ThemesSource/releases)
[![Format](https://img.shields.io/badge/format-JSON-yellow?style=flat-square)](https://www.json.org/)

**[🇬🇧 English version](README.md)**

</div>

---

## 🆕 Что нового в v2.0

- **Glass-эффекты** — полупрозрачные элементы с размытием
- **Glow-эффекты** — свечение для акцентных элементов
- **Gradient-кнопки** — градиентные заливки
- **Micro-анимации** — плавные hover/click переходы
- **Обновлённая палитра** — современные цвета

---

## 🌈 Доступные темы

| Тема | Описание | Стиль |
|------|----------|-------|
| **DefaultTheme** | Стандартная тема с фиолетовыми градиентами | Dark |
| **NanoDark** | Ультра-тёмная с кастомными иконками | Dark OLED |
| **NanoLight** | Светлая для дневного использования | Light |
| **MinecraftTheme** | Стилизация под Minecraft | Dark Green |
| **NeonTheme** | Киберпанк с неоновым свечением | Dark Neon |

---

## 📁 Структура темы

```
MyTheme/
├── theme.manifest.json    # Единственный обязательный файл
├── preview.png            # Превью темы (рекомендуется)
├── background.png         # Фоновое изображение (опционально)
├── banner.png             # Баннер (опционально)
├── icon_home.png          # Кастомная иконка (опционально)
├── icon_profiles.png
├── icon_versions.png
└── icon_settings.png
```

---

## 📄 theme.manifest.json — Полная спецификация

### Минимальный манифест

```json
{
    "name": "MyTheme",
    "version": "1.0.0",
    "author": "Your Name",
    "description": "Описание темы",
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
    "version": "2.0.0",
    "author": "Your Name",
    "description": "Моя крутая тема с glass-эффектами",
    "compatibility": "2.0.0",
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

## 🎨 Описание переменных

### Основные цвета

| Переменная | Описание | Пример |
|------------|----------|--------|
| `primaryColor` | Основной акцентный цвет (кнопки, ссылки) | `#818CF8` |
| `secondaryColor` | Вторичный цвет для градиентов | `#A78BFA` |
| `accentColor` | Цвет успеха/активных элементов | `#34D399` |

### Фоновые цвета

| Переменная | Описание | Пример |
|------------|----------|--------|
| `backgroundColor` | Основной фон приложения | `#0A0A0F` |
| `surfaceColor` | Фон sidebar и секций | `#12121A` |
| `cardColor` | Фон карточек и панелей | `#1A1A24` |

### Текстовые цвета

| Переменная | Описание | Пример |
|------------|----------|--------|
| `textColor` | Основной цвет текста | `#F8FAFC` |
| `textSecondaryColor` | Вторичный текст (подписи) | `#94A3B8` |

### Статусные цвета

| Переменная | Описание | Пример |
|------------|----------|--------|
| `errorColor` | Ошибки и предупреждения | `#F87171` |
| `successColor` | Успешные операции | `#4ADE80` |
| `warningColor` | Предупреждения | `#FBBF24` |

### Glass и Glow эффекты (v2.0)

| Переменная | Описание | Пример |
|------------|----------|--------|
| `glassColor` | Полупрозрачный фон glass-элементов | `#15FFFFFF` |
| `glassBorderColor` | Граница glass-элементов | `#25FFFFFF` |
| `glowColor` | Цвет свечения кнопок | `#40818CF8` |

### Другие настройки

| Переменная | Описание | Пример |
|------------|----------|--------|
| `borderColor` | Цвет границ | `#2A2A3A` |
| `fontFamily` | Шрифт | `Inter` |
| `borderRadius` | Скругление углов (px) | `16` |
| `animationDuration` | Длительность анимаций (сек) | `0.2` |

---

## 🆕 Создание новой темы

### Шаг 1: Создайте папку

```bash
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
    "compatibility": "2.0.0",
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

### Шаг 3: Добавьте превью (рекомендуется)

Создайте `preview.png` размером 400x300 пикселей со скриншотом темы.

### Шаг 4: Установите и протестируйте

```
1. Скопируйте папку в: %APPDATA%\ByBedrockLauncher\Themes\
2. Перезапустите лаунчер
3. Откройте вкладку "Темы"
4. Выберите вашу тему
```

---

## 💡 Примеры цветовых схем

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

## 🖼️ Требования к изображениям

| Файл | Размер | Формат | Описание |
|------|--------|--------|----------|
| `preview.png` | 400x300 | PNG | Превью в списке тем |
| `background.png` | 1920x1080+ | PNG | Фон приложения |
| `banner.png` | 1920x300 | PNG | Баннер на главной |
| `icon_*.png` | 24x24 | PNG + Alpha | Иконки навигации |

---

## ✅ Чек-лист качественной темы

- [ ] Достаточный контраст текста (минимум 4.5:1)
- [ ] Все обязательные цвета заданы
- [ ] `preview.png` присутствует
- [ ] Тема протестирована во всех разделах
- [ ] Нет слишком ярких/слепящих цветов
- [ ] Glass-эффекты не мешают читаемости
- [ ] Glow не слишком интенсивный

---

## 📦 Установка из релизов

1. Скачайте `.zip` из [Releases](https://github.com/ByBedrock/ThemesSource/releases/latest)
2. Распакуйте в `%APPDATA%\ByBedrockLauncher\Themes\`
3. Перезапустите лаунчер
4. Выберите тему во вкладке "Темы"

---

## 🤝 Как добавить свою тему

1. Fork репозитория
2. Создайте папку `YourThemeName/`
3. Добавьте `theme.manifest.json`
4. Добавьте `preview.png`
5. Создайте Pull Request

---

## 🔧 Миграция с v1.0

Если у вас есть тема старого формата:

1. Удалите `colors.json` — он больше не используется
2. Удалите секцию `resources` (пустые массивы)
3. Добавьте новые переменные:
   - `glassColor`
   - `glassBorderColor`  
   - `glowColor`
4. Обновите `version` и `compatibility` на `2.0.0`

---

<div align="center">

**Создано с 🎨 командой ByBedrock**

[🚀 Launcher](https://github.com/ByBedrock/Launcher) • [🧩 Modules](https://github.com/ByBedrock/ModulesSource) • [🎨 Themes](https://github.com/ByBedrock/ThemesSource)

</div>
