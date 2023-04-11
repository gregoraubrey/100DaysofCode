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

## Day 8
*20230327*

We had a great guest lecture today from Dave Adams, a former bootcamper, and then moved on to an introduction to Agile and UI and UX design.

- I finished the bonus section of the Recap Tasks this morning which was satisfying. I needed a hint from ChatGPT in a couple of places but I understood the code it recommended which was a good sign.
- I only got one question wrong on the morning quiz today, which which was question about callback functions. I asked ChatGPT for an explanation after the fact and I now feel like I have a grasp of what a callback function is so I'm not too concerned about that.
- After the quiz we had a guest lecture from Dave Adams who was a part of cohort 2 of the bootcamp 4 or 5 years ago now.
- He talked to us about his job working as an SRE (a job role I had never heard of before today!).
- According to Dave the responsibilities of an SRE include:
	- Finding performance bottlenecks and fixing them in order to increase the reliability of services.
	- Communicating and mentoring others in using best practices for building reliable software.
	- Monitoring processes to identify and solve issues before they magnify.
- He talked about how open he is with his managers and how, unlike in his previous career as a teacher, he feels like if he is not enjoying his work that he can afford to quit and find a new role, which certainly sounds liberating. In fact, he did just that before joining his current company.
- Dave mentioned how he never got on well with CSS and frontend design, hence why he drifted towards being an SRE.
	- This resonated with me, which could be a problem this week since as far as I know we will be focusing on UI and UX!
