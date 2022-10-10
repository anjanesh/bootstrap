---
layout: docs
title: Color
description: Bootstrap is supported by an extensive color system that themes our styles and components. This enables more comprehensive customization and extension for any project.
group: customize
toc: true
---

## Colors

{{< added-in "5.3.0" >}}

Bootstrap's color palette has continued to expand and become more nuanced in v5.3.0. We've added new variables for `secondary` and `tertiary` text and background colors, plus `{color}-bg-subtle`, `{color}-border-subtle`, and `{color}-text` for our theme colors. These new colors are available through Sass and CSS variables (but not our color maps or utility classes) with the express goal of making it easier to customize across multiple colors modes like light and dark. These new variables are globally set on `:root` and are adapted for our new dark color mode while our original theme colors remain unchanged.

Colors ending in `-rgb` provide the `red, green, blue` values for use in `rgb()` and `rgba()` color modes. For example, `rgba(var(--bs-secondary-bg-rgb), .5)`.

{{< callout warning>}}
**Heads up!** There's some potential confusion with our new secondary and tertiary colors, and our existing secondary theme color, as well as our light and dark theme colors. Expect this to be ironed out in v6.
{{< /callout >}}

<table class="table table-swatches">
  <thead>
    <tr>
      <th style="width: 340px;">Description</th>
      <th style="width: 200px;" class="ps-0">Swatch</th>
      <th>Variables</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="2">
        <strong>Body —</strong> Default foreground (color) and background, including components.
      </td>
      <td class="ps-0">
        <div class="p-3 rounded-2" style="background-color: var(--bs-body-color);">&nbsp;</div>
      </td>
      <td>
        {{< markdown >}}`--bs-body-color`<br>`--bs-body-color-rgb`{{< /markdown >}}
      </td>
    </tr>
    <tr>
      <td>
        <div class="p-3 rounded-2 border" style="background-color: var(--bs-body-bg);">&nbsp;</div>
      </td>
      <td>
        {{< markdown >}}`--bs-body-bg`<br>`--bs-body-bg-rgb`{{< /markdown >}}
      </td>
    </tr>
    <tr>
      <td rowspan="2">
        <strong>Secondary —</strong> For disabled component states, dividers, and lighter text.
      </td>
      <td class="ps-0">
        <div class="p-3 rounded-2" style="background-color: var(--bs-secondary-color);">&nbsp;</div>
      </td>
      <td>
        {{< markdown >}}`--bs-secondary-color`<br>`--bs-secondary-color-rgb`{{< /markdown >}}
      </td>
    </tr>
    <tr>
      <td>
        <div class="p-3 rounded-2 border" style="background-color: var(--bs-secondary-bg);">&nbsp;</div>
      </td>
      <td>
        {{< markdown >}}`--bs-secondary-bg`<br>`--bs-secondary-bg-rgb`{{< /markdown >}}
      </td>
    </tr>
    <tr>
      <td rowspan="2">
        <strong>Tertiary —</strong> For component hover colors, accents, wells, and text.
      </td>
      <td class="ps-0">
        <div class="p-3 rounded-2" style="background-color: var(--bs-tertiary-color);">&nbsp;</div>
      </td>
      <td>
        {{< markdown >}}`--bs-tertiary-color`<br>`--bs-tertiary-color-rgb`{{< /markdown >}}
      </td>
    </tr>
    <tr>
      <td>
        <div class="p-3 rounded-2 border" style="background-color: var(--bs-tertiary-bg);">&nbsp;</div>
      </td>
      <td>
        {{< markdown >}}`--bs-tertiary-bg`<br>`--bs-tertiary-bg-rgb`{{< /markdown >}}
      </td>
    </tr>
    <tr>
      <td>
        <strong>Emphasis —</strong> For higher contrast text. Not applicable for backgrounds.
      </td>
      <td class="ps-0">
        <div class="p-3 rounded-2" style="background-color: var(--bs-emphasis-color);">&nbsp;</div>
      </td>
      <td>
        {{< markdown >}}`--bs-emphasis-color`<br>`--bs-emphasis-color-rgb`{{< /markdown >}}
      </td>
    </tr>
    <tr>
      <td>
        <strong>Border —</strong> {{< markdown >}}For component borders, dividers, and rules. Use `--bs-border-color-translucent` to blend with backgrounds with an `rgba()` value.{{< /markdown >}}
      </td>
      <td class="ps-0">
        <div class="p-3 rounded-2" style="background-color: var(--bs-border-color);">&nbsp;</div>
      </td>
      <td>
        {{< markdown >}}`--bs-border-color`<br>`--bs-border-color-rgb`{{< /markdown >}}
      </td>
    </tr>
    <tr>
      <td rowspan="4">
        <strong>Primary —</strong> Main theme color, used for hyperlinks, focus styles, and component and form active states.
      </td>
      <td class="ps-0">
        <div class="p-3 rounded-2 text-bg-primary">Primary</div>
      </td>
      <td>
        {{< markdown >}}`--bs-primary`<br>`--bs-primary-rgb`{{< /markdown >}}
      </td>
    </tr>
    <tr>
      <td>
        <div class="px-3 py-2 rounded-2 border" style="background-color: var(--bs-primary-bg-subtle); --bs-border-color: var(--bs-primary-border-subtle); color: var(--bs-primary-text);">Background subtle</div>
      </td>
      <td>
        {{< markdown >}}`--bs-primary-bg-subtle`{{< /markdown >}}
      </td>
    </tr>
    <tr>
      <td>
        <div class="px-3 py-2 rounded-2" style="background-color: var(--bs-primary-border-subtle); color: var(--bs-primary-text);">Border subtle</div>
      </td>
      <td>
        {{< markdown >}}`--bs-primary-border-subtle`{{< /markdown >}}
      </td>
    </tr>
    <tr>
      <td>
        <div class="px-3 py-2 rounded-2" style="background-color: var(--bs-primary-text); color: var(--bs-body-bg);">Text</div>
      </td>
      <td>
        {{< markdown >}}`--bs-primary-text`{{< /markdown >}}
      </td>
    </tr>
    <tr>
      <td rowspan="4">
        <strong>Success —</strong> Theme color used for positive or successful actions and information.
      </td>
      <td class="ps-0">
        <div class="p-3 rounded-2 text-bg-success">Success</div>
      </td>
      <td>
        {{< markdown >}}`--bs-success`<br>`--bs-success-rgb`{{< /markdown >}}
      </td>
    </tr>
    <tr>
      <td>
        <div class="px-3 py-2 rounded-2 border" style="background-color: var(--bs-success-bg-subtle); --bs-border-color: var(--bs-success-border-subtle); color: var(--bs-success-text);">Background subtle</div>
      </td>
      <td>
        {{< markdown >}}`--bs-success-bg-subtle`{{< /markdown >}}
      </td>
    </tr>
    <tr>
      <td>
        <div class="px-3 py-2 rounded-2" style="background-color: var(--bs-success-border-subtle); color: var(--bs-success-text);">Border subtle</div>
      </td>
      <td>
        {{< markdown >}}`--bs-success-border-subtle`{{< /markdown >}}
      </td>
    </tr>
    <tr>
      <td>
        <div class="px-3 py-2 rounded-2" style="background-color: var(--bs-success-text); color: var(--bs-body-bg);">Text</div>
      </td>
      <td>
        {{< markdown >}}`--bs-success-text`{{< /markdown >}}
      </td>
    </tr>
    <tr>
      <td rowspan="4">
        <strong>Danger —</strong> Theme color used for errors and dangerous actions.
      </td>
      <td class="ps-0">
        <div class="p-3 rounded-2 text-bg-danger">Danger</div>
      </td>
      <td>
        {{< markdown >}}`--bs-danger`<br>`--bs-danger-rgb`{{< /markdown >}}
      </td>
    </tr>
    <tr>
      <td>
        <div class="px-3 py-2 rounded-2 border" style="background-color: var(--bs-danger-bg-subtle); --bs-border-color: var(--bs-danger-border-subtle); color: var(--bs-danger-text);">Background subtle</div>
      </td>
      <td>
        {{< markdown >}}`--bs-danger-bg-subtle`{{< /markdown >}}
      </td>
    </tr>
    <tr>
      <td>
        <div class="px-3 py-2 rounded-2" style="background-color: var(--bs-danger-border-subtle); color: var(--bs-danger-text);">Border subtle</div>
      </td>
      <td>
        {{< markdown >}}`--bs-danger-border-subtle`{{< /markdown >}}
      </td>
    </tr>
    <tr>
      <td>
        <div class="px-3 py-2 rounded-2" style="background-color: var(--bs-danger-text); color: var(--bs-body-bg);">Text</div>
      </td>
      <td>
        {{< markdown >}}`--bs-danger-text`{{< /markdown >}}
      </td>
    </tr>
    <tr>
      <td rowspan="4">
        <strong>Warning —</strong> Theme color used for non-destructive warning messages.
      </td>
      <td class="ps-0">
        <div class="p-3 rounded-2 text-bg-warning">Warning</div>
      </td>
      <td>
        {{< markdown >}}`--bs-warning`<br>`--bs-warning-rgb`{{< /markdown >}}
      </td>
    </tr>
    <tr>
      <td>
        <div class="px-3 py-2 rounded-2 border" style="background-color: var(--bs-warning-bg-subtle); --bs-border-color: var(--bs-warning-border-subtle); color: var(--bs-warning-text);">Background subtle</div>
      </td>
      <td>
        {{< markdown >}}`--bs-warning-bg-subtle`{{< /markdown >}}
      </td>
    </tr>
    <tr>
      <td>
        <div class="px-3 py-2 rounded-2" style="background-color: var(--bs-warning-border-subtle); color: var(--bs-warning-text);">Border subtle</div>
      </td>
      <td>
        {{< markdown >}}`--bs-warning-border-subtle`{{< /markdown >}}
      </td>
    </tr>
    <tr>
      <td>
        <div class="px-3 py-2 rounded-2" style="background-color: var(--bs-warning-text); color: var(--bs-body-bg);">Text</div>
      </td>
      <td>
        {{< markdown >}}`--bs-warning-text`{{< /markdown >}}
      </td>
    </tr>
    <tr>
      <td rowspan="4">
        <strong>Info —</strong> Theme color used for neutral and informative content.
      </td>
      <td class="ps-0">
        <div class="p-3 rounded-2 text-bg-info">Info</div>
      </td>
      <td>
        {{< markdown >}}`--bs-info`<br>`--bs-info-rgb`{{< /markdown >}}
      </td>
    </tr>
    <tr>
      <td>
        <div class="px-3 py-2 rounded-2 border" style="background-color: var(--bs-info-bg-subtle); --bs-border-color: var(--bs-info-border-subtle); color: var(--bs-info-text);">Background subtle</div>
      </td>
      <td>
        {{< markdown >}}`--bs-info-bg-subtle`{{< /markdown >}}
      </td>
    </tr>
    <tr>
      <td>
        <div class="px-3 py-2 rounded-2" style="background-color: var(--bs-info-border-subtle); color: var(--bs-info-text);">Border subtle</div>
      </td>
      <td>
        {{< markdown >}}`--bs-info-border-subtle`{{< /markdown >}}
      </td>
    </tr>
    <tr>
      <td>
        <div class="px-3 py-2 h-100 rounded-2" style="background-color: var(--bs-info-text); color: var(--bs-body-bg);">Text</div>
      </td>
      <td>
        {{< markdown >}}`--bs-info-text`{{< /markdown >}}
      </td>
    </tr>
    <tr>
      <td rowspan="4">
        <strong>Light —</strong> Additional theme option for less contrasting colors.
      </td>
      <td class="ps-0">
        <div class="p-3 rounded-2 text-bg-light border">Light</div>
      </td>
      <td>
        {{< markdown >}}`--bs-light`<br>`--bs-light-rgb`{{< /markdown >}}
      </td>
    </tr>
    <tr>
      <td>
        <div class="px-3 py-2 rounded-2 border" style="background-color: var(--bs-light-bg-subtle); --bs-border-color: var(--bs-light-border-subtle); color: var(--bs-light-text);">Background subtle</div>
      </td>
      <td>
        {{< markdown >}}`--bs-light-bg-subtle`{{< /markdown >}}
      </td>
    </tr>
    <tr>
      <td>
        <div class="px-3 py-2 rounded-2" style="background-color: var(--bs-light-border-subtle); color: var(--bs-light-text);">Border subtle</div>
      </td>
      <td>
        {{< markdown >}}`--bs-light-border-subtle`{{< /markdown >}}
      </td>
    </tr>
    <tr>
      <td>
        <div class="px-3 py-2 h-100 rounded-2" style="background-color: var(--bs-light-text); color: var(--bs-body-bg);">Text</div>
      </td>
      <td>
        {{< markdown >}}`--bs-light-text`{{< /markdown >}}
      </td>
    </tr>
    <tr>
      <td rowspan="4">
        <strong>Dark —</strong> Additional theme option for higher contrasting colors.
      </td>
      <td class="ps-0">
        <div class="p-3 rounded-2 text-bg-dark border">Dark</div>
      </td>
      <td>
        {{< markdown >}}`--bs-dark`<br>`--bs-dark-rgb`{{< /markdown >}}
      </td>
    </tr>
    <tr>
      <td>
        <div class="px-3 py-2 rounded-2 border" style="background-color: var(--bs-dark-bg-subtle); --bs-border-color: var(--bs-dark-border-subtle); color: var(--bs-dark-text);">Background subtle</div>
      </td>
      <td>
        {{< markdown >}}`--bs-dark-bg-subtle`{{< /markdown >}}
      </td>
    </tr>
    <tr>
      <td>
        <div class="px-3 py-2 rounded-2" style="background-color: var(--bs-dark-border-subtle); color: var(--bs-dark-text);">Border subtle</div>
      </td>
      <td>
        {{< markdown >}}`--bs-dark-border-subtle`{{< /markdown >}}
      </td>
    </tr>
    <tr>
      <td>
        <div class="px-3 py-2 h-100 rounded-2" style="background-color: var(--bs-dark-text); color: var(--bs-body-bg);">Text</div>
      </td>
      <td>
        {{< markdown >}}`--bs-dark-text`{{< /markdown >}}
      </td>
    </tr>
  </tbody>
