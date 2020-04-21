# Text Transform Module

This utility allows you to apply text transformations to elements

## Usage

### Included in core: ✅

### For modular setups:

```scss
@use '<path-to-node_modules>/@fulcrumui/css-utils/scss/modules/text-transform';
```

### Application

To apply this utility, use the pattern below:

```html
<element class="u-text-transform-[transformType]"></element>
```

### Options

#### `transformType`

| Option | Description |
| --- | --- |
| `none` | Will remove text transformations of an element within a parent of tranformed text |
| `capitalize` | Will capitalize the first letter of the element |
| `uppercase` | Will make all text within the element uppercase |
| `lowercase` | Will make all text within the element lowercase |

## Configurable ❌
