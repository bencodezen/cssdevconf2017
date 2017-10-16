# Design Systems 2.0: Creating Consistent Interfaces (#designsys2)
*By Micah Godbolt ([@micahgodbolt](https://twitter.com/micahgodbolt)) from Microsoft on October 9th, 2017 @ 4:00PM* - [Slides](http://bit.ly/designsys2)

## Description

HTML and CSS are all you need to create a Design System that unifies the visual appearance of your products, but as soon as you want to create consistent behavior between applications, you'll need to turn to JavaScript. More often than not, using a modern framework such as React, Vue, or Angular will save you lots of time, and keep you from reinventing the wheel. 

In this talk, I will discuss how moving interactivity into the Design System is not only a good choice today, but is most certainly how you will be creating Design Systems in the future. I'll also be discussing the React-powered Design System I've been helping to create which powers a few apps you might have heard of, including SharePoint, OneDrive, and Outlook for the web.

## Talk

- A design system should be able to handle any theme you throw at it
- An application adds a whole different layer to a design system since there are states to manage, interactions, etc.
- Making Design Systems Scale
    - One System Multiple Platforms
        - Theo: An abstraction for transforming and formatting Design Tokens. In other words, to rise above the constraints of being in X language and use JSON for instance to store it all in once place.
    - One Platform Multiple Systems
        - Imagine a situation where users want to use one version of a component in the left rail and the same component of a different version in the right rail.
    - CSS Modules
        - Turns your styles into an object that is unique and thus has a unique class name that scopes your styles
- All People
    - One Platform Many Themes
        - Tried using CSS Variables but there is browser support issues which makes it a less than ideal solution
    - One Page Many Themes
        - We don't want to create a system where you need to create styles for every single button to be X color. It'd be tedious to manage and not scalable at all.
        - The solution is runtime styles like CSS in JS (i.e., producing styles on the fly)
            - The shift to consider here is that we've moved from inline styles to style blocks. It doesn't matter where it comes from (i.e., Sass or JS) as long as the end result is true styles with selectors and such.
- All Sites
    - Some sites like to talk with you and interact with you. For example, the OneDrive web interface and selecting folders to do something like download.
    - Building buttons to perform actions on the page
        - Attempt 1: Attach onClick event to look for elements with class `selected` and then it's going to send that thing to the form and then... No good. Too much code. Too many dependencies with how something should work and makes it brittle.
            - Components need to be dumb and allows the application to perform what it needs to perform.
            - The idea behind this reminds me of declarative programming in that you don't define how it does everything, but simpy what it does and let the application contain the logic to do the rest
            - In other words, similar to how he talked about passing styles into components with dynamic generated styles, we can do something similar with the functionality of a component as well
- Use JSON Schemas to define data schema and serve as documentation
- Talks about TypeScript and how it helps to enforce Schemas
    - Brings up VSCode to show how it makes it easy to use TypeScript
- The answer to Design Systems 2.0 is JavaScript
    - Does this mean you need to become a JS rockstar? Absolutely not. Never forget that when you build an application of this magnitude, you are part of a team.

## Memorable Quotes

> "A Design System is a set of rules and assets that define how to express everything a visual language needs to say" - Micah Godbolt

> "Writing the correct CSS once is pretty easy. Making the CSS work in all situations, and for all people is the hard part." - Micah Godbolt

> "Telling someone they need to configure their build pipeline a certain way in order to use your product is a huge turn off." - Micah Godbolt

> "JavaScript is not replacing HTML and CSS. It is simply making it more powerful." - Micah Godbolt

> "We need to find the ways that JavaScript that power the things we love." - Micah Godbolt

## Presentation Notes

- Something about a slide with a single tweet gives it a lot of prominence and authority

## Resources

- [Micah's Slides](http://bit.ly/designsys2)
- [Design Tokens](https://developer.salesforce.com/docs/atlas.en-us.lightning.meta/lightning/tokens_intro.htm)

