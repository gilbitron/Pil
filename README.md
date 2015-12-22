# Pil
A simple Javascript library for progressive image loading. Based on
[Medium's progressive image loading](https://jmperezperez.com/medium-image-progressive-loading-placeholder/) technique.

### Usage

Your images will need a wrapper with the `pil` class:

```html
<figure class="pil">
    <img src="img/my-image.jpg" data-full-width="5616" data-full-height="3744" alt="">
</figure>
```

You will also need to add `data-full-width` and `data-full-height` attributes to your images so the lib can calculate the aspect ratio.

Next **you will need to create the thumbnail image** that will be loaded before the main image is loaded. By default it will be loaded
with a `-thumb` postfix. So for example if your image URL is `img/my-image.jpg` the thumb URL will be `img/my-image-thumb.jpg`, however
this can be overridden by providing a URL in the `data-pil-thumb-url` attribute.

Thumbnail images should be no larger than 100px. Jpegs should be no more than 20% quality.

Finally you can initiate Pil by calling:

```js
Pil.init();
```

## Browsers

Pil has been tested on:

* Chrome
* Firefox
* Safari (Desktop + Mobile)
* Opera
* IE9+

## Contribute

So you want to help out? That's awesome. Here is how you can do it:

* [Report a bug](https://github.com/gilbitron/Pil/labels/bug)
* [Ask for a feature](https://github.com/gilbitron/Pil/labels/enhancement)
* [Submit a pull request](https://github.com/gilbitron/Pil/pulls)

If you are submitting a pull request please adhere to the existing coding standards used throughout the code
and only submit **1 feature/fix per pull request**. Pull requests containing multiple changes will be rejected.

## Credits

Pil was created by [Gilbert Pellegrom](http://gilbert.pellegrom.me) from
[Dev7studios](http://dev7studios.com). Released under the [MIT license](https://raw.githubusercontent.com/gilbitron/Pil/master/LICENSE).
