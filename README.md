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

#### Workarounds with video backgrounds

The recommendation is to have the alternate image.

#### HTML5 video

* [HTML5 video jumpstart examples](http://callmenick.com/post/html5-video-jumpstart-examples)

* [HTML5 video background examples](https://envato.com/blog/video-background-html5-video/)

#### Workaround examples working with mobile

TBD — notice it would need to not use standard video, therefore it would be possible with simply using image, SVG, animated GIFs, and more. But also worth to consider exactly the very reasons for why the auto play is disabled in mobile devices.

Perhaps a better heuristics to this would be for a page to know its bandwidth capability via either depending on feature information provided by the browser user agent, or testing some conditions.

### Updating history and anchor management

TBD

### Looping

From a user experience standpoint, Alvaro Trigo’s fullPage.js library offers two approaches for looping experience. The first refers to when the bottom slide is reached, which moves back to the first, via a scrollbar animation. In another example, then the last slide is reached, it will bring the first at the end — a case referred as a continuous experience.

## Do it all frameworks (UX compound)

* [In development: React and Full page](https://github.com/subtirelumihail/react-fullpage)

* [Reveal.js](https://github.com/hakimel/reveal.js)

* [Alvaro Fullscreenjs](https://github.com/alvarotrigo/fullPage.js)

## UX considerations, issues

* [Check examples of fullscreen sites](https://colorlib.com/wp/fullscreen-html5-website-templates/)

* [Double tap/zoom function on mobile devices](http://stackoverflow.com/questions/10614481/disable-double-tap-zoom-option-in-browser-on-touch-devices)

* [Transforming (disabling) mobile doubletap as two clicks](https://gist.github.com/johan/2047491)

### Full page and larger-than-full-page sections

* [When slides data is bigger than screen](http://www.taboca.com/dd/fullPage.js-master/examples/responsiveAutoHeight.html#firstPage) is a case dealing to a condition when the slide content is too big and shows how to disable the whole system. However, it is important to observe that such a mode, of operation, is triggered based in a condition of responsiveness and not based in a user experience need. The trigger is simply the width of the page.

An issue, that should be addressed in this discussion, is to consider the means for knowing when the content is larger than its displaying element that has embedded it.
