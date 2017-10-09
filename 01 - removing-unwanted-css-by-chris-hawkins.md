# Removing Unwanted CSS (#unwantedCSS)
*By Chris Hawkins ([@chriswhawkins](https://twitter.com/chriswhawkins)) from BASE TWO on October 9th, 2017 @ 10:00AM*

## Description

The future of web development and build tools like webpack promise new and exciting ways to manage our CSS and only deliver exactly the necessary styles for the components on the screen. But right now today, we're still working on lots of projects using build tools like gulp and frameworks like bootstrap that come with a lot of styles we might not use but end up serving to every page.

After this session, you'll have some great ideas and familiarity with tools to help you trim down your unwanted CSS. Tools include: 

- Gulp + Sass and the usual suspects 
- UnCSS to check views against Sass/CSS 
PostCSS and ByebyeCSS to list selectors we want to be removed 
- Some browser and command line tools and tips to measure and test CSS performance

## Talk

- Shows case study of how the initial site used its SCSS file as the `global.scss` for the other sites
- This creates a logistical nightmare because of the dependencies and obvious difficulties that arise with QA 
- Went with "inline critical CSS"
- Used Chrome Audit to look at the site overall and help provide recommendations for solutions going forward.
     - It can even show unused CSS!
- Used Bootstrap as an example for how the Audit can show unused CSS can impact performance (via the Legacy Audit)
- Show new "Coverage" panel which shows unused CSS and you can see line to line what is being used and what is not
- Introduce UnCSS tool
    1. Load/execute views via jsdom
    2. Parse stylesheets with PostCSS
    3. Filter out unused selectors in the views via `document.querySelector`
- UnCSS is helpful, but requires very thorough QA because it is relentless about removing things. So it can be tedious in that regard.
- Introduces UI Toolkit Fabricator (which is like Pattern Lab)
    - Doesn't have hot module reload from the sounds of it
- Uses Storybook as well which allows you to develop components in a dedicated environment, but seems to have a tentative opinion on this tool
- Encounters scenario where they want to use a datepicker module but has to bring in the entire Blueprint library
- Another tool to checkout - CSS Bye Bye: Supply the selectors and watch them go bye bye

## Memorable Quotes

> "21% of the top 1 million websites use Bootstrap" - builtwith.com

## Cool Presentation Techniques

- Clever parody of Angel song pet commercial with CSS facts
- Good use of screen capture GIFs to illustrate some points

## Resources 

- [UnCSS GitHub Repo](https://github.com/giakki/uncss)
- [Optimize CSS Delivery by Google Developers](https://developers.google.com/speed/docs/insights/OptimizeCSSDelivery)
- [Fabricator UI Toolkit](https://fbrctr.github.io/)
- [Storybook UI Dev Component Environment](https://github.com/storybooks/storybook)
- [CSS Bye Bye](https://github.com/AoDev/css-byebye)
