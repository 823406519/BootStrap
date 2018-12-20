[0.0]: #Sizing
# Sizing

## SCSS
```SCSS
//_variables.scss

// This variable affects the `.h-*` and `.w-*` classes.
$sizes: () !default;
// stylelint-disable-next-line scss/dollar-variable-default
$sizes: map-merge(
  (
    25: 25%,
    50: 50%,
    75: 75%,
    100: 100%,
    auto: auto
  ),
  $sizes
);
```

```SCSS
// _size.scss
@mixin size($width, $height: $width) {
  width: $width;
  height: $height;
}
```

```SCSS
// utilitis/_sizing.scss
@each $prop, $abbrev in (width: w, height: h) {
  @each $size, $length in $sizes {
    .#{$abbrev}-#{$size} { #{$prop}: $length !important; }
  }
}

.mw-100 { max-width: 100% !important; }
.mh-100 { max-height: 100% !important; }
```

#### [⬆ Back to top][0.0]
