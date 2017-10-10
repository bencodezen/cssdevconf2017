# Flipping Tables: Displaying Data on Small Screens (#flipdata)
*By Stephanie Hobson ([@stephaniehobson](https://twitter.com/stephaniehobson)) from Mozilla on October 10th, 2017 @ 11:00AM*

## Description

- [ ] Will update when I get this from the organizers 

## Talk

- **When to Use Tables**
    - This should be based on content and what users will be trying to answer
    - It's appropriate to use tables if users want to...
        - Sort data
        - Compare data
        - Cross referencing data
    - Don't use tables when...
        - For displaying lists in a column... or multiple columns
        - Putting images next to something
        - Check out Nicole Sullivan's Media Object
        - In other words, don't use it for layout
- **Creating structure with HTML**
    - Covers best practices with tables which I can't cover properly here, but check out [this article from MDN on HTML table basics](https://developer.mozilla.org/en-US/docs/Learn/HTML/Tables/Basics)
    - You can have multiple table headers and bodies
    - You can put anchors on `<tbody>` which allows you to anchor to them
- **Designing Tables**
    - Provide a caption. Seriously.
    - Identify columns, rows, and headers with easily 
    - Enhance readability (use a monospace font for numbers)
    - Group similar data together
    - Use smart defaults
        - Identify what the users are trying to get
        - Front load calculations if you can
    - Design Advice
        - Avoid wrapping text
        - Used a phenomenal gif to show the start to finish
        - [ ] Update this list with the techniques once the slides are up
- **Adding Style with CSS**
    - [ ] Missed CSS property for this section. Will update once slides are up
    - `border-collapse` - "specifies whether a table's borders are separated (cells have distinct borders from each other) or collapsed (adjacent cells share borders)"
    - `caption-side` - Determines where you caption will be placed in relation to your table
    - `vertical-align` - Self explanatory
    - `col` is hard to use due to some interesting restrictions she mentions:
        - Can't target specific elements (e.g., `td`) within it 
        - Odd specificity issues because it sounds like your styles can be easily overridden
        - So probably want to avoid relying on it for styles
    - Because of old usage of tables for layouts, screen readers will try to guess whether or not the table is being used for layout or for data.
- **Adapting Tables to Small Screens**
    - **Shrink the content** - Abbreviations? But be careful with doing this
        - She mentions a clever trick of using `<abbr>` for the label and then using `:after` to show the full label on X media query
    - **Linearize or Flip** - Add `display: block` to the elements to generate cards
        - Clever use of `::before` content to generate labels when you need the header to make things make sense
        - Neat use of `data-` attribute for automatically creating labels 
            - `content: attr(data-head)` as one example of an HTML element with the label populated with the `data-head` attribute
    - **Remove Data** - Usually requires JS though
    - **Let Users Scroll** - Don't hide horizontal overflow. It might not be pretty, but at least it's functional and readable
        - Works well for large institutions that have so many tables that can't get individual intentions
        - You can fix the headers or columns with JS to create a better experience if needed
    - **Replace the Table Entirely** - This is not ideal as you lose out on the experience of having a graph (i.e., exploring data) but certainly an option if you're simply trying to make a point (i.e., replace the table with the text you're trying to make)
    - **Combo** - Combine any of the above techniques!
- Case Study of Converting MDN Tables to JSON
    - Apparently all the tables are actually hand coded
    - They are currently in the process of trying to componentize these tables
    - Interesting, they use `em` for media query to consider users who zoom in. I wonder if that also work for `rem` as well

## Memorable Quotes

> "Simplicity is about subtracting the obvious an adding the meaningful." - John Maeda

## Presentation Notes

- Great use of an animated emoji in relation to the topic (i.e., flipping tables which is punny)
- Very animated with her talk as far as communicating emotions
- Used sites that already fixed the problem and then broke it to illustrate the problem which makes the example instantly recognizable due to brand recognition (as opposed to creating a low-fi CodePen which can lose touch with the audience). This saves her time because then she doesn't have to go out of her way to create the "correct" way to do it. Brilliant.
- Like her ending "My name is Stephanie Hobson and I like to make websites that everyone can use." with her branding

## Resources

- [The Media Object by Nicole Sullivan](http://www.stubbornella.org/content/2010/06/25/the-media-object-saves-hundreds-of-lines-of-code/)
- [HTML Table Basic by MDN](https://developer.mozilla.org/en-US/docs/Learn/HTML/Tables/Basics)
