Scrapbook
=========

Useful bits and pieces.


Colour Contrast Functions
-------------------------

Taken from [a Gist by voxpelli](https://gist.github.com/voxpelli/6304812), these functions could be really useful in intelligent theming, so a pattern may be able to adjust it's theme colours if the base colour is very light or dark, for example.

~~~
@function color_luminance($color) {
  // Adapted from: https://github.com/LeaVerou/contrast-ratio/blob/gh-pages/color.js
  // Formula: http://www.w3.org/TR/2008/REC-WCAG20-20081211/#relativeluminancedef
  $rgba: red($color), green($color), blue($color);
  $rgba2: ();

  @for $i from 1 through 3 {
    $rgb: nth($rgba, $i);
    $rgb: $rgb / 255;

    $rgb: if($rgb < .03928, $rgb / 12.92, pow(($rgb + .055) / 1.055, 2.4));

    $rgba2: append($rgba2, $rgb);
  }

  @return .2126 * nth($rgba2, 1) + .7152 * nth($rgba2, 2) + 0.0722 * nth($rgba2, 3);
}

@function color_contrast($color1, $color2) {
  // Adapted from: https://github.com/LeaVerou/contrast-ratio/blob/gh-pages/color.js
  // Formula: http://www.w3.org/TR/2008/REC-WCAG20-20081211/#contrast-ratiodef
  $luminance1: color_luminance($color1) + .05;
  $luminance2: color_luminance($color2) + .05;
  $ratio: $luminance1 / $luminance2;

  @if $luminance2 > $luminance1 {
    $ratio: 1 / $ratio;
  }

  $ratio: round($ratio * 10) / 10;

  @return $ratio;
}
~~~