</table>

### Using the new colors

These new colors are accessible via CSS variables and utility classes—like `--bs-primary-bg-subtle` and `.bg-primary-subtle`—allowing you to compose your own CSS rules with the variables, or to quickly apply styles via classes. The utilities are built with the color's associated CSS variables, and since we customize those CSS variables for dark mode, they are also adaptive to color mode by default.

{{< example >}}
<div class="p-3 text-primary-emphasis bg-primary-subtle border border-primary-subtle rounded-3">
  Example element with utilities
</div>
{{< /example >}}

### Theme colors

We use a subset of all colors to create a smaller color palette for generating color schemes, also available as Sass variables and a Sass map in Bootstrap's `scss/_variables.scss` file.

<div class="row">
  {{< theme-colors.inline >}}
  {{- range (index $.Site.Data "theme-colors") }}
    <div class="col-md-4">
      <div class="p-3 mb-3 text-bg-{{ .name }} rounded-3">{{ .name | title }}</div>
    </div>
  {{ end -}}
  {{< /theme-colors.inline >}}
</div>

All these colors are available as a Sass map, `$theme-colors`.

{{< scss-docs name="theme-colors-map" file="scss/_variables.scss" >}}

Check out [our Sass maps and loops docs]({{< docsref "/customize/sass#maps-and-loops" >}}) for how to modify these colors.

