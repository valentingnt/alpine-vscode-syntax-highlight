# Alpine.js Syntax Highlight

JavaScript syntax highlighting for Alpine.js directives, magic properties, and methods in HTML, PHP, Twig, Liquid, and HEEX files.

## Features

- ✅ **Any** `x-*` directive (including core directives and those from Alpine.js plugins like `x-mask`, `x-resize`, etc.)
- ✅ Shorthand syntax (`@click` for `x-on:click`, `:class` for `x-bind:class`)
- ✅ Magic properties (`$store`, `$el`, `$dispatch`, `$watch`, `$refs`, `$nextTick`)
- ✅ Alpine methods (`Alpine.data`, `Alpine.store`)
- ✅ JavaScript expressions inside attribute values

## Setup

To apply the custom color `#48A9C1` (cyan) to Alpine.js syntax, add this to your VS Code `settings.json`:

**File → Preferences → Settings → Open Settings (JSON)**

```json
{
  "editor.tokenColorCustomizations": {
    "textMateRules": [
      {
        "scope": "alpinejs.directive",
        "settings": {
          "foreground": "#48A9C1"
        }
      },
      {
        "scope": "meta.attribute.alpine alpinejs.directive",
        "settings": {
          "foreground": "#48A9C1"
        }
      },
      {
        "scope": "variable.other.property.alpinejs",
        "settings": {
          "foreground": "#48A9C1"
        }
      },
      {
        "scope": "meta.embedded.inline.alpinejs variable.other.property.alpinejs",
        "settings": {
          "foreground": "#48A9C1"
        }
      },
      {
        "scope": "entity.name.function.alpinejs",
        "settings": {
          "foreground": "#48A9C1"
        }
      },
      {
        "scope": "meta.embedded.inline.alpinejs entity.name.function.alpinejs",
        "settings": {
          "foreground": "#48A9C1"
        }
      }
    ]
  }
}
```

Reload VS Code and you're done!

## Customizing the Color

Want a different color? Just change `#48A9C1` to any hex color in the settings above.

## Troubleshooting

If highlighting isn't working:

1. Make sure you've added the settings above to `settings.json`
2. Reload VS Code: `Cmd+Shift+P` → "Developer: Reload Window"
3. Use Scope Inspector to verify: `Cmd+Shift+P` → "Developer: Inspect Editor Tokens and Scopes"

## Credits

Based on the [original extension](https://marketplace.visualstudio.com/items?itemName=sperovita.alpinejs-syntax-highlight) with added support for Liquid templates and enhanced highlighting for all Alpine.js features.
