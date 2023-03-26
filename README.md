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

## Day 3
*20230322*

Today we were introduced to asynchronous JS and APIs which I am sure we will get lots of practice with in the coming days and weeks.

- My only mistake on the morning quiz was a question on what will and will not cause an event on the DOM (it turns out scrolling in the browser window will cause an event!)
- We spent some time in our trios solving Code Wars kata and we managed to get through four of them:
	- [Simple multiplication](https://www.codewars.com/kata/583710ccaa6717322c000105)
	- [Chuck Norris VII - True or False? (Beginner)](https://www.codewars.com/kata/570669d8cb7293a2d1001473/train/javascript)
	- [Sum of two lowest positive integers](https://www.codewars.com/kata/558fc85d8fd1938afb000014/train/javascript)
		- Solving this one introduced me to the syntax for the `.sort()` method: `numbers.sort((a, b) => a - b);`
	- [Grasshopper - Summation](https://www.codewars.com/kata/55d24f55d7dd296eb9000030/train/javascript))
		- Once again our solution was far less elegant than some others on display:
```js
var summation = function (num) {  
  let totalSum = 0  
  for (let i=1; i <= num; i++) {  
    totalSum = totalSum + i  
  }  
  return totalSum
}
```
- As opposed to:
```js
const summation = n => n * (n + 1) / 2;
```
- I particularly appreciated this concise solution because it reminded me of a story I had heard in school of Gauss, as a schoolboy, summing the numbers from 1 to 100 in no time at all by deriving the formula used above.
- After a lecture on asynchronous JS we got to work on a workshop coding up hands on a clock that would move in real time atop an image of a clock face.
- We then had a lecture introducing APIs, Promises, and fetch that led into an afternoon workshop building a page that retrieves cat facts at random when a button is pressed.
- As a trio we got through all the tasks of the workshop and even managed to find some time at the end to add an array of cat images that would change at random along with the cat fact on display when the button was pressed.

Another satisfying day today, and I was particularly glad to get the afternoon workshop finished, along with copious comments spelling out what each function was doing step by step. In the future I am sure that these will be superfluous, and indeed reliance on comments is proscribed in *Clean Code* in favour of well written code that speaks for itself but for the time being I find they help me both solidify my understanding of the code I have just written and give me confidence that when I look back over my work, I won't be stuck trying to work out what I was trying to achieve with each line.

## Day 4
*20230323*

There was less time spent coding today than usual as in the afternoon we split into groups and each researched a particular topic.

- I got everything right on today's morning quiz on async and fetch and finished quite quickly to boot which was encouraging.
- We then split into groups and spent some time working on Code Wars.
- We solved a couple of 7 kyuu kata:
	- [Friend or Foe?](https://www.codewars.com/kata/55b42574ff091733d900002f/train/javascript)
```js
function friend(friends){
  const regex = /^[a-zA-Z]+$/;
  for (let i=0; i < friends.length; i++) {
    if (friends[i].length !== 4 || !regex.test(friends[i])) {
      friends.splice(i, 1)
      i--;
    }
  }
  return friends
}
```
- [Get the Middle Character](https://www.codewars.com/kata/56747fd5cb988479af000028/train/javascript)
```js
function getMiddle(s)
{
  let stringLength = s.length
  if (stringLength % 2 === 1) {
    let oddMiddle = s.slice(Math.floor(stringLength/2),Math.ceil(stringLength/2))
    return oddMiddle
  }
  else {
    let evenMiddleTwo = s.slice((stringLength/2)-1, (stringLength/2)+1)
    return evenMiddleTwo
  }
}
```
- One of the submitted solutions made use of a JS method that I had not yet encountered, `substring()` to solve the kata in a much simpler way:
```js
function getMiddle(s)
{
  return s.substring(Math.ceil(s.length/2)-1, Math.floor(s.length/2)+1)
}
```
- We then had a lecture by Joseph on cognitive diversity in the workplace in which he talked about personality tests and how we can best get different types of people to work together.
- In preparation for the session we were asked to do [this personality test](https://www.16personalities.com/) and I got "Commander ENTJ-A" which seemed to fit me fairly well, although I am always somewhat sceptical of personality tests such as these so I expect I will take the results with a pinch of salt.
- We then had an engaging lecture by Paavan Buddhev on UX Design.
- Apparently we will be looking into UX Design more next week so that should flesh out my understanding but as things stand it seems like Paavan gets to do some interesting work.
- We then split into groups to research dev tools tabs, and I looked into **lighthouse**.
- We combined our research into a 5-minute video to be shared with our fellow bootcampers.
- We then spent the last half an hour or so working on our first 6 kyuu kata on Code Wars:
	- [Sum of Digits / Digital Root](https://www.codewars.com/kata/541c8630095125aba6000c00/train/javascript)
```js
function summing(n) {
  let digits = Array.from(String(n), Number);
  let summedTotal = 0;
  for (let i=0; i < digits.length; i++) {
    summedTotal = summedTotal + digits[i]
  }
  return summedTotal
}

function digitalRoot(nextSum) {
  let result = summing(nextSum)
  while (result >= 10) {
    result = summing(result)
  }
  return result
  }
```
- This was definitely the longest we have spent solving a kata and we needed a helping hand from ChatGPT near the end to get us over the line.
- As always, there was a better was of doing things, making use of some in-built JS methods that we have yet to come across, elucidated in the submitted solutions:
```js
function digital_root(n) {
  if (n < 10) return n;
  
  return digital_root(
    n.toString().split('').reduce(function(acc, d) { return acc + +d; }, 0));
}
```

Today was a pleasant change of pace with less new material which should hopefully give us all a chance to consolidate everything we have learned thus far this week ready for tomorrow's hackathon.

## Day 5
*20230324*

We spent the day working on a hackathon project using a [Pokemon API](https://pokeapi.co/) to build a game where a player types in a pokemon name and that pokemon's base HP stat is compared to that of the computer's randomly chosen pokemon to determine a winner.

- There was no morning quiz this morning as we were about to jump into the hackathon.
- Liz mentioned that a couple of bootcampers from cohort 4 spoke at the bootcamp 13 graduation ceremony yesterday and emphasised the benefits of learning how to effectively pair program from an early stage, saying that it has set them up well for their first couple of years in the industry.
- For today's hackathon there were various APIs that we could have chosen from.
 	- Pokemon
	- Dad jokes
	- Trivia questions
	- Dictionary
- We decided straight away that we would go for the pokemon API, since it offered such a breadth of information for each pokemon that we would be spoilt for choice when it came to sending GET requests to the API.
- With so many stats to choose from we decided to focus on just the base HP stat and quickly had a working game built in which the computer would randomly pick a Gen 1 pokemon with `Math.floor(Math.random() * 151 + 1);` and the user would type in a pokemon's name into a prompt.
- This would send a GET request to the API for the relevant pokemon and return the name, sprite image, and base HP stat, all to be displayed on screen.
- We had particular trouble getting the sprites to load in correctly so it was especially satisfying when they finally started to work, after we discovered that we had been referencing the wrong HTML id in our main.js file.
- By the time we were done for the day we had added a working score counter that kept track of both the player's and the computer's overall tally, and added some CSS styling to give the page a retro feel.
- To end off the day each group presented their work to fellow bootcampers which was certainly gratifying, and also allowed us to see some of the great work done by other groups who had gone in a completely different direction to us.
- I had another productive meeting with my mentor who recommended that I start on *The Clean Coder* when I get through *Clean Code*, and also lamented how some developers see the latter as the Bible rather than a guideline that need not always be followed to the letter.

It felt great today to combine a week's learning into one project that, as a group, we could all be proud of. I can only imagine what sorts of projects we will be building in a few weeks' time!

## Day 6
*20230325*

I was out of the house today until the late evening so I did not get a chance to do any coding until I was already very tired at the end of a long day. For that reason I decided to just try and solve some ostensibly simple Code Wars problems:

- [Determine offspring sex based on genes XX and XY chromosomes](https://www.codewars.com/kata/56530b444e831334c0000020/train/javascript)
```js
function chromosomeCheck(sperm) {
  if (sperm.includes("Y")) {
    return "Congratulations! You're going to have a son."
  }
  else
    return "Congratulations! You're going to have a daughter."
}
```
- [Is your period late?](https://www.codewars.com/kata/578a8a01e9fd1549e50001f1/train/javascript)
```js
function periodIsLate(last, today, cycleLength) {
  return today.getTime() - last.getTime() > cycleLength * 24 * 60 * 60 * 1000;
}
```
- [Remove String Spaces](https://www.codewars.com/kata/57eae20f5500ad98e50002c5/train/javascript)
```js
function noSpace(x){
  return x.replace(/ /g, "")
}
```
- [Simple Change Machine](https://www.codewars.com/kata/57238766214e4b04b8000011/train/javascript)
```js
function changeMe(moneyIn){
  if (moneyIn === "20p") {
    return "10p 10p";
  }
  else if (moneyIn === "50p") {
    return "20p 20p 10p";
  }
  else if (moneyIn === "£1") {
    return "20p 20p 20p 20p 20p"
  }
  else if (moneyIn === "£2") {
    return "20p 20p 20p 20p 20p 20p 20p 20p 20p 20p"
  }
  else if (moneyIn === "£5") {
    return "20p 20p 20p 20p 20p 20p 20p 20p 20p 20p 20p 20p 20p 20p 20p 20p 20p 20p 20p 20p 20p 20p 20p 20p 20p"
  }
  else return moneyIn;
}
```

I think it is pretty clear from my final solution that I was not at my best, as it is hardly the most elegant of solutions, and does not scale to support inputs outside of those specified in the kata. I guess it just goes to show how difficult it is to code when you are tired, and I am glad to have at least spent some time coding today.

## Day 7
*20230326*

I spent an hour or so working on the Recap Tasks we had been set on Friday that cover the content we learned during Week 2, and some more time reading *Clean Code* today.

- The Recap Tasks were split into tasks 1, 2, and 3, along with a couple of bonus tasks.
- I got throught the main 3 tasks, leaving me with just the bonus tasks to work on tomorrow before we kick things off for Week 3.
- Task 1 covered for loops and creating new arrays from existing ones.
- In completing it I learned of the `.startsWith()` method which helped me to create a new array only containing celebrities whose name starts with a vowel out of an existing one already filled with celebrities:
```js
let vowelCelebs = [];
for (let i = 0; i < celebs.length; i++) {
  if (celebs[i].startsWith('A') || celebs[i].startsWith('E') || celebs[i].startsWith('I') || celebs[i].startsWith('O') || celebs[i].startsWith('U')) {
    vowelCelebs.push(celebs[i]);
  }
}
```
- Task 2 covered `setInterval` and `clearInterval` and saw me create a function to increment the count of a `<p>` element (which had text content "0" in the HTML) by 1 until it had reached 12:
```js
let countingParagraph = document.querySelector("#count");
let incrementByOne = setInterval(()=> {
    if (Number(countingParagraph.textContent) >= 12) {
        clearInterval(incrementByOne);
    }
    else {
        countingParagraph.textContent = Number(countingParagraph.textContent) + 1;
    }
}, 1000);
```
- I had to use the `Number()` method to convert the text content from a string into a number, lest "1" just be conactenated to the end of a string.
- Task 3 covered async functions, fetch, and Promises as I had to send a GET request to a [cat API](https://thecatapi.com/) to get a random image of a cat:
```js
async function fetchCatImage() {
  let catRequest = await fetch("https://api.thecatapi.com/v1/images/search");
  let catData = await catRequest.json();
  let catImage = document.querySelector("#cat-here");
  catImage.src = catData[0].url;
}
```
- After writing up the `fetchCatImage` function I had to create a button element using JS and then add an event listener so that the function would be called every time the button was clicked.
- Other than initially forgetting the need for the `.appendChild()` method to make the new button element appear, it was pretty smooth sailing.
- I capped off the day by reading some more of Robert C. Martin's *Clean Code*, and plan to move on to *The Clean Coder* when I finish the former, hopefully within a few days.

Today's coding was pretty relaxed as the Recap Tasks just focused on consolidating things we had already been working on this week. It felt good to have remembered so much considering just how fast of a pace we are moving at, and I look forward to what Week 3 has in store!
