# Basics of TweenMax & TimelineMax w/ Sarah Drasner

## Introduction

- GreenSock is a company that makes TweenMax and TimelineMax. In other words, they are products but are still referenced as GreenSock as a whole in converstaion
- GSAP performs as well if not better than some native technologies
    - It's not that they're not leveraging native technologies
    - They are just doing it in clever ways and paying attention to exactly what they're animating
- Painting is one of the most expensive aspects of rendering, but GSAP's painting is really really low in comparison
- Visual benchmarks are important because it is a separate benchmark from straight up performance benchmarks like FPS
- Like it a lot because it helps a lot with workflow and cross-browser consistency
- The issue with CSS animations:
    - Sequencing animations is a manual process of delays and is not very sustainable
    - Adjusting timing of an animation is so critical to the workflow and this becomes very expensive
    - Basic coding workflow of having your animation be far from the element you're applying it to (i.e., scrolling down to your keyframe, then back up to the styles, then back down...)
- **Pro Tip**: Opacity and transform are the most performant and best bang for buck when it comes to animation on the web
- Killer workflow features:
    - Simple syntax
    - Timelines
    - Nested timelines
    - Draggable
    - And more (found in slides)
- Syntax
    - Think of the actions (i.e., `to`, `from`, etc.) as sentences
        - "Hey Tween[Max/Lite], grab this element and go ${action} ..."
    - `fromTo` is good at the beginning of an animation because when you need the animation to restart from a certain position
    - Stagger is amazing!!! For a cool example, check out this [SVG with Cycle Stagger CodePen by Sarah](https://codepen.io/sdras/pen/XmmjQb)
- Timeline
    - This is one of the primary features she loves
    - It makes things so easy to change things that would normally make you want to shoot yourself if you did it in raw CSS
    - **Pro Tip**: The industry standard for the timeline variable is `tl`
    - The primary difference between the two different Timelines is that TimelineMax allows you to loop while TimelineLite does not
    - You can nest timelines as well!
- **Pro Tip**: In order to avoid momentary display due to HTML/CSS rendering before JS does its thing, set the visibility to hidden on the animated elements to start (and then set back to visible with TweenMax/TweenLite)
- Percentage based transforms are cool! And unfortunately will never be part of the CSS animation spec, so it's a GreenSock specific thing!
- The animations are fully responsive
- **Pro Tip**: While you normally want to keep styles in CSS, this can become disjointed with team members because they don't know you need X styles for the animation. So Sarah recommends using the `TweenMax/TweeLite.set()` functionality to explicity associate the necessary styles directly with the animation to prevent any accidental code deletion!
- For frameworks, she wraps the animation in a component that only kicks off once the component is mounted. AWESOME!
- Animating Text
    - Split Text
        - A plugin that breaks text into characters, words, or lines and has no dependencies (not even TweenMax)
        - Support back to IE 8
        - **Big Plus:** Even though there are tons of open-source, it is what she recommends because it honors natural line breaks
- How would we turn a many element scene from day to night?
    - **Pro Tip:** Recommends HSLA for colors in animation
    