### All colors

All Bootstrap colors are available as Sass variables and a Sass map in `scss/_variables.scss` file. To avoid increased file sizes, we don't create text or background color classes for each of these variables. Instead, we choose a subset of these colors for a [theme palette](#theme-colors).

Be sure to monitor contrast ratios as you customize colors. As shown below, we've added three contrast ratios to each of the main colors—one for the swatch's current colors, one for against white, and one for against black.

<div class="row font-monospace">
  {{< theme-colors.inline >}}
  {{- range $color := $.Site.Data.colors }}
    {{- if (and (not (eq $color.name "white")) (not (eq $color.name "gray")) (not (eq $color.name "gray-dark"))) }}
    <div class="col-md-4 mb-3">
      <div class="p-3 mb-2 position-relative swatch-{{ $color.name }}">
        <strong class="d-block">${{ $color.name }}</strong>
        {{ $color.hex }}
      </div>
      {{ range (seq 100 100 900) }}
      <div class="p-3 bd-{{ $color.name }}-{{ . }}">${{ $color.name }}-{{ . }}</div>
      {{ end }}
    </div>
    {{ end -}}
  {{ end -}}

  <div class="col-md-4 mb-3">
    <div class="p-3 mb-2 position-relative swatch-gray-500">
      <strong class="d-block">$gray-500</strong>
      #adb5bd
    </div>
  {{- range $.Site.Data.grays }}
    <div class="p-3 bd-gray-{{ .name }}">$gray-{{ .name }}</div>
  {{ end -}}
  </div>
  {{< /theme-colors.inline >}}

  <div class="col-md-4 mb-3">
    <div class="p-3 mb-2 bd-black text-white">
      <strong class="d-block">$black</strong>
      #000
    </div>
    <div class="p-3 mb-2 bd-white border">
      <strong class="d-block">$white</strong>
      #fff
    </div>
  </div>
