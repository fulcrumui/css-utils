# Configuring

Configuring Fuclrum UI CSS Utilites to fit your needs is easy! You can choose to configure a lot or a little, the choice is up to you. There are a few different ways to configure Fulcrum UI's CSS Utilities The example below will show a full configuration to show you all of the possibilities for configuration.

> Configuring Fulcrum UI CSS Utilities requires your project to be using Dart Sass

## Example

```scss
/*
  Add the config and alter the values

  If you want to use the default values provided by Fulcrum UI you can simply omit that config property
*/

@use '<path-to-node_modules>/@fulcrumui/css-utils/scss/modules/config' with (
  $FONT_SIZE: ( /* Included by default */
    'start': 10,
    'maxSixe': 48,
  ),
  $GRID: ( /* Included by default */
    'columns': 16,
    'gutters': 10px,
  ),
  $KEYWORD_SIZES: ( /* Included by default */
    'x-small': 5,
    'small': 10,
    'medium': 20,
    'large': 50,
    'x-large': 100,
  ),
  $BREAKPOINTS: ( /* Included by default */
    'mobile': 425px,
    'tablet': 800px,
    'desktop': 1366px,
  ),
  $MARGINS: ( /* Module NOT included by default */
    'start': 10,
    'end': 50,
    'incrementBy': 10,
  ),
  $PADDING: ( /* Module NOT included by default */
    'start': 5,
    'end': 100,
    'incrementBy': 2,
  ),
  $SPACERS: ( /* Module NOT included by default */
    'start': 15,
    'end': 60,
    'incrementBy': 15,
  ),
);

// Add the whole library

@use '<path-to-node_modules>/@fulcrumui/css-utils/scss/fulcrum';

// Add additional modules not included by default if ou want to use them

@use '<path-to-node_modules>/@fulcrumui/css-utils/scss/modules/margin';
@use '<path-to-node_modules>/@fulcrumui/css-utils/scss/modules/padding';
@use '<path-to-node_modules>/@fulcrumui/css-utils/scss/modules/spacers';

```
