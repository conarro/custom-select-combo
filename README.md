custom-select-combo
===========================

![Custom Select Combo Example](https://www.evernote.com/shard/s39/sh/530817b9-3aa0-429b-935b-56c2a61e3311/3d42797ec05ec504b14866048b26078d/deep/0/Screenshot%206/24/13%204:26%20PM.jpg)

Creates a custom input alongside select dropdown to allow custom user input

## Usage

Create a select element:

```html
<select class="custom-select-combo">
  <option value='dog'>Dog</option>
  <option value='cat'>Cat</option>
  <option value='custom'>Custom</option>
</select>
```

And customize it:

```javascript
$('.custom-select-combo').customSelectCombo();
```

## Options

```javascript
$('.custom-select-combo').customSelectCombo({
  alwaysShowInput: false, // show input regardless of selection
  customInputTarget: null, // id of element to attach the custom input to
  hideSelectOnTrigger: false, // if true, hides original select box when trigger options are selected
  inputDimensions: 'auto', // dimensions of the custom input. [width, height], 'default' or 'auto'
  setInputValueOnTrigger: true, // set the value of the input when triggered
  triggerValues: ['custom'], // option values on which to trigger the custom input
  verbose: false // output stuff to console
});
```

Options can be set in the initialization object (as above), or data-attributes can be used:
```html
<select id="example" data-verbose='true' class="custom-select-combo">
  <option value='dog'>Dog</option>
  <option value='cat'>Cat</option>
  <option value='custom'>Custom</option>
</select>
```

For options that trigger the input box, custom values can be set that will be used as the input value instead of the option value:
```html
<select id="example" class="custom-select-combo">
  <option value='dog'>Dog</option>
  <option value='cat'>Cat</option>
  <option value='custom' data-input-value="Some custom value for the input">Custom</option>
</select>
```

## Copyright and license

Copyright (C) 2013 Kyle Conarro

Licensed under the MIT license.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