</div>

### Notes on Sass

Sass cannot programmatically generate variables, so we manually created variables for every tint and shade ourselves. We specify the midpoint value (e.g., `$blue-500`) and use custom color functions to tint (lighten) or shade (darken) our colors via Sass's `mix()` color function.

Using `mix()` is not the same as `lighten()` and `darken()`—the former blends the specified color with white or black, while the latter only adjusts the lightness value of each color. The result is a much more complete suite of colors, as [shown in this CodePen demo](https://codepen.io/emdeoh/pen/zYOQOPB).

Our `tint-color()` and `shade-color()` functions use `mix()` alongside our `$theme-color-interval` variable, which specifies a stepped percentage value for each mixed color we produce. See the `scss/_functions.scss` and `scss/_variables.scss` files for the full source code.

## Color modes

{{< added-in "5.3.0" >}}

### Dark mode

**Bootstrap now supports color modes, starting with dark mode!** After upgrading to v5.3.0, you'll be able to implement your own color mode toggler (see below for an example from Bootstrap's docs) and apply the different color modes as you see fit. Color modes can be toggled globally on the `<html>` element, or on specific components and elements, thanks to the `data-bs-theme` attribute.

For example, to change the color mode of a dropdown menu, add `data-bs-theme="light"` or `data-bs-theme="dark"` to the parent `.dropdown`. Now, no matter the global color mode, these dropdowns will display as intended.

