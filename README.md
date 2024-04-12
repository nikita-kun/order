# [Order](https://github.com/nikita-kun/order)
* Display lists of items: images, websites, text, documents
* List items in simple text files
* Layouts: horizontal, vertical, grid, slideshow
* Interact by hovering, scrolling, and clicking on active corners
* Sort lists by manually comparing pairs of items
* Single-file portable HTML app

## Examples 
*Click and scroll on window and tab corners!*

### Web pages
* [Horizontal tabs](https://nikita-kun.github.io/order/#viewMode=horizontal&viewStart=1&gallerySize=3&title=Web&url=./manual/example-web.txt)
* [Horizontal tabs with headers](https://nikita-kun.github.io/order/#viewMode=horizontal&viewStart=1&gallerySize=3&contentOnly=0&title=Web&url=./manual/example-web.txt)
* [Gallery](https://nikita-kun.github.io/order/#viewMode=gallery&viewStart=1&gallerySize=3&title=Web&url=./manual/example-web.txt)

### Photo album
* [Vertical feed](https://nikita-kun.github.io/order/#viewMode=vertical&viewStart=1&gallerySize=2&shuffleInput=1&title=Photos&url=./manual/example-photo.txt)
* [Gallery](https://nikita-kun.github.io/order/#viewMode=gallery&viewStart=1&gallerySize=2&shuffleInput=1&title=Photos&url=./manual/example-photo.txt)
* [Slideshow](https://nikita-kun.github.io/order/#slideshowDelay=15&slideshowStart=1&title=Photos&url=./manual/example-photo.txt)
* [Nested slideshows](https://nikita-kun.github.io/order/#viewStart=1&viewMode=horizontal&gallerySize=3&nested=1&title=NestedSlideshows&input=%23slideshowDelay%3D10%26slideshowStart%3D1%26title%3DPhotos%26url%3D.%2Fmanual%2Fexample-photo.txt%0A%23slideshowDelay%3D9%26slideshowStart%3D1%26title%3DPhotos%26url%3D.%2Fmanual%2Fexample-photo.txt%0A%23slideshowDelay%3D8%26slideshowStart%3D1%26title%3DPhotos%26url%3D.%2Fmanual%2Fexample-photo.txt)

### Screensavers (WebGL, heavy)
* [Slideshow](https://nikita-kun.github.io/order/#slideshowDelay=25&slideshowStart=1&title=Screensaver&url=./manual/example-screensaver.txt)
* [Vertical feed](https://nikita-kun.github.io/order/#viewMode=vertical&viewStart=1&title=Screensaver&url=./manual/example-screensaver.txt)

### Panorama
* [Horizontal](https://nikita-kun.github.io/order/#viewMode=horizontal&viewStart=1&gallerySize=3&shuffleInput=1&title=Panorama&url=./manual/example-panorama.txt)
* [Slideshow](https://nikita-kun.github.io/order/#slideshowDelay=60&slideshowStart=1&viewMode=horizontal&title=Panorama&url=./manual/example-panorama.txt)

### Item sorting
* [Sort numbers](https://nikita-kun.github.io/order/#sortStart=1&shuffleInput=1&viewMode=vertical&gallerySize=10&title=Sort&input=1%0A2%0A3%0A4%0A5%0A6%0A7%0A8%0A9%0A0)
* [Sort tasks](https://nikita-kun.github.io/order/#sortStart=1&shuffleInput=1&viewMode=vertical&gallerySize=10&title=Sort&input=wash%20dishes%0Adinner%0Asleep%0Aleisure%0Awork%0Awalk)
* [Sort photos](https://nikita-kun.github.io/order/#sortStart=1&shuffleInput=1&viewMode=vertical&gallerySize=5&title=Sort&filterComment=close&url=./manual/example-photo.txt)

### Other
* [Main menu](https://nikita-kun.github.io/order/)
* [Item CSS styling and item rewriting](https://nikita-kun.github.io/order/#viewStart=1&gallerySize=5&contentOnly=0&url=./manual/example-effect.txt)
* [Input list encoded in URL](https://nikita-kun.github.io/order/#input=1%0A2%0A3%0A4%0A5%0A6%0A7%0A8%0A9%0A0)
* [Input lists downloaded from URL](https://nikita-kun.github.io/order/#url=./manual/example-screensaver.txt&url=./manual/example-web.txt)

## Viewer URL parameters
* **title**: Window title
* **input**: Text items and URLs. Newline-separated and URL-encoded
* **url**: Load list from URL-encoded URL. Supports multiple values, `url=URL1&url=URL2`
* **slideshowShuffle**: Shuffle items in slideshow, if true
* **slideshowDelay**: Delay between slides in slideshow mode
* **slideshowPreTransitionDelay**: Slide fading delay
* **slideshowStart**: Start slideshow on load, if true
* **viewMode**: `gallery`, `horizontal`, or `vertical`
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
* **appendToInput**: Append string to every line of input, supports multiple values

## Functional tags, append to items after ` symbol
* **flip**: Flip item horizontally
* **randflip**: Flip item horizontally at random
* **spectrum**: Animate item colors, useful for screensavers
* **noslideshow**: Skip item from slideshow
* **nohide**: Disable lazy unloading for item, preserve state
* **slideshowdelay**: Custom slide duration for item
* **container**: Set HTML container for URL, `container=iframe, container=img`
* **rewrite**: Rewrite item using JS eval, `rewrite?"argon"="alpha"&"xenon"=Math.random()`
* **style**: CSS style item, `style=filter: saturate(0)`
* **styleflex**: CSS style item with details header, useful for custom layouts

## Considerations
* Some URLs refuse to be displayed, search for embeddable links
* Verify input: URLs and item lists may contain arbitrary code

[Source code](https://github.com/nikita-kun/order)
Copyright (c) 2024 Nikita Korzhitskii
