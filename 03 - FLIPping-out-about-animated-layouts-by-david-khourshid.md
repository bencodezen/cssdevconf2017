# FLIPping Out About Animated Layouts (#flipanim)
*By David Khourshid ([@DavidKPiano](https://twitter.com/DavidKPiano)) from Microsoft on October 9th, 2017 @ 12:00PM*

## Description

Say goodbye to jump cuts on the web! In this session, you'll discover what makes native apps feel so alive and how we can replicate those movements on the web. Learn how the FLIP technique can smoothly transform flexbox- and grid-based layouts at 60FPS. We'll dive into basic and advanced techniques for animating between states in many different situations with interactive demos. 

Why animate layouts (+ many examples) 
How native apps transition: 
- Android's Shared Element Activity Transitions 
- iOS's Layout Constraint Animations 

The FLIP technique (First, Last, Invert, Play) 
- using the Web Animations API 
- using GSAP 

Additive, interruptible & physics-based FLIP animations 

Choreographing FLIP animations 

Motion curves (a la Material Design) 

Tools, libraries & resources

## Talk

- Surprise User Experience (SUX)
    - Users often feel stupid when using our apps because there is so much context switching
- Jump cuts are really annoying because it just throws the next thing in your face right away
- How can we improve user experience on the web?
    - We improve the experience to reflect the experience of mobile apps
- Material Design: Transitions should be
    - Quick: efficient yet meaningful
    - Clear: simple and coherent
    - Cohesive: Unified by speed, responsiveness, intention
- Talks about transitions in native mobile development
    - `snapshotViewAfterScreenUpdates` - uses before and after snapshots to show the different states and animates from one to the other
    - `Shared Element Activity Transition` - Android technique for sharing animation between elements
- FLIP technique
    - **First** - the initial state (size & position before action)
    - **Last** - the last state (size & position after action)
    - **Invert** - take each of the dimensions (x, y, width (ratio), height(ratio)) and calculate what changed between the two (delta of sizes and positions)
        - `deltaX` = `last.left - first.left`
        - `deltaY` = `last.top - first.top`
        - `deltaW` = `first.width / last.width `
        - `deltaH` = `first.height / last.height`
    - **Play** - Then you animate the deltas!
- Advanced FLIP
    - Expand & Collapse
        - Attempt 0: Animate height and width. Just don't. Please.
        - Attempt 1: Animate clip-path
        - Attempt 2: Animate scale
        - Attempt 3: Animate 'clipped' transition
    - FLIPping Children Off Parents
        - Calculate FLIP based on parentBounds in order to get relativeBounds
- Announcing Flipping library

## Memorable Quotes

> "It's a great thing the Microsoft is handing out bottle openers becaues When I work on IE, I drink." - David Khoursid

> "If you have to write a long tutorial about how to use your app, you're doing it wrong." - David Khoursid

> "Animation brings user interfaces to life." - Nick Babich

## Presentation Notes

- Really clean slides that make it easy to compare his points
- Great use of typography for text

## Resources

- [Functional Animation in UX Design](https://uxplanet.org/functional-animation-in-ux-design-what-makes-a-good-transition-d6e7b4344e5e)
- [Species in Pieces](http://www.species-in-pieces.com/)
- [Building Performant Expand & Collapse Animations by Paul Lewis & Stephen McGruer](https://developers.google.com/web/updates/2017/03/performant-expand-and-collapse)
- [FlipJS](https://github.com/googlearchive/flipjs)
- [React FLIP Move](https://github.com/joshwcomeau/react-flip-move)
- [FLIPping GitHub Repo](https://github.com/davidkpiano/flipping)
