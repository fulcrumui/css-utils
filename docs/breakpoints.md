# Breakpoints Module

The breakpoint module allows you to set your breakpoints in one place, and then use them throughout your application with a keyword.

## Usage

> This module is intended to be used in your Scss files and requires Dart Sass.

### Included in core: ❌

### For modular setups:

```scss
@use '<path-to-node_modules>/@fulcrumui/css-utils/scss/modules/breakpoints';
```

### Application

To apply this utility, use the pattern below:

```html
<element class="example"></element>
```

```scss
.example {
  @include breakpoints.bp([option]) {
    // your rules for this breakpoint go here
  }
}
```

### Options

| Option | Description |
| --- | --- |
| `mobile` | Applies your mobile brekpoint <br /> **Default: `null`** |
| `tablet` | Applies your tablet brekpoint <br /> **Default: `775px`** |
| `desktop` | Applies your desktop brekpoint <br /> **Default: `993px`** |

## Configurable 🔜

<!-- [See how to configure the `$BREAKPOINTS` property](breakpoints-configuration.md) -->
