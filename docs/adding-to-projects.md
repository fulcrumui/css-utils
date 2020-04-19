# Using fulcrumui CSS Utilities

There are a few ways that you can utilize the fulcrumui CSS utilities in your application. There are examples below of some of the most common ways to utilize the fulcrumui CSS Utilities library in your projects. While there are other ways to use it as well, we encourage you to implement the library with one of the recommended ways below. Don't be clever 😉.

## **Option 1: Everything but the kitchen sink**

With this option you are able to leverage the full power of fulcrumui's CSS utilities! To use this method you would simply include the prebuilt minified stylesheet:

```scss
// for projects using Dart Sass

@use '<path-to-node_modules>/@fulcrumui/css-utils/dist/fulcrum.min.css';

// for projects still using node-sass (or other sass implementation) or Vanilla CSS

@import '<path-to-node_modules>/@fulcrumui/css-utils/dist/fulcrum.min.css';
```

Once you have included the minified CSS utils stylesheet in your project, you can begin to leverage the entire fulcrumui CSS utils library and all of it's modules.

This is by far the easiest way to include fulcrumui in your development. If you need more granular control, or if you would like to only use a few modules see the other options below.

> All the methods below assume that you have basic knowledge on the Dart Sass Module Import system. If you are not familiar with this please see the blog posts below before getting started.
>
> - [Sass Module Import System is Launched](https://sass-lang.com/blog/the-module-system-is-launched)
> - [A Hands-on First Look at the Sass `@use` Implementation (3 parts)](https://dev.to/gtyrkicksin216/a-hands-on-first-look-at-the-sass-use-implementation-part-1-3ajb)

## **Option 2: Modular (no config)**

_**NOTE:** This implementation requires you to be using Dart Sass in your development!_

```scss
@use '<path-to-node_modules>/@fulcrumui/css-utils/scss/modules/<module-name>';
```

You can now begin to use the included fulcrumui CSS Utility module in your development.

_**NOTE:** The modules path should not include the underscore or file extension!_

```scss
// DO

@use '<path-to-node_modules>/@fulcrumui/css-utils/scss/modules/margin';

// DON'T

@use '<path-to-node_modules>/@fulcrumui/css-utils/scss/modules/margin/_index.scss';
```

## **Option 3: Everything but the kitchen sink (with config)**

_**NOTE:** This implementation requires you to be using Dart Sass in your development!_

```scss
@use '<path-to-node_modules>/@fulcrumui/css-utils/fulcrum.scss' with (
  // config values here!
);
```

You can now use all of the fulcrumui CSS Utilities with the configuration values that you have provided! You also do not need to include configurations for each utility, as they are set up with default values. So if you want to customize the config values for 1 module, go for it. If you want to change the config values for all of the modules, you can do that too. It's entirely up to you!

## **Option 4: Modular (with config)**

_**NOTE:** This implementation requires you to be using Dart Sass in your development!_

```scss
@use '<path-to-node_modules>/@fulcrumui/css-utils/config' with (
  // config values here for the modules you want to change here!
);
@use '<path-to-node_modules>/@fulcrumui/css-utils/modules/margin';
// any other modules that you would like to use

// Then be sure to include the module you would want to use

@include margin.margins;
```

You can now use the fulcrumui CSS Utility you've included with the configuration values that you have provided! You only need to add the configuration **once**. It is also important to note that you **need to include the configuration before you include any of the fulcrumui CSS Utility modules**.
