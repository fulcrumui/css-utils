# Align Self Module

The Align Self module is used to easily align a flex-container's child using the `align-self` CSS rule.

## Usage

> For this Utility to be used, the parent container must be `display: flex;`

### Included in core: ✅

### For modular setups:

```scss
@use '<path-to-node_modules>/@fulcrumui/css-utils/scss/modules/align-self';
```

### Application

To apply this utility, use the syntax below for your class.

```html
<element class="u-align-self-[option<start|center|end>]"></element>
```

### Options

| Option | Description |
| --- | --- |
| `start` | Will align the element to the container's `flex-start` |
| `center` | Will align the element to the container's `center` |
| `end` | Will align the element to the container's `flex-end` |

## Configurable ❌

> This module does not have configurable options
