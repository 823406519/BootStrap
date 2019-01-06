## button
```SCSS
## button
In button.scss
```SCSS
// Future-proof disabling of clicks on `<a>` elements
a.btn.disabled,
fieldset:disabled a.btn {
  pointer-events: none;
}


// Specificity overrides
input[type="submit"],
input[type="reset"],
input[type="button"] {
  &.btn-block {
    width: 100%;
  }
}

```

## card
```SCSS
//
// Header navs
//
.card-header-tabs {
  margin-right: -$card-spacer-x / 2;
  margin-bottom: -$card-spacer-y;
  margin-left: -$card-spacer-x / 2;
  border-bottom: 0;
}

.card-header-pills {
  margin-right: -$card-spacer-x / 2;
  margin-left: -$card-spacer-x / 2;
}


//
// Accordion
//

.accordion {
  .card {
    overflow: hidden;

    &:not(:first-of-type) {
      .card-header:first-child {
        border-radius: 0;
      }

      &:not(:last-of-type) {
        border-bottom: 0;
        border-radius: 0;
      }
    }

    &:first-of-type {
      border-bottom: 0;
      border-bottom-right-radius: 0;
      border-bottom-left-radius: 0;
    }

    &:last-of-type {
      border-top-left-radius: 0;
      border-top-right-radius: 0;
    }

    .card-header {
      margin-bottom: -$card-border-width;
    }
  }
}
```

## carousel
```SCSS
// 1. .carousel.pointer-event should ideally be pan-y (to allow for users to scroll vertically)
//    even when their scroll action started on a carousel, but for compatibility (with Firefox)
//    we're preventing all actions instead
.carousel.pointer-event {
  touch-action: pan-y;
}



//
// Alternate transitions
//

.carousel-fade {
  .carousel-item {
    opacity: 0;
    transition-property: opacity;
    transform: none;
  }

  .carousel-item.active,
  .carousel-item-next.carousel-item-left,
  .carousel-item-prev.carousel-item-right {
    z-index: 1;
    opacity: 1;
  }

  .active.carousel-item-left,
  .active.carousel-item-right {
    z-index: 0;
    opacity: 0;
    @include transition(0s $carousel-transition-duration opacity);
  }
}
```