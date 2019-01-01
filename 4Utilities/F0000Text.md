# Text
## text monospace
```SCSS
.text-monospace { font-family: $font-family-monospace; }

// variables
$font-family-monospace: SFMono-Regular, Menlo, Monaco, Consolas, 
                        "Liberation Mono", "Courier New", monospace !default;
```
## text weight and italic
```SCSS
.font-weight-light  { font-weight: $font-weight-light !important; } // 300
.font-weight-normal { font-weight: $font-weight-normal !important; } // 400
.font-weight-bold   { font-weight: $font-weight-bold !important; } // 700
.font-italic        { font-style: italic !important; }
```
## text alignment
```SCSS
.text-justify  { text-align: justify !important; }

@each $breakpoint in map-keys($grid-breakpoints) {
  @include media-breakpoint-up($breakpoint) {
    $infix: breakpoint-infix($breakpoint, $grid-breakpoints);
    // $infix: ""|sm|md|lg|xl
    .text#{$infix}-left   { text-align: left !important; }
    .text#{$infix}-right  { text-align: right !important; }
    .text#{$infix}-center { text-align: center !important; }
  }
}
```

## text wrap
```SCSS
.text-nowrap{ 
    white-space: nowrap !important; 
}
```

## text truncate
```SCSS
// require `display: block` or `dispaly: inline-block`
.text-truncate { @include text-truncate; }
@mixin text-truncate() {
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
```

## text transform
```SCSS
.text-lowercase  { text-transform: lowercase !important; }
.text-uppercase  { text-transform: uppercase !important; }
.text-capitalize { text-transform: capitalize !important; }
```