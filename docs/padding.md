# Padding Module

This utility allows you to apply padding to all, or portions, of your element

## Usage

### Included in core: ❌

> Currently this module needs to be included in order to be used. The prefered method is to use the [Keyword Sizes Module](keyword-sizes.md) in place of this module.

### For modular setups:

```scss
@use '<path-to-node_modules>/@fulcrumui/css-utils/scss/modules/padding';
```

### Application

To apply this utility, use the pattern below:

```html
<element class="u-padding-[position]-[size<number(0-50)>]"></element>
```

### Options

#### `position`

| Option | Description |
| --- | --- |
| `top` | Will apply the adjustment to the top side of the element |
| `bottom` | Will apply the adjustment to the bottom side of the element |
| `block` | Will apply the adjustment to the top & bottom side of the element |
| `left` | Will apply the adjustment to the left side of the element |
| `right` | Will apply the adjustment to the right side of the element |
| `inline` | Will apply the adjustment to the left & right side of the element |
| `all` | Will apply the adjustment to all sides of the element |

#### `size`

| Option | Description |
| --- | --- |
| `number` | The amount of pixels to apply with the adjustment <br/> **Default**: 0-50 incremented by 5 (ie 0, 5, 10, 15...50) |

## Configurable ✅

[See how to configure the `$PADDING` property](padding-configuration.md)
