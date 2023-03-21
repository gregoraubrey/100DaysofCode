# 100DaysofCode

## Day 1
*20230320*

Today marks the start of the second week of the **School of Code** bootcamp (cohort 14). I thoroughly enjoyed last week and I am pleased to say that week 2 has got off on the right foot too!

- In the morning quiz my only mistake was mixing up which of `var`, `let`, and `const` are **function-scoped** and **block-scoped** in JS so I was pretty happy with that.
- I met my new programming partners for the week and we worked together on some basic [Code Wars](https://www.codewars.com) problems.
  - I was particularly happy to have remembered a code snippet from last week (`X % 2 === 0`) that helped us quickly solve a task involving selecting even numbers from an array.
- We had a lecture on the **DOM** and then jumped into a workshop that concerned coding in the functionality for a button to double the number of pennies shown on the screen each time it was pressed.
- As a team we managed to pretty quickly go through all the tasks so we had time at the end to add our own ideas, such as an if...else statement that changed the display from pennies to pounds when appropriate.
  - I threw in a little easter egg after the session too, should anyone spam the button enough times to exceed 1 trillion GBP:
  
 ```js
 function handleClick() {
  console.log("I'm just to prove it's working!");
  pennies *= 2
  if (pennies < 100) {
    document.querySelector('output').textContent = `${pennies} pennies`;
    titleUpdater(pennies + ' pennies')
  }
  else if (pennies < 100000000000000) {
    document.querySelector('output').textContent = `£${pennies/100}`;
    titleUpdater('£' + pennies/100)
  }
  else {
    document.querySelector('output').textContent = `£${pennies/100} - the country has entered hyperinflation 😭😭😭`;
    titleUpdater('HYPERINFLATION')
  }
}
```
- Perhaps the most gratifying part of the day was not getting the workshop done but spotting that someone was asking for a hand with a task we had finished and hopping into their breakout room and managing to help them solve the task - I'm sure I'll be relying on help from fellow bootcampers in the future so it feels good to help when I can.
- I also continued to read *"Clean Code"* by Robert C. Martin as per my mentor Shaun's recommendation and got up to the start of Chapter 6. I can't say in good faith that I am able to follow the code examples but the author's explanations of said code have been proving enough of a guide thus far.

In summary, an encouraging start to the week. I'm sure not all of my daily updates will be this long but I am glad to have got going. Here's to 99 days more!

## Day 2
*20230321*

Today was especially interesting as we delved into AI tools and how they can best be utilised to both learn and write code in an efficient manner.

- I got everything right in the morning quiz on the DOM!
  - This is my first time scoring 100% on one of the morning quizzes so I am delighted, whilst at the same time being acutely aware that this hardly guarantees I have internalised everything we have learnt thus far.
- We had a guest lecturer in the form of Piper who was part of cohort 4 of the School of Code.
- Their talk of ongoing impostor syndrome remninded me of similar sentiments expressed by some of my friends whilst at university.
- On a more positive note, they affirmed that your colleagues in tech will always be willing to take time out of their day to get you up to speed on something you do not yet know which is certainly reassuring.
- They also mentioned how companies are often keen to hire juniors specifically for their lack of experience, in the hope that they might be more easily moulded to fit the company work culture than an established developer, which seems a reasonable assumption to me.
- We split off for a short while into berakout rooms and as a trio my partners and I solved two Code Wars kata called [Sentence Smash](https://www.codewars.com/kata/53dc23c68a0c93699800041d/train/javascript) and [If you can't sleep, just count sheep!!](https://www.codewars.com/kata/5b077ebdaf15be5c7f000077/train/javascript)
  - The latter was particularly humbling, with one of the submitted solutions achieving in 1 line what we had managed in 9:
```js
countSheep=n=>[...Array(n).keys()].map(x=>`${x+1} sheep...`).join``
```
  - Whilst our offering was:
```js
var countSheep = function (num){
  let murmur = ""
  if (num > 0) {
	  for (let i=1; i <= num; i++) {
	  murmur = murmur + i + " sheep..."
	  }
  }
  return murmur
}
```
- After a lecture covering the `addEventListener()` method, we started on a workshop where we would use ChatGPT and/or GitHub Copilot to rebuild the rock, paper, scissors game from last Friday, now with added DOM functionality
- It never ceases to me amaze me what ChatGPT can do, with a single sentence prompt returning me fully functional HTML, CSS, and JS for a working game.
- What impressed me more, however, was Copilot's autocompletion of my comments in which I was attempting to spell out what each code block was achieving, which on more than one occasion actually helped me understand lines of code that ChatGPT had generated which were, until then, going over my head.
- Lastly, I continued to read *Clean Code* and got to the start of Chapter 8. Hopefully I can get it finished before I meet with my mentor on Friday.

All in all another jam-packed day! I feel like the Copilot autocompletion of comments will prove invaluable in helping me to read code that would otherwise be impenetrable at this early stage in my learning journey.
