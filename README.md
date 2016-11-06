# html-page-future-review

## One page

### Concept: one page scroll experience

### One page scroll libraries

* [One Page Scroll](https://github.com/peachananr/onepage-scroll)

## General

* [The future of blogging](https://www.elegantthemes.com/blog/editorial/the-future-of-blogging)

## Aspects

### Static / adjusting section height or full screen sections

* [Maje full screen sections with 1 line of CSS](https://medium.com/@ckor/make-full-screen-sections-with-1-line-of-css-b82227c75cbd#.fpuxlqwdk)
* [Using jQuery to adjust height dynamically](http://jsfiddle.net/senff/WdF89/1/
)
* [Stretching a section of a page to full height and width](https://css-tricks.com/forums/topic/stretch-a-section-of-page-to-full-height-and-width/)


### Dynamic / animations over visible sections

* [Alvaro Trigo's callback example](http://www.taboca.com/dd/fullPage.js-master/examples/callbacks.html) shows how animation, and other JavaScript behaviour, can be triggered when the section becomes viewed.

### Responsiveness

TBD  

### Fixed fullscreen background

In Alvaro Trigo’s fullPage, the [Fixed Fullscreen Background example](http://alvarotrigo.com/fullPage/examples/backgrounds.html) will bring a new slide that has a fixed background.  

### Managed scrolling

#### Always fixed elements (fixed header and footer)

Fixing header, or footer, is a common use case — see Alvaro's demo oon Fixed Header](http://alvarotrigo.com/fullPage/examples/fixedHeaders.html).

#### Fixing content as the user scrolls

* [Scroll-Then-Fix Content](https://css-tricks.com/scroll-fix-content/) uses a search top bar demonstration to show the general idea which depends on maintaining two states when the user scrolls down the page. A main, top-level larger search is first displayed, and, as the scrollbar position passes certain threshold, then a JavaScript function switches the stage of an element using DOM CSS operations.

* TBD Check if **Scrolling with fixed content** is the same thing — the case in which you are navigating (say) slides when suddenly some parts of the page gets fixed, til a further slide section down the page.

#### Managing scrollbar animation speed

In many modern pages, the behaviour of scroll is being modified. In Alvaro Trigo’s fullPage.js, the demos related are: [Easing demo](http://www.taboca.com/dd/fullPage.js-master/examples/easing.html) and [Scrolling speed](http://www.taboca.com/dd/fullPage.js-master/examples/scrollingSpeed.html).  

#### Disabling scrollbar animation controls dynamically

Alvaro Trigo’s One Section example shows how to isolate a given section out of the full page behaviour, which can be a desired use case to provide the standard scrollbar behaviour. From the documentation, he claims “Just place the rest of your page after the fullpage wrapper and use the option `fitToSection:false` and `autoScrolling:false`. And enjoy a great single slider.”

[Full Page example with the normal scrollbar behaviour](http://alvarotrigo.com/fullPage/examples/normalScroll.html#firstPage)


### Parallax

* [On theory of pure CSS parallax](http://keithclark.co.uk/articles/pure-css-parallax-websites/)

* [UX considerations: parallax attention getter or headache](UX considerations
)

* [Simple parallax demo](http://keithclark.co.uk/articles/pure-css-parallax-websites/demo1/)


* [Overview of parallax and wordpress](https://www.elegantthemes.com/blog/resources/wordpress-parallax-effect) 2014

### Video backgrounds

#### Video backgrounds not working on mobile - and UX considerations

Alvaro Trigo’s fullPage.js provides a great example of animated video background. This
Framework, as many others, recognises the [issue of video backgrounds](https://github.com/alvarotrigo/fullPage.js/issues/1903) not being enabled in mobile devices.

The disabled video backgrounds started with IOS and has to do with bandwidth and UX considerations. Also, in Android, after 4.1+, based in [this post](https://www.aerserv.com/why-does-video-autoplay-on-mobile-devices-not-work). Therefore, such issue is not related specifically to video backgrounds and it’s simply related to the autoplay feature of videos. 
