# dev-journal
Journal for tracking my dev progress

6.6.2023
- [useReducer](https://react.dev/learn/scaling-up-with-reducer-and-context) quick TL;DR
<img width="886" alt="Screen Shot 2023-06-07 at 2 25 56 PM" src="https://github.com/ploymahloy/dev-journal/assets/48275526/4168927a-199f-402c-bbc2-26b58fca81de">


6.5.2023
- I'm creating a drag and drop app for future reference based on a tutorial using tailwind, and I learned that Vite has a different set of installation instructions. I'm glad I finally figured that out. I was really about to lose it.

5.31.2023
- As of yesterday afternoon, I got a job working with my mentor! I'm very excited to be working again starting next week. Time to have my celebratory cigar!

5.28.2023 
- I built my first carousel component! This project is teaching me a lot. The one thing I can't seem to figure out, so far, is how to add transition animations. I know that in CSS you can add `transition: property time(s) transition-timing-function` to create a smooth effect. I've used this technique to add transitions to my hover effects. What I need to figure out is how to make my sidebar slide open (as opposed to jutting open), and fading my carousel controls in and out.

5.25.2023
- Just spent 40 minutes developing issues for Ethereal TV's streaming app. I'm going to try to keep a record of how much time I spend on what so I can determine where I need to improve. (Development) time is money.
- Finished building the sidebar component. I'm going to plow through these easier parts since I know there will be fewer, if any, obstacles along the way. Next up: footer.

5.22.2023
- Had a call with my mentor. He could use someone to do some front end work so he's trying to get me in. Something is going to happen soon!

5.21.2023
- I was able to confirm that `react-dnd` is the best option for making a Trello-style kanban board. I'm excited to get one of these components completed!

5.20.2023
- I've started using Vite to initialize and compile my React Typescript projects. I discovered the hot reloading colloquial for Hot Module Replacement (HMR). I like the idea that I can use the same tool to initialize a Vanilla, Vue, React, or Svelete project, AND have the option of using the Rust-built SWC. I'll explore that another day. I want to get this drag and drop functional. Once I do that, I'll have the hardest part (newest technique to me) in motion.
- Dear Lord, I just wasted over an hour trying to get 2 deprecated libraries to work in my app. The worst part is that the second library is the "updated" version of the deprecated one...but they're BOTH deprecated! So annoying. I took a break, and am going to take a stab at `react-movable`.
- `React-DnD`; final answer.

5.19.2023
- I'm realizing that this management app has so many potential starting points, and I am over-analyzing what I _should_ start building. Unironically, I chose to start building out the kanban board as the only thing I need to learn there is drag-and-drop. From there, I can easily track the progress of my own management app using the kanban board. I'll probably do some user authentication afterwards just because it's been on my list for some time now, and the product WILL require authentication.

5.16.2023
- Just redid my resume. Paul at Microsoft is giving it a second look. What a guy!
- Every day I've worked on this app I find that I need to learn yet another new way to visually represent data. I'm going to use D3.js to make this happen. Hopefully, I'll be able to use it for all charting; including the world map.
- I found code for native dual input sliders. I'm thinking a `readonly` version of this could work to represent availability on the ScheduleSync, but it's probably not going to be ideal. [CodePen](https://codepen.io/predragdavidovic/pen/mdpMoWo)

5.15.2023
- My cat, Charlie, died on Friday night. It really messed me up, but I've made my peace. 
- I spent quite a few hours researching how to make various charts. I think I'm going to use D3.js for the world map, but will start with the easier aspects of the app.

5.11.2023
- I got started on the Global Team Manager. I used a navy blue/seafoam green color scheme, and will use React Router to render components as "pages" while maintaining a navbar. 

5.10.2023
- I declared that I would be creating the Global Team Manager as my first product on LinkedIn last night. I'm excited to see where this takes me. I will have a great many challenges, and am excited for the journey ahead.
- The more I think about it, the more I want the `navigator.userAgentData.mobile` property to be supported better since it's such a powerful solution to a common problem. Apparently, I can contact the browser vendors directly or contribute to the code if allowed. I'll ask Jesse.

5.9.2023
- I discovered that I can use `var isMobile = navigator.userAgent.match(/(iPhone|Android|BlackBerry|Windows Phone)/i);` to determine whether the device accessing the site/app is mobile. I saw that there was a property `navigator.userAgentData.mobile: Boolean`, but it lacks the proper support to be fruitful; despite the fact that it is significantly more specific than `userAgent`. Nonetheless, [it works](https://codepen.io/ploymahloy/details/yLRKQqo).
- In the process of making the above discovery, I stumbled upon [this PDF](https://www.cs.virginia.edu/~up3f/cs4640/slides/4640meet09A-JS-object-DOM.pdf) diagramming the details of the Browser Object Model.
- Ran into a weird issue last night with the Keep clone. Everything is straight with it except the Modal keeps telling me `open` is declared, but I changed it because `open` is a reserved word. Now, I get an error when the value is named `open`, and I get a different error when the value is named something else; like `isOpen` or `modalIsVisible`. I'm going to consult the Oracles tomorrow and see what they think. Might as well post it on Stack Overflow tbh.
- I'm starting on the Global Team Manager. I've been hesitant since I don't know how Three.js shaders work, but I can start with a carousel showing each time zone as a png to start; THEN add the 3D globe with highlighted timezones. I'm really looking forward to this one as I already have an interested client!

5.8.2023
- Managed to get some more time with Mr. Warden. He helped me figure out why my app wasn't working.
  - Problem: Delete button deletes last note in array; not the selected note
  - Cause: Data was fine, but rendering was not. I was setting state in the Note component instead of passing the changed state up to the App component. This was causing the UI to bug out as the old note was still showing in the list.
  <img width="533" alt="Screen Shot 2023-05-08 at 9 30 19 PM" src="https://github.com/ploymahloy/dev-journal/assets/48275526/bd6a13b7-2454-4d71-a154-2ef06e6771a9"><br>
  - Solution: Pass state up to App component via functions. Not sure why I found this part difficult, but I know that I wanted to shape the updated note as an object; which was not doing me any good. One task at a time, no need to overcomplicate it.
- Tomorrow, I plan on adding a Node/Express backend to communicate with a MongoDB or SQL database. I haven't really decided, but as I write this I am leaning towards a document-oriented database as Google Keep is essentially a collection of documents. I'll review [this list](https://www.g2.com/categories/document-databases) tomorrow after my screening with Pocket Properties.

5.6.2023
- Had a 3 3/4 hour call with Jesse learning serverless with AWS. I have my notes on my local machine so I won't go into too much detail here, but I know that AWS Amplify takes a lot of ops work out of the equation. Once I finish the Keep clone (add a SQL backend), I think I'll give serverless a try when I create the filesharing app.

5.5.2023
- Just learned the basics of Redux via [this article](https://www.freecodecamp.org/news/redux-for-beginners/). I think the most surprising thing that I learned was that Redux is not specific to React, but JavaScript. In other words, I can use Redux in Vue! A challenge for my Vue music app perhaps? I meet with Jesse via Zoom in ~11 hours so I'll ask him what he thinks. I vote yes: good opportunity to practice Redux.

5.2.2023
- I'm going to my first conference! I'll be wearing my networking hat for sure. I'm glad that I was able to get all my fixes completed before going so I can confidently share my site with people.
- For some reason, the mobile resume link on my site was still linked to a relative path so I set the link for both the desktop and mobile menu to a constant with the value of the link<string>. I noticed a bunch of repeated code so I'll be working on that at some point, but the more pressing matter is adding an overlay for the mobile menu, and adding framed app demos (just found some templates!). Very exciting. 

5.1.2023
- Got to make some much needed changes today. I changed my profile pic on my website, fixed the Keep clone link, made my resume open in a new tab instead of hijacking the current page, and homogenized tooltips as there was a mixture of these three: `*JS, *.js *.JS`.

4.30.2023
- I found a really good post on how to dynamically generate the document title in Vue via [this post](https://stackoverflow.com/questions/62023604/where-to-find-or-how-to-set-htmlwebpackplugin-options-title-in-project-created-w). It goes into 6 different ways to do so! Saving this for future reference, and to my future self...you're welcome!
- I'm about to make a video on this and post it on LinkedIn. The Split HTML Attribute extension is great! Highlight, then use `Ctrl + Alt + Shift + A` to separate the element's attributes. Order of attributes can be customized, as can placement of the closing tag. Nice!
- I was also looking at iPad development in case I ever actually travel. It looks like GitHub's [Codespaces](https://code.visualstudio.com/docs/remote/codespaces) can be installed as a PWA! I'm going to try using it with a simulated network connection interruption and screen record the results. More video ideas! Yay!

4.27.2023
- To get myself excited about coding for the day (or first this part of the day) I ran with an idea that I had. I thought, "I wonder how I can code a knob like you would see on a guitar amp or in a DAW?" I think I'll eventually try to use Tuna.js and Tone.js to build a simple audio effects processor, and maybe a full-blown web-based DAW at some point with cloud storage and stuff of that nature.
- After going back and forth for about 30 minutes I was able to get the types right for all my event types in the Keep clone. onChange gets a ChangeEvent type, the form submit handler, onBlur, is type FormEvent, and the keypress handler is type Keyboard Event. Now that ChatGPT and Bard are at my disposal, I think I'll be able to learn types faster. Otherwise, I'll be drowning in docs and StackOverflow posts. Next step is to fix the id update failure.
- 45 more minutes later and I've removed fixed the modal display value bug by removing faulty edit logic, renamed classes to be simpler/less verbose, and fixed the modal's position on screen and size on smaller screens (without using a media query!), and fixed the favicon. All I need to do now is add the edit function, persist to local storage, then persist to a database and it will be finished (for its purpose).

4.26.2023
- I've been really dragging my feet on fixing the state-update bug in my Keep clone, but I at least know that, for my other project, I will be using react-globe.gl instead of three.js or D3.js as react-globe.gl provides me with many options that are easy to use. I guess it's more specific to the task I need it for. I still want to become competent in three.js as I find it to be incredibly interesting; regardless of the job market for 3D web devs.

4.25.2023
- I discovered [react.dev](react.dev/); which is much better than React Legacy docs that I have been looking at prior to this day... I am beyond perplexed that I managed to go this long without referring to the right documentation >.< Either way, I'm reading the docs and scanning for best practices related to props and state as I believe the issue with my Keep clone is that the state is not changing because the state is initialized with props.

4.20.2023
- I spent another day (yesterday) looking at three.js before moving everything to React. 
- Today I started the dashboard project. This will include a React Three Fiber globe where the user can select their timezone based on major cities representing timezones on the globe. There will also be a prompt to add team members to make global teamwork easier. I plan to include a view with the user and their team's timezones. Something like a card with each user showing h1: name, h3: location, h3: current time (except for semantic tags only!). Other features I'd like to implement are a messaging app, a project management tool, and a cloud storage system.

4.17.2023
- I had a second round interview with New Zealand dude. They seem to be in need of someone technically more advanced, but I told him that I was more than capable of doing 90% of the work in the first few days of the 1-month timeframe. With that being said, whether he is sold on me or not, I am also in the running for a role at Timmons with Jesse Warden! I really hope I get that as I think it would be lifechanging for my career.
- I started workinging in Three.JS! I got a wireframe sphere to render on screen. My next step (working on it tonight) is to add a countries layer over it to make progress on my timezone widget. <br>
![Image 4-19-23 at 7 34 PM](https://user-images.githubusercontent.com/48275526/233222256-85d2fdde-559c-4f64-87e0-59aa268c5888.jpg)


4.14.2023
- I had an impromptu interview with a founder of a startup in New Zealand. Looks like a challenging contract that could lead to a hire, but we'll see. Homie didn't seem to like the idea of using a contract? Again, we'll see.

4.11.2023
- I completed my new resume! I was really dragging my feet for some reason, but I'm really proud of my resume skills now. For future reference, I used [this](https://arc.dev/resume) site as a guide. I find that there aren't enough good definitive resources and every other recruiter/hiring manager looks for different things in their applicants' resumes. The aforementioned guide seems to boil it down to the basics; which I very much appreciate. I need to add it to LinkedIn, and replace the Resume link button on my site to a download.
- I finally did it. I took the plunge. I have begun learning three.js! After years of wanting to, but "not having the time," or whatever other excuse I've had, I'm finally investing time into a technology I really enjoy seeing. I need three.js for a business idea of mine that will be best served with a three.js-infused site. More details to come!

4.10.2023
- I was introduced to spleeter (eventually used mySpleeter) today and had some fun using it. I've always wanted to isolate the drums from certain songs as I have future plans to do a cover song YouTube channel, and I could never find free software to make it happen. As it turns out, this AI project does a fanTASTIC job and I highly recommend it. Not so much coding, but more of what portion of my day was influenced by code.

4.9.2023
- I discovered that, in Bash scripts, the `!` character needs to be escaped as shown below (otherwise `dquote>` will rear its ugly head): <br>
![image](https://user-images.githubusercontent.com/48275526/230819787-069f9419-c236-4b6e-9329-fed37b271b65.png)

4.5.2023
- Back on the job hunt. Fucking CRC, man. The Glassdoor reviews were awful and I can see why. So much micromanaging! A meeting dedicated to making sure we track our activities down to the 1/4 hour? Really? How about we get the devs to reports what they did the next day in stand-up like a normal dev team. Yeesh. Anyway, I'm relieved that I no longer have to pretend to appreciate C# even though TypeScript takes the good aspects of a type-system to make JavaScript code safer, among other things.

1.22.2023
- Did some work in [Rust by Example](https://doc.rust-lang.org/rust-by-example/index.html). I really like that there's a built in IDE and compiler so all the examples and exercises can be performed on the page. I highly recommend this for anyone learning Rust.
- It appears that in my efforts to help pre-career Junior Developers, I have acquired a mentee. He's in Bengladesh, and knows JavaScript and Python. He likes doing Leetcode, which is great, but he expressed his lack of understanding in where "the bar" was, as he stated, in terms of portfolio projects. I showed him my portfolio site, and told him that he should build a [landing page](https://games-market.vercel.app/) and deploy it (he doesn't have any deployed projects). He seems driven so I'm excited to see what he comes up with.

1.21.2023
- I downloaded [rustlings](https://github.com/rust-lang/rustlings/) and was reading through code, and realized the great possibility that I was wasting my time in learning the wrong technology for my product, despite ChatGPT and other sources stating that Rust is perfect for writing memory-safe firmware. 
- This led me to research [Firmware vs Embedded Software](https://www.andplus.com/blog/firmware-vs-embedded-software-what-s-the-difference-). After reading this, it affirmed my initial thought that what I need to write is, in fact, firmware. Ergo, all I need to do is learn Rust. 
 - After more research, I found out that Rust not only can create a GUI, but Rust allows for signal conversion, and a certain output connectivity (that I was worried about and will share once I have a patent). As of today, I am 100% on board with Rust and can focus on learning the language without any uncertainty in whether it's the right tool for the job. This is probably why it's a good idea to read about a language in context of its primary uses, community, ecosystem (frameworks and libraries) etc. before diving into learning a language. Unless you want to learn a language with no other motivation than "because you want to," it may not be the right tool for the job if you don't do your research. I got lucky from half-assed research.
 - On that note, I popped open the [Rust Playground](https://play.rust-lang.org/?version=stable&mode=debug&edition=2021) and started my evening's coding journey by writing a for loop. Nothing too crazy, but studying the syntax of this will help me in the long run. Strong foundations support great structures. Also, I can't eat a cow in one sitting, but give me a year and I'll make easy work of that cow; one steak at a time.
<img width="736" alt="Screen Shot 2023-01-21 at 9 33 54 PM" src="https://user-images.githubusercontent.com/48275526/213897964-6c2a955f-d743-4cb2-93c3-eaa02834e0bb.png">

1.16.2023
- Continuing along with the [Getting started - Rust Programming Language](https://www.rust-lang.org/learn/get-started) guide, starting with the "Adding dependencies section," I've learned that `cargo build` can be used to install dependencies; `ferris-says`, in this case.
- More dependencies can be found at [crate.io](crate.io)
- Terminology: Packages are often referred to as "crates." Rustaceans....crates....it's like a sailor wrote this language.
- After completing the "a small Rust application" section (copy/pasting the code), I ran the app and was provided with the output below. This concludes Rust's basic tutorial on the page (linked above) <br>
<img width="458" alt="image" src="https://user-images.githubusercontent.com/48275526/212725247-872c461b-02f4-4aba-a9ec-e27e121fc7bd.png">
- The crab shown in the console above is actually the Rust mascot, Ferris. It is named so as rust forms on iron; which is a ferrous metal.
<img width="458" alt="image" src="https://user-images.githubusercontent.com/48275526/212727204-efb58fdc-6ede-45f4-90ef-99540fc5dd20.png"><br>
- Starting off with this language, I will be focusing on the syntax of the language by writing basic for loops, for example. [Rust by Example](https://doc.rust-lang.org/stable/rust-by-example/) <-- this page will be able to provide me with examples of how Rust code is written.


1.15.2023
- I've decided to become a Rustacean! This will allow me to build audio plugins and firmware for my super secret guitar product that needs to be patented before I share any more details.
- I started my process here: [Getting started - Rust Programming Language](https://www.rust-lang.org/learn/get-started)
  - I downloaded Rustup, which is the Rust installer and version mgmt tool
  - Rustup comes with Cargo, a Rust build tool and package manager
    - It took me a good 3 minutes to remember that "build" refers to building an app for deployment...not creating a new app. LOL we're off to a great start here, folks. At least I know what `cargo build` does now. To make a new project, you run `cargo new <project name>` in the command line. I so miss working in the command line. My current role does not necesitate command line work. Not a bad thing, really, but we're creatures of habit.
- Got me a working command line app! Can't say I did much as the boilerplate code is "Hello World!"; which is the lamest barbed-wire tattoo shit ever. I changed it to "I'm Alive" because my apps will resemble Frankenstein's monster during my learning phase.
<img width="685" alt="image" src="https://user-images.githubusercontent.com/48275526/212582945-ae8aabe1-5359-4df1-89ae-d3466cdd4896.png">

===== Landed Dev Job 12/5 ======

11.12.2022
- Google Keep's card layout has always fascinated me as it was staggered and somewhat chaotic yet still very organized in its aesthetic. I couldn't figure out what it was called to even search for it, but I finally discovered that it's referred to as the masonry layout/masonry grid. Frameworks that help create this effect exist, but I like doing things myself and having total control so I found [this Codepen](https://codepen.io/kreigd/pen/KRYzdd?editors=1100); which is pure CSS.
- In other news, I deployed the Game's Market site without a hitch, surprisingly. All I really need to do is get the mobile menu functioning, which won't be hard. That and maybe redesign the layout of the About/Contact pages as they're not in-brand with the home page...and kinda suck tbh.
- Lastly, Rebecca from Robert Half reached out to me and we got on a call. I tweaked my resume to her suggestions (which were very welcome) and I'm hoping to get this Junior Dev role she has. It's a JSON developer role (LMAO) that pays $50k, which is somehow a staggering 20% increase from what I make currently. It's amazing how I can make more waiting tables part time than work full time at a damn Fortune 500 company with access to all their employee's data.

11.11.2022
- I always have trouble getting TailwindCSS installed properly in Next projects. To prevent myself from wasting time with this ever again, I'm attaching an article that ultimately saved me from sure insanity: [Debugging Tailwind CSS](https://blog.logrocket.com/debugging-tailwind-css-next-js/#setting-up-next-js-project-tailwind-css). Also, I like this sense of only logging TRUE progress. I don't want this journal to have any fluff. I might even trim it down but who cares. Not my db, not my problem.

11.8.2022
- I've been so busy focusing on building projects I forgot all about this journal. I took a step back from the Keep Clone as it was too difficult to implement an editable modal. I have a scratch project that contains code for an editable input field that I'll use to figure out how to implement into a modal. 
- In other recent development, I have started building a modernized version of Game's Farmers Market site. Their current site makes me cry, so I took that as inspiration.

10.29.2022
- I want to work with other developers ASAP so I forked 'first-contributors' and went through their tutorial. Fortunately, I'm comfortable with git and went through it without any trouble. 

10.26.2022
- I've been forgetting to log my learnings. My keep clone is coming along, but I realized that I've never truly implemented an edit function so I need to figure that out. THEN, I can link the mongodb database and deploy (nervous that it will take forever to figure that out with mongodb).

10.22.2022
- My dev journal came to the rescue! I couldn't get my modal close function to work in my Keep clone, but I remembered that I had the same issue in my Next Template project. All I had to do was pull up this journal, search 'modal', and I was able to find the solution! I'm so glad I started logging my progress.

10.20.2022
- Someone that's super SUPER new to development (no React experience) just got their first job so I'm definitely motivated to start applying again. I did some serious work on this keep clone today. I did a bunch of small things like box-shadow on hover, icon button background color matching...bunch of UI stuff, but was also able to recreate the form functionality from the project organizer sigNIFicantly quicker than the first go-round. It's great to see my progress paying off.

10.19.2022
- I began working on a new project. Persist: a Google Keep clone. I need more high quality, complex applications in my portfolio. Everyone has a todo app. Everyone has a weather app. I need to build that API, build that social media app, chat app, etc. if I want to stand out. Polishing my resume would help.

10.18.2022
- I built my first app at work today! I was getting sick of combing through spreadsheets for unique numbers so I made a program that filters through repeating numbers. I saved myseylf an easy 3 hours by doing this. I'm very happy to have done this AT WORK!

10.13.2022
- Working on my portfolio as a whole, I'm trying to make some small tweaks. I have a note taker from a bootcamp lesson we did and it is TRULY amazing how bad it is. The worst part is that we were provided the front end! UI is horrible, but fixing it was easy. Glad I fixed it.

10.9.2022
- Did some coding these past few days but just was not inspired to log my progress for whatever reason. Today, I address the button link color issue, and ended up fixing them and making some other improvements to the site along the way. Tomorrow I plan on converting the sidenav to a modal so I can add the detectOutsideClick hook and a backdrop. From there, I will more than likely implement a dark theme option switch (very excited to create the dark theme!!!).

10.5.2022
- Of course the day after I post about not making it a goal to code every day I make it so that I am, unintentionally. I guess the reverse psychology works! Anyway, I did a MAJOR overhaul of my personal site and am very proud of it. My next step is to work on my resume.

10.4.2022
- I'm definitely starting to take a step back to analyze where I'm falling short; not just in development skills. I'm also no longer concerned with coding every single day, but making meaningful progress every day that I can. Putting so much pressure on myself is why it's taking me so long to begin my career in the first place. Everyone is getting calls for interviews but me, it seems, so I went back to my portfolio site and started working on its appearance. Progress pic (ignore the Fill Murray):
<img width="1277" alt="Screen Shot 2022-10-04 at 10 33 23 PM" src="https://user-images.githubusercontent.com/48275526/193968932-532f892a-0eb3-42e7-b2d4-51d1ebf6d213.png">

9.30.2022
- This is becoming less of a dev journal and more of a dev job application tracker. Since my last entry, I've applied to 7 roles, and started networking with recruiters, hiring managers, and fellow job-seekers. In other news, I began coding in C++. I went through Mosh's C++ for Beginners video on YouTube and was glad I didn't skip over the basics. Now my more immediate objective is to build a vst plugin using the JUCE framework. The only problem for me is that I don't have a way of initializing a JUCE project in VSCode it seems so I may have to just download XCode just to follow the tutorial. 

9.28.2022
- I signed up fro Dev.to and Twitter today. I did so as a recommendation from an accidental LinkedIn connection. I was so eager to network I didn't realize that he was also on the job hunt. Fortunately, he was kind enough to offer me job hunting advice. He told me my portfolio was solid and more than enough to get contract work. Very good news.

9.27.2022
- Worked on learning C++ today. I'm also looking at part-time and contract work. I want this so bad.

9.26.2022
- Haven't taken a week from coding since I was understaffed at work. I gotta say, I'm extremely discouraged with the lack or response I've gotten from my applications. I can't seem to get anywhere in development so I'm probably going to start applying to IT roles just so I can start making some actual money. I at least worked on my website's navbar; though, I can't say I really got anywhere.

9.19.2022 
- After taking a few days off for life things, I started my portfolio refinement process by adding margins to the cards of the Project Organizer. I officially can't stand Bootstrap. Sass >>>>

9.15.2022
- Today I applied for a few more jobs, started learning D3.js, and refactored my Project Organizer.
  - Job Apps: I've noticed a few companies will tell you exactly what to expect from your time there before applying, while some job postings are just a jumbled paragraph of requirements and expectations. The clear winner, in my mind, is the one that takes the time to show off their transparency in a legible format. High standards go both ways, why should I work for a company that can't provide a decent job description?
  - D3.js: I had no idea that D3 was a DOM manipulation library! I thought it was just used for data visualization, but it is very similar to jQuery. The whole point in learning this library is so that I can create a decent chart for the Mortgage Calculator. Otherwise, I WILL delete it from my portoflio as it is extremely underwhelming in it's current state.
  - Project Organizer: This project was decent to begin with but it had a few issues. For starters, and I didn't even notice until last week, the grid doesn't expand past 3 cards per row. This makes the layout of the grid look strange on larger screens. This alone taught me to consider that responsive design includes extra large screens too. Second, there were some unused divs that I got rid of. Lastly, the logo was too large for screens smaller than 300px so I fixed that, too.

9.14.2022
- I need to work on freelancing and open source projects to get a competitive edge in the job market. Somehow, despite a booming job economy, there are still too many dev applicants. I started my evening by revamping my basic calculator. It looks more modern, and less noob-ish. I'm going to take a good look at some of my other projects. I know that I will be removing the mortgage calculator as soon as I have something to replace it with, or figure out a decent way to create create a donut chart from scratch.

9.13.2022
- Worked on the sorting algorithm project. I'm starting to feel discouraged again and haven't been motivated to code since I got rejected from 150 <--- ONE HUNDRED FIFTY companies last time and I'm getting more rejections now. If this field needs workers so bad then why on Earth can't I get a job??? I've shown my resume to friends, family and colleagues, polished it almost 50 times now over the past 2 years, worked on projects almost every day....GOD.

9.12.2022
- I applied to 2 contracts for front end development. I would love to have both, but one of them in particular is just HTML. THAT would be a great thing to have just to blast through during my down time at work. Also, I found a HTML/CSS/JS Sorting Algorithm visualizer project that I plan on rebuilding in React. I think it would show a different level of understanding of how software works in regards to data processing. Anyone can learn HTML. Engineers learn about Big O. 

Notes for Alg project: Add time complexities and timer display

9.11.2022
- Youtube is filled with terrible tutorials. I thought I found the right one, but after the 30 minute video was done, I only THEN discovered that it was for a Shopify app that would exist within Shopify itself, not a standalone site that used Shopify and GraphQL on the backend. Either way, I sent a reply to the people at Vaan Group and I'm going to do some more applications today. I also tweaked the Basic Calculator as it looked horrendous.

9.8.2022
- I heard back from a job! It's an ecommerce business so I'm going to take the weekend to work on my nextjs-tailwind-shopify app in hopes that I will impress the hiring manager.

9.7.2022
- I went to the library and was able to run `create-react-app`, which confirms that it is my NETWORK that is the issue. How I'm going to fix this is beyond me. I hate networking. It's unbelievabley boring.

9.6.2022
- I dug up an old laptop and put node on it just to try running `npm install` to see if it made a difference. The download still hangs, but I am looking forward to diagnosing error. If nothing else, I'll go to the local library to run `create-next-app` and `npm install` just to move the needle forward.
- Apps sent: 4

9.5.2022
- Node/npm took a massive crap a day or so ago and I'm still struggling to understand what's going on. I managed to determine it is a network error so I'm convinced that I may need to do something DNS-related as it wouldn't be the first time. In the mean time, I finished my resume and added it to my personal site and am going to finish my linkedin profile. The job hunt begins immediately after; very exciting!

9.4.2022
- I've been battling npm for hours now trying to understand what's going on. I can't use create react/next app or ever npm install. I've tried SO many different things, and I'm about to just clone an empty next project and use a TailwindCSS CDN just so I can get something going here. Again, there's no real guide, just bash your head against the wall until something works and learn from it.

9.3.2022
- Not a whole lot to log today other than some reading I've been doing. I want to get better with Typescript, but I find it difficult to convert Javscript projects to Typescript when I can't figure out how to fix the errors; which makes it pointless. I'm probably going to write an article at some point when I finally figure it out because there is no real guide on how to convert Javscript to Typescript. "Fix the errors" <-- yeah great advice. Super helpful. Might as well be saying "be good at coding."

9.1.2022
- Did work to my resume. Just need to finish it, the drag and drop puzzle, get a domain name, then I'm set for applications.

8.31.2022
- I've been working on the drag and drop puzzle. The logic is from a W3 Schools page so I'm really just focusing on the layout at this point. I've been so unmotivated these past few days and I can't pinpoint why...

8.30.2022
- I tweaked the mortgage calculator a bit; just the font-weight and mobile repsonse. I was going to add TailwindCSS but it didn't seem necessary. I don't like the idea of adding something that won't greatly contribute to the project. In addition to the All Access Clone, I think I need to put the song maker on hold. I was so damn close but I just need to get a portfolio finalized and THEN I can get that finished. I'm going to do a drag and drop puzzle in Typescript to give me my lucky number 7(th) project. After that, finish my resume and start applying. I need a damn dev job already.

8.28.2022
- I was able to find a video on how to update array state and it was increibley helpful, especially since the state is stored at the app level. I'm going to do some work on the song maker, which will utilize that logic, and add an overlay to the sidenav on the next template and my portfolio site. So 1 straightforward task times 2, and then all in on my last project. 

8.27.2022
- I ended up not having the Next Template modal fixed, but made a journal entry stating that I did so in an attempt in encourage me to make it happen. It worked, I'm not happy about the whole process because it was a stupid mistake, but I got it. I was wrapping the Artworks in an anchor tag that had the open function, and because the modal was nested in the anchor, I was not able to toggle the open/close state. All I need to do is make that sucka responsive and we're officially done as it is already deployed. Of course, I'll need to make sure I update the build; which I haven't done with Next before. I may get a job in 2024 at this rate, Jesus, Mary, and Joseph.
- Got the Next Template project update and all that. The only issue is in the logo. For some reason that specific Google font is not working so I added a backup font just to put a band-aid on it for the time being. I'm very pleased to know that all I have to focus on for the remained of this process is the loop station/beat maker/song maker; which will ultimately be the death of me.

8.26.2022
- Just deployed the next template to Vercel. It was suprisingly easy, but the errors I had to fix didn't show until the build failed . The failures listed were stupid stuff like "you have to use a &983475 whatever instead of a `'`. Anyway, I need to finish the song maker so I can finally deploy my personal site and apply to jobs!

8.24.2022
- I committed my song maker project as is because I want to be able to overhaul how the `soundArr` is passed throughout the app. Right now it's being edited in the Instrument component and it feels like it's working, but I also am unable to lift the value up so it's useless in it's current form. I need to do what my friend suggested and create a global variable (or state) and then build from there. I'm starting to think that Redux will be a good thing to learn for this project since the array will be used in every component of the app. More than likely, I'll save this for after I add the modal to the Next Template so that I can focus all my time and attention on the song maker.
- I got the modal in NextJS to work! I was confident that this would only take a youtube video to get right since I already know how to make a modal in React. All there is to do is pass the image source from the `pathArr` in the home file to the Modal component, and add some well-constructed placeholder text. After all, this is a template. I'm very excited because this means I will have 6/7 projects complete!

8.23.2022
- After talking to my friend on the phone, who is a React wiz, he mentioned that I need to make the `soundArr` app-level state since it's being used throughout the app. It makes sense, but it means I have to scrap my current solution to toggling cell values from 8/19. At least I have a better idea of how to move forward. Other than that, I spent my time coding today on cleaning up repeating components. One example of this is depicted below in the Next Template project. I consolidated all instances of the Artwork component by looping through an array of image src paths and rendering an Artwork component for each index in the array using `map()`.

Before:
<img width="272" alt="Screen Shot 2022-08-23 at 11 18 56 PM" src="https://user-images.githubusercontent.com/48275526/186315186-3c23b7db-715b-47f4-9b6f-79dcd6fa3577.png"> 
After:
<img width="220" alt="Screen Shot 2022-08-23 at 11 18 00 PM" src="https://user-images.githubusercontent.com/48275526/186315144-bb7bb8b8-fa20-43e9-b87a-3c02c46e92e8.png">

- All I have to do is get the song maker fully functional, add modals to the artwork card components, and deploy then I'm job ready!


8.22.2022
- Today marks a month since I began journaling and it has helped my development tremendously! It offers great reference for past lessons learned, it removes the emotional nature of the programming learning curve, and most importantly, it offers me insight on my skill development that I might not have otherwise.
- I started going through W3School's Intro to Java. Many big companies use Java in their tech stack and I think it's a critical tool to have under wraps if I want to be competitive in their applicant pools. I'll spend more time developing in Java once I finish my portfolio projects.

Edit: I think I'll end up doing some basic Java project just to have, but my main focus once I get my first dev job is C++, namely the JUCE framework for audio plugins (Think equalizers and compression tools used in Logic, Pro Tools and Cubase).

8.22.2022
- I'm really close to finishing the Next Template. In the future I may redo the grid system with CSS Grid instead of Flexbox, but it works on all sceen sizes for now. The only reason to rework it would be to make the images larger on larger screens (>1700px), but it's definitely not a priority. I'm going to create a modal for the grid cells and commit the MVP. I'll probably have it deployed with a bow on it by the time I get off work.

8.21.2022
- Earlier today I was working on the song maker. I can feel myself getting closer to how I want to shape the sound arrays. I knnow that I need to pass the data up to the App component from the Instrument component, but I'm unsure as to how I was to package multiple arrays. An array of arrays is the first thing that comes to mind, but how do I loop through an array of arrays? More for tomorrow.
- Second thing I did was work on the NextJS template. What a pain in the ass! Next Image is the most frustrating tool I've ever tried to learn how to use. The fussing from that component dropve me insane. Fortunately, I was able to make it work and my template is almost done (after a few hours' work, I'm getting faster!)

8.20.2022
- I got my grid system to work! All I had to do was `.fill()` my array with `0` after I declared the length dynamically. Then, all I had to do was replace the 0s with 1s when the button was set to active. Initially, the issue I had was that I initialized an empty array, and tried iterating through the empty array with map to replace the empty index with the value of the cell (0 or 1). I learned, however, that you can't map or iterate over an empty array. This is why I chose to initalize an array of 0s. Now all I have to do is send `soundArr` and `instrument` to the `Playback` component; where I'll loop through the arrays to tempo (setInterval), and play the sound file for the instrument when the array's index is `1`.
![Untitled (3)](https://user-images.githubusercontent.com/48275526/185759228-15dd5814-354c-4ce6-9c21-691c38c28c35.gif)

8.19.2022
- I have gotten closer to getting the song maker's grid system to work. Each row represents an array with each cell representing an index in the array. When I click on a cell, the console logs that number in the array (the index plus 1 since i starts at 1 and not 0).
- I was also able to get the Play button to work using `setInterval` and used state to create conditional rendering of the play and stop icons. All I need to do is pass the Boolean value of the cells to their respective arrays
![Untitled (2)](https://user-images.githubusercontent.com/48275526/185723491-16164f10-a55b-413b-9c52-ca56b098e54e.gif)

8.18.2022
- I couldn't focus to save my life today. I was able to pseudo code the song maker, but will probably end up building something in Vanilla JS just to get it working. It's just a matter of connecting the logic below to the grid. Everything else I know how to do, but of course I'm stuck so I can't do anything until I fix this.
<img width="422" alt="Screen Shot 2022-08-18 at 9 38 25 PM" src="https://user-images.githubusercontent.com/48275526/185524049-963656b2-a7e6-4abd-b28f-119ffa0090e4.png">


8.17.2022 
- I made a simple virtual calculator to add to my portfolio. It's by no means impressive, and it's my third app with 'calculator' in the name, but once I figure out this beat maker and design a template for NextJS I'll have 6 solid projects ready to be shown to prospective employers. Can't wait.

8.16.2022
- In light of yesterday's quandry, I have decided to make a beat/song maker of sorts. Inspired by the [Punk-o-matic](https://www.newgrounds.com/portal/view/147276), the project will be comprised of a selection of instruments that have a 5-6 sound files that a user can pick from to create a short song. 
- I made samples for a kick, snare, and hihat for a drum set. I want to start small just while I'm getting the logic down so I made 3 buttons that play each sample on click, respectively. The next step is to trigger the same function that plays the samples in time, say 100bpm. Raekwon from Wu Tang Clan made a lot of his beats around that tempo so I'll be starting there (and I might add an option to adjust this later in the project's development).

8.15.2022
- I feel like I squandered my day... I needed to add one more project to my portfolio site so I was kind of all over the place just trying to come up with something. I was working on a weather app in Vue, but it seemed too basic, even though it was built in Vue, so I switched gears. Then, I dug up an old to-do app project, but that was also 'too basic.' Then, I found I looked into memory games built in vanilla JS, and tic tac toe games. I'm more than likely going to go with a tic tac toe game initially built in vanilla JS to then recreate in Vue just to have some variety in my portfolio (I have no games or Vue projects). The bottom line, though, is that I wasted probably an hour just getting here. The concept of annoying oneself is new, but hey...coding...

8.14.2022
- I somehow managed to go this long without using tables. I may be able to pull off what I need to do without it, but I have a table of data to display and the `table` seemed to be the most obvious choice. I'm realizing there are so many weird quirks I need to learn regarding tables. It makes me wonder if I want to just hard-code the width of the cells and set `justify-content: space-between` and add padding. We'll see what happens after I sleep on it.

8.13.2022
- I can confirm that I will never use Bootstrap grid ever again after familiarizing myself with CSS Grid. I even found a [CSS Grid generator](https://cssgrid-generator.netlify.app/)! Of course, I'll be using this tool to speed up production, but also as a learning tool. Grid is too powerful to not master.
- Inching my way toward completing the home page of the All Access clone (thus, making it deployable), I discovered the text-overflow property. I had to figure out how to truncate (new term) text with an ellipsis in a few different places. It seems like CSS was the focal point of today's studies.

8.11.2022
- Relying on a CSS framework is a rookie mistake, and I refuse to rely on anything that allows me bypass learning critical skills. I made a basic grid [here on Codepen](https://codepen.io/ploymahloy/pen/GRxBVBo?editors=1100) and found it to take significantly less time. I know I'll end up using a CSS framework for my web dev roles, but knowing how to use them and choosing not to is more powerful than relying on them and using them as a crutch. IMO of course, and I'm sure there are arguments that rest on the concept principle of saving time in production. We'll see!

8.10.2022
- God almighty I am not destined to EVER be able to use bootstrap's grid system. All I want to do is add padding/gutters and nothing I'm doing is working. Over this.

8.9.2022
- I noticed a lot of blue is used throughout my apps so I redesigned the mortgage calculator. I'm coming really close to being able to deploy my portfolio site. Better get a domain soon... hireme.dev?

8.8.2022 
- It turns out that the reason I've been getting these hydration errors is because I'm refreshing the page as if I'm not developing on a live server (terminology) or whatever. When I commit my changes and start the server over, problem solved. Worked on the personal site today. Working on it some more now. Probably going to finish v1 tonight or tomorrow, then get the All Access Clone homepage done by the weekend, then finalize my resume (which is 80% of the way done). I'm very excited to be getting so close to job-ready!

8.7.2022
- Put in some WORK on my personal site. My breakpoints were all over the place! Had breakpoints set at 920 AND 900? Like what? I think it would help if, when I open VSCode, I focus on a specific objective to COMPLETION, of some variety. As of right now, I build one thing halfway, then something looks off so I jump to that, and I end up bouncing all over my project. Either way, all that's left to do for my personal site is to fill in the project cards (and link the buttons), and add the sidenav.
- I built the sidenav menu! I used the logic from the All Access dropdown menu. I'm starting to see how much better I'm getting with recognizing what needs to be written to produce an intended effect (and what effect is truly meant to be created, but that's more of a question of design).

![Untitled](https://user-images.githubusercontent.com/48275526/183334503-a7d5a3ec-2c2b-4d46-8c3e-3bd861b25894.gif)

8.6.2022 
- Got somewhere with the personal site. I need to figure out why I get a hydration issue just from wrapping react icons in a div. It's so frustrating because I know nothing about that so now I have to try to understand a relatively advanced topic just to get my icons to work in a grid. I had a rough week so I doubt that will happen today.
- I definitely needed to cool off for a bit. Coming up with the layout for a site is not my forte. Come to think of it, I didn't even bother to grab a reference. However, I did download Kevin Powell's Conquering Responsive Layouts course. It was free, which is wild because he's great at explaining CSS. Here's what I have as of right now:
<img width="500" alt="Screen Shot 2022-08-06 at 1 37 57 PM" src="https://user-images.githubusercontent.com/48275526/183259880-82e63dff-55d6-43b5-92ec-070db7cc5fb0.png">
- Got some more work done on the personal site. I also worked on the mortgage calculator and removed the inset box-shadow as it look way too dark. I'm probably going to end up changing how the form responds to different sized screens and blow the text up a bit as there's not but so much going on. I also tried to work on a CodeWars problem for the first time in a few months. I am rusty!

8.5.2022
- I can NOT put into words how much I hate my personal site. I redesigned it to include a more subtle variation of the Brutalist buttons I made a few days ago. It bothers me how hard it is for me to design a damn website. I know I just need a good reference, but I can't find one that I like that is also within reach in terms of my skillset. I spent a whole damn week and a half at least just writing a dropdown menu from scratch...

8.3.2022
- I might have my first freelance client! My friend works for a home improvement company and the owner, with whom he is close, has expressed interest in a website. Currently, the business gets their customers via word of mouth, and their Facebook pages seems to come up high on Google searches for services they provide. This could be a HUGE milestone, despite the technical works being as easy as I want it to be with templates being wideley available.

8.2.2022
- I was inspired to do something different and made a nav bar inspired by Brutalism ([CodePen](https://codepen.io/ploymahloy/pen/ZExrMXE?editors=1100)). I think I'll be dedicating all day tomorrow to the sorting algorithm visualizer. It was one of the projects that caught Google's eye for Clément Mihailescu, supposedly. I like the idea of impressing prospective employers. I like the idea of a coding job.
- Since I had a lazy day with coding, I decided to make another [CodePen](https://codepen.io/ploymahloy/pen/YzaedZQ) for kicks. I had been toying with the concept of an inverted color overlay for a few days and wanted to see it come to fruition:
![xray](https://user-images.githubusercontent.com/48275526/182512210-020cf044-a5c1-462e-9579-d90bd0e4a624.gif)

8.1.2022
- I made a list of things to accomplish this week. Since the mortgage app, dictionary app, and cli calculator are all somewhat small in scale, I've decided to add an eCommerce project site (in addition to the All Access clone) to my portfolio. I plan to have the eCommerce site, the homepage of All Access, my personal site (revamped), the dictionary app (revamped), and my resume done by this time next week. Time to execute!
- Stumbling through NextJS, I'm enjoying the process so much more because I have more knowledge to support me while debugging, for example. I had a hell of a time just staying awake at work so my lack of focus on code after work has not been surprising. Tomorrow is an earlier day for me so I'll make up the difference then. There's no sense in overdoing it...but I did end up starting on the All Access clone homepage anyway...less to do tomorrow!

7.31.2022
- I looked at the portfolio/projects of one of my cohorts from my bootcamp that got a dev job after graduation. The portfolio page had 'noob' written all over it, and the projects were not anything special. It inspired me to remove ChartJS from the mortgage calculator app, and added an svg pattern background with an inset box shadow to bring focus to the app itself. I'm going to do something similar to the dictionary app as it doesn't look incredibley appealing either. Once I get that done, I'm going to redeploy (chaged homepage urls) the two projects, rework my personal site as it's not super greatm and then start applying to jobs finally. I'm so close, and I can't wait to start my dev career.<br> Before && After:<br>
<img width="450" alt="Screen Shot 2022-07-31 at 9 01 31 PM" src="https://user-images.githubusercontent.com/48275526/182054013-599a3177-c67d-4b0f-8f31-0ee4dc58168e.png"><img width="450" alt="Screen Shot 2022-07-31 at 9 02 07 PM" src="https://user-images.githubusercontent.com/48275526/182054017-76b1be07-0b04-493f-9149-e59a9d57deeb.png">
- I redeployed THREE sites in about 15 minutes, and I feel great about that. I struggle with git sometimes because all I want is a `Command + Z` for whatever caused my good, but being able to navigate gh-pages well enough to redploy three sites in short order aligns with my desire to become more effective with my time. I have experienced efficiency in spending a good portion of my time learning logic and debugging, but now I feel as though I can apply these lessons to produce action faster, or at least as fast as expected in a developer on a production team. Next step is to revamp my personal site!


7.30.2022
- A week after I started logging my progress, I was able to create solve a problem I'm not sure could have been solved without the reflection that a journal provides. I tried learning Redux from some YouTube videos but I kept getting red errors despite following their instructions exactly. I think I'm going to give an article on Redux a try.
- Tying up some loose ends I've been sitting on a mortgage caclulator site for a while. Ive got the logic functioning properly, but it looks ridiculous. Fortunately, I spent the past week dealing with CSS properties in React so I should at least be able to make a site look right.

7.29.2022
- I found an [article](https://bobbyhadz.com/blog/react-add-event-listener-to-body) that may be the final piece of the puzzle. I just need to set up an event listener to detect clicks outside of the dropdown menu. Then, I can use that to trigger a function to close the menu (`display: 'none'`).
- Correction: The above article only attached an `eventListener` to the document `body`. I still need to figure out how to conditionally trigger an event based on the component that was click. Something like `if (e.target !== this.whatever) {setIsActive(false)}`. Still a work in progress.
- [This article](https://www.robinwieruch.de/react-hook-detect-click-outside-component/) on creating a custom hook to detect a click outside of the component is the one that I was looking at last night. If I can't apply the logic to my project for whatever reason, despite being very close, I'm just going to use headlessUI's [Menu (Dropwdown)](https://headlessui.com/react/menu). At this point I'm feeling satisfied in knowing that I have a definite solution available via headlessUI, but will be even more rewarded by creating the functionality from scratch. I'm frustrated by how long this has taken me and how many hours have been wasted even though it hasn't been a true 'waste,' rather a sub-optimal progression. 
I know that this is one of the hardest aspects of the project. I'll need to make modals (check), routing (check), and that's most of the project. It's unfortunate that I had to tackle this difficult part first, but I'm getting a better underestand of the useEffect Hook, and React logic in general. Another takeaway from this week will be the useOutsideClick Hook; which I plan to dissect and save for future use.
- I did it! Built the dropdown menu component all from scratch. I'm very satisfied with being able to do this without relying on a UI library. Speaking of libraries and frameworks, I got rid of the TailwindCSS in this project and am using SASS instead (hence the color change to the exact match of the original app). It makes things easier in my opinion as I seem to enjoy doing everything myself.
![Untitled (2)](https://user-images.githubusercontent.com/48275526/181924086-8bfb9fe4-e1b2-4d60-8e14-db5cc80bb581.gif)

7.27.2022
- Something I'm realizing is that if I can put into words what I'm trying to accomplish, I can better articulate a Google search. Better yet, if I can articulate what I'm trying to do in my code, the solution has already been posted thousands of times online. An example of this is something that happened today: I wanted to use font awesome icons as the `menu_title` in my dropdown menu component, but couldn't figure out how to do it. For whatever reason, I thought to make a vanilla js switch statement where if the `menu_title` prop value was a string, then it would display the string as the title. Otherwise, the title would display the icon based on key-value pairs (menu_title={1} ----> 1: <FontAwesomeIcon icon={faBars} />). This completely bypasses React's functionality and doesn't really make sense as a long-term solution. I even realized what was going on and said "wait, all I'm trying to do is pass the jsx as a prop value...." 10 seconds later I referenced a project that passes jsx as a prop value via curly braces `menu_title={<FontAwesomeIcon icon={faBars} />}`. Better by the day!
- In its current state, my dropdown menu component displays its submenu on hover. To mimic All Access, I need the dropdown menus to open only `onClick`. I initially attempted to use `state` to set the display property of the submenu from `hidden` to `block`. I ended up finding [this link](https://www.robinwieruch.de/react-hook-detect-click-outside-component/) which outlines how one developer created a custom hook to detect clicks outside of the component. My mission tomorrow is to absorb this, and apply it to the dropdown menu. The only thing left after that is to connect the routing to all the pages represented in the navbar's menus. I'm actually looking forward to solving this, whereas just a week ago I was agonizing over running into obstacles. The path to project MVP is much clearer now, despite having much more work to do.

7.26.2022 
- Something I am realizing about myself is that I make things harder than they need to be. Here I am trying to use JUST divs and spans to create a dropdown menu from scratch (see codepen from 7.24, it functions, but only in a vaccuum). I completely ignored that the STANDARD is to use a select tag with nested option tags. Knowing the standard and acknowledging it from the jump would have been more helpful. I need to start assuming that everything I am trying to accomplish at this stage has been done, redone, reformatted, and rebranded. I don't need to create problems, I need to create projects. I need to start my career.
- It works!
<img width="500" alt="Screen Shot 2022-07-26 at 11 10 40 PM" src="https://user-images.githubusercontent.com/48275526/181152536-fcb01691-57c1-4992-94ec-8e67207995f7.png">

7.25.2022
- I cannot get even my codepen to work in my NextJS project. I'm bashing my head against the wall trying to understand how this can work in my project. Days like these I think it best to call it a night.
- I coudn't help myself and tried again. I was able to get one option, the dropdown above the navbar, to come close to what I want. Although it's not in the navbar, it's a step in the right direction....I hope.... (Reflection: This is too little progress for a few hours' work. This is not sustainable. I need to be more productive, and THAT is where my frustration lies).
<img width="750" alt="Screen Shot 2022-07-25 at 9 36 32 PM" src="https://user-images.githubusercontent.com/48275526/180903766-f8110a6d-8766-4d1c-8dab-64de6b0d0526.png">

7.24.2022
- Taking some time to reflect on yesterday's issue, I realize at this point that my time should be spent less in building everything from scratch (dropdwon menus) and more on shipping completed works to show potential employers and clients. Using component libraries can be a crutch and will make debugging issues harder if the base knowledge is not there, but since I was able to solve my problem ([CodePen](https://codepen.io/ploymahloy/pen/GRxEPOp?editors=1100)), I think that I have earned the right to use said components to shorten this aspect of production. I'm going to be using MatierialUI just for the sake of its popularity. AntD is next on my list.
- Learned what it means to fork a repo and why, thanks to this video ---> [Git Fork vs. Git Clone: What's the Difference?](https://www.youtube.com/watch?v=6YQxkxw8nhE)

7.23.2022
- Rediscovered the sibling selector `+` in CSS. I had been trying to create a nested dropdown menu for my All Access clone project, and noticed the descendant selector `space` was not functioning correctly. Of course, this only works on descendant DOM elements and I had not paid proper attention to the relationship of the elements in my project! I will now add this [link](https://levelup.gitconnected.com/understanding-use-of-the-and-symbols-in-css-selectors-95552eb436f5) to my reading, posted here for reference.
