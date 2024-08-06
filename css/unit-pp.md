
# ``pp`` Unit

In CSS, [a pixel (in)famously is not a pixel](https://www.quirksmode.org/blog/archives/2010/04/a_pixel_is_not.html). There are (good) reasons for that, but sometimes, authors may wish to use the actual device pixel, or in other words, the physically smallest possible unit.

I therefore propose the ``pp`` unit, short for physical pixel. This unit would correspond to the device pixel, or in other words, the standard CSS pixel divided by the device pixel ratio.

## Use cases

Take my [×5](https://x5.acjs.net/) typeface microsite for example. Images there tend to be rather large (5008 by 5008 pixels), and at the same time very detailed, with every detail being equally important. In order to display these images as best as possible—especially on smaller screens—I want the images to be as small as possible, _without_ loosing any details as a product of re-rasterization.

Another project that would benefit from a unit like this is [allRGB](https://allrgb.com/), where images have a rather large number of pixels (16,777,216), and every pixel being displayed correctly is more important than whether the presented size correlates to other units on the website, like font sizes.

## Polyfill

This unit can currently be achieved with a combination of CSS variables and calculations, and a line of JavaScript.

```css
:root {
    --dpr: 1;
}

.example {
    width: calc(10px / var(--dpr));
}
```
```js
document.documentElement.style.setProperty('--dpr', window.devicePixelRatio);
```

However, the JavaScript has to run after the stylesheet already has laded, and this can cause the layout to "jump" on load. A ``pp`` unit native to the Web browser, would not have this problem.