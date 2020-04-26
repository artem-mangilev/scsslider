# scsslider

This is the scss mixin which simplifies creating of background image slideshow.

## Features

- you could set the delay between slides.
- you could set the time of transition between slides.
- you could put some content above the slider.
- you could put some slide-specific content.
- doesn't require JavaScript.

## Instalation

```
npm i scsslider
```

## Parameters

```scss
  @include scsslider(
    $image-urls, // a list of image urls which will be shown
    $slide-animation-time, // an animation time of slide (in seconds) from invisible state to visible or vice versa. Default: 2
    $delay, // delay between slides (in seconds). Default: 3
    $timing-function // timing function which will be applied to each slide. Supported values: ease-in-out. Default: ease-in-out
  )
```

## Basic usage

`scssslider` expects the following markup:

```pug
// this is the element which holds scsslider stuff, it could have whatever name you want
.slider
  // put your static content which will be shown above the slider in element with this class
  .slider-content
  // put your slides in element with this class
  .slides-container
    // element with this class represents a single slide. It could store some content too.
    .slide
    .slide
    .slide
```

Here is the way to initialize `scsslider` from scss:

```scss
@import "~scsslider"

// A number of images should match a number of .slide elements in order to
// display correctly 
$image-urls: (
  'https://sitewithimages.com/image-1.png',
  'https://sitewithimages.com/image-1.png',
  'https://sitewithimages.com/image-1.png'
)

.slider {
  @include scsslider($image-urls)
}
```

You could play around with other options [here](https://codepen.io/artem-mangilev/pen/GRpmEay).

## Browser support

- Chrome.
- Edge (versions based on Chromium).
- Firefox.

## Future plans

- If it possible, unbind a number of images urls from a number of `.slide` elements.
- Add support for `<img>`
