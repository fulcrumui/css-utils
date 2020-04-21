# Font Size Configuration

This configuration will allow you to set the minimum and maximum font-size for your Font Size Module

> The font size incrementer is not yet configurable. This will be provided in a later release, however for now all fonts are incremented by `2`

## How to configure your Font Size Module

> All configuration changes require Dart Sass to be used in your project

### Configuration Property: `$FONT_SIZE`

### Configuration Options

| Option | Description |
| --- | --- |
| `'start'` | The first value that the Font Size Uitility will create |
| `'maxSize'` | The last value the Font Size Utility will create |

## Examples

```scss
// add the Fulcrum UI config and change the values for the $FONT_SIZE property

@use '<path-to-node_modules>/@fulcrumui/css-utils/scss/config' with (
  $FONT_SIZE: (
    'start': 8,
    'maxSize': 50,
  ),
);

// Then add the Fulcrum UI Font Size Module if you're doing a modular setup

@use '<path-to-node_modules>/@fulcrumui/css-utils/scss/font-size';

// or if you want the whole library

@use '<path-to-node_modules>/@fulcrumui/css-utils/scss/fulcrum';
```
