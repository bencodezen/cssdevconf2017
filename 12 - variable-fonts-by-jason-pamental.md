# Best of: Variable Fonts and the Future of Web Design (#scaletype)
*By Jason Pamental ([@jpamental](https://twitter.com/jpamental)) from Isovera on October 10th, 2017 @ 4:00PM*

## Description

Typography is the most important aspect of great design and UX, but can’t come at the expense of performance or we risk our designs never being seen. Variable fonts are coming, and will change everything: with a single font file that can scale in size, width, weight and even x-height—exactly as the type designer envisioned—all controllable via CSS. 

- What are variable fonts, and when can they be used 
- Why type is the voice of your words, and how that voice just became a chorus 
- How to expand the dynamic range of your design with type 
- Where to be restrained and when to experiment: think character widths on small screens, or even responding to ambient light with stronger character weights

## Talk

- The thing he is passionate about is using typography well on the web
- Most of the web is words (and cat videos), but mostly words.
- Use of ancient text of beautiful typography as examples really calls to attention just how much typography impacts the beauty of what you're looking at
- Internet has not killed curly quotes, laziness has
- Details of typography that are important to him:  
    - fractions
    - curly quotes
    - dropcap
    - ligatures
    - proper hyphenation
    - nice section mark
    - etc.
- Dragon #1: The practice of typography for digital systems is *different*
    - Unfortunately, we can't control the web
    - You have to load multiple formats of a typeface which means large data downloads
    - You can play with scale of type based on screen size
- Dragon #2: Performance - Unstoppable force, meet immovable object
    - In other words, how content showing up at all trumps pretty much anything else in the way
    - Think of the scenarios where data transfer rate is unreliable
    - So we pull back in order to get better performance, but if we keep accepting pretty close and pretty okay, then all the progress starts to erode.
    - 26 billion is the number of times Open Sans was served by Google Fonts API *last week*
        - There are a lot of incentives to figuring out a better way to do this
- Solution: Variable Fonts
    - September 14th, 2016 at ATypl Warsaw
    - Enter Sandman, aka Variable Fonts
    - 2 dragons, 1 font
    - "A variable font is a single font file that behaves like multiple fonts" - John Hudson
    - Variation Axes in Action
        - Weight
        - Width
        - Slant
        - Italic
        - Optical size
        - Grade
    - It still allows flexibility for the designer to control the steps of interpolation between typographic properties
- But wait... don't forget Dragon #3: Context
    - One of the things about reading on a small screen is that you only get 30-45 character if you preserve the original body on desktop. By changing it to thinner typography, you can get an increase of ~10 letters on a page which is a pretty big deal.
    - German is about 40% long in English, this means you get an uneven rag on the right. But by narrowing the characters by a little bit, the German text looks so much better and is much more readable
    - What about being sensitive to lighting considerations? How about making something with a thicker grade for improved readability in low light?
- What about the future?
    - "All system, no soul." Let's get graphic design back in the room
    - Typography on print is impactful and is phenomenal in comparison to web
    - This is an opportunity to bring graphic design back into what we do...
        - Uses the example of Jen Simmons trying to bring design back into web with CSS Grid
    - A more modern redux of how print happens...
        - Author >> Editor >> Designer
    - On the web however, this has been flipped
        - Designer >> Author >> Editor
    - Jason Santa Maria self directed blog posts which resulted in beautiful blog posts, but ultimately ended up being unsustainable.
- How might we do better?
    - The CMS can play a part in design too
        - Shows wireframe of all the axes of variation for a typeface and allow editors
        - Treat mini-stylesheets as content the CMS saves
        - Build tools for designers that can lay these things out and do interesting things with typography and really create beautiful digital products
- Think about how being able to differentiate typography better will allow people who suffer from reading handicaps like dyslexia to better read your content.
    - If you simply increase the space between lines and words, you could improve the readability as much as 50% for users with issues reading
- **Allowing the typography to react to context and user needs with web typograph is a HUGE deal.**
- This is why he calls himself a "web typographer" and not just a "typographer" because the the problems are that different and the impact is greater than any other medium prior
- Status Check: Support
    - Beginning of October 2017 - iOS - Safari
    - Mid-October 2017 - Chrome
    - Edge & Mozilla - Q4 2017
    - Windows 10: Bahnscrift will have it built in at the OS level
    - Photoshop will have variable font support built in the next major release
- Q&A
    - How do you make a variable font?
        - A lot of type designers have to go through a new workflow in order to export them in this new format

## Memorable Quotes

> "Most of the web is words (and cat videos), but mostly words." - Jason Pamental

> "Words comunicate meaning; typography either amplifies or dilutes it. Every detail that's just 'ok' lessens our words' impact." - Jason Pamental

> "Internet has not killed curly quotes, laziness has." - Jason Pamental

> "In 3 seconds, 53% of your mobile audiecne will leave it's been 2.9 seconds - do you know where your web fonts are?" - Jason Pamental

> "If we keep accepting pretty close and pretty okay, then all the progress starts to erode." - Jason Pamental

> "If type is the voice of our words, that voice just became a chorus." - Jason Pamental

> "All system, no soul. Let's get graphic design back in the room." - Jason Pamental

> "If we serve everything in the same way, nothing gets special treatment." - Jason Pamental

## Presentation Notes

- Great use of personal things in his life (i.e., his dogs) as a way to talk about typography. This changes things up a bit and keeps it intersting
- Nice use of an overlay with "transparent" shapes to highlight parts of an image he wants the audience to pay attention to
- Phenomenal use of animation when the typography is changed
- Great use of overlay of a character to show contrast of a standard letter when changing the weight of it

## Resources

- [Slides](http://rwt.io/presentations/talk/variable-fonts-future-web-design)
- [Code Examples](http://rwt.io/vfdemos/index.html)
- [Jason Santa Maria](http://jasonsantamaria.com/articles/)
- [Axis-Praxis by @lorp](http://www.axis-praxis.org/)
- [Typogriphy Drupal Plugin](https://www.drupal.org/project/typogrify)
