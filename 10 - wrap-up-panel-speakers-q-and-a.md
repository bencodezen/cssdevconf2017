# Wrap-Up Panel: Speakers Q&A 
*By All Speakers on October 9th, 2017 @ 12:00PM*

## Description

An annual tradition — all CSS Dev Conf speakers together on stage for an hour to answer your last minute questions! 

## Discussion

### Slow internet connections on the rest of the world was very insightful. With more developers coming up with client-side apps, what is your word of wisdom with JS frameworks?

- **Harry Roberts:** If it's an all or nothing deal, that's scary. It's more about reliability and think about progressive enhancement. So reframe it from performance and more about resilience and reliability. How well does it fail is the way to think about it.

- **Estelle Weyl:** If you can't do a ten minute presentation on why you need the dependency, don't use it. If you just need a calendar widget, don't use React. Just use the calendar element.

### Do you have any experience with things like isomorphic React / universal JavaScript / server side rendered hybrid approach?

- **Harry Roberts:** Primarily has seen fully client-rendered apps

### How does DOM encapsulation affect best practices and what is it going to do to CSS best practices?

- **Micah Godbolt:** Figure out better ways to abstract styles (whether it's design tokens). By attaching small stylesheets with components it's been mostly alright in his experience. Keep global things in build state, but once it's on the client side, let it be dynamic.

- **Jonathan Snook:** Looking forward to HTTP2 and the ability to cache individual components. This has implications on the CSS (that is modularized) since it could be loaded on demand because it creates isolated assets

- **Harry Roberts:** Write good CSS like you always have because this prepares for the eventuality that if it's ever migrated, you can repurpose it. Don't slacken the discipline because otherwise you will pay for it later on. 

- **Matt James:** Isn't the C for cascading? But encapsulation shouldn't provide a loophole to write bad CSS. 

- **Dave Ruperts:** You can style `ul` elements again without being in fear of Harry Roberts. HTML imports are great but browsers "wouldn't support it." (joke jab)

- **Sarah Drasner:** It's dangerous when teams have become so reliant on encapsulation that they don't know how to write proper CSS. Encapsulation is not going to help you if you don't understand document flow and overall CSS architecture. I watched someone write 3000 lines of JS to do something that `position: absolute` does. The danger is when you think you don't have to learn how styles work because you have this tool.

### As far as workflow, are you using different templates (i.e., markup) for production and the design system? How does that work if you have different features? What are the logistics of actually supporting it? 

- **Vince Nalupta:** We try to keep our pattern library as a base layer. It is thought of as an API layer (i.e., a contract) with design which is the foundational layer. When it goes into production, then the apps layer things on top of it. The team needs to learn what is a pattern in order to keep a feedback loop back into the system. This means that they are ultimately different development paths for production and pattern libraries. This is good because designers who want to add code don't have to get embroiled in the mess that comes with updating production. 

- **Micah Godbolt:** Had the holy grail situation where the production templates were the same as the prototyping templates. This is similar to creating an NPM package for a React Component where it can be reused everywhere. It's a beautiful way to work and scales great since it allows you to work in a single codebase.

- **Matt James:** Keeping everything as a single source of truth makes things easier for communication.

### There's been a lot of talks about components and component-driven development. When components leak in logic (i.e., validation, fetching, etc.), should you separate those concerns? Should components only be visual? If so, where should it live?

- **Wes Bos:** Yes. Keep them separate. In React, you use Higher Order Component which allows you to compose components into a "mama component." 

- **Sarah Drasner:** Or in Vue, you can use mixins to bring function into components seamlessly.

- **Wes Bos:** Unfortunately React got rid of mixins

- **David Khoursid:** When it comes to managing state, a component can only be in a certain number of states. Like a button can be active, disabled, loading, etc. It's good to identify the possible states the component can be in which ultimately can help inform you what to do.

### Two parts: (1) Hiring. Everything seems to be a unicorn. How do you manage this? (2) Why aren't traditional computer science programs integrating front-end?

- **Estelle Weyl:** Not going to answer the second one because CSS didn't exist when I went to college. I've been in the workforce for 28 years. And the thing I discovered is that you should be looking for the right boss / environment you want to work. You are choosing them as much as they are choosing you. I don't interview at places that do whiteboarding.

- **Michael Rog:** Self-awareness is key. Really examining what the day to day existence in this organization looks like. Hire the person for what their day to day really looks like. If they need to whiteboard and debate algorithms, then definitely integrate that into the interview.

- **Harry Roberts:** Unless you need someone strategic, if you just need staff, go after junior developers! They have boundless enthusiasm and aren't burnout. Don't abuse or manipulate on this, but know that they are coming to work hungry. They are not usually set in their ways, which is contrary to someone senior who could be hard to integrate into the organization. Optimize for the role.

- **Mina Markham:** Everyone wants the unicorn but no one wants to train them. Smart people are capable of learning and can be taught any skill they lack. I am not great at JavaScript which closed a lot of doors for me. It was baffling to me because I'm great at learning if you give me the chance to learn. The answer to get them to stop looking for unicorns is to remind them that you can teach them and give them the skills that they lack.

- **Val Head:** My impression is that most people who make the CS degrees is that they think front-end is beneath them. Also, for the people who don't think that, it's hard for them to change the curriculum quickly. Unfortunately universities are just hampered by this.

- **Stephanie Hobson:** Courses need to be approved six months in advice. Frameworks live and die in that amount of time. 

- **Dave Rupert:** I could go get a CS degree or just go to a bootcamp and then get a job as a Junior React Developer.

- **Brenda Storer:** In bootcamps, the emphasis is on JS. They give you like a week for HTML and CSS. This is scary.

- **Stephanie Hobson:** What is being taught right now is that you can make an website in week 1.

- **Jason Pamental:** Teaches a class and it is currently under the design umbrella. Finding a way to bridge the gap between a design problem and a computer science problem is key to resolving it. 

### Can you talk about A/B testing and the hit on performance?

- **Estelle Weyl:** Don't test all the time and test everything. Test only what you need for a small group at a time.

- **Stephanie Hobson:** MDN does testing with TrafficCop (only useful if you use Python). It is HTML that is different and not using JS in order to do A/B testing.

- **Harry Roberts:** Client-side A/B testing is the devil because it makes everything slower. One particular tool asks you to paste an inline script that makes the entire page invisible then uses an external script that loads asynchronously and then makes the change and then removes `opacity: 0 !important` when it is done. You could click on things still but it was a huge single point of failure.

### Following up on the tag manager / tracking is evil question, how do we manage the relationship between business and developers?

- **Wes Bos:** Somewhere out there, there is marketing conference telling your developers to "just put this line of JS into the code." As much as we want to rally against it, you have to remember that you are on the same team and sometimes a slightly slower application could. Your job is to make it as fast as possible to get the best possible result.

- **Michael Rog:** It's not so much that A/B testing is evil. Big block of JavaScript is evil. It is our job as developers to have empathy for why we're doing what we're doing and solve it in a better way. Not convince people that they don't need this.

- **Harry Roberts:** Be conservative about what you do and educate people. The actual client who had that issue is that it is a nightmare scenario. Maybe the difference is worth that potential failure? Try to think of things as far as weighing the potential benefit versus the risk of the nightmare scenario.

- **Jason Pamental:** If they get that tool, they should use it responsibly and we have to be teachers as far as not simply complaining and educating them that we're ultimately just looking out for the health of the organization. Our end goal is for it to be successful. It's not set and forget it. It's "Yes you can have this tool, but this is how you use it properly."

### Do you have any advice for freelancers getting started?

- **Estelle Weyl:** Recommends finding some non-profits and joined a small-business group. You don't want to give away your service, but maybe cut your loss a little bit, and then increase with each transaction. The more you charge, the more the client trusts you know what you're doing. One trick I used when I didn't have many clients, I called places who were hiring for the things 

- **Wes Bos:** I've actually never had a job. I've always worked for myself. Call yourself a consultant, you can charge more. The thing is you need to be extremely visible for clients to find you. You need to appear as an expert.

- **Sarah Drasner:** I put out a ton of articles and open source things in the stuff I wanted to work in. Do a bunch of stuff in things you want to work on so people will actually pay you for it. The best piece of advice I ever got on being a consultant was from Val [Head], "If someone takes longer than 4 hours to negotiate signing a contract, they will prove to be a difficult client." You can tell in the initial stages how it's going to go.

- **Miriam Suzanne:** I have no degree. If you work for yourself, no one cares. If you have a portfolio, that's all that matters. Take on a part-time job and only take the clients that showcase what you want to do. Taking shitty clients is only going to get you more shitty jobs.

- **Jason Pamental:** The type of work you showcase is the one you want to do. You want to develop a reputation for the things you love to work on.

- **Val Head:** I did the same thing as Miriam. I was in a job that I didn't want to be in and converted to part-time and found clients in my free time. Don't rage quit your job. Just rage go part time.

- **Michael Rog:** Working on your business. Now you are simultaneously worker and manager. The important job of a manger is to put their people in a position to succeed. You are now responsible of that for yourself and to block out time to think about the work you are going to do and being self-aware of your finances and the lifestyle you want to live so that you can figure out how much you need to make to live the happy life that you want to have. It means having empathy with your clients and what they need, but you also need to give yourself mental space to set yourself for a cycle of success and not escalating stress.

- **Harry Roberts:** Don't be ashamed to ask for work. I offered to help with Etsy and Google half-joking and ended up getting hired / paid for the gigs.

### At your level, do you still deal with imposter syndrome? 

*Widespread laughter*

- **Paul Grant:** This was my first professional engagement for speaking. You have to understand that you know what you know. You've worked hard at building up a skillset. You got the job done and keep getting paid, so you must be doing something right. So someone is recognizing that you did the skills you said you could do. 

- **Estelle Weyl:** Almost everyone suffers from imposter syndrome. You need to realize that there are people who are actually imposters. This means you know you don't know everything and is a good thing as long as you don't let it wear you down. If you think you know everything, you stop learning.

- **Mina Markham:** I'm actively having imposter syndrome as I sit here next to Harry Roberts and in disbelief. The way I dealt with it is that I reminded myself that I was hired for a reason and that I'm still here. So I drowned the outside noise of measuring yourself against someone else. That was a big lesson to just focus on what you know how to do and that you are accomplishing the task I was given and that people are happy with the work that I am doing. 

- **Stephanie Hobson:** We never get over it. The thing that helps me speak with authority is that everyone is a specialist in something. It feels like everyone knows so much stuff, but I'm the expert on making tables. Even though I may not know as much as I would like to, I am proud of the things that I do know about. Take comfort in that you have gotten good at something, and that you can get good at those other things.

- **Jason Pamental:** It doesn't matter how long you have been in the industry. The only way you can get up in front a room to come in a room and say something of value. I always try to focus on hoping that someone is going to say something in a Q&A will teach me something. This makes it better because this keeps you honest and helps with burnout because you know you'll get something every time you give something. These events really keep me happy in my job.

## Memorable Quotes

- [ ] Need to process everything I typed before I fill this out
