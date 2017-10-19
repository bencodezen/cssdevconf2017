# Essentials of CSS Animation w/ Val Head

- CSS animation is fundamental to the rest of what we'll be doing the rest of the day
- It can often be the simplest answer to get things done
- The thing about CSS animation is that we have a bunch of things that sound like they can do the same thing. There may be times you may have to say "we have to animate the transition to transform and translate..."

## CSS Transforms

- Spoiler Alert: This doesn't make anything move.
- It allows you to modify the coordinate space of the CSS visual formatting space
- They are all in one property (i.e., `translate`, `rotate`, `scale`, `perspective`, etc.) and most importantly, **the order matters because it changes the end result**
- The `perspective` property requires a pixel
    - Lower numbers make the effect  more drastic it is
    - Higher numbers make it much flatter
    - Recommends 800px to 1000px as a starting point
    - It should generally be the first thing you define in a `transform`
    - You can also set it on the parent container and then manipulate the children separately

## CSS Transitions

- Transitions are animations.
- The minimum you need for a transition:
    1. Point A
    2. Point B
    3. Duration
- Shows interesting technique of setting just transition time (with no properties defined i.e., `.box { transition: 1s }`) on the parent element to impact the rest of the children
    - Granted, this is a little dangerous from a performance perspective; but just interesting to note
- You can make the transitions asymmetrical by adding a second `transition` state
    - **Counter-intuitive point:** *The Point B transition is the one that executed first especially on things like hover because that state gets set immediately.*
- For better readability, use comma separated values

## CSS Animations

- The minimum you need for an animation:
    1. `A named set of keyframes to assign
    2. `animation-name` - user designated name (which can pretty much be anything)
    3. `animation-duration` - the length of the animation
    - Optional
        1. `animation-delay` - how long the animation is delayed for
        2. `animation-iteration-count`: how many times the animation happens 
        3. `animation-direction`: which direction the animation goes
        4. `animation-fill-mode`: fills in the time outside the animation (at either end)
        5. `animation-timing-function`: this determines the cubic-bezier and takes the usual properties of `ease`, `ease-in-out`, etc.
- Why is this better than CSS Transitions?
    - You can define multiple stages of your animations
    - It seems to allow much more granularity with animations
    - You can have multiple `@keyframes`
- Tip: Remember that it is `@keyframes` and **NOT** `@keyframe`
- There is a shorthand to consider:
    - `animation: ${name} ${duration} ${delay} ${iteration-count} ${direction}`
        - **Pro Tip:** Even though there is no specific order required (except duration and delay needing to be one after the other), at least start with the animation name. And decide on a convention with your team.
- You can define stages in your `@keyframes` with percentages and/or keywords.
    - **Pro Tip**: You can do floats with the percentages!
    - **Pro Tip**: It's best to pick one or the other for consistency (i.e., `from` == `0%` and `to` == `100%`)
    - Example:
        ```
        @keyframes move {
            0% { ... }
            10% { ... }
            100% { ... }
        }
        ```
- The default timing function transition in CSS animation is `ease` and not linear like everywhere else
    - **Pro Tip**: When you use ease, it's going to try and use it as a global ease. Instead, try setting `animation-timing-function: linear` on the global and then define specific timing functions for the various frames
- Handy properties you can animate but were probably not aware of...
    - `z-index`
    - `transform-origin`
    - `animation-timing-function`

## CSS Variables

- AKA CSS Custom Properties
- Why they're a big deal...
    - They follow the CSS cascade (custom properties)
    - You can easily modify values with JavaScript
- Example
    ```
    transform: translate(calc(var(--mouse-x) * 1px - var(--radius)/2))
    ```
- This can make `@keyframes` much more dynamic because changing them after they're in your CSS file.
- **That means multiple elements can use the same keyframes but have DIFFERENT animations!!!!**
