# Flex Align Items Module

> TODO: possibly rename this to `place module`

This utility will help you easily position the contents of a flex-container

## Usage

> This utility class is meant to be applied **to the flex container** in order to align it's children. The container **will automatically be set to `display: flex;` by this utility**.

### Included in core: ✅

### For modular setups:

```scss
@use '<path-to-node_modules>/@fulcrumui/css-utils/scss/modules/flex-align-items';
```

### Application

To apply this utility, use the pattern below:

```html
<element class="u-[alignmentType<align|justify>]-[alignmentTarget<items|content>]-[alignmentPosition<start|center|end>]"></element>
```

### Options

#### `alignmentType`

| Option | Description |
| --- | --- |
| `align` | Applies the `align` flex positioning to the child elements |
| `justify` | Applies the `justify` flex positioning to the child elements |

#### `alignmentTarget`

| Option | Description |
| --- | --- |
| `items` | Applies the positioning to the flex items |
| `content` | Applies the positioning to the flex content |

#### `alignmentPosition`

| Option | Description |
| --- | --- |
| `start` | Will position the children to the `flex-start` of the parent |
| `center` | Will position the children to the `center` of the parent |
| `end` | Will position the children to the `flex-end` of the parent |

## Configurable ❌

[See how to configure the `$BREAKPOINTS` property](breakpoints-configuration.md)

## Example

```html
<element class="u-justify-content-center u-align-items-center"></element>
```
