# Order
* Use multiple websites and files in one tab
* Slideshow, feed, custom layouts
* Load items listed in text files or embedded in URL
* Interact by hovering, scrolling, and clicking on active corners
* Sort lists by manually comparing pairs of items
* Single-file portable HTML app

## Examples
*Note control corner buttons*

<!-- Meta example -->

### Web pages
* [Mobile feed](https://nikita-kun.github.io/order/#viewMode=feed&viewStart=1&gallerySize=2&contentOnly=0&title=MobileFeed&url=./intro/example-web.txt)
* [Horizontal tabs](https://nikita-kun.github.io/order/#viewMode=horizontal&viewStart=1&gallerySize=3&contentOnly=0&title=Web&url=./intro/example-web.txt)
* [Gallery](https://nikita-kun.github.io/order/#viewMode=gallery&viewStart=1&gallerySize=3&title=Web&url=./intro/example-web.txt)

### Photo album
* [Widescreen feed](https://nikita-kun.github.io/order/#viewMode=vertical&viewStart=1&gallerySize=2&shuffleInput=1&title=Photos&url=./intro/example-photo.txt)
* [Gallery](https://nikita-kun.github.io/order/#viewMode=gallery&viewStart=1&gallerySize=2&shuffleInput=1&title=Photos&url=./intro/example-photo.txt)
* [Slideshow](https://nikita-kun.github.io/order/#slideshowDelay=15&slideshowStart=1&title=Photos&url=./intro/example-photo.txt)
* [Nested slideshows](https://nikita-kun.github.io/order/#viewStart=1&viewMode=horizontal&gallerySize=3&nested=1&title=NestedSlideshows&input=%23slideshowDelay%3D10%26slideshowStart%3D1%26title%3DPhotos%26url%3D.%2Fintro%2Fexample-photo.txt%0A%23slideshowDelay%3D9%26slideshowStart%3D1%26title%3DPhotos%26url%3D.%2Fintro%2Fexample-photo.txt%0A%23slideshowDelay%3D8%26slideshowStart%3D1%26title%3DPhotos%26url%3D.%2Fintro%2Fexample-photo.txt)

### Screensavers (WebGL, heavy)
* [Slideshow](https://nikita-kun.github.io/order/#slideshowDelay=25&slideshowStart=1&title=Screensaver&url=./intro/example-screensaver.txt)
* [Vertical feed](https://nikita-kun.github.io/order/#viewMode=vertical&viewStart=1&title=Screensaver&url=./intro/example-screensaver.txt)

### Panorama
* [Horizontal](https://nikita-kun.github.io/order/#viewMode=horizontal&viewStart=1&gallerySize=3&shuffleInput=1&title=Panorama&url=./intro/example-panorama.txt)
* [Slideshow](https://nikita-kun.github.io/order/#slideshowDelay=60&slideshowStart=1&viewMode=horizontal&title=Panorama&url=./intro/example-panorama.txt)

### Styling
* [Item CSS styling and item rewriting](https://nikita-kun.github.io/order/#viewStart=1&gallerySize=2&contentOnly=0&url=./intro/example-effect.txt)
<!-- * **custom layout example** -->

### Item sorting
* [Sort numbers](https://nikita-kun.github.io/order/#sortStart=1&shuffleInput=1&viewMode=vertical&gallerySize=10&title=Sort&input=1%0A2%0A3%0A4%0A5%0A6%0A7%0A8%0A9%0A0)
* [Sort tasks](https://nikita-kun.github.io/order/#sortStart=1&shuffleInput=1&viewMode=vertical&gallerySize=10&title=Sort&input=wash%20dishes%0Adinner%0Asleep%0Aleisure%0Awork%0Awalk)
* [Sort photos](https://nikita-kun.github.io/order/#sortStart=1&shuffleInput=1&viewMode=vertical&gallerySize=3&title=Sort&filterInput=a1&url=./intro/example-photo.txt)

### Item input
* [Main menu](https://nikita-kun.github.io/order/)
* [Input list encoded in URL](https://nikita-kun.github.io/order/#input=1%0A2%0A3%0A4%0A5%0A6%0A7%0A8%0A9%0A0)
* [Input lists downloaded from URL](https://nikita-kun.github.io/order/#url=./intro/example-screensaver.txt&url=./intro/example-web.txt)

## Viewer URL parameters
* **title**: Window title
* **input**: Text items and URLs. Newline-separated and URL-encoded
* **url**: Load list from URL-encoded URL. Supports multiple values, `url=URL1&url=URL2`
* **noCache**: Disable URL caching of input lists
* **slideshowShuffle**: Shuffle items in slideshow, if true
* **slideshowDelay**: Delay between slides in slideshow mode
* **slideshowPreTransitionDelay**: Slide fading delay
* **slideshowStart**: Start slideshow on load, if true
* **viewMode**: `gallery`, `horizontal`, `vertical`, or `feed`
* **gallerySize**: Number of items in viewer
* **contentOnly**: Show content of items without header and action buttons, if true
* **viewStart**: Start viewer mode on load, if true
* **nested**: Flip menus and buttons horizontally, useful for nested presentation
* **filterInput**: Keep input items containing substring
* **filterComment**: Keep input items containing comment/tag
* **shuffleInput**: Shuffle input, if true
* **uniqueInput**: Remove duplicates from input, if true
* **lexicInput**: Sort input in lexicographic order, if true
* **excludeInput**: Remove input items containing substring. Supports multiple values, `excludeInput=argon&excludeInput=xenon`
* **prependToInput**: Prepend string to every line of input, supports multiple values
* **appendToInput**: Append string to every line of input, supports multiple values

## Functional tags, append to items after ` symbol
* **noscript**: Load item without javascript
* **flip**: Flip item horizontally
* **randflip**: Flip item horizontally at random
* **spectrum**: Animate item colors, useful for screensavers
* **noslideshow**: Skip item from slideshow
* **nohide**: Disable lazy unloading for item, preserve state
* **slideshowdelay**: Custom slide duration for item
* **container**: Override default container for URL, `container=iframe, container=img, container=object` (website and picture appearance depends on container) 
* **rewrite**: Rewrite item using JS eval, `rewrite?"argon"="alpha"&"xenon"=Math.random()`
* **title**: Override item title
* **link**: Override item link
* **cover**: Override item cover
* **autoplay**: Autoplay video or audio on appearance
* **topnavigation**: Allow item to navigate the top window, disabled by default
* **nocomment**: Hide item comment
* **style**: CSS style item, `style=filter: saturate(0)`
* **styleflex**: CSS style item with details header, useful for custom layouts

## Interface
*Click and scroll on window and tab corners!*

## Considerations
* Some URLs refuse to be displayed, search for embeddable links
* Verify URLs, they may contain arbitrary code

[Source code](https://github.com/nikita-kun/order)
Copyright (c) 2024 [Nikita Korzhitskii](https://nikita-kun.github.io/)
