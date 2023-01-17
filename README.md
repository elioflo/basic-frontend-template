### Media query mixin usage example

Responsive breakpoints are declare in `_variables.scss`

```scss
$min-tablet: 426px;
$min-laptop: 769px;
$min-desktop: 1025px;
$tablet: "(min-width: #{$min-tablet})";
$laptop: "(min-width: #{$min-laptop})";
$desktop: "(min-width: #{$min-desktop})";
```

and `_mixin.scss`

```scss
@mixin media-query($query) {
    @media #{$query} {
        @content;
    }
}
```
Using mixin

```scss
@import 'variables';
@import 'mixins';

.box {
  width: calc(100% - 2em);
  height: 500px;
  background-color: grey;
  border: 1px solid black;
  margin: auto;

  @include media-query($tablet) {
    width: calc(100% - 4em);
    background-color: greenyellow;
    border: 1px solid black;
  }

  @include media-query($laptop) {
    width: calc(100% - 6em);
    background-color: yellow;
    border: 1px solid black;
  }

  @include media-query($desktop) {
    width: calc(100% - 8em);
    background-color: blue;
    border: 1px solid black;
  }
}
```