- After Dave's lecture, we were introduced to our programming partners for the week and we worked on a task in which we had to try and recreate the look of the Google homepage without the internet and with just the use of a plain text editor like Notepad.
- Obviously this ended in disaster, which just goes to show how indsipensable modern development environments and research tools are for a programmer
- We then had a lecture introducing Agile. Some of the concepts reminded me of bits of advice I have read in *Clean Code* so it was no surprise to see Robert C. Martin's name listed on the [Agile Manifesto](https://agilemanifesto.org/) website.
- The lecture then moved on to talk about the differences between UI and UX design, with a particularly memorable example being a nice-looking glass ketchup bottle that is a nightmare to use versus a boring-looking plastic bottle that is far more wieldy.
- The final part of the day was spent getting as far through [Flexbox Froggy](https://flexboxfroggy.com/) and [CSS Grid Garden](http://cssgridgarden.com/) as possible in order to learn about Flexbox and CSS Grid.
- In our group we managed to get through all of Flexbox Froggy and got to the 26th out of 28 levels on CSS Grid Garden which I feel was pretty good going considering the time we had.
- My last coding-related activity of the day was reading more *Clean Code*. I also discovered, to my delight, that *The Clean Coder* is available for free on Audible for members, so that's my next listen sorted!

I have to admit that I was reticent about this week since I do not feel like UI and UX design will be my strong suit. With that said, I thoroughly enjoyed today so am excited for what the next few days will bring.

## Day 9
*20230328*

Our focus today was on design principles and we made a start on planning out an application process through paper prototyping.

- We began the day by spending half an hour or so on Code Wars:
- [Cat years, Dog years](https://www.codewars.com/kata/5a6663e9fd56cb5ab800008b/train/javascript)
```js
var humanYearsCatYearsDogYears = function(humanYears) {
  let catYears;
  let dogYears;
  if (humanYears === 1) {
    catYears = 15;
    dogYears = 15;
    }
  if (humanYears === 2) {
    catYears = 24;
    dogYears = 24;
    }
  if (humanYears >= 3) {
    catYears = 24 + (humanYears - 2) * 4;
    dogYears = 24 + (humanYears - 2) * 5;
  }
  return [humanYears, catYears, dogYears];
}
```
- [Remove the minimum](https://www.codewars.com/kata/563cf89eb4747c5fb100001b/train/javascript)
```js
function removeSmallest(numbers) {
  if (numbers.length === 0) {
    return [];
  }
  let smallest = Math.min(...numbers)
  let indexLocation = numbers.indexOf(smallest)
  return numbers.slice(0, indexLocation).concat(numbers.slice(indexLocation + 1));
};
```
- We struggled for a while to understand why `Math.min(numbers)` would not work before ChatGPT informed us of the **spread operator** which I swiftly added to my Anki deck.
- After trying to use the `splice()` method on `numbers` we realised that, in order to pass the kata, we were not allowed to manipulate the argument.
- That led us to the strange-looking final line of the function in which we take two slices, one going from the initial index up until the smallest value, and then one going to the end of the array and starting from the index one above the smallest value, before concatenating the two of them to make one long array.
- After Code Wars we had a morning quiz on Agile, UI, and UX in which I got everything right which was encouraging.
- We then had a lecture on [the 5 stages in the design thinking process](https://www.interaction-design.org/literature/article/5-stages-in-the-design-thinking-process):
	- Empathise
	- Define
	- Ideate
	- Prototype
	- Test
- In the Agile style, these stages do not have to be followed linearly.
- We then split into groups and had to come up with our own idea for a type of bootcamp and then plan out an application process.
- We decided on the *School of Chess* and spent the rest of the day planning out a hypothetical application process.

We did not spend much time coding today, focusing instead on design principles. I am interested to see how we develop our *School of Chess* idea in the coming days but am still undecided as to where I stand with UI and UX!

## Day 10
*20230329*

We focused on UI design today, learning about wireframes, CSS custom properties (variables), and CSS specificity.

- We started the day with some Code Wars as usual:
- [Gravity Flip](https://www.codewars.com/kata/5f70c883e10f9e0001c89673/train/javascript)
```js
const flip=(d, a)=>{
  if (d === 'L') {
    a.sort(function(a, b) {return b - a;});
  }
  if (d === 'R') {
   a.sort(function(a, b) {return a - b;});
  }
  return a
}
```
- [Split Strings](https://www.codewars.com/kata/515de9ae9dcfc28eb6000001/train/javascript)
```js
function solution(str){
   if (str.length === 0) {
     return [];
   }
   else if (str.length % 2 === 0) {
     let substring = str.match(/.{1,2}/g);
     return substring;
   }
   else {
     let substring = str.match(/.{1,2}/g);
     let finalItem = substring[substring.length - 1];
     finalItem = finalItem.substr(0, 1) + "_";
     substring.pop();
     substring.push(finalItem);
     return substring;
   }
}
```
- The above was a 6 kyuu which felt great to solve, and taught me the `match()` method.
- One of the submitted solutions managed to solve it in a much simpler way:
```js
function solution(s){
   return (s+"_").match(/.{2}/g)||[]
}
```
- We then had a morning quiz on the design thinking process and UX, in which I only got one question wrong. It concerned the prototyping stage of the design thinking process and the answer made sense after talking it through with some fellow bootcampers after the quiz.
- We moved on to a lecture on UI which covered the elements and principles of design and highlighted some great websites for getting a colour palette together for a website.
- We played around with https://coolors.co/ for a while, making a few different colour palettes that could be saved for future use.
- We then moved on to CSS variables and specificity which was a nice change of pace, since we had not spent much time learning coding since the Code Wars in the morning.
- The afternoon workshop involved attempting to recreate the Google homepage as we had done earlier in the week, and thankfully the results were slightly better this time, albeit still nowhere near good enough to fool anyone!

All in all a satisfying day, and the colour palette tools were great fun to work with.

## Day 11
*20230330*

Today was nice and varied, with a lecture on mindset, a guest lecture on UI/UX, and some research in the afternoon on best practices when making forms.

- We started the day in our groups with some Code Wars:
- [Decreasing Inputs](https://www.codewars.com/kata/555de49a04b7d1c13c00000e/train/javascript)
```js
function add(...args) {
  let value;
  let dividedVaLue;
  let totalSum = 0;
  let array = args.filter(input => input !== undefined);
  if (array.length === 0) {
    return 0;
  }
  for (let i = 0; i < array.length; i++) {
    value = array[i];
    dividedVaLue = value/(i + 1)
    totalSum = totalSum + dividedVaLue
  }
  totalSum = Math.round(totalSum)
  return totalSum;
}
```
- Through solving this kata I learned about **rest parameter syntax**, for which I duly made an Anki card.
- We then got to work on a 6 kyuu kata called [Convert string to camel case](https://www.codewars.com/kata/517abf86da9663f1d2000003/train/javascript) but did not finish it in time before getting called for a lecture.
- I came back to the kata during lunch and, with the guiding hand of ChatGPT, managed to get a working solution:
```js
function toCamelCase(str) {
  let words = str.split(/[-_]/g);
  let firstWord = words[0];
  let changeToCamelCase = firstWord.charAt(0) + firstWord.slice(1).toLowerCase();
  let capitalisedWords = words.slice(1).map(word => {
    return word.charAt(0).toUpperCase() + word.slice(1).toLowerCase();
  });
  let camelCaseWords = [changeToCamelCase, ...capitalisedWords];
  return camelCaseWords.join('');
}
```
- I'm not sure if my solution is simply cumbersome or if I am just too new to coding, but despite understanding each line in isolation, it still takes me a long time to read through this function and understand it as a whole.
- As always, somebody came up with a much slimmer solution:
```js
function toCamelCase(str){
  return str.replace(/[-_](.)/g, (_, c) => c.toUpperCase());
}
```
- In the morning quiz on UI I got three questions wrong, one of which being a design choice error. Even after seeing the explanation (don't align related items to different sides) I still preferred the incorrect answer!
- We then had a mindset lecture on communication and effective listening which is doubtless a huge part of any developer's day so I'm glad we spent time on it today.
- Next we were lucky enough to have the CTO of a UK startup and one of their UX/UI designers give a lecture on design and what it is like transitioning into a new career.
	- This lecture was full of great nuggets of wisdom and I took copious notes.
- We then spent the afternoon in groups each working on a different research task.
- Ours was tasked with forms and we came together to produce a 5-minute video by the end of the day on best practices and the various HTML elements that a form would feature, such as `<button>`, `<textarea>`, `<radio>`, etc.
- To end the day I decided to work on a 7 kyuu kata called [Insert dashes](https://www.codewars.com/kata/55960bbb182094bc4800007b/train/javascript) on my own and was delighted to, for the first time (at least as far as I can remember), solve it rather painlessly, with my initial idea about how to tackle the kata being correct.
	- I know it is only a basic problem but it felt so satisfying to just have everything click and to solve it quickly and easily.
```js
function insertDash(num) {
   let numString = num.toString()
   let numArray = numString.split("")
   
   for (let i = 0; i < numArray.length; i++) {
     if (numArray[i] % 2 === 1 && numArray[i + 1] % 2 === 1) {
       numArray.splice(i + 1, 0, "-")
     }
   }
  return numArray.join("")
}
```

Today was definitely my favourite day of the week thus far. We had two great lectures, and solved a few gratifying Code Wars kata. I wonder what we will be working on in tomorrow's hackathon?

## Day 12
*20230331*

For today's hackathon we went through the full design process of building a landing page for a bootcamp of our choosing.

- As a group we started off by making some user personas on [Hubspot](https://www.hubspot.com/make-my-persona).
- We then created user stories based on our user personas that helped elucidate key design features, such as accessibility for colour-blind users.
- After installing the drawio extension we created a flow diagram within our repo to outline the user journey through our website.
- We then chose a colour palette that contained dark and light browns to fit with our "School of Chess" theme.
- We tested these colours for contrast and settled on `#964D22`, `#FFFFFF`, `#000000`, `#FFE9C5`, and `#800000`.
- Just before lunch we completed a low-fidelity wireframe to inform us when it came to coding the site up using HTML and CSS.
- During our lunch break I had a mentor meeting in which we discussed a variety of topics, from recommended reading on object-oriented programming, to the pros and cons of ChatGPT and GitHub Copilot for programmers.
- After lunch we made a start on our HTML and CSS.
- We made use of the CSS variables that we had learned about earlier in the week to easily reuse the colours from our colour palette as decided on earlier in the day.
- We used flexbox to style our header buttons to be spread out across the top of the screen and made them change colour when hovered over with the cursor for extra visibility and clarity for the user.
- Before time was up we managed to get an image, in the form of a pawn, working as a button which would link back to our homepage when clicked but were unable to get a YouTube video working as the page would refuse to connnect to youtube.com.
- We then gave a 2-minute presentation on our work and listened to other groups do the same.
- Some of their work was particularly inspiring, with one group making clever use of `position: fixed` to create a nav bar that always stayed at the top of the screen.

This week was not my favourite in terms of the topics we were diving into but I nonetheless learned a lot and thoroughly enjoyed working in my group. I have no idea what is in store for us next week but I expect that by delving into more JS I will be more within my comfort zone.

## Day 13
*20230401*

Today was certainly not my busiest in terms of coding but I still went over some JS in preparation for next week and I believe that this revision will see me feel ready for Monday.
- I read some more *Clean Code* and hope to have it finished in the next few days.
- I then went over some of the code I had written for workshops in week 2 in order to refresh the JS that we had been forsaking this week as we studied UI/UX design.
- After combing through my code I made a few more Anki cards to help me remember concepts that might not otherwise stick in my memory.

This is by far the shortest write-up so far in my 100 Days of Code journal but I am still happy with what I worked on today, especially considering how little time I had to work with. I fear tomorrow may be similar in terms of commitments but I hope at the very least to get a couple more chapters of *Clean Code* finished by the end of this week.

## Day 14
*20230402*

Today I had some friends round to play some poker and just hang out. This meant that I had precious little time to focus on the recap tasks so will have to work on them tomorrow morning.

- I read through the School of Code's guide to clean code which was listed as one of our recap tasks.
- Most of what it said was already familiar to me thanks to my reading *Clean Code*, for example the section on picking expressive names for functions and variables that will be of use to colleagues who have to look at your code in the future.
- In the section on white space they wrote:
	- "Although some of this is opinionated, it's widely thought that space allows our eyes to scan and identify items of interest more easily that clutter. Hopefully you'll agree, and space things out where possible."
- My mentor similarly recommended that I space out code in the same way that paragraphs are used to space out text in a book.
- On the other hand, I have heard it said that too much white space is bad since it means you cannot have as much meaningful code on your monitor at one time, which could actually make reading and understanding the code take longer.
	- I will try and follow my mentor's advice regarding use of white space but can also imagine the benefits of more compactly written code.
- The section on comments was informative, with a couple of examples of good and bad use of comments:

**Bad**
```js
function printMessage() {
  //calls a function
  const comment = document.getElementbyID("comments").value; // declares a variable
  if (comment !== null && comment !== "") {
    //starts an if statement if there's a comment
    return console.log("What a meaningful comment"); //prints a string to the console
  }
}
```
**Good**
```js
//checks to see if there's a comment. If so, returns a message.
function printMessage() {
  const comment = document.getElementbyID("comments").value;
  if (comment !== null && comment !== "") {
    return console.log("What a meaningful comment");
  }
}
```
- I feel like I have fallen into the trap recently of over-commenting, paranoid as I am that I will come back to the code and not understand what it is doing.
- I talked to my mentor about this on Friday and his recommendation that I try not to rely on comments lest I never actually become "fluent" in code makes sense to me.
- Lastly, I installed Node.js LTS as per the recap tasks and checked that it was working by running `node -v` and `npm -v` in a terminal emulator.

Despite not getting much actual coding done today, I was glad to have met up with some friends whom I had not seen in months, so I feel like it was worth it. I am excited to get back in the coding swing tomorrow!

## Day 15
*20230403*

Today we were introduced to **Node.js**, a runtime environment for JS. We were also lucky enough to have an insightful guest lecture from Nadeem, a developer with over 30-years' industry experience, and one of his colleagues, Elly, who is a former SoC bootcamper.

- We started the day by giving feedback to our programming partners from last week which was rewarding and helpful in equal measure.
- We then moved onto a guest lecture from Nadeem and Elly from Talis.
- They talked about TDD, which I knew a bit about thanks to *Clean Code* but was nonetheless glad to have a formal introduction to.
- Nadeem and Elly explained the pros and cons of manual and automatic testing and then revealed that at Talis they use fully automated testing.
- Elly gave some great advice in terms of how to deal with all the new things to learn when you start work at a new company.
	- She recommended just focusing on what you have to learn to solve the issue in front of you.
	- For example, if she has a ticket on sending a query to a database, then the only thing she has to learn about in this moment is how to send a query to a database.
- Nadeem was refreshingly candid and was full of wise words throughout the lecture:
	- He stressed the importance of "disagree and commit" which, funnily enough, was one of the core company values at my previous job.
	- He explained that during an interview he is much more interested in a candidate's capacity for self-motivation and their potential for working well in a team than their current level of coding knowledge.
	- He mentioned how "great software developers are lazy" since they understand that the only problem that needs solving is the one in front of them right now, and they aim to solve it as quickly and with as little effort as possible. Nadeem said that you will probably end up editing this code in the next few days anyway so there is no sense in getting emotinoally invested in it and falling into the trap of "premature optimisation" (which in his view is the main factor separating juniors from seniors).
- Next we met our new partners for the week. I am in a trio this week and both of my partners seem lovely! I was able to help one of them with some bash issues they were having and they were really appreciative of it which felt great.
- We then moved on to a lecture on Node.js
- I learned about `$_` in bash which lets you print the last argument of the previous command that you ran within the terminal:
```bash
touch index.html && code $_
```
- We learned about using `npm init -y` to initialise a new project and create a `package.json` file.
- We ended the day with a workshop putting our nascent Node.js knowledge into practice.
- As a group we got through all the main tasks so got to move onto the bonus tasks.
- I ended up installing a [to-camel-case](https://github.com/ianstormtaylor/to-camel-case) package and got it working in a test `.js` file which was a satisying way to end the day.

Today was really enjoyable, especially the guest lecture. The brief work we did with Node.js already feels more up my street than last week's UI/UX design so I am looking forward to what tomorrow has in store.

## Day 16
*20230404*

Today we started writing our own tests in JS to be checked via [Jest](https://jestjs.io/docs/getting-started) with `npm run test` (or simply `npm t` for short).

- We started the day with some Code Wars.
- We went straight for a 6 kyuu titled [Triple your Money!](https://www.codewars.com/kata/64294e2be00c71422d1f59c2/train/javascript) but soon discovered that it was very maths-heavy.
- We stuck at it, created and adjusted a plan, and managed to work through the problem slowly but surely, ending up with a pair of simultaneous equations before we were called back for a lecture.
- With a bit more time tomorrow I am sure we can get through this one!
- We then had a morning quiz on Node.js, NPM, and ESM in which I managed to get 100%.
	- I really flew through today's quiz which is an encouraging sign and reinforces that this is more my style than the UI/UX design of last week which will need more of my attention.
- We read through some of the [Jest documentation](https://jestjs.io/docs/getting-started) to start getting used to combing through docs which is a key skill for any developer.
- We then moved on to the **AAA Pattern** of **Arrange**, **Act**, and **Assert** which is a key concept in TDD.
- We ended the day with an afternoon workshop in which we wrote various tests across 3 tasks and 1 bonus task.
	- As a group we managed to get through the 3 main tasks and make a start on the bonus task so I am confident that we are ready for tomorrow.

Today was really enjoyable and a fairly gentle introduction to writing tests for our code but I am sure that the unit testing will only get harder from here!

## Day 17
*20230405*

Today marked a definited jump in difficulty as we started writing end-to-end tests.

- We started the day with some Code Wars:
- [Vowel Count](https://www.codewars.com/kata/54ff3102c1bad923760001f3/train/javascript)
```js
function getCount(str) {
  let count = 0
  let array = str.split("");
  for (let i=0; i<array.length; i++){
    if (array[i] === "a" || array[i] === "e" || array[i] === "i" || array[i] === "o" || array[i] === "u") {
    count++;
    }
  }
  return count;
}
```
- I managed to formulate the plan for this **7 kyuu** kata for our team almost instantly and it worked as intended!
- Someone managed to solve it in a much nicer way using a regex:
```js
function getCount(str) {
  return (str.match(/[aeiou]/ig)||[]).length;
}
```
- [Disemvowel Trolls](https://www.codewars.com/kata/52fba66badcd10859f00097e/train/javascript)
```js
function disemvowel(str) {
  let array = str.split("");
  for (let i = array.length - 1; i >= 0; i--) {
    if (/[aeiou]/ig.test(array[i])){
      array.splice(i, 1);
    }
  }
  return array.join("");
}
```
- This **7 kyuu** kata caused us issues since we were trying to start the for loop at `i = 0` and then work upwards.
- This causes the `splice()` method to skip the next letter after each successful deletion.
- By working backwards from `i = array.length - 1` (i.e. the final index) towards `i = 0` the issue of `splice()` changing the indices does not affect us since it only changes the indices above `i`, not below it.
- Once again someone solved it in a much simpler way:
```js
function disemvowel(str) {
  return str.replace(/[aeiou]/gi, '');
}
```
- I made an Anki card for `replace()` using this concise solution as a code example on the back of the card.
- A few minutes later I had a thought about another way to counteract the `splice()` issue of skipping an index:
```js
function disemvowel(str) {
  let array = str.split("");
  for (let i = 0; i < array.length; i++) {
    if (/[aeiou]/ig.test(array[i])){
      array.splice(i, 1);
      i--
    }
  }
  return array.join("");
}
```
- My thought was correct because this code passed on Code Wars too!
	- It feels great to come up with multiple ways of solving a problem, although I am not sure how good of a solution this last one is in terms of memory usage
- We then had a morning quiz on testing in which I got 100% and finished with time to spare which felt great!
- We then had a lecture recapping some of the testing we learned yesterday before moving on to [Playwright](https://playwright.dev/).
- After a brief introduction to Playwright and end-to-end testing we spent the afternoon completing a workshop that was much harder than anything we have previously worked on in testing since it required a lot of our own research into the documentation rather than applying what we had learned in lectures.
- As a group we struggled to get various portions working and found it frustrating but after a short break I came back to the workshop after we had finished for the day and managed to see things with a clearer perspective, successfully rattling off a few basic tests in a row.

All in all, today was one of the harder days so far but I am not too worried as I am sure we will have time to consolidate our learnings and get much faster at writing end-to-end tests.

## Day 18
*20230406*

Today we worked through some more testing cases, heard a guest lecture on LinkedIn and how best to curate your profile, and spent the afternoon on a hackathon covering end-to-end testing.

- Instead of doing Code Wars in the morning, as a group we consolidated what we had learned yesterday about testing with [Playwright](https://playwright.dev/docs/intro) and made sure that we understood all the work we had produced in yesterday's workshop.
	- I feel this was definitely worthwhile as it set us up well for this afternoon's hackathon.
- We then had a mindset lecture on *the inner critic* and building resilience.
- We watched [this YouTube video](https://www.youtube.com/watch?v=d5aVvM4_zpQ) and then discussed different types of inner critic:
	- **The Perfectionist**
	- **The People-Pleaser**
	- **The Pusher**
- I feel like **the Pusher** fits me best, and it was definitely interesting to think about how different people self-assess and self-criticise in their own ways.
- We then moved on to a guest lecture by two LinkedIn employees who covered a variety of topics:
	- How to kickstart your content creation.
	- The anatomy of a great LinkedIn post.
	- Curating your profile.
- I have always seen LinkedIn as a very static social media, only to be updated when you get a promotion or start work at a new company.
- It seems like LinkedIn have made a deliberate push to move the platform from purely professional to both professional and personal.
- I can see the networking benefits of consistently posting on LinkedIn but I also feel very uncomfortable with the idea of spamming my contacts with content that will probably mean very little and not be of much interest to most of them.
- We then moved on to an afternoon hackathon (since tomorrow is a bank holiday) in which we had to read and understand a simple to-do list app and then start writing tests for a sensible user flow that we would come up with.
- It took us a while to get into the swing of things but once we penetrated the syntax, we started to make decent progress.
- I had a mentor meeting just after 17:00 and we spent some time talking about TDD.
- I was surprised to hear that many engineers and many companies do not follow a testing philosophy.
	- I feel like it has already been drilled into me, and had (perhaps naively) assumed that this was an industry standard that all developers would embody.
	- My mentor did mention that he would not want to work at a company that does not follow TDD so it clearly works for him!
	- We also talked about the importance of breaking things since it shows that you are pushing boundaries and adding new functionality to the codebase.
		- One of the guest lecturers this week said that if you are not breaking anything, then you are not *doing* anything.
		
This week was the hardest so far, at least for me. Nonetheless, I feel like it went well and am not worried about testing, as we will be getting more than enough practice and can only get better and faster at writing tests from here. I am sure that before we know it, testing using Jest and Playwright will be as easy as writing a "Hello World!" program. Next week we will be moving on to **React** which is exciting, although I must admit I have no idea what to expect. My mentor mentioned that it adds some object-oriented functionality to JS which sounds interesting. I guess I will found out more soon enough!

## Day 19
*20230407*

Today's bank holiday was not a particularly busy day for me in terms of coding but I did spend some more time consolidating what we learned this week about testing.

- I watched a series of six videos that were linked in one of this week's workshops that explained testing in simple terms.
- The videos started with very basic tests written with if statements that would throw an error `if (result !== expected)`.
- Each video added a layer of complexity in terms of code and convenience in terms of the usefulness of the test.
- Eventually, the code ended up looking just like the tests we were writing this week.
- Thanks to the way that the narrator broke the testing process down and then built it back up, testing has become much clearer to me and I look forward to using Playwright in this week's Recap Tasks.
- I also watched some videos and read some short articles on React in preparation for next week.
- I think I will do some more research in the coming days just to make sure I am in the best possible position come Tuesday.

Overall a fairly relaxed day that I feel I have earned after a tough week learning to write tests. Tomorrow I am meeting up with some fellow bootcampers in London which should be fun, and will be a great opportunity to share our experiences and reflections thus far.


## Day 20
*20230408*

Today I met up with some of my fellow bootcampers in London.

- We planned to meet up in King's Cross in the afternoon and were blessed with good weather.
- A group of five of us walked along the canal for a couple of hours before eventually reaching a bar in Paddington.
- We were joined by a few more bootcampers along with one graduate of bootcamp 13 with whom I had a really informative conversation.
- We talked about interview prep, experiences on the bootcamp, mentors, and more.
- After coming home I spent some time readig *Clean Code*.
	- I have nearly finished it now but there has been a lot more code to read in recent chapters which I must admit has left me stumped, as I have struggled to understand the syntax considering I have only studied JS thus far.
- I spent the evening reading up a bit more on React in order to prepare for next week.

It was really enjoyable meeting up with some fellow bootcampers, having only ever seen them on the other side of a screen thus far. I hope we can organise another meet-up soon!

## Day 21
*20230409*

I spent today reading up some more on testing and React in order to consolidate last week's work and get prepared for Tuesday.

- In terms of testing, [one article](https://blog.logrocket.com/javascript-testing-best-practices/) broke down how to write **detailed test descriptions** into three layers:
	1. The unit to be tested, or test requirement
	2. The specific scenario or action to be tested
	3. The expected result
- [Another article](https://www.freecodecamp.org/news/how-to-start-unit-testing-javascript/) highlighted the benefits of writing unit tests:
	1. Be confident that the code works as intended
	2. Make better architectural decisions
		- E.g. you will not be tempted to give more than one responsibility to a code block as this would make unit testing difficult
	3. Understand functionality before writing code
- In terms of React, [one article](https://survivejs.com/react/getting-started/introduction-to-react/) explained the **Virtual DOM** that exists on top of the real DOM and allows for efficient state manipulation.
	- "Whenever changes are made to it, it figures out the best way to batch the changes to the underlying DOM structure. It is able to propagate changes across its virtual tree".
- I feel like the testing concepts have really sunk in but the React concepts not so much.
- I suppose it is only natural since I have not had any hands-on experience with React yet.

Tomorrow I will work on the recap tasks and should hopefully find them manageable considering all the reading I have done on testing, and after that I will try and get ready for React on Tuesday!

## Day 22
*20230410*

I spent today working on the recap tasks ready for tomorrow.

- The first task had me plan my own Code Wars kata and use Jest to write tests for it.
- After writing a slew of tests I got to work on the actual code that would solve the kata:
```js
function toScreamingKebab(...args) {
    const array = args.map(item => String(item));
    const uppercaseArray = array.map(item => item.toUpperCase());
    const hyphenatedUppercaseArray = uppercaseArray.map(item => item.replace(/[_-\s]+/g, "-"));
    const finalString = hyphenatedUppercaseArray.join("-");
    return finalString;
}
```
- The above code takes one or more arguments, turns them all into strings, makes them uppercase, adds hyphens where appropriate within each string, then adds a hyphen between each argument.
- I found writing the plan for this and executing it to be very straightforward, likely due to the amount of time I spent writing tests and thinking about how the function should work.
	- Through doing this exercise I can see why TDD can lead a developer to write better code.
- The second recap task involved using Playwright to write an e2e test of a simple tweeting application.
- I had issues with Playwright not recognising text that my tests were inputting into the textboxes but other than that the tests worked as expected.

Tomorrow we finally start on React which should be good fun.

## Day 23
*20230411*

Today we made a start on React and learned about props.

- We started the day with some Code Wars in our new groups.
- [No oddities here](https://www.codewars.com/kata/51fd6bc82bc150b28e0000ce)
```js
function noOdds( values ){  
  return values.filter( num => num %2 === 0)  
}
```
- It felt great to get a one-line solution, even if it was only a 7 kyuu kata.
- [Training on Multiples of 3 or 5](https://www.codewars.com/kata/514b92a657cdc65150000006/train/javascript)
```js
function solution(number){
  if (number < 0) {
    return 0
  }
  let arr = []
  for (let i = number - 1; i >= 3; i--) {
    arr.push(i)
  }
  arr = arr.filter(x => x % 3 === 0 || x % 5 === 0)
  return arr.reduce((currentTotal, value) => currentTotal + value, 0)
}
```
- This 6 kyuu kata took us significantly longer to solve but it was worth it as I learned about the `reduce()` method, for which I duly made an Anki card.
- I find that trying to solve Code Wars kata is a great way to learn about JS methods and get to apply them straight away.
- Somebody else submitted a much simpler solution that I like (other than their use of `var` instead of `let`):
```js
function solution(number){
  var sum = 0;
  
  for(var i = 1;i< number; i++){
    if(i % 3 == 0 || i % 5 == 0){
      sum += i
    }
  }
  return sum;
}
```
- We moved on to an introductory lecture on React in which we covered the basics of what React actually is, and the reasons why developers might want to use it:
- **Synchronous**
	- React will keep your app in sync with changes
- **Simplicity**
	- Simple to use once you get the hang of it
- **Modular**
	- Reusable components to break down big tasks
- **Scalable and Maintainable**
	- Your app can grow and maintain efficiency
- **Performance**
	- Reduces latency
- **Open-source**
	- It is free to use and you can contribute to it too
- Widely used and influential
	- Once you know React, other frameworks are similar
- We learned about **JSX**, a syntax extension that lets us write HTML-like code within JS files that will compile down to normal JS code.
- ChatGPT gave me a useful example that compared normal JS code and JSX:
```javascript
const button = document.createElement('button');
button.textContent = 'Click me';
button.addEventListener('click', handleClick);
```

```jsx
<button onClick={handleClick}>Click me</button>
```
- We spent the rest of the day working on two workshops.
- The first was fairly manageable but the second was much more conceptually difficult as we were working with **props** that we had only just learned about in the afternoon.

Today was enjoyable but I am not sure that I have fully grasped props yet. I am not too worried though, since we will have ample time to practise in the coming days.
