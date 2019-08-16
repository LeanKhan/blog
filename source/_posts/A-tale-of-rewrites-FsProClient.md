---
title: "A tale of rewrites: FsProClient"
date: 2019-08-16 00:25:27
tags:
  - fs-pro-client
  - frontend
  - code
  - yarns
categories:
  - technologies
  - fs-pro-client
---

# A Tale of Rewrites: FsProClient

<!-- TODO:
    - Ask about this title
 -->

#### _What is Fs-Pro sef?_

FS-Pro stands for Football Simulator _Pro_. Pro doesn't have a particular meaning yet. At first it was 'professional' but that sounded too serious. It'll come.

<!-- TODO:
    - Add image of initial site
    - Add link to football-simulator repo
 -->

FsPro is a football manager simulation game kini. I and my brother have this football game we play, but it's only a simulation. We use dice to simulate results and record them with pen and paper: with league tables and all. One Friday February 22nd, 2:17pm I decided to automate it. What started out as a simple js file to randomize match results has turned into this _really awesome coding exprience!_. For those few weeks when it was called 'Football-Simulator' I never wrote so much javascript in my life (I haven't been writing js for that long anyways; < 1 yr>), I stretched my knowledge of CSS and frontend development so much, I loved EVERYTHING. It was rough and gritty but it worked.
I created an Express server to serve the `index.html` page with one javascript file and connected it to a MongoDB database, we played our three leagues and everything was fine.

Until we wanted to add more functionality.

<!-- TODO:
    - Add images of old app here
 -->

We wanted to make it realer. This meant:

- Increasing the number of players to 11 from 7
- Adding functionality to buy, sell and trade players
- Add web sockets for real time communication between managers (us)

<!-- TODO:
    - Add image of file structure under
 -->

Each part of our app was a separate html file so it meant I would have to register sockets for each page? tough.
Then there was the Transfer Hub. Where you can buy and sell players. As I began working on it I noticed more and more parts of the app needed to be dynamic and I was repeating A LOT of things. I was stuck tbh. I started making the transfer hub April 20th. Didn't do anything till May 23rd. Then on May 25th, I couldn't continue.

<!-- TODO:
    - Add links to Vue website
 -->

#### I decided to rewrite it in Vue.

_gasp_

I know.

> #### _So Vue innit?_

I chose Vue because I liked it. Using a framework meant I wouldn't have to repeat code and I it's easir to make some things dynamic. But I missed writing my JavaScript _vanilla_ yunno?

Other pros were:

- Better routing
- Faster development
- Babel. Meaning I could run it on the old iPad we used for testing

My setup was Vue + TypeScript because I wanted to share classes and interfaces with the server.
But mehn, setting up was not beans.

Things were going alright until I was adding more views. I didn;t know how to structure my codebase in the form of 'modules' so I could separate concerns and all. That bothered me for a while. So...

#### I decided to rewrite it in Angular _hohohoho_

<!-- TODO:
    - Add links to Angular website
 -->

_gasp x2_

I knowwww.

> #### _Beht why tho?_

The first framework I used was Angular. I started learning Vue after I got frustrated with Angular and its complexity. But for a few months now I have been working on a team whose main frontend stack is Angular. So obviously I had to use it then. During that time, I began to appreciate the framework even more. We were building a large scale enterprise app so I got to see Angular being used in that capacity. It was during that time that I decided to move it to Angular.

The pros of choosing Angular:

<!-- TODO:
    - Add emoji here
 -->

- It's modular architecture is perfect for FsPro. It's easier for me to understand.
- Supports TypeScript out of the box. - Awesome!
- It feels more 'solid'. (not an actual pro) lol

<!-- TODO:
    - Add links to Nebular
 -->

So that's the setup now. Angular 8 + Nebular UI system. The repo is public from the onset because I need epp.

Find it {{ here }}.

I am so proud of what FsPro is turning out to be, it has great potential. I don't even know what it really is yet.

From February 22nd when I made the first commit in Football Simulator to August 14th when I initialized FsProClient, we have tried. Hopefully no more rewrites :)))

> #### _wawu, so if this is FsProClient what about the server?_

Read about it {{ here }}

<!-- TODO:
    - Beg Joshua to review it.
    - Rename the screenshots appropriately and add them where necessarry.
    - Add emojis where appropriate
 -->

Thank you Jesus! <3
