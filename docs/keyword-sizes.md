# Keyword Sizes Module

This utility allows you to apply margin & padding to an element, as well as use spacers with a keyword. This module is by far the most powerful sizing/spacing module to use in applications to create page rhythm continuity. It leaves little to no room for 'eyeballing it', and allows you to change your page rhythm in a central location if you decide change it later on. Once it is changed in that one location it will be updated wherever you are using the Fulcrum UI Utility class with that keyword

## Usage

### Included in core: ✅

### For modular setups:

```scss
@use '<path-to-node_modules>/@fulcrumui/css-utils/scss/modules/keyword-sizes';
```

### Application

To apply this utility, use the pattern below:

```html
<element class="u-[utilityType]-[position*]-[keyword]"></element>
```

### Options

#### `utilityType`

| Option | Description |
| --- | --- |
| `padding` | Will apply the adjustment to the element's padding |
| `margin` | Will apply the adjustment to the element's margin |
| `spacer` | Will make the element act like a spacer to separate sections |

#### `position*`

> *This value is only used with `margin` & `padding`. If used with `spacer` or omitted from `margin|padding` the utility classes will not apply adjustments to the element.

| Option | Description |
| --- | --- |
| `top` | Will apply the adjutment to the top of the element |
| `bottom` | Will apply the adjustment to the bottom of the element |
| `block` | Will apply the adjustment to the top & bottom of the element |
| `left` | Will apply the adjustment to the left of the element |
| `right` | Will apply the adjustment to the right of the element |
| `inline` | Will apply the adjustment to the left & right of the element |
| `all` | Will apply the adjustment to all sides of the element |

#### `keyword`

> All keywords represent a `px` representation of their number

| Option | Description |
| --- | --- |
| `small` | Will apply the small value to the adjustment <br/> **Default**: 15 |
| `medium` | Will apply the small value to the adjustment <br/> **Default**: 30 |
| `large` | Will apply the small value to the adjustment <br/> **Default**: 45 |
| `x-large` | Will apply the small value to the adjustment <br/> **Default**: 60 |

## Configurable ✅

[See how to configure the `$SIZING` property](keyword-sizes-configuration.md)
