# Keynote Address
*By Harry Roberts ([@csswizardry](https://twitter.com/csswizardry)) on October 10th, 2017 @ 9:00AM*

## Description

We’re all—I hope!—well aware that performance is important; it’s great for business and it’s great for our users. But things are still not fast enough. With more and more emerging markets coming online, and more and more apps moving to the web platform, we’re reaching an intersection where connections are getting slower and websites are getting heavier. In this talk, we’ll learn just what these emerging markets mean to us, and how we can begin to move in the right direction.

## Talk - Why Fast Matters

- His work has transitioned from writing large scale CSS to focusing on performance
- Case Studies on the ROI of Focusing on Performance (Sourced from [wpostats.com](http://www.wpostats.com))
    - "The trainline reduced latency by 0.3 seconds [...], and customers would spend an extra 8.1M pounds a year"
    - "Netflix saw a 43% derease in their bandwidth bill after turning on gzip"
    - "GQ cut load time by 80% and saw an 80% increase in traffic. Median time spent on the site increased by 32%."
- Three major points to takeaway from the case studies:
    1. It will make you money
    2. It will save you money
    3. It makes users happier
- It's not just about the financial benefits though, take a look at the following real world examples Harry encountered in 2017:
    - "Sorry I didn't reply to your email mate... I could see it but couldn't open it because the internet out [in Thailand] is shit." - Harry's Buddy Warren
        - It's not like Harry sent a large file attachment or anything. He just sent a basic text email and his friend still encountered this
    - "I am currently at my parent's place in Rawatbhata, Rajasthan [India]. Since my parents don't have a computer they only consume internet through theri smartphone [...] providers which in our town are still 2G. Right now I have connected my laptop via WiFi hotspot. Opening Gmail in basic HTML version takes 30s to a minute." - Anon
        - **Takeaway:** Their entire internet experience is pretty much entirely in 2G. Wrap your mind around that!
    - A conversation on Twitter
        - Harry: "I have a weird question for you: does my site take a long to load for you?" 
        - User: "I don't think so. I click on your website and it opens within minute"
            - **Takeaway:** Umm.. a minute is normal in in Nepal? Yikes!
- The Next Billion Users
    - This is an initiative spearheaded by Google and set towards the next billion users set to come online in the near future.
    - Some interesting statistics about proportion of users on cellular internet subscriptions as opposed to broadband internet
        - In Bangladesh, 83.4% of users
        - In India, 1 billion (78.8%)
        - In Pakistan, 125.9 million (66.9%)
        - In Indonesia, (132.3% because they have multiple devices)
        - Of the four countries mentioned:
            - Only 1.45% have broadband internet
            - 90.35% are on cellular internet
    - This means we're building for a totally different profile of users
- How fast is fast enough?
    - Just be faster than your nearest competitor
    - Things get markedly easier if you simply want something.
- Tools to Consider
    - [Dareboost](https://www.dareboost.com/en/home)
    - [SpeedCurve](https://speedcurve.com/)
- To get started...
    - Step 0: Want a Fast Website
    - Step 1: Understand the Problem ...Properly Understand It
        - If you are can be fast on an old Android device on 2G connection, then you've really achieved something.
        - It doesn't mean much if our site / apps are fast when on the latest Macbook Pro with broadband internet
        - Use CharlesProxy as a way to throttle your internet or test 
        - It's not just connection that's the problem... the devices we use to test performance on is a big issue as well!
            - **Google recommends that we use Moto G4 to test our sites or apps on.**
            - The iPhone 7 Plus is two to three times faster than the Moto G4. 
            - There's no replacement for real devices.
    - Step 2: Know Where Everything Comes From
        - What does this script do?
        - Which team is in charge of this thing?
        - Are we even using this?
        - So know what's going on and call meetings / find out what's going on
        - Know your liabilities...
            - We call everything "assets," but they're really liabilities
            - Tag Managers
                - That one line of JS that allows non-technical people to run arbitrary bits of JS on the page and often creates a crazy performance hit!
                - They're not inherently bad, but often misunderstood or misused 
                - Be wary of them
        - A technique to find out what is causing performance issue in Chrome Dev Tool
            - Performance >> Bottom-Up >> Group By Domain
        - By adding A/B testing tool, it increased the first paint from 0.8s to 2.1s on a fashion e-commerce site. YIKES!
        - In the Experiment section of Chrome Dev tools, there is a way to show the "Product" of where scripts are coming for and shows statistics on the request
        - Third parties will make you vulnerable
            - He disabled Adobe Tag Manager on Sky.com and it made the site only return a white screen for 1.3 minutes before Google finally timeouts.
            - If you want to simulate this, just point third-party domains to blackhole servers to simulate fallen outages. Check slides for an eaxmple
    - Step 3: Measure Everything
        - Measure before and measure after
        - How do we know:
            1. What's wrong?
            2. When it's right?
        - In Google Analytics...
            - Behavior >> Site Speed >> Page Timings
            - This shows you what are problem regions for your site
        - Performance Budgeting (aka Monitoring Performance Alerts)
        - Sets up a brutal network conditions...
            - Low upload / download
            - Added connection latencies
            - Intentionally add package loss during connection
- Closing
    - Care: Prioritize, consider, and champion performance
    - Understand: Your customers, the problem, the landscape
    - Measure: Everything you can, before and after

## Memorable Quotes

> "I will move mountains. I will miss my mother's funeral for this event." - Harry Roberts

> "To be truly mobile first, you must test you website on those connections. Not simply having media queries." - Harry Roberts

> "The best way to start setting goals for your performance goals is to just be faster than your nearest competitor." - Harry Roberts

> "If you can optimize for the lowest device, you get the rest of the devices for free." - Harry Roberts

> "There's no replacement for real devices when it comes to performance testing." - Harry Roberts 

> "[Making your users download all these scripts] is disrespectful to our users because they are paying for it. Literally paying for it." - Harry Roberts

> "We call everything "assets," but they're really liabilities when it comes to performance." - Harry Roberts

> "Don't prioritze your own metrics over your users' experience. There's no point having a site if your users can't get to it. In other words, don't get in the way of people trying to give you money." - Harry Roberts

> "Imagine having to work a whole month just to afford your yearly data plan." - Harry Roberts

## Presentation Notes

- Did a great job building up just enough statistics to drive home his point
- Fantastic use of scrolling through a network request report to show 
- Has numerous of real case studies that makes the story that much more effective
- Really liked how he used both client work as well as his own personal site which made the problem relatable because it didn't allow you to disregard his advice by thinking "well my site is not as big as X company so it's not as big of a deal to me."

## Resources

- [Harry's Slides](https://speakerdeck.com/csswizardry/why-fast-matters)
- [What Does My Site Cost?](https://whatdoesmysitecost.com/)
- [Building for Billions](https://developers.google.com/web/billions/)
- [Dareboost](https://www.dareboost.com/en/home)
- [SpeedCurve](https://speedcurve.com/)
- [CharlesProxy](https://www.charlesproxy.com/)
- [Jana Insight](http://www.jana.com/insights)
