# Contrast Module

This module allows you to use a funciton to ensure that the text of your element meets WCAG accessibility standards by making the text black or white given a background hex color.

## Usage

> This module is intended to be used in your Scss files and requires Dart Sass.

### Included in core: ❌

### Application

```scss
@use '<path-to-node_modules>/@fulcrumui/css-utils/scss/modules/contrast';
```

To apply this utility, use the pattern below:

```html
<element class="example"></element>
```

```scss
.example {
  color: contrast.contrast([value]);
}
```

### Options

| Option | Description |
| --- | --- |
| `value` | A hexidecimal value or a SCSS variable representing a hexidecimal value |

## Configurable ❌

<!-- [See how to configure the `$BREAKPOINTS` property](breakpoints-configuration.md) -->
