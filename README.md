# Carousel for Angular

<img src="https://badgen.net/bundlephobia/min/angular-responsive-carousel" />

A simple solution for horizontal scrolling images with lazy loading.

Live demo can be found on [home page](http://ivylab.space/carousel).

## Installation

Install the npm package.
```
  npm i angular-responsive-carousel
```
Import module:
```ts
  import {IvyCarouselModule} from 'angular-responsive-carousel';

  @NgModule({
      imports: [IvyCarouselModule]
  })
```

## Usage
Put the contents of your cells in containers with the `carousel-cell` class.

```html
<carousel>
    <div class="carousel-cell">
        <img src="path_to_image">
    </div>
    <div class="carousel-cell">
        ...
</carousel>
```

Or prepare an image array for the carousel. If necessary, specify in the settings the sizes of the cells and the carousel container. And also select the method of arranging images inside the cells using the objectFit property.

```html
<carousel
    [images]="images">
</carousel>
```
```ts
images = [
    {path: 'PATH_TO_IMAGE'},
    ...
]
```

## Properties

| name | type | default | description |
|------|------|---------|-------------|
| height | number | | Carousel height. |
| width | number | | Carousel Width. |
| cellWidth | number, '100%' | 200 | Cell width. |
| loop | boolean | false | Infinite loop. |
| autoplay | boolean | false | Automatically start the carousel after initialization. |
| autoplayInterval | number | 5000 | The interval between scrolling the carousel. Used together with autoplay. |
| pauseOnHover | boolean | true | Stops autoplay if the cursor is over the carousel area. |
| dots | boolean | false | Carousel progress bar. |
| overflowCellsLimit | number | 3 | The number of carousel cells that will be stored for in the DOM tree outside the scope. |
| margin | number | 10 | Cell spacing. |
| minSwipeDistance | number | 50 | Minimum distance for swipe. |
| transitionDuration | number | 200 | Animation duration. |
| transitionTimingFunction | 'ease', 'ease-in', 'ease-out', 'ease-in-out', 'linear' | 'ease' | Smooth animation function. |
| counter | boolean | false | Counter. |
| counterSeparator | string | " / " | Counter separator. |
| borderRadius | number | 0 | Border radius for carousel cells. |
| arrows | boolean | true | Arrows for image navigation. |
| arrowsOutside | boolean | false | Arrows on the outside of the carousel container. |
| arrowsTheme | 'light', 'dark' | 'light' | Arrow color theme. |

## Browser support

IvyCarousel supports the most recent two versions of all major browsers: Chrome (including Android 4.4-10), Firefox, Safari (including iOS 9-13), and Edge.