{{< example class="d-flex justify-content-between" >}}
<div class="dropdown" data-bs-theme="light">
  <button class="btn btn-secondary dropdown-toggle" type="button" id="dropdownMenuButtonLight" data-bs-toggle="dropdown" aria-expanded="false">
    Default dropdown
  </button>
  <ul class="dropdown-menu" aria-labelledby="dropdownMenuButtonLight">
    <li><a class="dropdown-item active" href="#">Action</a></li>
    <li><a class="dropdown-item" href="#">Action</a></li>
    <li><a class="dropdown-item" href="#">Another action</a></li>
    <li><a class="dropdown-item" href="#">Something else here</a></li>
    <li><hr class="dropdown-divider"></li>
    <li><a class="dropdown-item" href="#">Separated link</a></li>
  </ul>
</div>

<div class="dropdown" data-bs-theme="dark">
  <button class="btn btn-secondary dropdown-toggle" type="button" id="dropdownMenuButtonDark" data-bs-toggle="dropdown" aria-expanded="false">
    Dark dropdown
  </button>
  <ul class="dropdown-menu" aria-labelledby="dropdownMenuButtonDark">
    <li><a class="dropdown-item active" href="#">Action</a></li>
    <li><a class="dropdown-item" href="#">Action</a></li>
    <li><a class="dropdown-item" href="#">Another action</a></li>
    <li><a class="dropdown-item" href="#">Something else here</a></li>
    <li><hr class="dropdown-divider"></li>
    <li><a class="dropdown-item" href="#">Separated link</a></li>
  </ul>
