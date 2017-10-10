# Element-First Design with Context-Aware CSS (#contextcss)
*By Michael Rog ([@MichaelRog](https://twitter.com/michaelrog)) from Build For Humans on October 9th, 2017 @ 11:00AM*

## Description

Typically, "responsive" development is bound to viewport characteristics. Wouldn't it be great if we could style elements to "do the right thing" based on their own width or height, without having to care about the width or height of the browser?

## Talk

- There are three hard problems in computer-science
    - cache invalidation
    - naming things
    - context-aware CSS
- Modern web apps are complicated
    - Deeper component nesting
    - Lots of states
    - Multiple languages
- Wishlist for Modern CSS Developers
    - Support all devices
    - Accommodate user-generated content
    - Enable design agility
    - Produce trustable / maintainable code
- CSS makes bad things easy because...
    - Complicated selectors
    - Gratuitous overrides
- Element-first === no styling through strucuture / ancestry
- We're already moving towards context-aware CSS:
    - `@media`
    - `vw` / `vh` / `vmin`
    - `currentColor
- `currentColor` represents the computed value of the text color based on the context that you are styling
    - You can use it in any place that would normally expect a color value
- In the past, we have been so concerned with viewport, but what we really want is to be responsive to the amount of space available.
- Component should not be concerned with deciding their dimensions. The layout should decide it for them.
- So we need a solution that is...
    - Easy to document
    - Easy to onboard and ensure consistency
    - Easy to grok technically
    - Feels "declarative"
- CONTAINER QUERIES
    - There probably won't be a native way to do so in CSS for a long time because as we're rendering a page, we're rendering styles and layout in a sequence and it can create a circular loop when the layout changes the styles to changes the layout which changes the styles...
    - But we can fake it!
    - Introduces a number of tools found in resources:
        - Prollyfill for CSS CQ
        - CSS Element Queries
        - EQCSS
        - Context Classes
    - The thing to note is that it is a paradigm shift in how we think of styling because it responds to an event instead of viewports. Kind of like async CSS.
- The next steps are...
    -  CSS Modules
        - A cool thing is that not only do we get a single-class / single-use paradigm which makes debugging easier, but we're now writing styles just for that component and near the markup for that component
    - New media queries
        - Check for hover capabilities
        - See spec for more
    - Custom properties (i.e., CSS variables)
        - Provides context for other calculations
        - Examples of usage is theming colors and passing colors down based on theme
    - Resize Observer
        - JS Promise that you can attach to an element and watch whether or not it has changed size / animated / etc.
        - Far off implications are things like Houdini (i.e., write a callback that takes over the entire rendering process and can hijack everything)
- What do we do?
    - Get cozy with the history
    - Use the tech/techniques we have
    - Study the tech that's coming

## Memorable Quotes

> "CSS makes bad things easy." - Michael Rog

> "Element-first means no styling through structure or complicated ancestry" - Michael Rog

> "The more shallow we keep the cascade, the more pleasant our lives will be." - Michael Rog

> "What we really want is for the component to be responsive to the amount of space available." - Micahel Rog

> "The thing to note is that it is a paradigm shift in how we think of styling because it responds to an event instead of viewports. Kind of like async CSS." - Michael Rog

## Presentation Notes

- Good use of "sample code" integrated with humor
- Appreciate the use of history prior to techniques to provide context and appreciation for what the talk is primarily centered on
- Clever use of emoji changing moods in code demo

## Resources

- [Molten Leading by Chris Coyier](https://css-tricks.com/molten-leading-css/)
- [Flexbox + Grid CodePen](https://codepen.io/snookca/pen/LWabjj)
- [Prollyfill for CSS CQ](https://github.com/ausi/cq-prolyfill)
- [CSS Element Queries GitHub](https://github.com/marcj/css-element-queries)
- [EQCSS](http://elementqueries.com/)
- [Context Classes](https://github.com/michaelrog/ContextClasses.js)
- [CSS Modules](https://github.com/css-modules/css-modules)
- [Moar Media Queries!](https://www.w3.org/TR/mediaqueries-4)
- [Resize Observer](https://developers.google.com/web/updates/2016/10/resizeobserver)
