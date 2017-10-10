# What's New in JavaScript (#newjs)
*By Wes Bos ([@wesbos](https://twitter.com/wesbos)) on October 10th, 2017 @ 10:00AM*

## Description

As we start to get comfortable with new ES6 features of JavaScript, both the language and the web platform is charging forward with many new features. This talk will cover some of the best things that are brand new to JavaScript as well as things that we can look forward to in the coming months and years. Strap yourself in for a fast-paced talk full of hot tips as we rocket ourselves into the future of JavaScript. 

## Talk

- **Promises**
    - Think of it as an I.O.U. for something that will happen in the future
    - These requests take time, so we simply kick off the process and go off to do other things
    - Uses making breakfast concept to illustrate async issues
        - Do you need to finish making coffee before you start making breakfast?
    - We want to start one thing and come back when it's finished
    - Most new browsers APIs are built on promises or observables...
        - `fetch()` - It's like the jQuery `$.get()` function
        - [`axios`](https://github.com/axios/axios) - A data fetching library
    - It's easy to make your own as well
        - What you do it you have your function return a `Promise` which uses a pattern that allows you to `resolve` or `reject` things based on conditions you determine
    - The beauty of promises is that is helps us avoid "Christmas Tree Callback Hell"
    - What's the deal with `.then()` since it's still kinda callback-y?
    - Any code that needs to come after the promise still needs to be in the final `.then()` callback which still makes it undesirable.
- **Async + Await**
    - So this is the solution we ultimately want.
    - You mark your functions as `async` and then throw `await` in front of things you need to finish before it moves down the rest of the function "synchronously"
    - JavaScript is almost entirely asynchronous / non-blocking. In other words, it doesn't block rendering and allows the rest of your site to do stuff while it's doing something else. 
        - This is nice, but it's hard to read/write
    - Uses comparison between PHP and JS of how PHP looks synchronous but doesn't have JS performance benefits, but JS Promises reads funny. Async + Await is the answer to this discreprancy.
    - How to Use It:
        1. Mark your function with `async`
        2. Mark the asynchronous function you're waiting for that returns an asynchronous repsonse like a `Promise` with `await`
    - Remember that Async + Await is still using JS Promises. It's pretty much just syntactic sugar for the most part (as far as I can tell)
    - Error Handling
        - Most people use `try { ... } catch { ... }` 
        - He'll do a blog post on this eventually, but this is something to be addressed later
- **Intersection Observer**
    - How do you know when an element is on the screen?
    - With intersection observer, you can be alerted when an element is fully or partially scrolled into or out of view!
    - Uses
        - Animate elements in on scroll
        - Play video on scroll in
        - Lazy load images only when scrolled
        - Use with sticky headers
    - How you use this:
        1. Setup a config object for options:
            - You can set the threshold for when you want to be alerted
        2. Set an empty Intersection Observer
        3. Give it a callback which allows you to map over the various entries and then perform actions based on properties like `isIntersecting` and `intersectionRatio`
            - Fun note: You can actually `unobserve` the target entry as well!
        4. Give it stuff to observe!
            - You use something like `observer.observe` allows you to trigger everything you setup
- **Payment Request API**
    - Every single online stores needs to reinvent the checkout form
    - We're all just trying to do the same thing - collect credit card information
    - This API is a standardized browser method to collect payment information from your user
    - Payments are stored in the browser / phone instead of you saving credit card
    - So, does the browser charge your card? NOPE!
        - The various APIs give you the data in some sort of form (i.e., token) and you bring it to your payment provider who then actually does the charging.
    - Is it secure?
        - It's either the same or more because you never have to touch a credit card number. Because with this method, if a token gets stolen it's not connected to your number. It's a separate transaction.
- **Get User Media**
    - Not new at all apparently. He wrote a blog post in 2011 and even though it is 2017, "Safari still doesn't give a shit."
    - September 2017 / iOS11
        - `PlaysInline` and `GetUserMedia()` - This allows you to watch videos without getting that black rectangle box on iOS
        - What's cool is that it is Promise based
- **Resize Observer**
    - It tells you when a specific element has been resized
    - You create a `new ResizeObserver(callback)` with a callback (that contains the entries it finds)
    - In other words, it is a gateway drug to element queries
- When can we use all of this?
    - `Async + Await` - Widely supported (especially with Babel)
    - `Intersection Observer` - Has an official W3 polyfill
    - `Resize Observer` - Polyfillable, but expensive
    - `Web Payment` is easily polyfillabe (or fallback to checkout form)
    - `GetUserMedia` is everywhere

## Memorable Quotes

> "It's [Syntax Podcast] not one of those podcasts that makes you feel like you're falling behind in your career." - Wes Bos

> "JavaScript waits for no one. It's like this kid that's like 'I want some data' but then goes off and does something else before the data is ready." - Wes Bos

> "I see }); as winky frowny neck beard emojis" - Wes Bos

## Cool Presentation Techniques

- Love the custom font which gives the overall presentation a personal style / flair 
- Great analogy of making breakfast to async to make it easier to understand because it's so relatable
- Appreciate how he uses multiple examples (one complex and one simple) to make sure his point is driven home
- Great progression of examples to show how you start from one point (i.e., callback hell) to something more modern (i.e., Promises) to something even better (i.e., Async + Await)
- Don't forget that sometimes a low tech / fidelity example is acceptable. He didn't know how to make flying animated objects and had a low fidelity desktop scroll example which proved humorous and still delivered the message at the same time. So don't be obsessed with perfectly designed slides, being organic is actually quite refreshing and charming when done properly.
- Great usage of screenshot GIFs to illustrate the examples of the new features coming. This is particularly effective in his talk because he has to cover a lot of topics and live demos aren't as effective when you just want to give an overview of a topic and it also means it lets the audience see it over and over again while he further elaborates on it.
- Also really like his integration of subtle jokes in his code examples which shows an attention to detail because it's easy to just throw a random string `foo` or `bar` to make your example, but at the same time, it's that much duller and probably less effective to making your point

## Resources

- [axios](https://github.com/axios/axios)
