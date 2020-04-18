# 1.0.0-beta1 (2020-04-18)

## Bug Fixes

- Margin, padding, and spacer utilities have been aligned to standard config implementations.
  - `'start'` now represents the value that is used as the first value to be used for the utility
  - `'end'` now represents the last value to be used for the utility
  - `'incrementBy'` has replaced `'multiplier'` and represents the amount by which the utility increments it's value by addition instead of multiplication (which is what `multiplier` previously did)

- A bunch of documentation updates in preparation for the website being launched

- CHANGELOG cleanup to only represent the `@fulcrumui/css-utils` library and remove the `fulcrum-css` legacy library

# 1.0.0-beta0 (2020-04-05)
<!-- write release notes -->

## Breaking Changes

- FulcrumCSS is now using DartSass to take advantage of the 'new' module import system. This allows FulcrumCSS to either be used as is right out of the box or to be fully configurable to fit your needs.
- **Flex grid has been removed** in favor of the new implementation. See the documentation on how to use the new and improved grid implemenation.

## Features

- FulcrumCSS is now using Dart Sass! (is there an echo in here?)
  - Config file has been added with configurations for:
    - Grid columns
    - Grid Gutters
    - Breakpoints
    - Sizing (page rhythm)
    - Margins
    - Padding
    - Spacers
    - Font Size
  - You can either choose to utilize the compiled FulcrumCSS file as is, or you can utilize the fulcrum.scss file to adjust the configuration of the above modules

### Bug fixes

- Removed unused modules from main level import
