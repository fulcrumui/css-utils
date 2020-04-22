# Grid Layout Configuration

This configuration will allow you to set the gutters and number of columns in the Layout Grid Module

## How to configure your Layout Grid Module

> All configuration changes require Dart Sass to be used in your project

### Configuration Property: `$GRID`

### Configuration Options

| Option | Description |
| --- | --- |
| `'columns'` | Sets the number of columns that the Grid Layout has <br/> **Default**: 12 |
| `'gutters'` | The gutter width between columns <br/> **Default**: 15px <br/> **NOTE: The gutters property MUST NOT be unitless** |

## Examples

```scss
// add the Fulcrum UI config and change the values for the $FONT_SIZE property

@use '<path-to-node_modules>/@fulcrumui/css-utils/scss/config' with (
  $GRID: (
    'columns': 6,
    'gutters': 30px,
  ),
);

// Then add the Fulcrum UI Margin Module if you're doing a modular setup

@use '<path-to-node_modules>/@fulcrumui/css-utils/scss/grid-layout';

// or if you want the whole library

@use '<path-to-node_modules>/@fulcrumui/css-utils/scss/fulcrum';
```
