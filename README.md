# dev-journal
Journal for tracking web dev progress.


7.27.2022
- Something I'm realizing is that if I can put into words what I'm trying to accomplish, I can better articulate a Google search. Better yet, if I can articulate what I'm trying to do in my code, the solution has already been posted thousands of times online. An example of this is something that happened today: I wanted to use font awesome icons as the `menu_title` in my dropdown menu component, but couldn't figure out how to do it. For whatever reason, I thought to make a vanilla js switch statement where if the `menu_title` prop value was a string, then it would display the string as the title. Otherwise, the title would display the icon based on key-value pairs (menu_title={1} ----> 1: <FontAwesomeIcon icon={faBars} />). This is completely bypasses React's functionality and doesn't really make sense as a long-term solution. I even realized what was going on and said "wait, all I'm trying to do is pass the jsx as a prop value...." 10 seconds later I confirm that jsx is passed as a prop value via curly braces `menu_title={<FontAwesomeIcon icon={faBars} />}`. Better by the day!

7.26.2022 
- Something I am realizing about myself is that I make things harder than they need to be. Here I am trying to use JUST divs and spans to create a dropdown menu from scratch (see codepen from 7.24, it functions, but only in a vaccuum). I completely ignored that the STANDARD is to use a select tag with nested option tags. Knowing the standard and acknowledging it from the jump would have been more helpful. I need to start assuming that everything I am trying to accomplish at this stage has been done, redone, reformatted, and rebranded. I don't need to create problems, I need to create projects. I need to start my career.
- It works!
<img width="391" alt="Screen Shot 2022-07-26 at 11 10 40 PM" src="https://user-images.githubusercontent.com/48275526/181152536-fcb01691-57c1-4992-94ec-8e67207995f7.png">

7.25.2022
- I cannot get even my codepen ^ to work in my NextJS project. I'm bashing my head against the wall trying to understand how this can work in my project. Days like these I think it best to call it a night.
- I coudn't help myself and tried again. I was able to get one option, the dropdown above the navbar, to come close to what I want. Although it's not in the navbar, it's a step in the right direction....I hope.... (Reflection: This is too little progress for a few hours' work. This is not sustainable. I need to be more productive, and THAT is where my frustration lies).
<img width="631" alt="Screen Shot 2022-07-25 at 9 36 32 PM" src="https://user-images.githubusercontent.com/48275526/180903766-f8110a6d-8766-4d1c-8dab-64de6b0d0526.png">

7.24.2022
- Taking some time to reflect on yesterday's issue ^, I realize at this point that my time should be spent less in building everything from scratch (dropdwon menus) and more on shipping completed works to show potential employers and clients. Using component libraries can be a crutch and will make debugging issues harder if the base knowledge is not there, but since I was able to solve my problem ([CodePen](https://codepen.io/ploymahloy/pen/GRxEPOp?editors=1100)), I think that I have earned the right to use said components to shorten this aspect of production. I'm going to be using MatierialUI just for the sake of its popularity. AntD is next on my list.
- Learned what it means to fork a repo and why, thanks to this video ---> [Git Fork vs. Git Clone: What's the Difference?](https://www.youtube.com/watch?v=6YQxkxw8nhE)

7.23.2022
- Rediscovered the sibling selector `+` in CSS. I had been trying to create a nested dropdown menu for my All Access clone project, and noticed the descendant selector `space` was not functioning correctly. Of course, this only works on descendant DOM elements and I had not paid proper attention to the relationship of the elements in my project! I will now add this [link](https://levelup.gitconnected.com/understanding-use-of-the-and-symbols-in-css-selectors-95552eb436f5) to my reading, posted here for reference.
