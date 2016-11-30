[![Build Status](https://travis-ci.org/tmcw/wcag-contrast.svg)](https://travis-ci.org/tmcw/wcag-contrast)

## wcag color constrast

[WCAG](http://www.w3.org/WAI/intro/wcag.php) [contrast ratio](http://www.w3.org/TR/WCAG20/#contrast-ratiodef)
measurement and scoring.

### API

<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

#### luminance

Get the contrast ratio between two relative luminance values

**Parameters**

-   `a` **[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** luminance value
-   `b` **[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** luminance value

Returns **[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** contrast ratio

#### rgb

Get a score for the contrast between two colors as rgb triplets

**Parameters**

-   `a` **[array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)** 
-   `b` **[array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)** 

Returns **[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** contrast ratio

#### hex

Get a score for the contrast between two colors as hex strings

**Parameters**

-   `a` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** hex value
-   `b` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** hex value

Returns **[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** contrast ratio

#### score

Get a textual score from a numeric contrast value

**Parameters**

-   `contrast` **[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** 

Returns **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** score

### `luminance(a, b)`

Return contrast as a numeric ratio given two relative luminances

### `rgb(a, b)`

Return contrast as a numeric ratio given two rgb triplets

### `hex(a, b)`

Return contrast as a numeric ratio given two hex values

### `score(contrast)`

Return score in ('AAA', 'AA', '') given contrast ratio as number.

### example

```js
var contrast = require('wcag-contrast');
var ratio = contrast.rgb([0, 0, 0], [255, 255, 255]); // is 21
var score = contrast.score(ratio); // is 'AAA'
```
