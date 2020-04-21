# Browser Compatibility Module

> TODO: Edit this to include other browser detection

This module is intended to target IE 10/11 with CSS media queries to allow you to write rules that will specifically target these browsers.

## Usage

> This module is intended to be used in your Scss files and requires Dart Sass.

### Included in core: ❌

### For modular setups:

```scss
@use '<path-to-node_modules>/@fulcrumui/css-utils/scss/modules/browser-compat';
```

### Application

To apply this utility, use the pattern below:

```html
<element class="example"></element>
```

```scss
.example {
  @include browser-compat.ie10plus {
    // your rules for ie browsers go here
  }
}
```

### Options

| Option | Description |
| --- | --- |
| **NONE** | This module does not accept options |

## Configurable ❌
