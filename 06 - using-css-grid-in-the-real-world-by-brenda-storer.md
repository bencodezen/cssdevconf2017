# Using CSS Grid in the Real World (#realgrids)
*By Brenda Storer ([@brendamarienyc](https://twitter.com/brendamarienyc)) from Thoughtbot on October 9th, 2017 @ 5:00PM*

## Description

The new CSS Grid specification is here! Sure, it's fun to play with, but is it truly ready or even practical to use for everyday work? As a designer and front-end developer at a software development agency, I've been using CSS Grid in production websites and it is already making my life easier. In this talk, I'll show you some examples that will include:

Layouts achieved with a few lines of code that previously required messy hacks or JavaScript

- Examples of different syntax and units for CSS Grid 
- Fallbacks for older browsers 
- How CSS Grid improves accessibility

## Talk

- Interest in new spec items usually peaks until someone asks about browser compatibility
- It went from 0 - 70 in a month for browser support because vendor prefixes are becoming a thing of the past and feature flags are the new way forward
- Microsoft Edge is going to get Grid support on October 17, 2017!
- Step by Step Guide to Writing CSS Grid
	- Step 1: Identify a Good Use Case
		- Flexbox vs Grid
			- Flexbox is great for laying out items in one direction... in rows... or columns...
			- Grid allows you to lay out elements in two directions: rows & columns
				- Grid shares the similar paradigm of flexbox where you have a grid parent and then the direct children of that parent are grid children
	- Step 2: Write Grid Code
		- Don't worry about the fallback. Just write grid code.
		- A benefit of grid code is that is simplifies the markup because the visual aspect will be taken care of by grid
	- Step 3: Fallback Gracefully with Feature Queries
		- Use `@supports` 
			- If the browser doesn't recognize `@support`, it skips it anyways.
		- Fallin' back with Flexbox
		- Order matters
			- The fallback should be first as default
			- Grid code shoudl be last so it can override any of the default styles
		- A few things to consider...
			- [Disable grid in autoprefixer is default for Autoprefixer v7.0+](https://twitter.com/autoprefixer/status/849744717570899968)
			- Some syntax is not supported in Sass until v3.5
				- Sass rails is only running Sass v3.1
	- Step 4: Ship It!
- What things can CSS Grid do that CSS couldn't do before
	- Control placement around unknowns
	- Using media queries with grid
- Can CSS Grid replace Masontry?
	- Not really, but kinda sometimes sorta?
	- Needs autoprefixer grid support disabled
- Graceful Degradation
	- Who made the rules that web pages must look the same in every browser?

## Memorable Quotes

> "Vendor prefixes were probably never meant to be shipped to production. And because they were, it created a whole slew of problems for us." - Brenda Storer

> "It's okay that when I look back at my old code I sometimes say, 'What was I thinking?' That means I'm still learning and growing." - Brenda Storer

## Presentation Notes

- Great use of a faux graph: "Emotional Reaction to new CSS Specs"
- Nice use of abstract shapes to represent mental models of how grid works

## Resources

- [CSS Layout Club Meetup in NYC](https://www.meetup.com/CSS-Layout-Club/)
- [Should I try to use the IE implementation of CSS Grid Layout?](https://rachelandrew.co.uk/archives/2016/11/26/should-i-try-to-use-the-ie-implementation-of-css-grid-layout/)