</div>
{{< /example >}}

### Nesting color modes

Use `data-bs-theme` on a nested element to change the color mode for a group of elements or components. In the example below, we have an outer dark mode with a nested light mode. You'll notice components naturally adapt their appearance without modification, but the nested `data-bs-theme="light"` needs help to reset some global styles. This is because `data-bs-theme` doesn't reset the globally declared `<body>` colors, so we have to add `.bg-body` and `.text-body`.

{{< example class="" >}}
<div data-bs-theme="dark">
  <nav aria-label="breadcrumb">
    <ol class="breadcrumb">
      <li class="breadcrumb-item"><a href="#">Color modes</a></li>
      <li class="breadcrumb-item active" aria-current="page">Dark</li>
    </ol>
  </nav>

  <p>This should be shown in a <strong>dark</strong> theme at all times.</p>

  <div class="progress mb-4">
    <div class="progress-bar" role="progressbar" aria-label="Basic example" style="width: 25%" aria-valuenow="25" aria-valuemin="0" aria-valuemax="100"></div>
  </div>

  <div class="dropdown mb-4">
    <button class="btn btn-secondary dropdown-toggle" type="button" id="dropdownMenuButtonDark2" data-bs-toggle="dropdown" aria-expanded="false">
      Dark dropdown
    </button>
    <ul class="dropdown-menu" aria-labelledby="dropdownMenuButtonDark2">
      <li><a class="dropdown-item active" href="#">Action</a></li>
      <li><a class="dropdown-item" href="#">Action</a></li>
      <li><a class="dropdown-item" href="#">Another action</a></li>
      <li><a class="dropdown-item" href="#">Something else here</a></li>
      <li><hr class="dropdown-divider"></li>
      <li><a class="dropdown-item" href="#">Separated link</a></li>
    </ul>
  </div>

  <div data-bs-theme="light" class="p-3 bg-body text-body rounded">
    <nav aria-label="breadcrumb">
      <ol class="breadcrumb">
        <li class="breadcrumb-item"><a href="#">Color modes</a></li>
        <li class="breadcrumb-item"><a href="#">Dark</a></li>
        <li class="breadcrumb-item active" aria-current="page">Light</li>
      </ol>
    </nav>

    <p>This should be shown in a <strong>light</strong> theme at all times.</p>

    <div class="progress mb-4">
      <div class="progress-bar" role="progressbar" aria-label="Basic example" style="width: 25%" aria-valuenow="25" aria-valuemin="0" aria-valuemax="100"></div>
    </div>

    <div class="dropdown">
      <button class="btn btn-secondary dropdown-toggle" type="button" id="dropdownMenuButtonLight2" data-bs-toggle="dropdown" aria-expanded="false">
        Light dropdown
      </button>
      <ul class="dropdown-menu" aria-labelledby="dropdownMenuButtonLight2">
        <li><a class="dropdown-item active" href="#">Action</a></li>
        <li><a class="dropdown-item" href="#">Action</a></li>
        <li><a class="dropdown-item" href="#">Another action</a></li>
        <li><a class="dropdown-item" href="#">Something else here</a></li>
        <li><hr class="dropdown-divider"></li>
        <li><a class="dropdown-item" href="#">Separated link</a></li>
      </ul>
    </div>
  </div>
</div>
{{< /example >}}

### Custom color modes

