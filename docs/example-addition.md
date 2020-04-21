# Example of a Modular implementation with a configuration

```scss
@use './config' with (
  $MARGINS: (
    'start': 10,
    'end': 30,
    'incrementBy': 5,
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

> **Important!!!**
>
> To ensure that Fulcrum UI CSS Utilities are able to override any styles that you have defined elsewhere, make sure that your `@use`  statements referencing fuclrumui are placed last in your `@use` group!
