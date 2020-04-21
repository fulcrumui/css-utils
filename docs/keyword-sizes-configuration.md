# Keyword Sizes Configuration

This configuration will allow you to set the sizes of the Keyword Sizes Module, as well as add additionl keywords and sizes if you require even more options.

> Sizes must be **unitless** and are represented as `px` values of their number when consumed

## How to configure your Keyword Sizes Module

> All configuration changes require Dart Sass to be used in your project

### Configuration Property: `$SIZING`

### Configuration Options

| Option | Description |
| --- | --- |
| `'small'` | **Default**: 15 |
| `'medium'` | **Default**: 30 |
| `'large'` | **Default**: 45 |
| `'x-large'` | **Default**: 60 |
| `...`* | **Default**: N/A |

> The `...` represents custom values that you can provide. The keyword 'key' must be a quoted string, and the value must be a **unitless** number that will be represented by `px`.
>
> **Example** `'x-small': 10` would be represented by `10px` when using the `x-small` keyword

## Examples

### Simple configuration

```scss
// add the Fulcrum UI config and change the values for the $FONT_SIZE property

@use '<path-to-node_modules>/@fulcrumui/css-utils/scss/config' with (
  $SIZING: (
    'small': 10,
    'medium': 15,
    'large': 20,
    'x-large': 25,
  ),
);

// Then add the Fulcrum UI Font Size Module if you're doing a modular setup

@use '<path-to-node_modules>/@fulcrumui/css-utils/scss/keyword-sizes';

// or if you want the whole library

@use '<path-to-node_modules>/@fulcrumui/css-utils/scss/fulcrum';
```

In the example above you can see that we are just adjusting the sizes of the default values provided. In the next example we will look at how to adjust the default values, as well as how to add extra values.

### Additional config values

```scss
@use '<path-to-node_modules>/@fulcrumui/css-utils/scss/config' with (
  $SIZING: (
    'x-small': 5,
    'small': 10,
    'medium': 15,
    'large': 20,
    'x-large': 25,
    'friggin-huge': 100,
  ),
);
```

In the above example, we are not only adjusting the default values, but also adding an `x-small` keyword and a `friggin-huge` keyword. Below we will see how to add additional properties while leaving the default keywords in tact.

```scss
@use '<path-to-node_modules>/@fulcrumui/css-utils/scss/config' with (
  $SIZING: (
    'x-small': 5,
    'friggin-huge': 100,
  ),
);
```

In the example above, the `small|medium|large|x-large` values are preserved with their default values, and the `x-small|friggin-huge` keywords are added to the config as additional values!
