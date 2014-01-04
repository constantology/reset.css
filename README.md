# reset.css

my own version of the (un)popular(?) reset.css.

totally untested unproperly and probably unother unthings.

## About

Default font is `10px, Arial` and `rem` units — with an `em` unit fallback — are used throughout.

This means `1[r]em === 10px`, so using something like:

```css

    .my-css-class {
        font-size : 1.6em; font-size : 1.6rem;
        padding   :  .8em; padding   :  .8rem;
        }

    /* equates to: */

    .my-css-class {
        font-size : 16px;
        padding   :  8px;
        }

```

## Recommended

To maintain the `1[r]em === 10px` convenience, **do not** arbitrarily bump up the `font-size` or change the `font-family` of any element.

Instead only change the font `font-size` or change the `font-family` for a specific style.

### Example

```css

/* BAD: you've just made a global "unreset" and are playing with peoples' lives */

    body {
        font-family : 'helvetica neue', helvetica, sans-serif;
        font-size   : 1.2em; font-size : 1.2rem;
        }
    h1, h2, h3, h4 {
        font-family : georgia, "times new roman", serif;
        padding     :  .8em; padding   :  .8rem;
        }
    h1 { font-size  : 2.4em; font-size : 2.4rem; }
    h2 { font-size  : 2em;   font-size : 2rem; }
    h3 { font-size  : 1.6em; font-size : 1.6rem; }
    h4 { font-size  : 1.2em; font-size : 1.2rem; }

/* GOOD: you've not affected the stress levels of anyone else working with the same CSS as you */

    /* applied to any element that has text directly in it, rather than on the body element  */
    .standard-text { 
        font-family : 'helvetica neue', helvetica, sans-serif;
        font-size   : 1.2em; font-size : 1.2rem;
        }

    /* awesome! now we can apply these styles to any element without screwing up the document outline */
    .title-1, .title-2, .title-3, .title-4 {
        font-family : georgia, "times new roman", serif;
        padding     :  .8em; padding   :  .8rem;
        }
    .title-1 { font-size  : 2.4em; font-size : 2.4rem; }
    .title-2 { font-size  : 2em;   font-size : 2rem; }
    .title-3 { font-size  : 1.6em; font-size : 1.6rem; }
    .title-4 { font-size  : 1.2em; font-size : 1.2rem; }

```

## Nicies — or possibly not so nicies(???)
- `.unselectable` disables user selection for an element and its children
- `.selectable` enables user selection for an element and its children
- `.selectable-text` enables user selection of **text only** for an element and its children
- all elements with a `disabled` attribute are automatically assigned the **default cursor** and have **pointer events disabled**
- all button like elements — button, input buttons and any element matching `[role="button"]` — are automatically assigned the **pointer cursor**
- canvas, menu, nav, svg, video, disabled and button like elements have user selection disabled

## File size

- ≅ 1.48kb (gzipped)
- ≅ 3.62kb (unzipped)

## License

(The MIT License)

Copyright (c) 2011 christos "constantology" constandinou http://muigui.com

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the 'Software'), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

![Analytics](https://ga-beacon.appspot.com/UA-15072756-2/constantology/reset.css/readme)
