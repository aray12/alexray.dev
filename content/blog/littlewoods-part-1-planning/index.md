---
title: "Littlewoods, Part 1: Planning"
date: "2019-01-05T22:12:03.284Z"
description: Overview of inspiration, concept, and planning for Littlewoods, our home for degenerate friends to gamble.
---

For the last several years my buddy Matt has hosted a betting pool for [The Masters](https://www.masters.com). Originally, we would all get together via -- virtually or in-person -- and draft. Once we had the board setup, it was up to Matt to send daily updates to the group. These updates were calculated manually... As a result, the updates were error prone. Probably more importantly though, they failed to foster that endearing and competitive environment filled with a bunch of shit-talking buddies. How were we supposed to marginalize a friend's intelligence during Sunday's action when we don't know who is leading? 

Seems like this is clearly a problem that a little bit of technology could solve. Matt would typically set up a Google Sheet that would calculate scores based on his inputs. I took this base and ran with it. Instead of manually inputting data, I found a "public" API with leaderboard data. From there I built a macro that maintained our own leaderboard based on this "public" API. Finally, we used vlookups and some basic calcs to determine scores. 

To be clear, this solution works. I wouldn't call it perfect, but it works. That said, I had always wanted to take the idea and build a web application. A web application would improve some of UX issues with Google Sheets (slow, debugability, UI limitations), but it also opens up so many other possibilities (message board, Twitter integration, dope live draft).

---

This is Part 1 and is going to provide a general overview initial planning I've gone through prior to starting the project. There won't actually be any coding. 

- Littlewoods, Part 1: Planning
- [Littlewoods, Part 2: Real-Time API](/littlewoods-part-2-real-time-api)
- To be continued

---

#### So, why Littlewoods?

Pretty reasonable question... As the joke goes -- "There are two hard things in computer science: naming things and cache invalidation". I Googled "betting pool" and the Wikipedia mentions [Littlewoods as the first institution to use the concept](https://en.wikipedia.org/wiki/Betting_pool#History). That's it... 😎

#### What is the point of this?

So given we have a working solution to our basic use-case, what is the objective of this project? Well, I love when software brings people together. This is an opportunity for software to help unite different friend groups located across the country for a weekend. Also, I want to play around with some different tech and I don't feel like building a Todo App...

**So the project has the following objectives:**

1. Build an MVP
2. Gain some experience in new tech
3. Host it for FREE!

### Build an MVP

From a development perspective, I want to treat this like a work project. We should define the core problem and solve for that only. What is the minimal amount of development we can do and still produce something useful? There are a bunch of things that would be cool. We could build a live draft that removes options as they are picked and auto-drafts based on current vegas winner odds. We could add a message board for some friendly shit-talking. But those aren't the true pain points that inspired the project. 

**So I have settled on the following problem definition:**

> Participants want to view the status of the pool in real-time from any device

Base on that we can define the following functional requirements

- A user should be able to view the most up-to-date pool leaderboard
- A user should be able to view the most up-to-date tournament leaderboard
- A user should be able to view everyone's most up-to-date team, which includes position and points

### Gain some experience in new tech

The last time I did a deep dive into the general React and JS ecosystem was years ago. I think it'd be fun to explore and dive into some tech I have been watching recently. Some possible options are:

- TypeScript
- Next.js
- Netlify
- Firebase

### Host it for FREE!

Basically, I don't want this to cost me anything. 

### Roadmap

As I evaluate this idea, there are definitely features I would like to include. The intention is that we get the MVP working and then iterate on top of that. This is not a immutable path forward. There should be constant re-prioritization at each step.

1. **Authenitication**: the MVP will be accessible to everyone using a browser! The URL will probably be somewhat random, but still accessible. Since this is purely for viewing that is fine for the MVP.
2. **Live Draft**: I would love to be able to conduct the draft from directly in the app.
3. **Message Board**: a lightweight messaging feature would promote group "involvement". I am not totally sure of value here since most people already have a plethora of group messaging apps available. Might be unnecessary.
4. **Twitter Integration**: a simple Twitter feed would keep people updated even if they don't have time to actively watch the tournament all weekend.