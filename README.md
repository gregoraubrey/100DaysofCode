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

## Day 24
*20230412*

Today we covered `useState` in React and worked more on props over the course of a couple of workshops.

- We started the day with some Code Wars kata.
- [Digit*Digit](https://www.codewars.com/kata/546e2562b03326a88e000020/train/javascript)
```js
function squareDigits(num){
  let arr = num.toString().split("")
  for (let i = 0; i < arr.length; i++){
    arr[i] = arr[i] ** 2
  }
  let str = arr.join("")
  return parseInt(str);
}
```
- This first one helped me learn how to use `parseInt()` correctly.
- [The Feast of Many Beasts](https://www.codewars.com/kata/5aa736a455f906981800360d/train/javascript)
```js
function feast(beast, dish) {
  let beastL1 = beast.charAt(0)
  let beastLFin = beast.charAt(beast.length-1)
  let dishL1 = dish.charAt(0)
  let dishLFin = dish.charAt(dish.length-1)
  if (beastL1 === dishL1 && beastLFin === dishLFin) {
      return true 
  }
  else {
     return false    
  }
}
```
- Someone solved it cleverly in one line:
```js
function feast(beast, dish) {
	return beast[0] === dish[0] && beast[beast.length - 1] === dish[dish.length - 1]
}
```
- The regex in this solution seems crazy to me:
```js
const feast = (...args) => /^(.).*(.),\1.*\2$/.test(args);
```
- We then had a morning quiz on yesterday's intro to React in which I only got the final question wrong because I used `:` instead of `=` to assign values to props.
- We then read through [State: A Component's Memory](https://react.dev/learn/state-a-components-memory) in our group.
- Next came a lecture that covered the `useState` hook before we moved onto a morning workshop building a random name generator that changes the name displayed on screen at the press of a button by selecting a random index in an array full of names.
- The afternoon workshop involved getting whatever the user typed into an input field to show up in real time in four different list items, each with its own typeface.
- We managed to get it working just before 17:00 which was extremely satisfying considering how little progress we had made during yesterday's workshops in comparison.
- I also had an "aha" moment in terms of object destructuring and was able to get my components working with and without destructuring:
- **with:**
```js
export function Item({text, font}) {
    return (
        <li style={{ fontFamily: `${font}` }}>
        {text}
        </li>
    );
}
```
- **without:**
```js
export function Item(props) {
    return (
        <li style={{ fontFamily: `${props.font}` }}>
        {props.text}
        </li>
    );
}
```

I thoroughly enjoyed today, especially towards the end when things started falling into place in terms of how to use props.


## Day 25
*20230413*

Today we learned about immutability, the spread operator, and the `map()` function and how it can be used in React.

- We started the day with some Code Wars:
- [Sort array by string length](https://www.codewars.com/kata/57ea5b0b75ae11d1e800006c/train/javascript)
```js
function sortByLength (array) {
  return array.sort((a, b)=> a.length - b.length);
};
```
- We solved this in one line because we knew about `sort()`
- [Highest and Lowest](https://www.codewars.com/kata/554b4ac871d6813a03000035/train/javascript)
```js
function highAndLow(numbers){
  let arr = numbers.split(" ")
  arr.sort((a,b) => a - b)
  let HighLowArr = [arr[arr.length - 1], arr[0]]
  return HighLowArr.join(" ")
}
```
- Someone solved it using `Math.max()` and `Math.min()` which I liked:
```js
function highAndLow(numbers){
  numbers = numbers.split(' ');
  return `${Math.max(...numbers)} ${Math.min(...numbers)}`;
}
```
- [Extract the domain name from a URL](https://www.codewars.com/kata/514a024011ea4fb54200004b/train/javascript)
```js
function domainName(url) {
  url = url.replace("http://", "").replace("https://", "").replace("www.", "");
  let endChar = url.indexOf(".");
  return url.substring(0, endChar);
}
```
- This was the first **5 kyuu** kata I have solved (I think!)
- It took us a while and we only got it finished during lunch
- I like this solution that someone submitted:
```js
function domainName(url){
  url = url.replace("https://", '');
  url = url.replace("http://", '');
  url = url.replace("www.", '');
  return url.split('.')[0];
};
```
- We then had a quiz on `useState` in which I got 2 questions wrong, one of which was because I forgot that the `useState` hook must be called within the functional component body, and not inside an if statement.
- We moved on to a mindset lecture on decision making where we learned about **dot voting** as a way to quickly make decisions that we could otherwise deliberate on for hours.
- Next was a lecture on **immutability** and the **spread operator**.
- We made a start on a workshop that covered array methods but did not have much time before we were called back to have a go at a second workshop.
- The second workshop was on how we can make use of what we learned today within React but we did not have much time on this one either!

Today was absolutely jam-packed but I feel like I learned a lot. I look forward to putting some of it into practice during tomorrow's hackathon!


## Day 26
*20230414*

Today was Hackathon Friday, so we spent the whole day working on a **to-do list** React app.
- We started off by planning out our components and the parent-child structure.
- We decided to have `Input` and `List` that would both receive props from `App`.
	- Looking back, we could have broken things down further and split `Input` into a *submit button component* and an *input field component*, and similarly split `List` into a *list item component* and a *delete button component*.
	- This would have helped with separartion of concerns and made our components more modular and therefore more useful when it comes to reusing them, since you could access, say, the delete button without also accessing a list item.
- We struggled at times to get our heads around which variable names were referencing what in the code.
	- I am sure that this could have been remedied by starting off on the right foot with a more robust plan and tree diagram.
- We learned about the `trim()` method, which we used in an if statement:
```js
function handleClick() {
    if (text.trim() !== "") {
      console.log("Adding item:", text);
      setItems([...items, text]);
      setText("");
    }
  }
```
- This allowed us to not make an empty list item appear when the button is clicked whilst the input field is empty.
- The `trim()` method makes it so that the same applies even if the user spams the spacebar and then clicks the button, since the whitespace is trimmed down before being compared to `""`.
- The rest of the function adds the current value of the input field to the end of the `items` array by using the **spread operator** to spread out each index already in the `items` variable.
- Then we set the value of the input field back to an empty string so the user can start typing in a new to-do.
- We also added a `console.log` to check that the value of the input field was being correctly passed into the function.
- By the end of the day we had a working app and were nearly there with one of the bonus tasks which involved adding a button or checkbox to each list item that would strike through the text.
- It was fun hearing from other groups during the presentations at the end, and it was really motivating to see the great work that they had produced.
- Just after 17:00 I had an excellent mentor meeting that lasted for a full hour and was jam-packed with useful learnings and insights.
- We talked about a whole range of topics:
	- OOP vs functional programming.
	- Strongly-typed vs weakly-typed languages, and "casting" variables in the former.
	- Memory management and how best to approach learning it.
	- Having the confidence to break programs and push the envelope of what the code can do.
	
This week has flown by, and thanks to the bank holiday on Monday we have had to whizz through React. I feel like I have learned so much in such a short space of time, although I recognise that there are definite gaps in my knowledge, for example my understanding of state variables and passing in unique keys when rendering components is not quite there yet. I cannot wait to jump into some more React next week and take things even further!


## Day 27
*20230415*

Today I spent time consolidating what we learned this week by reading articles, watching videos, and testing out some code.

- I practiced switch statements after forgetting how they worked earlier this week by following along with [this YouTube video](https://www.youtube.com/watch?v=2gE2K8i5tvs&list=WL&index=75) that was nice and short but contained all the info I needed to remember how to use switch statements going forwards.
- I then made an Anki card just to make sure I don't forget the syntax I practiced today.
- I watched [another video](https://www.youtube.com/watch?v=NIq3qLaHCIs&list=WL&index=74&t=1s) from the same channel that covered array/object destructuring.
- I followed along as the code went from simple examples of skipping items in an array (`const [first, second, third, , , sixth] = alphabet;`) to using object destructuring within the parameters of a function:
```js
function printPerson({ name, age, address: { city, country } }){
	console.log(`Name is ${name}, age is ${age}, city is ${city}, and country is ${country}.`);
}
```
- I feel like I understand enough about destructuring now to use it with confidence, although I am still not sure what is going on under the hood when you destructure an object.
- I also read a few short articles on the basics of React and plan to dive deeper tomorrow as I work on the recap tasks for this week's content.

Today was fairly relaxed and afforded me a much-needed rest after the lightning-quick pace with which we zoomed through the basics of React this week. I hope that what I have worked on today will stand me in good stead for tomorrow when I work on the recap tasks.

## Day 28
*20230416*

If yesterday was relaxed then today was the complete opposite! I spent the day reading more about React then started work on the recap tasks in the evening. Little did I know just how challenging they would be!

- I read a few more articles on React throughout the day, not to learn anything new but rather to consolidate what I have already learned this week.
- After dinner, I began work on the recap tasks thinking that they would take me no more than a couple of hours.
- Unfortunately, I was sorely mistaken as the tasks involved building a funcional blog post page where the user could type in an **author** box and in a **comment** box too before clicking a **submit** button to have the inputs render at the end of a comment list underneath the blog post.
- Conceptualising how the app would function and thinking about parent-child relations in terms of passing down props was not too difficult, and only took a few minutes of consideration.
- The implementation started off smoothly enough but became a nightmare when the program got bigger and it came time to code the funcionality for having the `CommentForm` component receive a prop in the form of a function for handling the clicking of the submit button:
```js
function handleCommentSubmit(commentData) {
    let author;
    if (commentData.author.trim() === "") {
      author = "Anon Author";
    }
    else {
      author = commentData.author;
    }
    const newComment = {
      id: comments.length + 1,
      author: author,
      content: commentData.comment,
    };
    setComments([...comments, newComment]);
  };
```
- It took a fair bit of help from ChatGPT to break things down and explain concepts but eventually I got a working MVP that would take a user's name and their comment, and then append it to the end of the current list of comments.

I will definitely need to have a reread of my code tomorrow so I don't forget everything I have worked on today. It was tough at times to keep track of all the different variable names, props, and functions throughout all the files containing my components, so looking over the code with a fresh perspective should help cement everything I have learned in making this app. Despite how long it took and how tired I am right now, it feels great to have it working at last, and I know I will be able to refer back to this project next week if I get stuck on something, so that should be a great help.


## Day 29
*20230417*

Today we learned about the `useEffect` hook in React and made a simple app using it along with the Pokemon API that we used a few weeks ago in a hackathon.

- We started off the day by giving feedback to our programming partners from last week.
- The three of us gave each other some encouraging feedback about how we had handled the hackathon last Friday and agreed that we would like to work together again, given the chance.
- We then had a guest lecture by a UX designer who talked through the whole process of redesigning his company's US website which has been his main focus lately.
- He talked about **Miller's Magic Number 7** which I had not heard of, and **Jakob's Law of Web Experience** which we had talked about briefly in Week 3.
- Next was a lecture on `useEffect` and some time spent [reading the documentation](https://react.dev/learn/synchronizing-with-effects).
- We also learned about **pure functions** and how React assumes that every component in a project is a pure function.
- Pure functions always return the same output given the same input, and do not modify any data outside of the function's scope.
- We ended the day with a workshop that involved using `fetch` to send a GET request to the [Pokemon API](https://pokeapi.co/?ref=public-apis) (that I used in my Week 2 hackathon) and then change the ID to a random number between 1 and 151 every time a button is clicked, which would cause the page to display the sprite, name, and pokedex number of the new Pokemon.
- Here is a snippet from the `PokemonViewer` component:
```js
function PokemonViewer({ id }) {
  const [pokemon, setPokemon] = useState(null);
  useEffect(() => {
    async function fetchPokemon() {
      const response = await fetch(`https://pokeapi.co/api/v2/pokemon/${id}`);
      const data = await response.json();
      console.log(data);
      setPokemon(data);
    }
    fetchPokemon();
  }, [id]);
```
- And one from the `App` component:
```js
function App() {
  const [id, setId] = useState(null);
  function handleClick() {
    let randomId = Math.floor(Math.random() * 151) + 1;
    setId(randomId);
    console.log(id);
  }
```

Today felt much more well-paced than much of last week, and I was able to finish the whole of the workshop just after 17:00 which is a good sign. I still feel like I need to look over the recap tasks from Sunday just to consolidate all the code I wrote, so I will do that tomorrow.


## Day 30
*20230418*

Today we learned about the `useReducer` hook in React and consolidated some of what we had learned yesterday and last week.

- We started off the day with just under an hour of Code Wars.
- [Adding Big Numbers](https://www.codewars.com/kata/525f4206b73515bffb000b21/train/javascript)
```js
function add(a, b) {
  let aArr = a.split("").map(Number).reverse();
  let bArr = b.split("").map(Number).reverse();
  let resultArr = [];
  let carry = 0;
  for (let i = 0; i < Math.max(aArr.length, bArr.length); i++) {
    let sum = (aArr[i] || 0) + (bArr[i] || 0) + carry;
    resultArr.push( sum % 10);
    carry = Math.floor(sum / 10);
  }
  if (carry > 0) {
    resultArr.push(carry);
  }
  return resultArr.reverse().join("");
}
```
- This was my first time solving a **4 kyuu** kata!
- We needed some help from ChatGPT to explain why we could not use `BigInt()` and then realised that the whole point of the kata was to find a way around it.
- [Remove the minimum](https://www.codewars.com/kata/563cf89eb4747c5fb100001b/train/javascript)
```js
function removeSmallest(numbers) {
  let newArray = [...numbers]
  let lowestNumber = Math.min(...numbers)
  newArray.splice(newArray.indexOf(lowestNumber), 1)
  return newArray;
}
```
- This **7 kyuu** kata was fairly quick to solve and was a nice contrast with the previous kata that had taken us around 40 minutes to solve.
- We then had a morning quiz on `useEffect` in which I only made one mistake, opting to put the word `async` before the callback function (`useEffect(()=> {`) instead of before the function on the line below (`function getJoke() {`).
- After the quiz we had a short lecture on **switch statements**, since they appear in the docs for `useReducer`.
	- I felt very comfortable here since I talked about switch statements during my progress interview last Thursday as a way to improve some of code I was shown, and I also revised them over the weekend.
- Next we learned about `useReducer` and [read some documentation](https://react.dev/learn/extracting-state-logic-into-a-reducer).
- We started work on a workshop that saw us refactoring an app with two buttons (one for adding 1 to a count and one for subtracting 1) by replacing `useState` with `useReducer`.
- We did not get the whole task finished before lunch but we had some time before the end of the day to get it done which was satisfying.
- The second part of the task involved refactoring an app that lets the user input a name, and upon the click of a button makes that name appear at the end of an unordered list.
- We took it from `useState` to `useReducer` and also added a unique key to each list item by including an extra key-value pair in the object:
```js
function namesReducer(state, action) {
  switch (action.type) {
    case "ADD_NAME":
      return {
        names: [...state.names, {
          name: action.payload.newName,
          id: action.payload.id,
        }],
      };
    default:
      throw new Error();
  }
}
```
- The rest of the day was given over to us to spend time looking back over all we have studied thus far in React to give us a chance to brush up on areas that we did not get the first time round.
- Our group used this time to add the unique key functionality shown above, before splitting off to read over some docs that we used last week.

Today was confusing at first but after seeing a couple of examples of `useReducer` in action I feel like I have a decent grasp of how to use it. I am sure that things will only get clearer the more we see this hook come up in the code that we read or write.


## Day 31
*20230419*

Today we started learning how to test React components using [React Testing Library](https://testing-library.com/docs/react-testing-library/intro/).

- We started off the day with a pretty unsuccessful Code Wars session.
- We started work on one kata before discovering that people had left comments saying that the tests do not work as intended for JS, so we had to cut our losses and move on to another one.
- [Find Cracker.](https://www.codewars.com/kata/59f70440bee845599c000085/train/javascript)
```js
function findHack(arr) {
  let lettersArr;
  let sum = 0;
  let hackers = [];
  for (let i = 0; i < arr.length; i++) {
    if (arr[i] && arr[i][2]) { // Check if arr[i] and arr[i][2] are defined
    lettersArr = arr[i][2]
    sum = 0;
    for (let j = 0; j < lettersArr.length; j++) {
      switch (lettersArr[j]) {
          case "A":
            sum = sum + 30;
            break;
          case "B":
            sum = sum + 20;
            break;
          case "C":
            sum = sum + 10;
            break;
          case "D":
            sum = sum + 5;
            break;
          default:
            break;
      }
      console.log(sum);
      if (lettersArr.length >= 5 && lettersArr.every((x)=> x === "A" || x === "B")) {
        sum = sum + 20
      }
      if (sum > 200) {
        sum = 200
      }
      }
      if (sum !== arr[i][1]) {
        hackers.push(arr[i][0]);
      }
    }
  }
  return hackers
}
```
- The above is our attempt thus far (that does not pass the tests).
- We may well come back to this **6 kyuu** kata tomorrow.
- After Code Wars we had a morning quiz on `useReducer` in which I scored 100% which was delightful after the fruitless Code Wars session prior.
	- I say fruitless, it was still useful despite our not passing any of the kata, as we had the chance to practise writing switch statements and build on our problem solving skills in general.
- Next came a lecture on using `git checkout -b new_branch_name` to create new branches, and the consequences of that, such as solving merge conflicts when attempting to merge the new branch into master/main.
- I felt fairly confident in this having gone through the [Oh My Git!](https://ohmygit.org/) game as part of the pre-course learning.
- We moved onto a workshop in which our group of 3 had to make various edits to a file in our own branches before attempting to push the changes and merge the branches into main.
- We managed it without too many hiccups, although one member of our group was used to using VS Code's graphical VCS instead of the CLI, so we had to lend a helping hand in terms of explaining the basic git commands and what they accomplish.
- After that we had a lecture on testing React componenents during which we were sent into breakout rooms to read through three doc pages:
	- [Introduction](https://testing-library.com/docs/react-testing-library/intro/)
	- [Code example](https://testing-library.com/docs/react-testing-library/example-intro)
	- [Details on render](https://testing-library.com/docs/react-testing-library/api#render)
- We then came back and discussed our learnings from this reading and discussed a few key questions that we had been posed before we began looking at the docs.
- I really enjoyed this method of going through the docs with specific questions in mind and then sharing our thoughts in the main room, and the more practice we get reading documentation the better, since I know it will be a big part of any developer's future.
- Having read the docs, we worked on a second workshop, this time focusing on using React testing library to test a pre-built app that takes a user input and adds it to a list, and then allows the user to click on the list item to strike through it.
- This was fine as soon as we read up on mocking and `jest.fn()` which was needed in order to complete each task.
- I duly made an Anki card on the concept of **mocking** so I don't forget about it in a few days' time!

Overall today was well-paced and the testing felt reasonably comfortable and manageable since it built on the testing we have done with Jest and Playwright. The more practice we get with git branches, the better, and I am sure that we will get a lot of that during next week's project!


## Day 32
*20230420*

Today we focused on the Agile methodology to make sure we understand what an Agile team actually looks like, in preparation for next week's project.

- We started the day with some Code Wars as usual.
- [Who likes it?](https://www.codewars.com/kata/5266876b8f4bf2da9b000362/train/javascript)
```js
function likes(names) {
  if (names.length === 0) {return "no one likes this"};
  if (names.length === 1) {return `${names[0]} likes this`};
  if (names.length === 2) {return `${names[0]} and ${names[1]} like this`};
  if (names.length === 3) {return `${names[0]}, ${names[1]} and ${names[2]} like this`};
  if (names.length > 3) {
    return `${names[0]}, ${names[1]} and ${names.length - 2} others like this`;
  }
}
```
- We solved this **6 kyuu** kata pretty quickly, and our first idea of how to go about it was the right approach, which felt great!
- One of the submitted solutions used a switch statement which, looking back, makes much more sense than having a load of if statements one after the other.
	- I am surprised that none of us thought to use a switch statement since we have just practiced them. I suppose we just came up with our approach so quickly that we never stopped to look back and refactor our code before submitting, which could be an area for improvement.
- [Count characters in your string](https://www.codewars.com/kata/52efefcbcdf57161d4000091/train/javascript)
```js
function count(string) {  
  const occurrences = {};  
  for (let i = 0; i < string.length; i++) {  
    const char = string[i];  
    if (occurrences[char]) {  
      occurrences[char]++;  
    }
    else {  
      occurrences[char] = 1;  
    }  
  }  
  return occurrences;
}
```
- This was another **6 kyuu** kata but this one was much harder.
- I had to work on this one after the Code Wars session and needed guidance from ChatGPT to get it working.
- The `if (occurrences[char])` condition was the main issue I was having. Once I understood that, the rest seemed fairly simple in comparison.
- After Code Wars we moved onto the morning quiz which covered git branching and React testing.
- I got 100% again which felt great, and reaffirmed my confidence that I had taken in yesterday's material.
- Next came a mindset lecture on **Team Dynamics** and how best to realign after an issue has come up.
- We talked about "psychological safety" which was apparently the critical factor to team performance according to Google's Project Aristotle, although I must confess I had never heard of the phrase before today.
- Our next session was a lecture on the Agile methodology in which we dived into the 4 core values and the 12 Agile principles, at one point splitting up into groups and matching up the principles to the core values as we saw fit.
	- We found that a large percentage of the principles could be linked to more than one core value which suggests a cohesion and synergy throughout the whole methodology.
- Our final task of the day was to research various terms to do with Agile development, such as **scrum**, **product backlog**, **kanbans** (which we used at my previous job!), and **Extreme Programming** to name a few.

Overall, today was not too heavy on the coding, although the second Code Wars kata certainly took some time and effort. I feel the itch to dive back into React having hardly touched it today and I feel I am ready to hit the ground running in tomorrow's hackathon!


## Day 33
*20230421*

Today we spent the whole day on a hackathon in which we were given free rein to pick an API and make whatever React app we could think of.

- We were given [this list](https://apilist.fun/) of APIs for inspiration, and we ended up picking [Intellexer](https://apilist.fun/api/intellexer) because the possibilities seemed really interesting since it uses big data.
- We used [Postman](https://www.postman.com/) for the first time which let us test out the functionality of the API in a quick and easy manner.
- After one of our team members signed up to Intellexer for free, we got given an API key and started to get responses on Postman.
- Not all of the features were working, such as the summarisation of multiple URLs, so in the interest of time and getting an MVP up and running, we scaled back and decided to focus our app on just the spell-checker feature of the API.
- This required us to use the POST method to send a string of one or more misspelled words to the API, which would then return a response that we could parse into an object that contained the corrected string nested within a one-item array as one of the key-value pairs of the object.
- We used [Trello](https://trello.com/), which we learned about yesterday, to try and adopt an Agile workflow by moving small tasks through the pipeline, although after we finished making a workspace, we never went back to it for the rest of the day, so there is room for improvement there.
	- I am sure that Trello will prove indispensable next week when we will be working on a project for a week instead of just a day.
- We also used Figma to make a lo-fi wireframe of our intended MVP that still ended up having more features than the final result.
	- I guess the takeaway is that the MVP should be just that, the smallest possible implementation that does the job. We definitely started out with lofty ambitions that slowed us down at points. Having a clear idea of a bare-bones MVP would have streamlined our work and helped us to get a working app much sooner.
- After some issues retrieving the relevant string from the API's response, we got a working app that was simple enough (although not at all simple to make at the time!).
- There was an input field, a submit button, an undo button, and an unordered list underneath the input field that would save all of the corrected text.
- Each time the button was clicked (unless the input field was empty, thanks to `if (text.trim() !== "") {`, a `fetch` request would go to the API containing the current value of the input field (thanks to an updating state) at the time the button was clicked.
- The response would be parsed, then the relevant string would be filtered out and sent down as a prop to the Output component, once again thanks to an updating state via the following function which adds the latest string to the array containing all the previous responses:
```js
setCorrectedText(prevCorrectedText => [...prevCorrectedText, data.processedSentences[0]]);
```
- The function that is called `onClick` when the undo button is pressed is similar:
```js
function handleUndo() {
    setCorrectedText(prevCorrectedText => prevCorrectedText.slice(0, -1))
}
```
- We hastily added some CSS right at the end to make the app look clean and professional, and then it was presentation time!
- As always it was a delight to see what other people had come up with, from pictures of Mars to cocktail recipes.
- Our presentation went well because we had devoted a few minutes before 16:00 to planning out who would say what and in which order, and that was definitely time well-spent.

Today was a real lesson in making sure the MVP is truly as minimal as can be. Despite not managing to implement all the features we would have liked, we ended up creating a legitimately useful spell-checker, and used POST for the first time. I had a mentor meeting after 17:00 in which we talked about looking back on an app and thinking, "wow, I could have made that in an hour or two", which he says is part and parcel of creating software: you never know exactly what you are building until it is done, and then once you look back the path seems obvious, but only because you have already trodden it. I am going to take it easy over the weekend and just revise some of the React from this week before we begin our project on Monday. Exciting times ahead!


## Day 34
*20230422*

I did not do too much coding today, choosing to take a break after a long week. Nonetheless, I am happy with how I spent my time and look forward to a more active day tomorrow.

- I went through some videos on React once more just to make sure I am keeping on top of things:
	- [What Is React Testing Library?](https://www.youtube.com/watch?v=JKOwJUM4_RM&list=WL&index=69)
	- [Learn useReducer In 20 Minutes](https://www.youtube.com/watch?v=kK_Wqx3RnHk&list=WL&index=67&t=3s)
- I also read some more of *The Clean Coder* which I am greatly enjoying so far, although I am only 3 chapters in.
- The author's attitude towards professionalism and the responsibility of a clean coder to be honest about delivery times and thorough in their implementing and testing of code has left an impression on me, and I hope I can emulate this approach in my career.
- I also went back over the workshops we did this week and read through the code to make sure I remembered what it was all doing and why it was there.
- In some cases I needed a hint from ChatGPT but on the whole I was pretty comfortable looking back on the code we had written, which is a good sign that I am not just using what we learn in the lectures and then forgetting it all the next day.

Tomorrow I will look into the tasks we have been set this weekend in order to get ready for Monday, and hopefully get through another decent chunk of *The Clean Coder* so that I will be ready to start on a new book sometime next week.


## Day 35
*20230423*

Today I went through the tasks we were set for the weekend and spent some more time reading *The Clean Coder*.

- This week's recap tasks were not focused on writing code but rather researching in preparation for Monday.
- I acquainted myself with [Midjourney](https://docs.midjourney.com/docs/quick-start), which will apparently help us "create user-centric and visually appealing designs more efficiently".
	- Some of its creations are startlingly good, and had me thinking both about the ways in which this technology will disrupt existing industries, and the issues around copyright law and its enforcement.
- Next I looked into the basics of a couple of React UI libraries:
	- [Material UI](https://mui.com/)
	- [Chakra UI](https://chakra-ui.com/)
- By leveraging UI libraries we can spend more time on the features and functionality of our app rather than focusing on designing components, so I am sure that these will come in handy next week.
- The last things to look into were [Trello](https://trello.com/), which I had already used briefly during Friday's hackathon, and [FigJam](https://www.figma.com/figjam/), a real-time collaboration program that could help us brainstorm ideas.
- I ended the day by reading some more of *The Clean Coder* and hope to have it finished in the next couple of days.

All in all this weekend has been fairly laid-back, with a bit of revision, reading, and research to tide me over before Monday. I am honestly not sure what to expect from the first day of our week-long project but I am certainly excited!


## Day 36
*20230424*

Today marked the start of our week-long project!

- I began the day by meeting my three teammates for this project, two of whom I have worked with in previous weeks.
	- We got on really well when we worked together last so that bodes well for this week.
- Chris Meah gave a brief introduction to project week and had us work in our teams on **10-second intros** that outlined why we were interested in technology, which are sort of like an elevator pitch but for yourself instead of a product or business.
- Our first task as a team involved coming up with a manifesto, which ended up being 10 bulletpoints that we all agreed on fairly quickly, with topics ranging from how to approach writing code, to how to treat one another.
- Our brief was to pick up on a common issue that has been affecting bootcampers in their learning journey and, over the course of a week, make an app that could alleviate that issue.
- We brainstormed and used dot-voting on [FigJam](https://www.figma.com/figjam/) to eventually decide upon a flashcard app to help people remember content from past weeks that they would otherwise forget due to not seeing it come up in their code for an extended period of time.
- Next, we drafted up an MVP along with various stretch goals.
	- We were very careful to make the MVP as minimal as possible, so that we would not run into the issue I had in the previous hackathon in which our initial conception of an MVP ends up actually being far too complicated to achieve within the given timeframe.
	- There is no harm in labelling some fairly standard features as stretch goals in this case (e.g. the ability to add tags to a flashcard).
- We made a very basic lo-fi wireframe using [Figma](https://www.figma.com) before making a [Trello](https://trello.com/) workspace based on a community template.
- That was all we had time for today before our new daily retrospective, in which we agreed that we had done a good day's work and were excited to pick up from where we had left off tomorrow.

I feel like we have made a really strong start to project week and cannot wait for tomorrow so we can make more progress!


## Day 37
*20230425*

Today we completed a hi-fi wireframe and made a start on coding our app!

- We kicked the day off with a stand-up meeting in which we discussed our targets for the day and made one or two changes to the Trello workspace to reflect our discussion.
- After this we had a guest lecture from a former bootcamper (cohort 2) who talked about his experiences in the industry thus far.
- He gave some really useful advice in terms of spotting whether a company will be good for your development or not, and talked through various misconceptions that we might have about the industry and about a normal working day.
- His insights into the Personal Development Plan you have at a company were valuable, and he is the first guest lecturer to have mentioned a PDP.
- He mentioned that by the time we reach the end of the bootcamp and are working on our final project, an average day for us will be quite similar to an average day for him in industry, which is both exciting and intimidating in equal measure.
- After the guest lecture, we got back to work on our project and finsihed up our component tree so that we could split up the files amongst the four of us and start coding them up.
- Before we made a start on coding, we made a hi-fi wireframe together.
- I used [Midjourney](https://www.midjourney.com/) to generate a plethora of sample images that we could use in our wireframe (and eventually our final app).
	- I must not be very good at prompt engineering, since I tried and failed multiple times to get Midjourney to create a sheet of paper with torn edges.
	- Instead, it kept creating strange pieces of art with shards of paper growing out of a sheet of A4.
- After we agreed on the final version of our hi-fi wireframe, we split into pairs and made a start on coding up the components.
- My partner and I worked on the `Input` component and made a random number generator that would be used to select a random index of the array containing all the flashcard data inputted by the user.
- We worked in separate branches and merged them into `main` when we were done, but had to deal with a minor merge conflict due to both pairs making slight changes to the `App` component.
- This was easy enough to resolve on GitHub, although had we had more time at the end of the day I would have liked to try and have a go at resolving the issue purely in the terminal to get some practice in.
	- This just goes to show the importance of separation of concerns in an app, and of being explicit when agreeing on who will work on what in a project, so that one team's work does not impede another's.
- We did not have much time for coding before it was time for our end-of-day retro but I am not concerned as we will have all of Wednesday and Thursday to dive into the coding side of things.

I feel like we are keeping a good pace and I expect that by the end of the day tomorrow we will have completed our MVP and be deciding on which stretch goal to aim for first. I can't wait to get back to the code and get it all working!


## Day 38
*20230426*

Today we got our MVP functional and then spent the rest of the afternoon trying to sort out some styling with CSS.

- We began with our daily stand-up meeting in which one of my teammates explained that he had been researching local storage last night and was interested in trying to integrate it into our app, so that the flashcard array would not be wiped if the user refreshes the webpage.
- We got our MVP working just before lunch which was very satisfying, since it meant that we would have more than a day free to work on additional features.
- After lunch, I worked with my aforementioned teammate on implementing the local storage functionality and got it working which felt great since we had managed to add a feature that we have not studied at any point thus far during the course.
- We then spent the rest of the afternoon as a group of four attempting to sort out all the styling using the Midjourney images I generated.
	- We definitely need to work on our CSS knowledge because getting the CSS to work in the way we had envisioned was just as hard as coding up the logic of our flashcard app!
- We ended the day with a retro in which we agreed that we would split into two teams tomorrow to work on testing and the rest of the CSS.
- I ended the day by running `prettier -w` on our components to make sure that the formatting stays consistent.

Today was the most enjoyable of the week so far since we managed to get our MVP done and dusted. Having it completed really takes the pressure off so I am looking forward to testing tomorrow and hopefully adding some of the additional features that we laid out in our stretch goals on Monday.
