# Best of: Introducing a Design System to a Legacy Product (#legacy)
*By Paul Grant ([@cssinate](https://twitter.com/cssinate)) from Martello Technologies on October 10th, 2017 @ 3:00PM*

## Description

Imagine a product that has been on the market for a number of years without having a designer employed. How can you, as a newly-hired front-end designer, introduce a face-lift and design system without completely interrupting an existing workflow?

- Explaining the value of a design system to your team
- Identifying current problems
- Creating scalable and modular solutions to those problems
- Getting everyone on board and contributing to the new design system
- Simultaneously dumping the old and using the new

## Talk

- The Legacy Codebase He Walked Into
    - Every component was put into an iFrame when he got onto his project
        - This seems like the precursor to Web Components 
    - They used glyphicons on everything but everything was a tool and you had to try to memorize what went where.
    - Even though there were a lot of mistakes, the quote by Norm Kerth below is the attitude to keep in mind.
- Design Systems 101
    - Examples
        - [Atomic Design - Brad Frost](http://bradfrost.com/blog/post/atomic-web-design/)
        - [Lightning Design System - Jina Bolton](https://www.lightningdesignsystem.com/)
    - Terms
        - A **style guide** is "a document containing definitions for typefaces, colors, spacing, and other design considerations"
        - A **pattern library** is "a website where a developer finds patterns for components"
        - A **design system** is "the whole kit and kaboodle"
    - Naming Conventions Systems to Consider
        - [BEM](http://getbem.com/)
        - [OOCSS](https://www.smashingmagazine.com/2011/12/an-introduction-to-object-oriented-css-oocss/)
        - [ITCSS](https://itcss.io/)
        - [SMACSS](https://smacss.com/)
    - CSS Preprocessors
        - Options
            - [Sass](http://sass-lang.com/)
            - [LESS](http://lesscss.org/)
        - Primary Benefits
            - Partials which allow you to modularize your styles
            - Variables
        - [Pattern Library Generators Repo by David Hund](https://github.com/davidhund/styleguide-generators)
- The Sale
    - Your product exists because you believe you have something different than the rest of the market. So why use Bootstrap?
    - Work is getting duplicated
    - UI/UX has inconsistencies
    - Sloppy code means sloppy work
    - It's not something that you do immediately. It can be rolled out over time so it's not a big halt on all the projects. In other words, start small like a few hours a week.
    - Because at the end of the day, it will make future feature development faster.
- The Groundwork
    - Open-source as a project model for internal work
    - You're not a dictator at what comes in. You are inviting people to add code to it
    - Getting started...
        - Step 1. Establish your tech stack
            - He currently uses [jekyll](https://jekyllrb.com/) for his pattern library    
        - Step 2. Generate a basic list of components
            - Follow someone else's best practice
        - Step 3. Create a demo
            - Build something using it
            - This is to sell the...
                - Why?
                    - Reduce code duplication
                    - Better and more consistent user experience
                    - 
                - How? 
                    - Pattern library
                    - Good documentation
                    - Naming convention
                - What?
                    - The design library
- The Obstacles
    - "Don't go into a tunnel you can't see the end of." - Harry Roberts
    - In other words, iterate piece by piece
    - While it might look like little has changed, this is actually a win because it means your design system is actually working
- Pro Tip
    - Prefixes are a great way to indicate whether the CSS, JS, automated testing, or etc. has changed.
    - Create a Hulk Smash partial that has crazy stuff in it
- Specificity
    - Four levels...
        - Type selectors 
        - Class selectors
        - ID selectors
        - !important
    - Shows how specificity is calculated. See [CSS Specificity Calculator](https://specificity.keegan.st/) for dynamically generated scores of how specific your selectors are
- Wrapping Up
    - New features should use the design system going forward
    - Roll out to the older components one at a time
    - Tackle conflicts by using a single file of overrides

## Memorable Quotes

> "Regardless of what we discover, we understand and truly believe that everyone did the best job they could, given what they knew at the time, their skills and abilities, the resources available, an the situation at hand." - Norm Kerth

> "Clarity > Efficient > Consistency > Beauty" - Jina Bolton

> "The idea behind a great design system is to write really great CSS once." - Paul Grant

> "Everyone can do better than Bootstrap. You're on the market because you're better than everyone else, so why use Bootstrap?" - Paul Grant

> "Rolling out a pattern library is infinitely harder than building one." - Dave Rupert

> "Don't go into a tunnel you can't see the end of." - Harry Roberts

## Presentation Notes

- When the room is really bright, the typography can be easily washed out especially on dark themes with grey text, but bright colors on dark themes stand out really well
- Amazing use of "The Boss" video game to tell the story
- Used pixel art game to tell a narrative which was incredible
- Great use of sound effects from 80's

## Resources

- [Refactoring CSS Without Losing Your Mind](https://vimeo.com/181328942)
- [Lightning Design System](https://www.lightningdesignsystem.com/)
- [Atomic Design by Brad Frost](http://bradfrost.com/blog/post/atomic-web-design/)
- [Pattern Library Generators Repo by David Hund](https://github.com/davidhund/styleguide-generators)
- [Design Systems Slack Channel](http://designsystems.herokuapp.com/)
