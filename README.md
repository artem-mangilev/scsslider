# scsslider

## Features

- you could set the delay between slides.
- you could set the time of transition between slides.
- doesn't require JavaScript.

## Instalation

```
npm i scsslider
```

## Use

Basic usage:

```scss
@import "~scsslider"

$image-urls: (
  'https://sitewithimages/image-1',
  'https://sitewithimages/image-1',
  'https://sitewithimages/image-1'
)

.slider-container {
  @include scsslider($image-urls)
}
```

You could play around with other options [here](https://codepen.io/artem-mangilev/pen/yLYONmg).

## Browser support

- Chrome.
- Edge (versions based on Chromium).

## Future plans

- Add support to Firefox and other browsers.
- Improve performance.