While the primary use case for color modes is light and dark mode, custom color modes are also possible. Create your own `data-bs-theme` selector with a custom value as the name of your color mode, then modify our Sass and CSS variables as needed. We opted to create a separate `_variables-dark.scss` stylesheet to house Bootstrap's dark mode specific Sass variables, but that's not required for you.

For example, you can create a "blue theme" with the selector `data-bs-theme="blue"`. In your custom Sass or CSS file, add the new selector and override any global or component CSS variables as needed. If you're using Sass, you can also use Sass's functions within your CSS variable overrides.

{{< scss-docs name="custom-color-mode" file="site/assets/scss/_content.scss" >}}

<div class="bd-example text-body bg-body" data-bs-theme="blue">
  <div class="h4">Example blue theme</div>
  <p>Some paragraph text to show how the blue theme might look with written copy.</p>

  <hr class="my-4">

  <div class="dropdown">
    <button class="btn btn-secondary dropdown-toggle" type="button" id="dropdownMenuButtonCustom" data-bs-toggle="dropdown" aria-expanded="false">
      Dropdown button
    </button>
    <ul class="dropdown-menu" aria-labelledby="dropdownMenuButtonCustom">
      <li><a class="dropdown-item active" href="#">Action</a></li>
      <li><a class="dropdown-item" href="#">Action</a></li>
      <li><a class="dropdown-item" href="#">Another action</a></li>
      <li><a class="dropdown-item" href="#">Something else here</a></li>
      <li><hr class="dropdown-divider"></li>
      <li><a class="dropdown-item" href="#">Separated link</a></li>
    </ul>
  </div>
</div>

```html
<div data-bs-theme="blue">
  ...
</div>
```

## Color Sass maps

Bootstrap's source Sass files include three maps to help you quickly and easily loop over a list of colors and their hex values.

- `$colors` lists all our available base (`500`) colors
- `$theme-colors` lists all semantically named theme colors (shown below)
- `$grays` lists all tints and shades of gray

Within `scss/_variables.scss`, you'll find Bootstrap's color variables and Sass map. Here's an example of the `$colors` Sass map:

{{< scss-docs name="colors-map" file="scss/_variables.scss" >}}

Add, remove, or modify values within the map to update how they're used in many other components. Unfortunately at this time, not _every_ component utilizes this Sass map. Future updates will strive to improve upon this. Until then, plan on making use of the `${color}` variables and this Sass map.

### Example

Here's how you can use these in your Sass:

```scss
.alpha { color: $purple; }
.beta {
  color: $yellow-300;
  background-color: $indigo-900;
}
```

[Color]({{< docsref "/utilities/colors" >}}) and [background]({{< docsref "/utilities/background" >}}) utility classes are also available for setting `color` and `background-color` using the `500` color values.

## Generating utilities

{{< added-in "5.1.0" >}}

Bootstrap doesn't include `color` and `background-color` utilities for every color variable, but you can generate these yourself with our [utility API]({{< docsref "/utilities/api" >}}) and our extended Sass maps added in v5.1.0.

1. To start, make sure you've imported our functions, variables, mixins, and utilities.
2. Use our `map-merge-multiple()` function to quickly merge multiple Sass maps together in a new map.
3. Merge this new combined map to extend any utility with a `{color}-{level}` class name.

Here's an example that generates text color utilities (e.g., `.text-purple-500`) using the above steps.

```scss
@import "bootstrap/scss/functions";
@import "bootstrap/scss/variables";
@import "bootstrap/scss/maps";
@import "bootstrap/scss/mixins";
@import "bootstrap/scss/utilities";

$all-colors: map-merge-multiple($blues, $indigos, $purples, $pinks, $reds, $oranges, $yellows, $greens, $teals, $cyans);

$utilities: map-merge(
  $utilities,
  (
    "color": map-merge(
      map-get($utilities, "color"),
      (
        values: map-merge(
          map-get(map-get($utilities, "color"), "values"),
          (
            $all-colors
          ),
        ),
      ),
    ),
  )
);

@import "bootstrap/scss/utilities/api";
```

This will generate new `.text-{color}-{level}` utilities for every color and level. You can do the same for any other utility and property as well.
