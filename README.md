# dev-journal
Journal for tracking web dev progress.

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
