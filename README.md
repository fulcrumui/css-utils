# CSS Utilities

**We are diligently working to get the documentation for Fulcrum UI CSS Utilities completed. Until then, please see some examples below.**

Fulcrum UI CSS utilities is a library that allows you to *leverage* commonly used CSS to apply simple styles and position to elements by simply adding markup. By using Fulcrum UI CSS Utilities you can focus on writing verbose, clean markup, while reducing CSS redundancies caused by commonly used styles. The Fulcrum UI CSS Utilities uses single class rules that only ever carry a specificity of 020, which makes this ideal to use alongside BEM methodology to increase development efficiency and decrease development time.

The Fulcrum UI CSS Utilities are lighweight and modular. You can either import the whole library, or you can simply import what you need. Fulcrum UI CSS Utilities leverages the power of Dart Sass, and aims to be fully configurable. We are constantly adding new features to Fulcrum UI. If there is a feature you are looking for but is not listed in the roadmap, feel free to let us know what you would like to see added!

## Installing Fulcrum

To install Fulcrum UI CSS Utilities, all you need to do is

```bash
yarn add @fulcrumui/css-utils
# or
npm i @fulcrumui/css-utils
```

## Using Fulcrum

There are a few ways that you can utilize the Fulcrum UI CSS utilities in your application.

### **Option 1: Everything but the kitchen sink**

With this option you are able to leverage the full power of Fulcrum UI's CSS utilities! To use this method you would simply include the perbuilt minified stylesheet:

```scss
// for projects using Dart Sass

@use '<path-to-node_modules>/@fulcrumui/css-utils/dist/fulcrum.min.css';

// for projects still using node-sass (or other sass implementation) or Vanilla CSS

@import '<path-to-node_modules>/@fulcrumui/css-utils/dist/fulcrum.min.css';
```

Once you have included the minified CSS utils stylesheet in your project, you can begin to leverage the entire Fulcrum UI CSS utils library and all of it's modules.

This is by far the easiest way to include Fulcrum UI in your development. If you need more granular control, or if you would like to only use a few modules see the other options below.

### **Option 2: Modular (no config)**

_**NOTE:** This implementation requires you to be using Dart Sass in your development!_

```scss
@use '<path-to-node_modules>/@fulcrumui/css-utils/scss/modules/<module-name>';
```

You can now begin to use the included Fulcrum UI CSS Utility module in your development.

_**NOTE:** The modules path should not include the underscore or file extension!_

```scss
// DO

@use '<path-to-node_modules>/@fulcrumui/css-utils/scss/modules/margin';

// DON'T

@use '<path-to-node_modules>/@fulcrumui/css-utils/scss/modules/margin/_index.scss';
```

### **Option 3: Everything but the kitchen sink (with config)**

_**NOTE:** This implementation requires you to be using Dart Sass in your development!_

```scss
@use '<path-to-node_modules>/@fulcrumui/css-utils/fulcrum.scss' with (
  // config values here!
);
```

You can now use all of the Fulcrum UI CSS Utilities with the configuration values that you have provided! You also do not need to include configurations for each utility, as they are set up with default values. So if you want to customize the config values for 1 module, go for it. If you want to change the config values for all of the modules, you can do that too. It's entirely up to you!

### **Option 4: Modular (with config)**

_**NOTE:** This implementation requires you to be using Dart Sass in your development!_

```scss
@use '<path-to-node_modules>/@fulcrumui/css-utils/config' with (
  // config values here for the margin module!
);
@use '<path-to-node_modules>/@fulcrumui/css-utils/modules/margin';
// any other modules that you would like to use

// Then be sure to include the module you would want to use

@include margin.margins;
```

You can now use the Fulcrum UI CSS Utility you've included with the configuration values that you have provided! You only need to add the configuration **once**. It is also important to note that you **need to include the configuration before you include any of the Fulcrum UI CSS Utility modules**.

**Larger example below:**

```scss
@use './config' with (
  $MARGINS: (
    'start': 10,
    'end': 30,
    'multiplier': 5,
  ),
  $PADDING: (
    'start': 10,
    'end': 60,
    'incrementBy': 2,
  ),
  $SPACERS: (
    'start': 15,
    'end': 60,
    'incrementBy': 15,
  ),
);
@use './modules/margin';
@use './modules/padding';
@use './modules/spacers';

@include margin.margins; // will now have all margin rules from 10-30 incremented by 5 (10, 15, 20...30)
@include padding.padding; // will now have all padding rules from 10-60 incremented by 2 (10, 12, 14...60)
@include spacers.spacers; // will now have all spacers from 15-60 incremented by 15 (15, 30, 45, 60);
```

You can now use these utility classes on elements like so:

```html
<!-- This will apply 10px of block & inline margining to the element -->
<section class="example-element u-margin-all-10"></section>
```

## **Important!!!**
To ensure that Fulcrum UI CSS Utilities are able to override any styles that you have defined elsewhere, make sure that your `@use` statements referencing fuclrumui are placed last in your `@use` group!
