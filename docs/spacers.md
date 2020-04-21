# Spacers Module

This utility allows you to apply a class to an empty element to use as a spacer between sections.

## Usage

### Included in core: ❌

> Currently this module needs to be included in order to be used. The prefered method is to use the [Keyword Sizes Module](keyword-sizes.md) in place of this module.

### For modular setups:

```scss
@use '<path-to-node_modules>/@fulcrumui/css-utils/scss/modules/spacers';
```

### Application

To apply this utility, use the pattern below:

```html
<element
  class="u-spacer-[size<number(0-50)>]"
  aria-hidden="true"
></element>
```

> Be sure to add `aria-hidden="true"` to any elements used as spacers to remove it from the accessibility tree

### Options

#### `size`

| Option | Description |
| --- | --- |
| `number` | The size of the spacer in pixels <br/> **Default**: 0-50 incremented by 5 (ie 0, 5, 10, 15...50) |

## Configurable ✅

[See how to configure the `$SPACERS` property](spacers-configuration.md)
