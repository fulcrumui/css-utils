# Font Size Module

This utility allows you to centralize your font sizing and set a sizing rhythm for you application

## Usage

### Included in core: ✅

### For modular setups:

```scss
@use '<path-to-node_modules>/@fulcrumui/css-utils/scss/modules/font-size';
```

### Application

To apply this utility, use the pattern below:

```html
<element class="u-font-size-[option<number>]"></element>
```

### Options

| Option | Description |
| --- | --- |
| `number` | An even number that is provided by the config <br/> **Default**: 8-50 |

## Configurable ✅

[See how to configure the `$FONT_SIZE` property](font-size-configuration.md)

## Example

```html
<element class="u-font-size-22">Some text here</element>
```
