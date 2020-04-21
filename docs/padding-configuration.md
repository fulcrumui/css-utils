# Padding Configuration

This configuration will allow you to set the padding values to be included in the Padding Module

## How to configure your Padding Module

> All configuration changes require Dart Sass to be used in your project

### Configuration Property: `$PADDING`

### Configuration Options

| Option | Description |
| --- | --- |
| `'start'` | The number to start creating padding at <br/> **Default**: 0 |
| `'end'` | The number to stop creating padding at <br/> **Default**: 50 |
| `'incrementBy'` | The number which to increment each padding by <br/> **Default**: 5 <br/> **Example:** If you change this value to 10, the padding module will create padding with the sizes 0, 10, 20...50 |

## Examples

```scss
// add the Fulcrum UI config and change the values for the $FONT_SIZE property

@use '<path-to-node_modules>/@fulcrumui/css-utils/scss/config' with (
  $PADDING: (
    'start': 0,
    'end': 30,
    'incrementBy': 10
  ),
);

// Then add the Fulcrum UI Padding Module if you're doing a modular setup

@use '<path-to-node_modules>/@fulcrumui/css-utils/scss/padding';

// or if you want the whole library

@use '<path-to-node_modules>/@fulcrumui/css-utils/scss/fulcrum';
```

The above configuration will create padding classes from 0-30 in steps of 10 (ie 0, 10, 20, 30)
