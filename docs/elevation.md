# Elevation Module

The elevation module allows you to apply box shadow to elements such as cards, buttons, etc. This module can either be applied to an element directly, extended in your SCSS, or both.

## Usage

> This module requires Dart Sass if it's being extended in your SCSS files.

### Included in core: ✅

### For modular setups:

```scss
@use '<path-to-node_modules>/@fulcrumui/css-utils/scss/modules/elevation';
```

### Application

To apply this utility, use the pattern below:

```html
<element class="u-elevation-[option<number(1-10)>]"></element>
```

### Options

| Option | Description |
| --- | --- |
| `1` | Will apply `box-shadow: 1px 1px 4px #c8cdd0` |
| `2` | Will apply `box-shadow: 2px 2px 5px #c8cdd0` |
| `3` | Will apply `box-shadow: 3px 3px 6px #c8cdd0` |
| `4` | Will apply `box-shadow: 4px 4px 7px #c8cdd0` |
| `5` | Will apply `box-shadow: 5px 5px 8px #c8cdd0` |
| `6` | Will apply `box-shadow: 6px 6px 9px #c8cdd0` |
| `7` | Will apply `box-shadow: 7px 7px 10px #c8cdd0` |
| `8` | Will apply `box-shadow: 8px 8px 11px #c8cdd0` |
| `9` | Will apply `box-shadow: 9px 9px 12px #c8cdd0` |
| `10` | Will apply `box-shadow: 10px 10px 13px #c8cdd0` |

## Configurable ❌
