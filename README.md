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

#### Responsible height disabled auto scroll slides

This [amazing demo](http://www.taboca.com/dd/fullPage.js-master/examples/responsiveHeight.html) disables the slides when window size is smaller then height X.

See the section entitled **Full page and larger-than-full-page sections**.

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

* [Check out gradient-matching background sectins](ttps://github.com/alvarotrigo/fullPage.js#who-is-using-fullpagejs)

* [Double tap/zoom function on mobile devices](http://stackoverflow.com/questions/10614481/disable-double-tap-zoom-option-in-browser-on-touch-devices)

* [Transforming (disabling) mobile doubletap as two clicks](https://gist.github.com/johan/2047491)

### Full page and larger-than-full-page sections

* [When slides data is bigger than screen](http://www.taboca.com/dd/fullPage.js-master/examples/responsiveAutoHeight.html#firstPage) is a case dealing to a condition when the slide content is too big and shows how to disable the whole system. However, it is important to observe that such a mode, of operation, is triggered based in a condition of responsiveness and not based in a user experience need. The trigger is simply the width of the page.

An issue, that should be addressed in this discussion, is to consider the means for knowing when the content is larger than its displaying element that has embedded it.

### Touch pan and auto scrolling

The automatic scrolling can be an issue when the user has a full flexibility to pan, for example with mobile devices. FullPage.js, for example, won’t have a mode of navigation that can support a touch-and-pan (when the user is scrolling with a finger) which could disable the autoScrolling feature.

### Scroll detection and lazy fit-scroll

In Alvaro's [Normal scroll demo](http://www.taboca.com/dd/fullPage.js-master/examples/normalScroll.html) as you position the scroll page to a certain area, it will asynchronously (lazy-fit) the scrollbar so the current section is fit to the full screen size.

This could be interesting, if there was a way for the user to fit, i.e. to disable this easily or flip/tap enable/engage in this as needed.

## Ideas, considerations on standards, cross-browser issues and more

### CSS3 animations and performance

Based in [CSS3 demo from FullPage.js](http://www.taboca.com/dd/fullPage.js-master/examples/css3.html), it seems as a good approach that improves performance in mobile and other devices. Nevertheless, as the frameworks aims to maintain compatibility among browsers, the jQuery Animate is also used.

A consideration is to make an analysis of the jQuery and jQuery animation library extensions, for such cases; therefore to know when/detect the conditions in which JS data can be sent, perhaps dynamically, therefore to establish a managed control on performance versus aimed animation experience.

### Touch-action

https://developer.mozilla.org/en-US/docs/Web/CSS/touch-action#Browser_compatibility https://msdn.microsoft.com/en-us/library/windows/apps/hh767313.aspx lets user manipulates the tag such as pan and zoom, etc.


### Overscroll

The overscroll js library is tiny and enables a user experience behavior which brings animation when user scroll beyond possible, beyond top or beyond bottom of  a page — https://github.com/tholman/overscroll. This won’t work in all browsers but since it’s a IOS thing, the actual experience could lead to something interesting.

* Idea — perhaps double tap to overscroll, or an over over scroll, could move/bring a new section or change how page?

### Considerations about scrollbar

Perfect scrollbar project
https://github.com/noraesae/perfect-scrollbar

### Meta viewport

https://developer.mozilla.org/en/docs/Mozilla/Mobile/Viewport_meta_tag


### Touchstart event for mobile handling


http://stackoverflow.com/questions/24058241/touch-device-single-and-double-tap-events-handler-jquery-javascript


## Other future

### CSS Basic Box Model
https://drafts.csswg.org/css-box-3/#the-width-and-height-properties
