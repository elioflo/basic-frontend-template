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

### Useful resources

- [SitePoint](https://www.sitepoint.com/html-forms-constraint-validation-complete-guide/) Post about form validation.
- [w3school](https://www.w3schools.com/) - To consult about doubts that appeared.
- [mdn_](https://developer.mozilla.org/en-US/) - MDN Web Docs has the most up-to-date and accurate information and the content is presented in an easy-to-understand manner. I also like that it's available in many languages (very important!).
- [css-tricks](https://css-tricks.com/) To seek guidance and learn about CSS regarding any doubts or questions that have appeared.
- [SitePoint](https://www.sitepoint.com/html-forms-constraint-validation-complete-guide/) Post about form validation.
- [web.dev](https://web.dev/learn/forms/) A course about HTML forms to help you improve your web developer expertise..
- [w3school](https://www.w3schools.com/) - To consult about doubts that appeared.
- [mdn_](https://developer.mozilla.org/en-US/) - MDN Web Docs has the most up-to-date and accurate information and the content is presented in an easy-to-understand manner. I also like that it's available in many languages (very important!).
- [css-tricks](https://css-tricks.com/) To seek guidance and learn about CSS regarding any doubts or questions that have appeared.
- [w3school](https://www.w3schools.com/) - To consult about doubts that appeared.
- [mdn_](https://developer.mozilla.org/en-US/) - MDN Web Docs has the most up-to-date and accurate information and the content is presented in an easy-to-understand manner. I also like that it's available in many languages (very important!).

## Author

- Frontend Mentor - [@elioflo](https://www.frontendmentor.io/profile/elioflo)
- Twitter - [@7532elioflo](https://twitter.com/7532elioflo)