# Grid Layout Module

Kiss Bootstrap goodbye 💋👋. This is another of the more powerful modules in the Fulcrum UI CSS Utilities toolkit. Fulcrum UI's CSS Utilities Grid Layout Moudle provides an easy way to layout your content withing a flexbox based grid system with no nonsense. You can choose granular control or simply apply 1 class to your parent and 1 class to your child to get the desired layout.

## Usage

> It is recommended to utilize the flex modules as much as possible, however if your application still uses floats this module can come in handy

### Included in core: ✅

### For modular setups:

```scss
@use '<path-to-node_modules>/@fulcrumui/css-utils/scss/modules/element-floats';
```

### Application

To apply this utility, use the pattern below:

#### Simple application

```html
<element class="u-row">
  <child-element class="u-row__column"></child-element>
  <child-element class="u-row__column"></child-element>
  <child-element class="u-row__column"></child-element>
</element>
```

In the above example the columns will be evenly distributed within the row

#### More granular control

##### No Gutters

If you don't want gutters, simply apply the `m--no-gutters` modifier to the row

```html
<element class="u-row m--no-gutters">
  <child-element class="u-row__column"></child-element>
  <child-element class="u-row__column"></child-element>
  <child-element class="u-row__column"></child-element>
</element>
```

##### Wrapping content in the row

By default the content in the row will not wrap if it overflows the container (ie you have more than the number of columns, or you have an element with a min width and the row shrinks). If you prefer the content to wrap you can simply apply the `m--wrap` modifier to the row.

```html
<element class="u-row m--wrap">
  <child-element class="u-row__column"></child-element>
  <child-element class="u-row__column"></child-element>
  <child-element class="u-row__column"></child-element>
</element>
```

##### Granular control of your columns

> By default all columns will be broken onto the next line and made 100% of the column

```html
<!-- If you want to make the columns to span a certain number of 'columns' -->
<element class="u-row">
  <child-element class="u-row__column m--desktop-3"></child-element>
  <child-element class="u-row__column m--desktop-2"></child-element>
  <child-element class="u-row__column m--desktop-7"></child-element>
</element>

<!-- If you want to offset your element by a certain number of columns -->
<element class="u-row">
  <child-element class="u-row__column m--desktop-3"></child-element>
  <child-element class="u-row__column m--desktop-3 m--desktop-offset-6"></child-element>
</element>

<!-- If you only want to take up as much space as the content of the column -->
<element class="u-row">
  <child-element class="u-row__column m--desktop-auto-width"></child-element>
</element>
```

The syntax for granular configuration is

```html
<element class="u-row">
  <child-element class="u-row__column m--[breakpoint]-[columnValue]"></child-element>
</element>
```

### Options

#### `breakpoint`

Breakpoints are set by default with the config, but they can be adjusted. If you would like to adjust your breakpoints, please see the section on [configuring the $BREAKPOINTS property](breakpoints-configuration.md)

> **NOTE: Configuring the $BREAKPOINTS property for this module will effect the Breakpoints Moudle as well. This is by design to ensure continuity throughout the app on different devices.**

| Option | Description |
| --- | --- |
| `'mobile'` | Will apply the adjustment for the mobile breakpoint <br/> **Default**: null |
| `'tablet'` | Will apply the adjustment for the tablet brekpoint <br/> **Default**: 775px |
| `'desktop'` | Will apply the adjustment for the desktop brekpoint <br/> **Default**: 993px |

#### `columnValue`

The number of 'columns' that you would like the element to span

| Option | Description |
| --- | --- |
| `number` | A number that exists within the number of columns in the config <br/> **Default: 1-12** |

## Configurable ✅
