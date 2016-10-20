# CSS Font Lock
This is a scss mixin used to create CSS locks for responsive typography.

**Demo: [https://alexerlandsson.com/github/css-font-lock/](https://alexerlandsson.com/github/css-font-lock/)**

## What is a CSS lock?
A CSS lock is a technique used to smooth change the font size depending on viewport width between to breakpoints.

## How to use?
Include the mixin in your scss file as follows:

```scss
@include css-font-lock($min-size, $max-size, $min-width, $max-width);
```

Change the variables to desired values in either `px` or `em`. Please not that the output will be presented in px. The mixin contains a calculation of em to px with the default font-size of 16px. However, you can change that base value by include another variable in the mixin with the new value. Example:

```scss
@include css-font-lock($min-size, $max-size, $min-width, $max-width, 14px);
```

## Variables
Variable 			| Description
--------------------| ----------------------------
$min-size			| Font minimum size. Will be displayed on viewport smaller than $min-width.
$max-size			| Font maximum size. Will be displayed on viewport larger than $max-width.
$min-width			| Breakpoint where the font reaches its minimal font size.
$max-width			| Breakpoint where the font reaches its maximum font size.
$base-font-size		| **Optional.** Base font size used to calculate values set in `em`. Default 16px if not passed into the mixin.

## Browser Compatibility
![Chrome](https://github.com/alrra/browser-logos/blob/master/chrome/chrome_64x64.png?raw=true) | ![Safari](https://github.com/alrra/browser-logos/blob/master/safari/safari_64x64.png?raw=true) | ![Firefox](https://github.com/alrra/browser-logos/blob/master/firefox/firefox_64x64.png?raw=true) | ![Opera](https://github.com/alrra/browser-logos/blob/master/opera/opera_64x64.png?raw=true) | ![IE](https://github.com/alrra/browser-logos/blob/master/internet-explorer/internet-explorer_64x64.png?raw=true)
----|-----|-----|-----|-----|
<div align="center">Yes</div> | <div align="center">Yes</div> | <div align="center">Yes</div> | <div align="center">Yes</div> | <div align="center">9*+</div>

## License
The MIT License (MIT)

Copyright (c) 2016 Alexander Erlandsson

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
