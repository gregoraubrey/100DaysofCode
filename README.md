# 100DaysofCode

## Word Count: 43594

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


## Day 39
*20230427*

Today we put the finishing touches on our app and planned out our presentation ready for tomorrow.

- We kicked off the day with our daily stand-up in which one of my teammates showed us the CSS he had been working on to try and get our images to appear in the right place.
- We merged these changes into `main` with no conflicts.
	- This is one area in which we have improved a lot. We were having all sorts of merge conflicts when we started out but in the last two days we have not had a single one.
- Today it was my turn to go and present to the coaches what we had been up to, so I talked about how we had finished our MVP and were planning to finalise our CSS, sort out the one bug we had noticed, and then start planning out our presentation.
- The bug in our code showed up whenever a user refreshed the page and then immediately clicked Test Me before adding another flashcard.
- In this case, only the premade flashcards would show up, and the flashcards saved in local storage would only resurface when the Add Flashcard button had been pressed (successfully) at least once.
- We realised that our state variable was causing the issue, since it was declared as:
```js
const [data, setData] = useState(dummyDataSet);
```
- The issue here is that when the state initially renders upon the reloading of the page, the `data` array is always set to the original `dummyDataSet` variable which contains three premade flashcards.
- In order to fix this we had to set the `data` array to the value of the local storage first, and only use the value of `dummyDataSet` if there was no local storage to be found:
```js
const [data, setData] = useState(
    JSON.parse(localStorage.getItem(keyName)) || dummyDataSet
  );
```
- The variable `keyName` in this instance is just a long string of random characters.
	- This was based on a recommendation from one of my teammate's mentors, since if we had gone with a common name such as "data", then if any other program used that same name, we would have run the risk of having our local storage overwritten.
- After that quick fix, I worked with another teammate on testing using React Testing Library whilst the other half of the team finalised the CSS, including putting our team logo (created by Midjourney) in the corner of the app.
- We certainly did not achieve 100% code coverage but we did write some useful passing tests, such as one that checks if clicking the Add Flashcard button appends the data in the input boxes to the end of the array.
- In future projects I would like to at least try following [Red, Green, Refactor](https://www.codecademy.com/article/tdd-red-green-refactor)/[the three laws of TDD](http://butunclebob.com/ArticleS.UncleBob.TheThreeRulesOfTdd) since they make so much sense to me conceptually.
	- I do not feel too bad about not adhering to them in this case since we had such a short amount of time to actually write the code for an entire project.
	- With that said, I definitely want to get into the habit of writing good unit tests as soon as possible since I know they will be indispensable in industry.
- In the afternoon we watched a couple of recordings of presentations given by the previous cohort that one of the coaches had shared with us.
- Using these videos as inspiration, we set to work on a Google Slides document, making use of all the screenshots we had taken along the way to show the journey of our app.
	- Taking screenshots at regular intervals was definitely a good idea and one to use again as it has made planning our presentation so much easier.
- We ended the day with a retro in which we all agreed that we had done a good day's work and were delighted to finally have the CSS debacle behind us.

Tomorrow we will finalise our presentation before delivering it in front of some of School of Code's employer partners which is a real privilege and should be a lot of fun!


## Day 40
*20230428*

Today we finalised and practised our presentation before delivering it to the SoC judges.

- We began the day with our daily stand-up in which we merged one small change that a teammate had made on a separate branch which removed the grey border from the input textboxes and rounded the edges slightly.
- We then got to practising, attempting to get our whole presentation done in as close to ten minutes as possible by timing ourselves with each trial run.
- At one point, one of the coaches came and watched a trial run and gave us some feedback and mentioned some potential questions that the judges might ask, such as:
	- Git branching - what was your strategy?
	- How did you make decisions when there was a conflict?
	- Working as a team - how did you handle feedback?
- We kept practising until it was finally presentation time in the afternoon.
- The presentation went really well, and one of the judges complimented us on how smoothly the presentation went and said that it was clear that we had practised a lot!
- It felt amazing to have a week of hard work culminate in such a successful presentation!
	- I can only imagine how good it will feel to present at the end of our 5-week project.
- Just after 17:00 I had a mentor meeting in which we discussed various topics including...
	- people's attitude to learning and progressing beyond junior and mid-level roles.
	- how to incorporate TDD into my own work now so that it does not feel foreign when I am in a job.
		- This is something that I am very keen to get in the habit of following since, despite writing some good tests, we only implemented our tests after writing the code to make them pass during this project.
	- how much actual presenting software developers do, and how it changes depending on their seniority.
	
Today was definitely my favourite day thus far on the bootcamp! My teammates and I all agreed that we worked brilliantly together and are going to be sad not to be able to continue that relationship come next week. I cannot wait to dive into back-end work now!


## Day 41
*20230429*

Today I took it easy after a long week working on our project, choosing to look over some code I had written in previous weeks and read some more of *The Clean Coder*.

- I looked back at the whole codebase for our week-long project and focused especially on the CSS, since that is definitely a weak-point of mine right now.
	- I spent some time reading up on CSS Grid and Flexbox again as all four of us on the team had issues with getting elements to appear in their intended place on the page.
- I looked over some of the code I had written that made use of `useEffect`, since that did not come up in our project this week.
- I also rewatched a couple of short introductory videos to said hook on YouTube.
- In the evening I read some more of *The Clean Coder*.
	- I am really glad that my mentor recommended it to me as I am finding it very useful, and a lot easier of a read than *Clean Code* in which most of the example code and some of the concepts went right over my head.
- I am nearly done with *The Clean Coder* now and hope to have it finished by Monday.

All in all a restful day, though a deserved one in my eyes. Tomorrow I intend to do some more revision and finish *The Clean Coder*.


## Day 42
*20230430*

Today I spent more time going over previous topics and then finished *The Clean Coder* in the evening.

- I looked over some of my code that featured `useReducer` in the same way that I looked back at `useEffect` yesterday.
- I rewatched [this YouTube video](https://www.youtube.com/watch?v=kK_Wqx3RnHk) on `useReducer` just to make sure I was understanding the code I was reading correctly.
- In the evening I finished reading *The Clean Coder*.
- I have taken a lot of notes on a variety of topics from this excellent book, including:
	- Not building "walls of ownership" around code.
	- Calculating the cost of being in a meeting.
	- The Three Laws of TDD.
	- Working overtime as a developer.
- I am not sure what book to read next, although I am leaning towards [The Object-Oriented Thought Process by Matt Weisfeld](https://www.goodreads.com/book/show/4795641-the-object-oriented-thought-process) which was recommended to me by my mentor as a good introduction to OOP.

It is always a nice feeling to finish a book, especially when I have gained so much from the reading experience! Tomorrow is a bank holiday so I think I will take the opportunity to do some more revision and perhaps start on another book if I feel like it.


## Day 43
*20230501*

Today I started reading another programming book and read through some programming articles I had saved for later.

- I decided that I would make a start on the fifth edition of [The Object-Oriented Thought Process by Matt Weisfeld](https://www.goodreads.com/book/show/4795641-the-object-oriented-thought-process?from_search=true&from_srp=true&qid=WMwHuvxxft&rank=1).
- I have only finished the introduction but am feeling encouraged since the author has stressed that this is a book for beginners about concepts and is not targeted towards any one specific OO language.
- I also spent some time reading various programming articles that I had saved for later over the last couple of weeks.
	- These articles covered everything from testing to job hunting.
	- I try to go through my backlog at least once every couple of weeks just to avoid ending up with a daunting pile of articles that I will realistically never get around to reading.
	
Today was not too involved as I spent a lot of the day outside enjoying the sunshine. I am itching to get back into the swing of things tomorrow!


## Day 44
*20230502*

Today we began revising topics that we have studied thus far, which will be our focus for this week.

- I had been under the impression that we would start work on the back-end this week but it turns out that we will be spending a week revising all of the front-end material we have learned before moving onto the back-end next week.
- We will also be learning more about employability and job-hunting this week which sounds interesting.
- We began the day with some Code Wars in our project group but we mostly just chatted about last week.
- We did get a couple of **7 kyuu** kata done:
- [String ends with?](https://www.codewars.com/kata/51f2d1cafc9c0f745c00037d/train/javascript)
```js
function solution(str, ending){
  return str.endsWith(ending)
}
```
- [Alphabet war](https://www.codewars.com/kata/59377c53e66267c8f6000027/train/javascript)
```js
function alphabetWar(fight) {
  let array = fight.split("");
  let leftScore = 0;
  let rightScore = 0;
  for (let i = 0; i < array.length; i++) {
    switch(array[i]) {
      case "w":
        leftScore += 4;
        break;
      case "p":
        leftScore += 3;
        break;
      case "b":
        leftScore += 2;
        break;
      case "s":
        leftScore += 1;
        break;
      case "m":
        rightScore += 4;
        break;
      case "q":
        rightScore += 3;
        break;
      case "d":
        rightScore += 2;
        break;
      case "z":
        rightScore += 1;
        break;
      default:
        break;
    }
  }
  if (leftScore > rightScore) {
      return "Left side wins!";
    }
    if (leftScore < rightScore) {
      return "Right side wins!";
    }
    else {
      return "Let's fight again!";
    }
}
```
- We solved this kata initially with eight if statements but then refactored the solution into one switch statement.
- Someone submitted a clever solution that was much more concise:
```js
function alphabetWar(fight) {
    let map = { w: -4, p: -3, b: -2, s: -1, m: 4, q: 3, d: 2, z: 1 };
    let result = fight.split('').reduce((a, b) => a + (map[b] || 0), 0);
    return result ? (result < 0 ? "Left" : "Right") + " side wins!" : "Let's fight again!";
}
```
- We then had a lecture on how to hold a retro at the end of a project, before being sent back to our breakout rooms to perform said retro focusing on 5 key points:
	- What to do more of.
	- What to do less of.
	- What do start doing.
	- What to stop doing.
	- What to keep doing.
- I found this a useful exercise and, since we all did this individually at the start, we were able to see some common themes come up, such as everyone saying we need to revise CSS!
- We then all performed a personal "Learning Audit" in which we graded everything we had covered thus far on a scale from 1 to 5.
- The rest of the afternoon was given over to us to make a study plan and begin tackling the topics that we felt most needed our attention.
	- For me that was CSS Grid today.
- We also got some written feedback for our presentation from the judges which was very positive, and made for a gratifying end to the day.

Today certainly was not what I was expecting but I appreciate having the opportunity to consolidate what we have learned, as it really does seem like a lot when you look at all the topics listed on one page!


## Day 45
*20230503*

Today we had an introductory lecture on the post-course employability sessions and spent the afternoon doing self-directed learning.

- We did some Code Wars in our new group in the morning:
- [Persistent Bugger.](https://www.codewars.com/kata/55bf01e5a717a0d57e0000ec/train/javascript)
```js
function persistence(num) {
  let count = 0;
  let array = num.toString().split("").map(Number);
  let product;
  console.log(array)
  
  if (num >= 10) {
    product = array.reduce(function(a,b) {
      return a * b;    
    }, 1)
    count++;
    console.log(`product is ${product}`);
    console.log(`count is ${count}`);
    } 
  
  while (product >= 10) {
    array = product.toString().split("").map(Number);
    product = array.reduce(function(a,b) {
      return a * b;    
    }, 1)
    count++;
    console.log(`product is ${product}`);
    console.log(`count is ${count}`);
  }
  return count;
}
```
- We solved this **6 kyuu** kata once we realised that a while loop would be all we needed to abstract away the infinite if statements that check if the product of the latest multiplication was at least 10.
- Unfortunately, we still needed one if statement at the start so there is some duplication in our solution that could be improved.
-  Someone submitted a clever solution:
```js
function persistence(num) {
   var times = 0;
   
   num = num.toString();
   
   while (num.length > 1) {
     times++;
     num = num.split('').map(Number).reduce((a, b) => a * b).toString();
   }
   
   return times;
}
```
- Next came a lecture on employability that was really encouraging and showcased the ways in which SoC continues to support its graduates long after the course has ended.
- During the afternoon's self-directed learning I took the chance to read some more of *The Object-Oriented Thought Process* and then span up a quick React project to make a to-do list just to see if I could remember how to do it on my own.
	- I am still in the process of making this so I will return to it tomorrow in the afternoon (assuming we have another self-directed learning session).

I really enjoyed today's employability lecture and it has filled me with confidence that the SoC team will do everything they can to help all us bootcampers to launch our careers in tech.


## Day 46
*20230504*

Today we spent the morning learning all about networking and how to write a good CV for a tech role. In the afternoon we had more self-directed learning time.

- We began the day with some Code Wars:
- [Beginner - Lost Without a Map](https://www.codewars.com/kata/57f781872e3d8ca2a000007e/train/javascript)
```js
function maps(x){
  return x.map(int => int * 2)
}
```
- We started off nice and easy with the above basic **8 kyuu** kata using the `.map()` method.
- [Max sum between two negatives](https://www.codewars.com/kata/6066ae080168ff0032c4107a/train/javascript)
```js
function maxSumBetweenTwoNegatives(a) {
  let negativeIndices = [];
  let summedValues = [];
  let sum = 0;
  for (let i = 0; i < a.length; i++) {
    if (a[i] < 0) {
      negativeIndices.push(i);
    }
  }  
  if (negativeIndices.length < 2) {
    return -1;
  }
  for (let i = 0; i < negativeIndices.length - 1; i++) {
    sum = 0;
    for (let j = negativeIndices[i] + 1; j < negativeIndices[i + 1]; j++) {
      sum += a[j];
    }
    summedValues.push(sum);
  }
  return Math.max(...summedValues);
}
```
- This **7 kyuu** kata was much more of a challenge, the nested for loop especially.
- Someone solved it in a much shorter way:
```js
function maxSumBetweenTwoNegatives(a) {
  let i=0,c=0,m=-1;
  while(i<a.length&&a[i]>=0) i++;
  while(++i<a.length){
    if(a[i]<0){ m=m<c?c:m; c=0; }
    else c+=a[i];
  }
  return m;
}
```
- We had a lecture on how to write a good CV for a tech role and we spent some time drafting one up.
	- We have until the 19th of May to come up with a first draft of a CV to hand in to the coaches, which should be more than enough time to update my current iteration.
- We then had a second lecture that focused on networking and attending meetups in particular as a great way to meet new developers and potentially hear about job listings before they go live.
- The coaches also fed back some really useful tips based off of their interactions with employer partners and what they look for in a junior developer:
	- Keep coding on a regular basis after the bootcamp.
	- Update your GitHub accordingly, and even contribute to open-source projects.
	- Prepare for interviews by researching the company.
- We spent the afternoon doing more self-directed learning.
- I took the time to finish my to-do list React app that I started yesterday.
- I certainly was not able to do it all from memory but I was happy with what I could do by heart, and with some help from ChatGPT (especially on the CSS!) I managed to make myself a useful little app.
- I then created a public GitHub repo called [to-do-list-with-react](https://github.com/gregoraubrey/to-do-list-with-react) and pushed my local repo up, preserving my commit history.

It felt great to make a clean, functional app on my own and the employability lectures this morning were very insightful, so today was probably the best day of the week so far!


## Day 47
*20230505*

Today we had a hackathon that involved building a fake e-commerce website using the [Fake Store API](https://fakestoreapi.com/).

- One of our team members was at a funeral today so there were only two of us to work on the project.
- We started things off by making a `.drawio` file and building a component tree:
	- App
		- NavBar
		- ProductList
			- ProductItem
		- ShoppingCart
			- CartItem
		- Footer
- We did not get around to implementing the CartItem component since we did not have time to work on a feature that shows what is currently in your cart.
	- We did, however, manage to implement all the other componenents, even though we got a bit carried away when writing the ProductList component and had to cut and paste some of that code into ProductItem:
```js
import React, { useState, useEffect } from "react";
import fetchProductsFromAPI from "../API/index.js";
import "./index.css";
import ProductItem from "../ProductItem";

function ProductList({ selectedCategory, handleClick }) {
  const [products, setProducts] = useState([]);

  useEffect(() => {
    async function fetchThenSetProducts() {
      const fetchedData = await fetchProductsFromAPI();
      setProducts(fetchedData);
    }
    fetchThenSetProducts();
  }, []);

  return (
    <div>
      <h1>Product List</h1>
      <ul className="product-list">
        {products
          .filter((x) => !selectedCategory || x.category === selectedCategory)
          .map((item) => {
            return <ProductItem item={item} handleClick={handleClick} />;
          })}
      </ul>
    </div>
  );
}

export default ProductList;
```
- The logic below was originally written into ProductList before we refactored:
```js
import React from "react";
import "./index.css";

function ProductItem({ item, handleClick }) {
  return (
    <li key={item.id} className="product-item">
      <h3>{item.title}</h3>
      <p>{item.description}</p>
      <img src={item.image} alt={item.title} className="item-image"></img>
      <p>£{item.price}</p>
      <button className="cart-button" onClick={() => handleClick(item)}>
        Add to cart
      </button>
    </li>
  );
}

export default ProductItem;
```
- The feature I was happiest to get working was one that tracked and displayed the live total of a user's cart price by reading the `price` property of each object in the `cartCount` array:
```js
const [cartCount, setCartCount] = useState([]);
```
- Here is the function that handles a user clicking on the "Add to cart" button:
```js
function handleClick(item) {
    console.log(
      "handleClick has been called. See the current cartCount array below:"
    );
    console.log(cartCount);
    setCartCount([...cartCount, item]);
  }
```
- Here is the ShoppingCart component that tracks the number of items in the cart, and the total price:
```js
import React from "react";
import { faShoppingCart } from "@fortawesome/free-solid-svg-icons";
import { FontAwesomeIcon } from "@fortawesome/react-fontawesome";
import "./index.css";

function ShoppingCart({ cartCount }) {
  const totalPrice = cartCount
    .reduce((accum, item) => {
      return accum + item.price;
    }, 0)
    .toFixed(2);

  return (
    <div className="cart-icon-container">
      <div className="cart-icon-wrapper">
        <FontAwesomeIcon icon={faShoppingCart} />
        <p className="cart-count">({cartCount.length})</p>
      </div>
      <p className="total-price">£{totalPrice}</p>
    </div>
  );
}
export default ShoppingCart;
```
- The presentation went really well and we got some lovely compliments in the Zoom chat!
- I had a mentor meeting in which we talked a bit about *The Object-Oriented Thought Process*, networking, and keeping your skills sharp in a language/framework that you are not currently using each day at work.

Today was hectic considering we got a React app up and running with just two people but it was certainly a fun experience. Next week we move onto the backend and I can't wait!


## Day 48
*20230506*

Today I took things easy by just going over the codebase for yesterday's hackathon to make sure I did not forget any of the logic, and then reading some articles and making some brief edits to my CV.

- I found it really worthwhile looking over the codebase from Friday, and I think I will come back to it again next week just to keep things fresh, especially since we will be working on the back-end and no longer React.
- I then read a couple of articles on React and how to build a mental model of the library:
	- [A visual guide to React mental models](https://obedparla.com/code/a-visual-guide-to-react-mental-models/)
	- [A visual guide to React mental models - part 2](https://obedparla.com/code/a-visual-guide-to-react-mental-models-part-2-use-state-use-effect-and-lifecycles/)
- The first article focused on the basics of React whilst the second handled `useState` and `useEffect` which I found particularly beneficial as my understanding of state is still a bit fuzzy if I am being honest.
- I ended the day by making a couple of edits to my CV, which mainly involved trimming down unnecessary sections such as irrelevant work experience.
	- I will spend more time on this tomorrow to get it presentable since my mentor has generously offered to look over my CV for me.

Today was nice and quiet and I assume tomorrow will be similar since I plan to focus primarily on editing my CV. I hope to read some more of *The Object-Oriented Thought Process* also.


## Day 49
*20230507*

Today I spent some time working on my CV (which took longer than I thought), read some more, and went back over the code from the hackathon again along with the code from the week-long project.

- I spent some time working on an introductory paragraph to my CV which I found harder than expected.
	- I will have to finalise it tomorrow so that I can send it on to my mentor.
- After progress ground to a halt on the CV, I decided to move onto some reading.
	- I am deliberately trying to go slowly as I read *The Oject-Oriented Thought Process* as most of these ideas are completely new to me.
- In the evening I spent some more time going over the codebase for Friday's hackathon.
- I reminded myself of the `reduce()` method that I used to display a live total of the cart price:
```js
import React from "react";
import { faShoppingCart } from "@fortawesome/free-solid-svg-icons";
import { FontAwesomeIcon } from "@fortawesome/react-fontawesome";
import "./index.css";

function ShoppingCart({ cartCount }) {
  const totalPrice = cartCount
    .reduce((accum, item) => {
      return accum + item.price;
    }, 0)
    .toFixed(2);

  return (
    <div className="cart-icon-container">
      <div className="cart-icon-wrapper">
        <FontAwesomeIcon icon={faShoppingCart} />
        <p className="cart-count">({cartCount.length})</p>
      </div>
      <p className="total-price">£{totalPrice}</p>
    </div>
  );
}
export default ShoppingCart;
```
- I also briefly went over the codebase for the week-long project in order to not forget any of our work from two weeks ago.

Today was another relaxed day, apart from the frustration of struggling to finish a draft of my CV. I am sure that I will be able to get it done tomorrow when I come back with a fresh perspective.


## Day 50
*20230508*

Today I got a first draft of my CV done and read up a little on Node.js in preparation for starting on the back-end tomorrow.

- I spent some time in the morning working on my CV and was finally able to come up with an introductory paragraph that I am happy with.
- I will send this on to my mentor tomorrow after proofreading it one last time.
- In the afternoon I spent some time reading some articles and watching some videos on Node.js:
	- [W3Schools Introduction to Node.js](https://www.w3schools.com/nodejs/nodejs_intro.asp)
	- [What is Node js? | Simplified Explanation](https://www.youtube.com/watch?v=yEHCfRWz-EI)
	- [Node.js Ultimate Beginner’s Guide in 7 Easy Steps](https://www.youtube.com/watch?v=ENrzD9HAZK4&t=5s)
- I feel prepared for tomorrow and keen to get going with writing some code!

It felt great to finally get my CV into a state that I am happy with, and reading up on Node.js has definitely got me excited for the week ahead!


## Day 51
*20230509*

Today we made a start on Node.js and used the UUID package to create objects with a unique identifier.

- We started the day by giving feedback to our group from last week.
- None of us had a lot to say considering we really only spent one day writing code together, and one of our team members was away that day.
- Next we met up with our new pair programming partners for the week.
	- My partners this week seem really nice, and we worked well together today which is a good sign.
- The first thing we did together was some Code Wars:
- [Target Date](https://www.codewars.com/kata/569218bc919ccba77000000b/train/javascript)
```js
function dateNbDays(a0, a, p) {  
  let initialDate = new Date(2016, 0, 1);  
  let finalDate;  
  let days = 0;  
  let currentAmount = a0;
  while (currentAmount < a) {  
    currentAmount = currentAmount + currentAmount * (p / 36000);  
    days = days + 1;  
  }
  finalDate = new Date(initialDate.getTime() + days * 24 * 60 * 60 * 1000);  
  let year = finalDate.getFullYear();  
  let month = ("0" + (finalDate.getMonth() + 1)).slice(-2);  
  let day = ("0" + finalDate.getDate()).slice(-2);
  let formattedDate = `${year}-${month}-${day}`;  
  return formattedDate;  
}
```
- This was only a **7 kyuu** kata but it took us a long time to solve.
- It was worth it, however, as we learned about various date methods in JS.
- Next up was a lecture on Node.js where we learned about various terms such as...
	- I/O
	- Runtime environment
	- Event-driven programming
	- Blocking and non-blocking
	- JavaScript engine
- We moved onto a mini workshop in which we used ` import fs from "node:fs/promises";` to write JSON data to a file and then read it in another file.
- In the afternoon we tackled a workshop that involved writing various functions and using the [NPM UUID package](https://www.npmjs.com/package/uuid)
- We had to write various functions that handled operations such as deleting an object if its UUID matches the argument passed into the function, adding a new object to the array, and changing the text property of a specific object.
- For the final function, our code was not passing the test that was provided but we had no idea why.
- One of the coaches joined our room and said that our code looked fine, and when she ran it on her computer it passed the test, which was certainly strange.

Today was great fun, and a much more gentle introduction than what I was expecting. If it stays this easy then the back-end will be a doddle, but I am sure that things will only ramp up from here!


## Day 52
*20230510*

Today we learned about some web fundamentals and built our first REST API in the afternoon!

- We started the day off with some Code Wars:
- [Help the bookseller !](https://www.codewars.com/kata/54dc6f5a224c26032800005c)
```js
function stockList(listOfArt, listOfCat){
  // For loop to find the codes start with ListOfCat
  // 
  let matches = [];
  let letter;
  for (let i = 0; i < listOfCat.length; i++)
    {
      letter = listOfCat[i]
      for (let j = 0; j < listOfArt.length; j++) 
      {
        if (listOfArt[j].startsWith(letter)) 
          {
            matches.push(listOfArt[j])
          } 
        else { 
          // push starting letter to matches along with number 0
          matches.push(`(${letter} : 0)`)
        } 
      }
    } console.log(matches);
}
```
- This was all we managed on this **6 kyuu** kata.
- We have made some good progress so I am sure we will be able to get it finished during tomorrow's Code Wars session.
- Next we had an excellent guest lecture by a back-end engineer who was a part of cohort 4 of the bootcamp.
	- I particularly enjoyed her advice around collaborating with seniors in order to learn as quickly as possible.
- After the guest lecture came a quiz on Node.js and File System on which I scored 100%!
	- I expect the quizzes will get harder from here since today is only our second day covering the back-end.
- Our next lecture covered web fundamentals:
	- IP addresses (IPv4 and IPv6)
	- Ports and Sockets
	- Domain Names and DNS
	- The Client-Server Model
	- HTTP and HTTPS
	- Popular HTTP Methods
	- HTTP Status Codes
- We then made a start on **Express.js** to send a simple GET request:
```js
import express from "express";

const app = express();

const port = 3000;

// req for request, res for response
app.get("/", (req, res) => {
  res.send("Hello World");
});

app.listen(port, () => {
  console.log(`Server is up and running on port: ${port}`);
});
```
- In the afternoon we stared using **Thunder Client** instead of the browser so that we could send POST requests as well.
- This all culminated in a workshop in which we used various HTTP methods (GET, POST, PATCH, DELETE) to update an array of objects that each contained a UUID (generated using [an NPM package](https://www.npmjs.com/package/uuid)) and a quotation as a string.
- As a group we managed to finish the whole workshop with time to spare which was a great feeling after a long day!

Today's lectures were definitely the most challenging thus far on the back-end but the fact that we were able to finish the workshop fills me with confidence for the rest of the week!


## Day 53
*20230511*

Today we had lectures on middleware in Express.js and an introduction to RESTful APIs, before attempting to build our own API in the afternoon.

- We started the day off with some Code Wars:
- [Help the bookseller !](https://www.codewars.com/kata/54dc6f5a224c26032800005c)
```js
function stockList(listOfArt, listOfCat) {
  let books = [];
  let letter;
  let sum;
  let quantity;
  let totalSum = 0;
  for (let i = 0; i < listOfCat.length; i++) {
    letter = listOfCat[i];
    sum = 0;
    for (let j = 0; j < listOfArt.length; j++) {
      if (listOfArt[j].startsWith(letter) === true) {
        quantity = parseInt(listOfArt[j].split(" ")[1]);
        sum += quantity;
      }
      totalSum += sum
    }
    books.push(`(${letter} : ${sum})`);
  }
  if (totalSum === 0) {
    return ""
  }
  return books.join(" - ");
}
```
- We got this **6 kyuu** from yesterday working!
- Somebody used a clever if statement to return `""` when there are zero books:
```js
function stockList(listOfArt, listOfCat) {
  if (!listOfArt.length || !listOfCat.length) return ''
  return listOfCat.map(w => {
    const s = listOfArt.reduce((a, b) => a + (b.charAt(0) === w ? +b.split(' ')[1] : 0), 0)
    return `(${w} : ${s})`
  }).join(' - ')
}
```
- [Salesman's Travel](https://www.codewars.com/kata/56af1a20509ce5b9b000001e/train/javascript)
```js
function travel(r, zipcode) {
  if (!r.includes(zipcode)) {
      return `${zipcode}:/`
      }
  const array = r.split(",");
  let copy = [...array];
  console.log(array);
  for (let i = 0; i < array.length; i++) {
    if (!array[i].includes(zipcode)) {
      //filter this index out
      copy.filter(()=> )
    }
  }
}
```
- The above is our progress thus far on a **6 kyuu** kata that we had a look at after finishing the one we began yesterday.
- We had a morning quiz on Express.js and web fundamentals on which I scored 100% again which felt great, although once again the questions were not particularly challenging.
- Next up was a lecture introducting middleware as software that exists between two layers.
- We had a go at writing some custom middleware functions:
```js
app.use((req, res, next) => {
  console.log("Hello from the middleware 👋");
  console.log(`[${new Date().toISOString()}] ${req.method} to ${req.path}`);
next();
});
```
- After playing around with custom middleware functions we had a guest lecture about RESTful APIs and what this entails, such as the server being client-state agnostic and using nouns instead of verbs in the path.
- We then had a lecture on third-party middleware libraries and how to use them.
	- We learned about [morgan](https://www.npmjs.com/package/morgan) and how it can be useful for logging various bits of metadata in the console when a client sends a request, such as the path, the date and time, and the HTTP status code.
- Our afternoon task involved first implementing a custom middleware function before adding a third-party middleware function and then serving a static image file from the `public` folder.

Learning about middleware was confusing at first and I am not sure that I totally grasp the concept, but the implementation in the afternoon task went much smoother than I expected and we finished with time to spare which always feels good. Tomorrow we have the hackathon and I can only assume we will be building a RESTful API from scratch which should be a fun challenge!


## Day 54
*20230512*

Today we had a hackathon in which we built a RESTful API from scratch and hooked it up to a pre-built front-end.

- We started the day off with a quiz where I got one question wrong because I put down morgan as built-in middleware when it is actually third-party (the answer was `express.json()`).
- After that we moved straight onto the hackathon for the day, which concerned recipe objects with properties of "title", "image", "instructions", and 
ingredients".
- We began by writing up all our CRUD funcionality with functions that read from the `recipes.json` file, parsed the data, performed the relevant action on the data, then wrote to file after stringifying the updated recipe array.
- Below is one example that we used for PATCH requests:
```js
// UPDATE A RECIPE BY ID
export async function updateRecipeByID(id, updatedRecipe) {
    try {
        const data = await fs.readFile(fileName);
        const recipes = JSON.parse(data);
        const index = recipes.findIndex((r) => r.id === id);
        if (index === -1) {
            throw new Error("We couldn't find a recipe by this ID!");
        }
        recipes[index] = { id, ...updatedRecipe };
        await fs.writeFile(fileName, JSON.stringify(recipes));
        return recipes[index];
    } catch (error) {
        console.log(error);
        throw error;
    }
}
```
- We then wrote up the functions that send the requests to the server.
- Below is the example for a PATCH request:
```js
app.patch("/api/recipes/:id", async (req, res) => {
  try {
    const recipe = await updateRecipeByID(req.params.id, req.body);
    res.status(200).send({
      success: true,
      payload: recipe,
    });
  }
  catch (error) {
    console.error(error);
    if (error.message === "We couldn't find a recipe by this ID!") {
      return res.status(404).send({
        success: false,
        payload: [],
        message: error.message,
      });
    }
    res.status(400).send({
      success: false,
      payload: [],
    });
  }
});
```
- After we finished coding up the bare-bones of the API, we spend a couple of hours trying to make our API as RESTful as possible by adding expressive error messages and by using the most appropriate HTTP status codes, such as `201` for "created" when a POST request was successful.
- After making the API as RESTful as we could, we hooked it up to the pre-built front-end and had it working in our browsers which was a great feeling, as it is the first time we have ever linked the back-end and the front-end!
- We had some time to spare at the end of the day so we coded up a delete button to go on each recipe card that would send a DELETE request to the server with the relevant ID.
- Below is a snippet of the code from the `createRecipeView()` function that I wrote up to add the delete button and have it functional:
```js
  const deleteButton = document.createElement("button");
  deleteButton.innerText = "Delete Recipe";
  deleteButton.addEventListener("click", async ()=> {
    try {
      const response = await fetch(`${url}/api/recipes/${id}`, {
        method: "DELETE",
      });
      if (response.ok) {
        article.remove();
      } else {
        console.error(`Error: ${response.statusText}`);
      }
    } catch (error) {
      console.error(`Fetch error: ${error}`);
    }
```
- We spent 20 minutes or so at the end of the day preparing our presentation which was well worth it because our presentation went really well and we got some nice compliments in the chat about our documentation of the day's work (since we had been taking screenshots of our progress throughout).
- I ended the day with another excellent mentor meeting in which we talked about various topics to do with the back-end such as REST versus other types of APIs, the differences between different languages in the back-end, how to structure your API to be useful for front-end colleagues, and why people do not always follow the guidelines around what the HTTP methods should be used for and how that can cause issues down the line.

This week has flown by but I have enjoyed every minute of it. Next week we are moving onto SQL and, much like this time last week, I have no idea what to expect but I am keen to dive in!


## Day 55
*20230513*

Today I (finally!) had my graduation ceremony so I spent very little time coding.

- I spent about half an hour in the morning going over the notes I had written during the lectures this week.
- I definitely need to take a closer look at the HTTP status codes and what they mean.
	- Despite using a lot of them yesterday, I could not remember what they stood for apart from the basic ones like `200` and `404`.
	- I made some Anki cards to help me remember what the most common HTTP status codes mean.
- After the ceremony I spent a little bit of time reading some more of *The Object-Oriented Thought Process* and that was it for the day.

Today was not about coding but rather celebrating all my hard work for the last 4 years at university and during my year abroad. It was so nice to see some of my friends whom I have not seen in almost a full year! Tomorrow I will get back on track and do the recap tasks we have been set for the start of next week.


## Day 56
*20230514*

Today I completed the recap task and read some articles that I had saved over the last week or so.

- The recap task involved coding up a back-end similar to the one we made during the hackathon.
- My API had to be RESTful, and support all the CRUD routes.
- I found it very smooth sailing which was encouraging, and I made a git commit after each function was up and running in order to have a verbose commit history and keep track of my work.
- There are some bonus tasks such as adding relevant HTTP status codes and building a front-end that I would like to work on next week if I can find the time.
- During one of the lectures this week, somebody asked a question about why we could manipulate the contents of an array despite its being declared with `const`.
- This prompted me to read an article called [The "const" Deception](https://www.joshwcomeau.com/javascript/the-const-deception/) to better understand what this keyword means.
- I read another article that I had saved a while ago titled [The Interactive Guide to Rendering in React](https://ui.dev/why-react-renders).
	- I feel it is important to keep coming back to React whilst we focus on the back-end because I would hate to waste time at the start of the final project having to relearn a bunch of React concepts that I understood when we were first studying them.
- The last article I read was titled [Git Merge – The Definitive Guide](https://www.freecodecamp.org/news/the-definitive-guide-to-git-merge/).
	- Since git is something that I will be using day-in day-out as a developer, I think it is worth getting good at now.
	- Whether I am working on the front-end, the back-end, or both, git is going to be an indispensable part of my workflow.

Today was great fun as I completed the recap task in much less time than I was expecting. It shows just how much of the week's content I have already managed to grasp and gives me confidence going into next week.


## Day 57
*20230515*

Today I was not online as I attended my Gold Duke of Edinburgh's Award Scheme Presentation (having completed it in 2018!). This meant that I had some catching up to do in the evening.

- Before I left home in the morning I messaged my new pair programming partners for the week to ask if they could let me know what they cover during the day and tell me what I should be getting on with in the evening.
- At 17:00 they let me know that I should work through some [SQLBolt](https://sqlbolt.com/lesson/) lessons to learn the basics of SQL.
- It seems that we were pretty much left to our own devices today to learn SQL which is lucky for me since I did not miss a lecture-heavy day.
- I spent some time in the evening going through a few of the SQLBolt lessons and plan to continue tomorrow morning.

Today was great fun, meeting up with some people I have not seen in years at the DofE event. In terms of SQL, it seems simple enough so far but I am sure that it will only get harder from here.


## Day 58
*20230516*

Today we learned some more about SQL and tested out our knowledge by practising some queries.

- We started the day with a Code Wars session during which I actually spent the whole time going through more [SQLBolt](https://sqlbolt.com/lesson/) in order to catch up what I missed yesterday.
	- My pair programming partner was really helpful and gave me hints when I got stuck on some of the exercises at the end of each lesson.
- Next we had a guest lecture by [Stuart Langridge](https://www.kryogenix.org/) that was really eye-opening, and felt very different from most of the other guest lectures we have had so far on the course.
	- Stuart focused on knowing your worth (avoiding unpaid internships, unpaid overtime, etc.)
	- He talked about the importance of paying it forwards and building a good reputation instead of withholding information from your colleagues for short-term gain.
	- I asked a question about automated testing and he linked testing to doing maintenance on a car.
		- Unlike for cars, with software there is no yearly MOT so if the code is not thoroughly tested, it will start to rot.
- We then had a quiz on SQL in which I scored 100% despite having to take a guess at one or two of the answers.
- Next up was a lecture on Entity Relationship Diagrams (ERD).
- In the afternoon we worked through a set of [SQL Joins & Subqueries](https://pgexercises.com/questions/joins/) questions.
- After solving a few of these problems (and taking a long time to wrap our heads around self-joining!) we spent a short while using [Lucid Chart](https://www.lucidchart.com/pages/) to build our own ERD.

Today was fairly well-paced as we spent a lot of the time directing our own learning which was a refreshing change of pace. I really appreciated Stuart's talk and took away some true nuggets of wisdom.


## Day 59
*20230517*

We looked at PostgreSQL today and the `dotenv` NPM package, which allowed us to keep our database URL in a secure `.env` file.

- We started the day with some Code Wars.
- [Reverse Vowels In A String](https://www.codewars.com/kata/585db3e8eec141ce9a00008f/train/javascript)
```js
function reverseVowels(str) {
  const vowelArray = [];
  const indexArray = [];
  const strArray = str.split("");
  let counter = 0;
  for (let i = 0; i < strArray.length; i++) {
    if (/^[aeiou]$/i.test(strArray[i])) {
      vowelArray.push(strArray[i]);
      indexArray.push(i);
      strArray.splice(i, 1, " ");
      }
  }
  vowelArray.reverse();
  for (let i = 0; i < strArray.length; i++) {
    if (i === indexArray[counter]) {
      strArray.splice(i, 1, vowelArray[counter])
      counter++;
    }
  }
  return strArray.join("");
}
```
- We completed this **6 kyuu** kata this morning.
- I ranked up to **5 kyuu** after submitting the solution which was a nice surprise!
- Someone solved it in a much simpler way:
```js
const reverseVowels = str => {
  let vowels = str.replace(/[^aeiou]/gi, '').split('');
  return str.replace(/[aeiou]/gi, _ => vowels.pop());
};
```
- We then had a morning quiz on "Advanced SQL".
	- I scored 100% once more but this quiz was much harder than some of the previous ones and a couple of the questions gave me pause.
- Next up was a lecture on [ElephantSQL](https://www.elephantsql.com/), a cloud-based DBAS (database as a service) company.
	- By using ElephantSQL we do not have to manage the database and we do not have to host it on our local machine.
- We spent half an hour or so tinkering with ElephantSQL queries, creating a `books` and an `authors` table and selecting various rows from them.
- The only query that gave us issues was one that required the use of `GROUP BY` and `HAVING` since we had not seen these keywords before:
```SQL
-- Find all authors who have written more than one book.
SELECT authors.first_name, authors.last_name 
FROM authors 
JOIN books ON books.author_id = authors.id 
GROUP BY authors.id 
HAVING COUNT(books.id) > 1;
```
- After acquainting ourselves with ElephantSQL, we had a lecture on the [dotenv NPM package](https://www.npmjs.com/package/dotenv) which allows us to "load environment variables from a `.env` file into `process.env`" to use the documentation's own words.
- We combined this with [node-postgres](https://node-postgres.com/) in order to write an `app.js` file that could query our ElephantSQL database:
```js
///// app.js /////

// import the pg package
import pg from "pg";

// set the database connection string
const connectionString = process.env.DB_CONNECTION_STRING;

// create a new client to use
const client = new pg.Client({
  connectionString, // this is shorthand for `connectionString: connectionString`
});

// connect to the database
await client.connect();

// send a query
const result = await client.query("SELECT * FROM books;");
console.log(result.rows);

// close the connection
await client.end();
```
- We ended the day by adding another JS file that served as a database reset script.
	- It contained a function that dropped the two tables, then created them again and inserted the starting data into them.
- I had some time to spare at the end so I also made a JS file that inserted an extra book each time it was executed.

We learned a lot today and I am not sure that I am going to retain it all at the first time of asking. I hope we get to keep putting this into practice tomorrow before Friday's hackathon. On another note, I am going to be attending a React meetup tomorrow in Shoreditch with some fellow bootcampers which should be a fun way to spend the evening!


## Day 60
*20230518*

Today we learned about parameterised queries and the MVC design pattern.

- We started the day with a quiz on "Connecting Node to Postgres".
	- I got 100% again which was satisfying, although the quiz was not particularly hard today.
	- One of the things I learned through doing the quiz is that there are two times when you should use a pool over a client:
		- When you need to perform a large number of database queries.
		- When you need to handle many simultaneous connections.
- Next up was a lecture on parameterised queries.
- We learned about SQL injection attacks and how using placeholders (parameters) can help prevent these from happening.
- Here is a simple example that we saw during the lecture:
```js
// Import the pg package
import pg from "pg";

// Set the database connection string
const connectionString = process.env.DB_CONNECTION_STRING;

// Create a new client to use
const client = new pg.Client({
  connectionString,
});

// Connect to the database
await client.connect();

// Send a query
const id = 1;
const values = [id];
const query = `SELECT * FROM BOOKS WHERE id = $1;`;
const result = await client.query(query, values);
console.log(result.rows);

// Close the connection
await client.end();
```
- After learning about parameterised queries we had a guest lecture from [Dileep Marway](https://uk.linkedin.com/in/dileepmarway).
	- He talked about QA which was completely new to me outside of the brief mention that it gets in *Clean Code* (or was it *The Clean Coder*?) in which Robert Martin laments the dynamic that can grow between engineers and QA when QA gets bonuses for finding bugs.
	- I asked a question about the risks of QA being pushed out of a job due to engineers being encouraged to write their own automated tests.
	- Dileep gave a good response in which he highlighed the unique skills of a QA to spot potential issues in the future.
		- He gave one example of a QA who managed to keep the company's website up during Black Friday by considering a potential issue months in advance.
- After lunch, we were introduced to MVC before working on a workshop in which all of the code was separated out into different files.
- It took a while for us to get our heads around all the files in the repo, but eventually things started to make sense and we got the workshop finished by connecting the library to our ElephantSQL database.
- In the evening I attended the [React Advanced Meetup](https://www.meetup.com/React-Advanced/) with ten or so fellow bootcampers.
	- It was a pleasure to meet everyone in person and mingle, although to be honest we did hardly any networking!
	- The talks were interesting, if a little over my head.
	- One speaker talked about [tree-sitter](https://github.com/tree-sitter/tree-sitter), which I have heard of in the context of adding syntax highlighting to Neovim, but other than that, I did not really understand most of what was said.
	- Nonetheless I had a great time and am keen to attend another meetup soon!

Today was a lot of fun, especially the meetup in Shoreditch in the evening. I have been told that there is no hackathon tomorrow so I wonder what we will be doing instead?


## Day 61
*20230519*

Today had a very different feel to most Fridays on the course. Instead of a hackathon, we had two representatives from [Couchbase](https://www.couchbase.com/) come and spend the day giving us an introduction to the platform.

- In my group, we started off the day by comparing our CVs, since we were supposed to submit them to the employability team by the end of the day.
- Next we were straight into the tasks that we would spend the whole day on:
	- learning about NoSQL and how it compares to SQL.
	- Learning about Couchbase.
	- Downloading and configuring Couchbase.
	- Connecting to the database with the Node.js SDK.
	- Accessing data.
- It all felt a bit chaotic, with a lot of new terms like "bucket" and "cluster" getting foisted upon us before we were hurried on to a new topic.
- Eventually, I did manage to get everything set up and was able to send successful GET, POST, PUT, and DELETE requests, although I am not sure that I could recreate the code on my own a second time!
- I had a very productive meeting with my mentor after 17:00.
	- We talked about the good bits and bad bits of my CV.
		- I later made some of the changes that we talked about before submitting it to the employability team in the evening.
	- We talked about the meetup I attended yesterday and I told him about some of the talks from that evening:
		- We discussed monolithic versus microservices architecture in particular, and the pros and cons of each.
	- We also discussed QA and the role it plays in the software development process.
	- Lastly, we talked about salaries, how to make sure that you are being paid your worth, and why (especially as a junior) you should aim to find a company that will help you learn and progress rather than just one that will pay you a high salary.

Today was a bit underwhelming considering how we were just thrown into the deep-end with Couchbase without really understanding why we were learning it and what its use case was. With that said, today's meeting with my mentor was extremely productive and lasted well over an hour, which I am very grateful for.


## Day 62
*20230520*

I did not do much coding today, instead opting to have a restful day after a long week.

- I spent some time in the morning reading a freeCodeCamp article titled [How to Write Clean Code – Tips and Best Practices (Full Handbook)](https://www.freecodecamp.org/news/how-to-write-clean-code/).
	- This served as a good refresher of some of the concepts that I had read about in *Clean Code*.
	- I think it would be worth coming back to this article every few months just to check in and make sure that I am following clean code principles.
- I had a brief look at the recap tasks that we were set on Friday evening and feel confident that I can get them done tomorrow.
- The last thing I did today was to read through the code I wrote in all of the tasks/workshops this week.
	- After reading through my code, I feel confident in my knowledge of the basics of SQL, but a lot of what we covered on Friday is still quite hazy.

I really enjoyed having a laid-back day today and making the most of the sunshine during the day. Tomorrow I will tackle the recap tasks we have been set for Monday.


## Day 63
*20230521*

Today I worked on the recap task ready for Monday.

- I started off by doing a simple **8 kyuu** Code Wars kata to get myself warmed up:
- [Calculate average](https://www.codewars.com/kata/57a2013acf1fa5bfc4000921/train/javascript)
```js
function findAverage(array) {
  if (array.length === 0) {
    return 0;
  }
  let sum = array.reduce((accum, b)=> {
    return accum + b;
  }, 0)
  return sum/array.length;
}
```
- I had to add the initial if statement after my original solution failed a test in which the argument was just `[]`.
	- My function at the time was returning `NaN` instead of `0`.
- When it came to the recap task, I did not have much work to do on my own branch since we had already made a start on adding appropriate HTTP status codes on Thursday.
- I added expressive error messages and `404` status codes for some of the functions that did not yet have them:
```js
export async function searchAuthorsByName(req, res, next) {
  if (req.query.search !== undefined) {
    const authors = await authorModel.searchAuthorsByName(req.query.search);
    if (authors.length === 0) {
      return res
        .status(404)
        .json({ success: false, payload: "No author found by that name." });
    }
    return res.status(200).json({ success: true, payload: authors });
  }
  next();
}
```
- In this case, if the length of the `authors` array is `0`, then that means that no author was found, so we return `404` and a helpful error message.
```js
export async function getBookById(req, res) {
  const book = await bookModel.getBookById(req.params.id);
  if (!book) {
    return res
      .status(404)
      .json({ success: false, payload: "No book found by that id." });
  }
  res.status(200).json({ success: true, payload: book });
}
```
- In this function, the if statement uses similar logic to return `404` if there is no book that corresponds to the ID that the user submitted.
- My goal with these changes was to tick off two of the RESTful API principles:
	- Use appropriate HTTP status codes.
	- Give expressive error messages.

Apparently next week we will be looking at TypeScript which should be exciting as, to my knowledge, it aims to make JS strongly-typed, which is something I have talked about with my mentor.


## Day 64
*20230522*

Today we had a guest lecture from Talis on their software development process, and we made a start on learning about authentication and authorisation.

- We began the day by giving feedback to our pair programming partners from last week.
- We all had pretty similar things to say to each other, and since we did not do a hackathon on Friday there was not that much feedback to really give.
- Next we had a guest lecture in which two Talis employees talked us step-by-step through their development process.
	- They stressed the importance of **pscyhological safety** in a team which is something that Joseph talked about in one of his mindset sessions a few weeks as being the number one factor for a great team (according to a Google study).
	- They also talked about their fully automated testing and the fact that they have no QAs.
		- This prompted me to ask a question that referred back to Dileep's talk last week on the benefits of QAs.
		- Nadeem responded with an interesting point on domain knowledge, saying that it is difficult for both the developers and the QAs to share the same domain knowledge, yet this is what is needed for them to be on the same wavelength and work harmoniously.
- In the afternoon we had a lecture on authenticationa and authorisation before we were sent down to our breakout rooms to do our own research.
- We started on a workshop that involved using [Supabase](https://supabase.com/).
	- We followed their [quickstart guide on React](https://supabase.com/docs/guides/getting-started/quickstarts/reactjs) to spin up a login page but did not have time to get any further along in the workshop (although apparently we will be continuing with it tomorrow).
- In the evening I did a few Code Wars kata on a whim, including:
- [Total amount of points](https://www.codewars.com/kata/5bb904724c47249b10000131/train/javascript)
```js
function points(games) {
  let score;
  let points = [];
  for (let i = 0; i < games.length; i++) {
    score = games[i].split(":");
    if (score[0] > score[1]) {
      points.push(3);
    }
    else if (score [0] < score[1]) {
      points.push(0);
    }
    else {
      points.push(1);
    }
  }
  return points.reduce((accum, b)=> accum + b, 0)
}
```
- Solving this one felt great because my first solution immediately passed all the tests.
	- Oftentimes when I am solving a kata I end up getting a bit of syntax wrong, even if my plan is solid, so it was a nice surprise to see that I used the `reduce()` method correctly at the first time of asking.
	- Admittedly, my function is a little overkill for the exact requirements (e.g. storing each result in an array and accounting for draws) but it is at least a little futureproofed if, say, you need access to the result of a particular match.

Today was good fun, even if it took a while to get to grips with Supabase. To be honest I feel like I am still not entirely there but I know we will be coming back to it tomorrow so I am not concerned.


## Day 65
*20230523*

Today we spent more time trying to get to grips with Supabase, and had an interesting guest lecture on DevOps.

- We started the day with some Code Wars:
- [Length and two values.](https://www.codewars.com/kata/62a611067274990047f431a8/train/javascript)
```js
function alternate(n, firstValue, secondValue){
  const array = [];
  for (let i = 0; i < n; i++) {
    if (i % 2 === 0) {
      array.push(firstValue);
    }
    else {
      array.push(secondValue);
    }
  }
  return array;
}
```
- We decided to just try and get a quick win under our belts so that we could jump straight into looking at Supabase once more, hence we picked this fairly rudimentary kata to solve.
- Having solved the kata and spent some time looking at the Supabase docs, we were brought back into the main room for a guest lecture on DevOps and quality engineering by Rik Marselis.
- A lot of the concepts were things we had heard about before in the lectures on the Agile methodology.
	- With that said, there was also a lot that was new to us, since we have not really talked about DevOps that much.
	- Rik recommended a few books on DevOps and SRE during his lecture which I might add to my reading list.
	- He said that the main issue he comes across is people not knowing how to do good testing, so once more that word comes up and plays a crucial role!
- We then spent some more time on our React app using Supabase.
	- We implemented a logout button that, when clicked, called a `handleLogout` function that simply executed `supabase.auth.signOut()`.
	- We learned a bit more about JWTs and then managed to add a new role called "admin" that had read *and* write permissions.
	- The next step would have been adding a form in the front-end that would allow a user to attempt to write data to our "leaderboard" table but we ran out of time.
	
Today was definitely still a bit confusing but I feel like I am slowly but surely getting to grips with Supabase. If we use it in our final project then I am sure I will have a chance to get to know its ins and outs!


## Day 66
*20230524*

Today we learned about TypeScript and had a really enjoyable guest lecture from [Dr. Murray Hoggett](https://www.murrayhoggett.com/).

- We started the day in standard Code Wars fare:
- [Sum of a sequence](https://www.codewars.com/kata/586f6741c66d18c22800010a/train/javascript)
```js
const sequenceSum = (begin, end, step) => {
  let total = 0;
  for (let i = begin; i <= end; i += step) {
    total += i;
    console.log(total);
  }
  return total
};
```
- I hit 300 "honour points" after completing this short **7 kyuu** kata, which apparently allows me to submit my own kata to the site now.
	- I may well submit the screaming kebab case kata I composed for one of the end-of-week recap tasks a while ago.
- Next up was a guest lecture from a former bootcamper (back when the bootcamps were still held in person!) called Murray Hoggett.
- His candour was much appreciated as he tackled a wide variety of topics such as salaries, how long to spend at a company, and the pros and cons of working for start-ups.
	- My favourite piece of advice was his recommendation that we plan out a daily schedule for learning new concepts, practicing our coding skills, and applying to jobs and stick to it as soon as the bootcamp ends.
	- The temptation would be to take a break and relax after 16 weeks of hard work but the real hard work starts after the course has finished during the hunt for our first job in tech.
- Following this guest lecture, we had a quiz on authentication and authorisation on which I scored 100% once more which was satisfying.
- Next, we moved onto a lecture that introduced TypeScript before we [had a go ourselves](https://www.typescriptlang.org/play) at writing some very basic TS:
```js
type Account = {
  amount: number;
  uniqueId: string;
  isValid: boolean;
  addressLines: string[];
};

let billy: Account = {
    amount: 300,
    uniqueId: "abcdefg",
    isValid: true,
    addressLines: ["123", "Green Avenue", "New York"]
}

function printAmountAndId(account: Account) {
  return `You have ${account.amount}, and your unique ID is ${account.uniqueId}`
}

console.log(printAmountAndId(billy))
```
- As I look at this code now, I feel like the `printAmountAndId` function should have what it returns declared as a string only: `function printAmountAndId(account: Account): string {...}`
- We spent the rest of the day working on a handful of mini projects using TS:
	- Converting an existing RPS game from JS to TS.
	- Writing a simple web app that sends a fetch request to the [Dad Joke API](https://icanhazdadjoke.com/api) when a button is clicked, and then prints the joke that the API returns within a `<p>` element on the page.
		- It felt a little bit alien to be using Vanilla JS syntax again such as ` getElementById()` after using React for what feels like an age.
		- Perhaps I need to spend some more time using Vanilla JS, since React does tend to be overkill anyway unless the website is very big and is glad of reusable components.
	- Writing a simple RESTful API that reads from a local `.json` file and writes to it.
		- We only had time to implement a GET request for the whole list of items in the `.json` file, and then a GET request that searches by ID.
- It felt great to be able to tackle exercises that would have taken a whole day mere weeks ago in about an hour each today, all whilst getting to grips with TS at the same time.

Today was a real energiser after the torpor of going through the Supabase docs. Tomorrow we will be using TS together with React which should be even more exciting!


## Day 67
*20230525*

Today we learned some more TypeScript and implemented it in a simple React app.

- We started the day with a guest lecture from a former bootcamper who offered various pieces of advice.
	- She said we should prepare for both kata-style interview questions and those in which they show you buggy code and ask you to find the errors.
	- She gave some sage advice for the final project, both in terms of planning and working together as a team.
- We then had a quiz on the TypeScript we learned yesterday on which I scored 100% because the questions were fairly simplistic, likely owing to the fact that we have not actually learned much TypeScript yet.
- After a lecture covering some more TypeScript and reinforcing what we learned yesterday, we moved on to an afternoon workshop in which we had to transform a React app todo list using JS files to one that used TS files and achieved the same functionality.
- We struggled at one point where the solution involved defining multiple types, but other than that things went quite smoothly, and our app worked in the browser when all was said and done.
- We attempted to work on a stretch goal of letting the user press the Enter key instead of clicking the 'Add' button but did not manage to get it working in time.
- In the evening I did a Code Wars kata:
- [Find Duplicates](https://www.codewars.com/kata/5558cc216a7a231ac9000022/train/javascript)
```js
function duplicates(arr) {
  const duplicates = [];
  arr.filter((item, index) => {
    if (arr.indexOf(item) !== index && duplicates.indexOf(item) === -1) {
      duplicates.push(item);
    }
  });
  return duplicates
}
```
- This was only a **7 kyuu** kata but it took me quite a while due to my lack of familiarity with the filter method.

Today was fairly smooth sailing since we were just building on the TS we learned yesterday. Taking a step back, since we will likely have a hackathon tomorrow, that means that today marks the final day of teaching on the course which is a sobering thought. With that said, we have long had all the skills we need to teach ourselves so I am not too concerned. I hope tomorrow's hackathon goes well!


## Day 68
*20230526*

We spent today doing a hackathon in which we had to make a weather app in React using TypeScript.
- We started off by initialising a TS React project with `npx create-react-app weather-checker --template typescript`.
- We then made a `.drawio` file and drew up a component tree diagram so that we were all on the same page and had a clear vision of what the final app would look like, along with the steps we needed to take to get it coded up.
- We all signed up to the free tier of the [Open Weather Map API](https://openweathermap.org/api) and each got a unique API key.
- Each of us made a `.env` file to store our personal key and we added `.env` to the `.gitignore` file so as not to accidentally publicise our key.
- After reading the docs and understanding the syntax for a fetch request using a city name, we managed to code up the bare-bones of an app that printed the weather data to the console as an object after parsing the JSON response from the API.
	- We reached this point just before 12:00 which felt great as it meant we had the whole afternoon to work on beautifying things and adding extra features.
- One feature that I added and was quite proud of was a way of sanitising the user's input into a form the API would understand:
```ts
function handleClick(): void {
    // Remove any extra spaces and make the city lowercase
    // "     neW      yORk     "
    // "new york"
    const cleanCity = city.trim().replace(/\s+/g, " ").toLowerCase();
    console.log(`The text being used in the fetch request is: ${cleanCity}`);
    if (cleanCity) {
      setSearched(false);
      fetchRequest(cleanCity)
        .then((data: Weather | null) => {
          setWeatherData(data);
          setSearched(true);
          setCity("");
        })
        .catch((error) => {
          console.error(error);
          setCity("");
        });
    }
  }
```
- In an ideal world the comments here would be superfluous, however, I do not feel comfortable enough with regex syntax to trust that I will be able to come back to this and immediately understand what our regex does here.
- One issue we were having is that the app would crash whenever the API returned an error (because the user had inputted an invalid city name).
	- This was happening because the `WeatherDisplay` component was expecting to receive an object with a certain structure, whereas the error objects sent by the API had a completely different structure to the normal responses.
- I managed to fix this by adjusting our `Weather` type to include an optional `message`:
```ts
export type Weather = {
  coord: Coord;
  weather: WeatherElement[];
  ...
  message?: string; // This property is only present if the API returns an error so we need to make it optional
};
```
- Since the `message` only appears in error responses, we could add an if statement at the top of the component:
```ts
 if (weatherData?.message) {
    return <p>No city found by that name. Please try again.</p>;
  }
```
- We cut things pretty close at the end of the day so did not have much time to prepare for our presentation.
	- With that said, it still went relatively smoothly, with me introducing some of the code before handing over to my partners who showed off the app and did a retro of the day.
- I had a really productive mentor meeting just after 17:00 that lasted a full 90 minutes!
	- We covered topics ranging from [OpenID](https://openid.net/what-is-openid/) to the differences between an interface in TS and in OO languages.

Today was a great day and I have really enjoyed working with my pair programming partners this week. I feel like I need to brush up on authentication and authorisation a bit, but feel quite confident on TS (at least the little TS we have covered). Next week we start our final project which is a crazy thought. It feels like only yesterday we were learning what a boolean was!


## Day 69
*20230527*

Today I did very little in terms of coding since I wanted to take a break after another long week. I did my first Parkrun since I was about 12 or 13 years old which felt great!

- I read over all the code we wrote during the hackathon yesterday to make sure that I still understood exactly how our app worked.
	- This included some new styling that one of my partners had added in the evening on Friday to make the weather display look cleaner and more readable.
- I read a little bit more of *The Object-Oriented Thought Process*.
	- Progress has definitely been slow on this book since it does not relate to the programming we are doing on the course.
	- Nonetheless, I really want to understand OOP so I will keep plugging away, even if it takes me a while to finish the book.

I had a really enjoyable day today, doing Parkrun and then taking advantage of the sunshine in the afternoon. I did not get much coding done but I am fine with that considering that we have reached the end of a long week.


## Day 70
*20230528*

Today I did not get much coding done either as it was the final day of the season in the Premier League.

- I started the day off by reading a bit more of *The Object-Oriented Thought Process*.
	- I used ChatGPT to elucidate a couple of the concepts that were coming up in the book and it proved to be quite effective.
- I rewatched one of the lectures on Supabase since I was feeling a little bit shaky on authentication and authorisation.
- After that I went round to a friend's house to watch the Prermier League matches and that marked the end of my coding for today.
	- (Other than reviewing my programming Anki cards.)

Another quiet day today in terms of coding, but I was never expecting to get much done what with it being the final day of the season.


## Day 71
*20230529*

Today I read some programming articles and looked back at some SQL syntax.

- I saw that Nadeem had made a post on LinkedIn with an article he recommended for us bootcampers since we are going to be starting on our final project tomorrow:
	- [Planning Engineering Projects Effectively](https://betterprogramming.pub/planning-engineering-projects-effectively-eac5855d2e76)
	- I hope I will be able to apply some of the lessons I learned from this article in the planning stages of the project this week.
- I read a couple more aricles later on in the day:
	- [Books that Junior Developers should read](https://www.freecodecamp.org/news/9-books-for-junior-developers-in-2019-e41fc7ecc586/)
	- I have added a few of the books mentioned in this article to my to-be-read list.
	- In fact, I have already read two of the books on this list which feels good!
- [How You Can Use AI to Improve Your Code Quality](https://www.freecodecamp.org/news/how-to-use-ai-to-improve-code-quality/)
	- I have already been applying some of the techniques in this article but I had never thought of using AI to come up with coding ideas.
	- I liked the description the author gives of the programmer as the captain who guides the AI.
- In the evening I had a brief look at some of the SQL syntax we have learned since I missed one day during which we covered it.

I really enjoyed the articles I read today and feel like the one Nadeem recommended has set me up well for tomorrow when we start work on our final project.


## Day 72
*20230530*

Today marks the beginning of our final project! I got to know my team and we came up with a list of problems from which we will choose one and, eventually, build an app to solve it.

- We began the day by giving feedback to our partners from last week.
	- The three of us all agreed that we had made a really good team and were sad to see each other go.
	- We also talked about the importance of teamwork and soft skills as they pertain to employability.
- Next up the teams were announced (six per group).
- We spent some time getting to know each other and discussing our hobbies and backgrounds.
	- I have already worked with two of the people in my group which will hopefully mean that we can hit the ground running if and when we work together in a sub-team.
- I showed my team the manifesto that we used in the Week 7 Project and, after taking some inspiration from it, we each wrote down some points that were important to us personally before reconvening and producing our manifesto.
- Next up came a short talk from Chris Meah who told a story about a bootcamper who scored 100% on an Experian technical test (the first person to ever score full marks on that tech test) but did not end up receiving a job offer due to not being a team player and lacking the soft skills that the company was looking for.
	- This hammers home the importance of working together effectively during this project.
	- Working cohesively is far more important (and impressive) than producing a great app.
- We spent the afternoon sharing problems that we are having right now, problems that we have in general, and problems that are having a global impact nowadays.
- From these problems we started to brainstorm potential app ideas.
- We ended the day by using dot voting to decide on the problem that we felt had the best combination of relevance to the team members and scope for a full-stack application.
	- We are leaning towards choosing "sustainability/waste" although this is subject to change.

All in all, I feel like today was a success and I am really excited to spend the next few days planning out our app!


## Day 73
*20230531*

Today we decided on our problem statement and spent some time coming up with ideas for features that we would like to see in an app that solves that problem.

- We kicked the day off with a stand-up during which we sorted out the Trello board for the day and reflected on yesterday's work.
- I then went into a separate breakout room to have a "stand-up of stand-ups" with one of the coaches and a representative from various other teams.
	- Each morning one team member will have to go and let the coaches know how we are getting on, so I will not be doing it again until next week.
- After that we went on a short break at which point I started work on a kata just to get the gears turning:
- [Product of Largest Pair](https://www.codewars.com/kata/5784c89be5553370e000061b/train/javascript)
```js
// function maxProduct(a) {
//   a.sort((a, b)=> b - a);
//   return a[0] * a[1];
// }

function maxProduct(a) {
  let largest = 0;
  let secondLargest = 0;
  for (let i = 0; i < a.length; i++) {
    if (a[i] > largest) {
      secondLargest = largest;
      largest = a[i];
    }
    else if (a[i] > secondLargest) {
      secondLargest = a[i];
    }
  }
  return largest * secondLargest;
}
```
- I could not see why my original, commented-out solution was being considered to be "too slow" by the tests but ChatGPT suggested that using `sort()` could take a long time if the input array is very long.
- My second solution used a for loop that goes through the array just once and, for that reason, it was faster and thus passed the tests!
- We spent the rest of the morning deciding on a problem statement.
	- Through a round of dot voting we decided on: "People have items they don't need and want to be able to swap them for items they do need."
- We then did some [Disney Ideation](https://idea-sandbox.com/blog/disney-brainstorming-method-dreamer-realist-and-spoiler/) to come up with potential ideas for an app that addresses our problem statement.
- After lunch, we split into two sub-teams.
	- The team I was in focused on making user personas and user stories.
	- The other team did some market research and looked into what competitors (such as [Swopped](https://www.swopped.co.uk/) and [Vinted](https://www.vinted.com/)) are doing and how we could try to improve on their work.
- We reconvened a couple of times to present our work and get the other sub-team's input before ending the day with a retro.

Today was a productive one and I can already feel our ideas coming together. It feels like we are all operating on the same wavelength which is certainly exciting!


## Day 74
*20230601*

We had another productive day today, creating a Google Form survey to do some market research and building a lo-fi wireframe.

- We started the day with our stand-up meeting during which we laid out our plan for the day.
- Next up was a guest lecture delivered by Kim and Bryce from [Squibble](https://squibble.design/).
	- They talked about work inside an agency which is not something that any of our previous guest lecturers have touched on so there were a lot of good learnings to take away.
	- A key point that Kim hammered home is that you have to explain things in simple terms to the client, since they will likely have no idea about the technical side of things.
- We then had a short lecture from Tom on **sprint demos** and how to run one.
	- We have our first sprint demo tomorrow, and will have one each Friday for the remainder of the final project.
- Afterwards, I worked on a Code Wars kata during a break to try and keep my skills sharp:
- [Adding Arrays](https://www.codewars.com/kata/59778cb1b061e877c50000cc/train/javascript)
```js
function arrAdder(arr) {
  const sentence = arr[0];
  for (let i = 1; i < arr.length; i++) {
    for (let j = 0; j < sentence.length; j++) {
      sentence[j] = sentence[j] + arr[i][j];
    };
  };
  return sentence.join(" ");
};
```
- I came across an interesting issue since I had originally added the line `console.log(sentences);` at the end of the inner for loop to see exactly what was happening but this caused the test to time out.
	- When I moved the console log outside of the inner for loop (so that it would only run at the end of each run-through of the outer for loop) it logged all the data correctly with no errors.
	- It seems like there were too many console logs being printed when that line of code was being executed as part of the inner for loop which caused the program to time out, even though the logic of my code was sound.
	- I sent my mentor a Slack message about this so hopefully we can dive into what is going on here tomorrow.
- In my final solution I removed the console log altogether and the code passed without issue.
- Looking back, I could have rewritten `sentence[j] = sentence[j] + arr[i][j];` as ` sentence[j] += arr[i][j];` which is a bit easier on the eye.
- The next task we worked on as a group was making a Google Form survey to send out to fellow bootcampers and the wider School of Code community with some questions pertinent to our topic:
	- We asked for the respondent's age, gender, motivations for using an app like ours (if they would use it at all), and features they would like to see.
- After getting 20 or so responses, we looked at the data and used the responses to guide our final decision on what would be in the MVP and what would be in the stretch goals (and how important each stretch goal would be).
- At one point in the afternoon, Nadeem popped into our breakout room to see how we were getting on and gave us some really good advice:
	- He said that, being a group of six, we should split up into three pairs when coding (i.e. never work solo).
	- We could swap one person out from a pair each day which would allow us all to get used to every part of the codebase and work with different team members, whilst also keeping one "domain expert" working on the same bit of code they were working on before and getting their new partner up to speed at the start of the day.
		- We really are very lucky to have such an experienced developer set aside their time to help us throughout this course.
	- He also suggested working on the front-end first, together, and then moving on to the back-end so that we know exactly what data the front-end wants by the time we start building the back-end and do not end up with any crossed wires where the back-end team makes features that the front-end does not even use whilst the front-end team assumes features that the back-end team is not implementing.
- The last thing we worked on was our lo-fi wireframe on Figma.
	- We each spent some time making our own version before coming together and using everyone's ideas to come up with a final lo-fi design that we were all happy with.

Today went really well and it was nice to get some advice from Nadeem and hear him say that we are doing well (as far as he could tell!).


## Day 75
*20230602*

Today we planned and delivered a Google Slides presentation during our sprint demo then finalised our lo-fi wireframe and added details to it.

- We started off with a stand-up during which we decided who would work on what for the presentation.
- We spent the whole morning preparing the presentation before delivering it just after noon.
	- It went really well, and the fact that we had practised really shone through since we kept it to exactly 9 minutes which was our target.
	- The coaches said that they were really impressed which was lovely to hear.
	- Their only constructive feedback was to spend a little more time explaining what features are a part of the MVP.
- We spent the rest of the day finalising our lo-fi wireframe for mobile and desktop.
	- We got some feedback on different mobile designs to help us decide which to stick with.
- I used Midjourney to make a coin icon that we will use to display how many tokens a user has and we added the image to our lo-fi wireframe.
- We ended the day with a retro in which we congratulated each other on a great first week and laid out what we aim to achieve next week, including a component tree and our rotation system for letting everyone get experience with all parts of the codebase.
- I had another excellent mentor meeting just after 17:00 in which we discussed whether to start with the back-end or front-end, contract testing, and TDD.

This week has flown by and I am delighted with our progress. I can't wait to keep up the good work on Monday!


## Day 76
*20230603*

Today I looked over my [to-do-list-with-react](https://github.com/gregoraubrey/to-do-list-with-react) repo to see if I still understood all the code I had written.

- I found most of the code to be self-explanatory, which was reassuring, although there were a couple of moments in which I had to focus to work out what was going on:
```js
function toggleCompleted(key) {
    console.log(`toggleCompleted has been called onClick`);
    setTodos(
      todos.map((x) => {
        if (x.id === key) {
          return {
            ...x,
            completed: !x.completed,
          };
        }
        return x;
      })
    );
  }
```
- For this function in the `App` component, it took me a while to understand that the return statement is just returning the current value of the todo but with its `completed` property (which is a boolean) swapped to the opposite.
```js
<span className={x.completed ? "text-completed" : ""}>
  {x.text}
</span>
```
- Here, I used a ternary operator to give the `<span>` a class name of "text-completed" only if the `completed` property is truthy (i.e. it is set to `true` and not `false`).
```css
.text-completed {
  text-decoration: line-through;
  color: #999;
}
```
- The CSS file adds strike-through to any element with the "text-completed" class name, which elucidates the inclusion of the ternary operator in the JSX.

I did not do much coding today but I feel happy enough to have gone through an old project and been able to understand most of it straight away.


## Day 77
*20230604*

Today was similar to yesterday in that I mostly spent time looking over work from previous weeks to make sure I still understood it all.

- I started things off by reading some more of *The Object-Oriented Thought Process*.
	- I feel like I will make quicker progress after we have finished the final project but feel that right now this is not the most relevant book to be reading as we will not be making use of OOP in our app.
- Next, I watched a couple of the videos the coaches had recorded on some of the Supabase workshops.
	- I expect we will be using Supabase to make a login page for our website so hopefully I can save the team some time by brushing up on how to use it now.
- In the afternoon, for similar reasons, I looked over our work on SQL and made some Anki cards on the syntax of basic SQL queries since I had not done so when we were initially learning it.

Today was relaxed, much like yesterday, but as a consequence I feel full of energy for tomorrow!


## Day 78
*20230605*

Today we got a lot of work done on the hi-fi wireframe and decided on our tech stack.

- In our morning stand-up we recapped last week's work and planned out today's tasks.
- One of the main tasks was getting the hi-fi wireframe as close to done as possible.
	- The reason we wanted to have it close to done is that the earlier we get it finished, the earlier we can send a Figma prototype to people to get their impressions.
	- Their insights could help us spot mistakes we have made or opportunities for improvement that would have otherwise gone unnoticed.
- The other two main tasks were building a component tree diagram and deciding on our tech stack.
- We decided to split into two sub-teams of three, with one handling the Figma work and one handling the component tree and the tech stack.
- I worked on the latter team and we managed to build a basic component tree, although it still needs some work.
- We did, however, make great progress in terms of choosing a tech stack.
	- We briefly considered MongoDB but decided that a relational database would be better for our purposes.
	- Therefore, Supabase was a natural choice since we already have experience with it, and we also know that it can handle our authentication and authorisation which is great.
	- After some deliberation with the other sub-team about the pros and cons of using TS, we ultimately decided that we would go with it over JS.
		- I was particularly glad that we came to an agreement on this since I think coding our entire project in TS will be a manageable challenge that will leave us feeling confident in our TS skills by the end.
		- It should hopefully make it a bit easier for me to learn a strongly-typed language in the future.
- We wrapped the day up with a retro in which we agreed that we had done a good day's work and that we had a clear idea of what to do tomorrow, namely flesh out the component tree and finalise the Figma protoype so that we can send it out to people to get their thoughts.

I think we have made a good start to the second week of the project and I look forward to tackling the component tree once more tomorrow.


## Day 79
*20230606*

Today we finalised our hi-fi wireframe and made some more progress on building out our component tree.

- In the morning stand-up we agreed that we would all work together to get the hi-fi wireframe done as quickly as possible.
- We decided to replace the **log in** and **sign up** buttons on the landing page with a single call to action in the form of a large **get started** button.
	- This button would lead to a page in which the user could click on either the **log in** or the **sign up** tab before inputting an email and password.
- This helped our landing page look a little more streamlined and we all agreed that this was an improvement over yesterday's design.
- We added a **home** button in the shape of a little house to each page and set up the Figma links so that clicking it would always take the user back to the homepage.
- After finishing up all of the links and testing the prototype out ourselves, we sent some friends and family a link to let them test out our website as it would appear for a mobile user.
	- We got some useful feedback suggesting that our **list item** page was not obvious in how it should be navigated.
	- No doubt we will get some more feedback trickling through in the coming days that will change our plans.
		- This feels like how an Agile team would operate so I am glad that we are working in this way.
- After sending out our prototype, we devoted the rest of the day to talking through the component tree.
	- This proved to be more challenging than we had anticipated.
	- For this reason, we acknowledged during our retro that we would have to continue working on it tomorrow and make it a priority.

Today felt like pretty slow going whilst we were using Figma, since none of us are comfortable with it to the point that we can navigate the site quickly and get our ideas out onto the screen just as we had envisioned them. Despite that, sending out our prototype is a big milestone and one we can be proud of.


## Day 80
*20230607*

Today we researched React Router and got a good chunk of work done on our component tree.

- In our stand-up we decided that we would start the day with some React Router research.
	- We thought that it would be pointless trying to take the component tree design any further without a strong understanding of how React Router works.
- One of our team members had actually used React Router during the week 7 project so he was able to give us a breakdown of what it does and he talked us through the code they wrote for their project.
- I also did some research of my own by doing some googling and then asking ChatGPT some questions.
	- It turns out that React Router does not actually make a multi-page site but rather lets an SPA give the illusion of multiple pages by unmounting and mounting certain components when the path changes.
- We had another guest lecture from Rik Marselis which was an AMA session.
	- I asked a question about which DevOps books he would recommend and he gave me some book suggestions (one of which he co-authored!):
		- [Quality for DevOps teams](https://www.goodreads.com/book/show/57524240-quality-for-devops-teams)
		- [The Phoenix Project: A Novel About IT, DevOps, and Helping Your Business Win](https://www.goodreads.com/book/show/17255186-the-phoenix-project?from_search=true&from_srp=true&qid=TbzyYR3GO7&rank=1)
		- [The DevOps Handbook: How to Create World-Class Agility, Reliability, and Security in Technology Organizations](https://www.goodreads.com/book/show/26083308-the-devops-handbook?from_search=true&from_srp=true&qid=zOTlIRYdY3&rank=1)
- After lunch, we got stuck in on the component tree, armed with our new knowledge about React Router.
- We spent the rest of the day working on this.
	- It took a few iterations but we ended up with a tree that we were all happy with, and had just started adding markers for state and props before it was time for our retro.
- In our retro we reflected on just how quickly a component tree can scale when you add features to an app.
- We also agreed that tomorrow we would keep working on adding state and props markers to the tree, before making a repo on GitHub and adding all of the boilerplate to it.
	- i.e. running `npx create-react-app swapping-app --template typescript` and creating all of the components.

Today was certainly tiring, as we were working on the same task for pretty much the whole day. Nonetheless, it is important that we get this step right as it will really speed up our development process if we are all on the same page and our component tree is sensibly designed.


## Day 81
*20230608*

Today we had a guest lecture from an employer partner, set up our repo before adding the React boilerplate, and set up Netlify ready for CI/CD.

- In our stand-up we agreed that today we should set up the repo and make a decision on how to handle deployment.
- The first task of the day was finishing off yesterday's work on the component tree by finalising the props and state markers on our diagram.
- By the time we had finished with that, it was time for an introduction to one of the employer partners.
- The talk was really useful and the speakers were very candid, even saying straight-up that the starting salary is 34,000 GBP.
	- I have to say I am always surprised by just how open people seem to be in the tech community.
- After lunch we made our mono-repo (which is what we had decided on earlier this week) and ran `npx create-react-app swapping-app --template typescript`.
- We then made a `components` directory within `src` and added the 14 components that comprised our tree.
	- We ran into an issue in which git was not tracking the 14 newly-created empty directories but this was solved easily enough by adding a dummy `.tsx` file to each one.
	- After consulting with ChatGPT I learned that git does this by design since it is supposed to track the contents of files and not directory structure.
		- I also learned that if you *do* want to track an empty directory, you can just create a `.gitkeep` file inside the directory in question.
	- After sorting out the empty directory issue, we used a VS Code extension called [ES7+ React/Redux/React-Native snippets](https://marketplace.visualstudio.com/items?itemName=dsznajder.es7-react-js-snippets) to flesh out the `.tsx` files by typing `tsrfc` and letting the extension generate a TS React functional component.
- Next up we looked into a few options for deployment, such as Netlify, Supabase, Heroku, Vercel, and Firebase.
	- We concluded that Netlify would be the most appropriate for our situation thanks to its having a free tier and a good reputation for being quick to set up and use, even for beginners.
- In our retro we reflected on a good day's work and were happy to have ticked off everything that we were supposed to have finished today according to our Trello board.

Tomorrow we have the second sprint demo which means that we will have to devote the morning to preparing a presentation. After that, we will have the afternoon to get stuck into the code!


## Day 82
*20230609*

Today we prepared and delivered a sprint demo on this week's work, then spent the afternoon trying to get GitHub Actions to work so we could automate our unit tests.

- In the stand-up we laid out who would work on what for the spring demo.
	- My section was the decisions we made this week, such as TS vs JS, mono-repo vs multi-repo, and the tech stack we settled on.
- We spent about 30 minutes practicing and timing our presentation.
- When it came time to deliver the presentation, we finished it right on time, so our prep was definitely worth it.
- We got some useful feedback from the coaches, such as making sure we have a very clear git strategy since we will be working in a mono-repo.
- After lunch, we researched GitHub Actions and how we could use it to automate our tests each time we push to `main` or do a pull request.
- We learned about `.yml` files and made one in `.github/workflows` but the "Actions" page on GitHub kept saying that the commands listed in the file had failed to execute.
- We got very stuck at this point and ended up not making any more progress for the rest of the afternoon.
- Just after 17:00, I had the idea to add `pwd` to the `.yml` before and after we `cd` into the directory containing our components and our `package.json`.
	- I discovered, by looking at the output on the GitHub website, that the same path was being printed for both of the times that we ran `pwd`, meaning that something was going wrong with the `cd` command.
	- After consulting with ChatGPT, I learned that each command is run in a brand new shell session, so the solution was to run all the commands one after the other in one shell session by adding a `|` at the start.
	- It felt incredibly satisfying to see the first green tick on the "Actions" page after implementing these changes, and made the painful couple of hours we spent trying to understand what was going wrong feel worth it.

This week has absolutely flown by! I cannot wait to sink my teeth into the coding next week and see how much of the MVP we can get done, drawing on our extensive planning to guide us.


## Day 83
*20230610*

Today I did very little coding and instead took advantage of the warm weather outside.

- In the morning I read a couple of very short articles on React and SQL.
	- I feel like it is important to have a strong grounding in the basics before we sink our teeth into the coding next week.
	- If we are getting stumped by basic React syntax in the front-end and SQL syntax in the back-end (on Supabase) that we have already covered and used in hackathons then I dread to think what will happen when we encounter issues that we do not have experience with.
- In the afternoon I looked over the sprint demo we gave on Friday to remember what we have done this week (Monday feels like so long ago already!).
- I also looked over our Trello board to remind myself of our plans for next week.

Today was a quiet one on the coding front but I have worked hard for the last five days so I am not too fussed about not doing a lot today, especially when the weather was so nice.


## Day 84
*20230611*

Today I once again did very little on the coding front and instead made the most of the lovely weather.

- I began the day by reading an article I had saved titled [What is YAML? The YML File Format](https://www.freecodecamp.org/news/what-is-yaml-the-yml-file-format/).
	- I decided to read this since we had such issues with the `.yml` file for our automated testing via GitHub Actions on Friday.
- In the afternoon I revised `useState`, `useEffect`, and `useReducer` just to make sure that I am ready for next week when we begin coding up the front-end of our application.

That was all for today, as I spent the rest of the day outside enjoying the weather. I can't wait for tomorrow when we will begin work on writing the code for our React components.


## Day 85
*20230612*

Today we made a start on coding up our components and worked in three pairs for the first time.

- In the morning I bought a Udemy course that was on offer titled [Introduction to Testing in Go (Golang)](https://www.udemy.com/course/introduction-to-testing-in-go-golang/).
	- I am very interested in learning how best to follow TDD, ideally as early as possible in my software development career.
	- I feel like this course makes perfect sense for me based on my desire to both learn more about implementing testing and learn a new language for the back-end.
	- With all that said, I do not plan on making a start on the course until we have finished our final project since I do not want to get distracted with Go when we already have enough on our plate as is with JS.
- We kicked off the day with our stand-up in which we reflected on the previous two weeks and discussed what had gone well and what could have gone better.
	- We agreed that we were not adhering closely enough to the 15/15/15 rule from our manifesto and instead being a bit too stubborn when we could have saved ourselves a lot of time by asking for help at an earlier stage.
- On the coaches' recommendation, we picked out one feature from our MVP to deliver (as a minimum) in Friday's sprint demo.
	- We went with the search functionality on the home page of our app.
- My pair programming partner and I worked on the `ListDisplay` and `DisplayCard` components whilst the other two pairs worked on the `SearchBar` and `PopUp` components.
- We finished our work fairly quickly which gave us ample time to write unit tests.
	- Although we had a few issues with our final unit test (which checked that the correct props were being handed down to `DisplayCard`) we eventually got all the tests to pass which was very satisfying and reassuring.
- We all reconvened and talked through our work, which served as our code review time.
- After this, we got to work merging the changes into `main`, since each pair had spent the day working on their own branch.
	- We had a couple of merge conflicts since another pair had made a couple of edits to `DisplayCard` but it did not take too long to sort things out and combine the necessary bits from both teams.

Today really flew by with all of that coding. I am not sure whether that is a good or a bad thing but I know I feel full of energy for more of the same tomorrow!


## Day 86
*20230613*

Today we continued coding up our app and got the homepage behaving as we wanted.

- In our stand-up we agreed on the work that each sub-team would focus on today.
	- My partner and I would continue with `ListDisplay` and `DisplayCard` so that they implemented the search results created by the `SearchBar` component.
	- One team researched Material UI.
	- The last team worked on the `PopUp` component.
- After finishing our morning work, we all got together just after lunch to merge one by one.
	- We had a couple of merge conflicts due to multiple groups adding new props to `ListDisplay` but these were easily sorted.
- We had all incorporated unit tests for our components as well which was reassuring, although these did occasionally break due to a merge in which, say, a new prop was now being handed into a component which was not yet reflected in that component's tests.
- We incorporated the `data.json` dummy data file into `ListDisplay` such that the initial list of items printed on the page is taken straight from that JSON file
	- This will allow us to demo our app on Friday with a dataset whilst also setting us up for coding our back-end since we know exactly the data structure that our front-end components are expecting to receive

Today, much like yesterday, went really quickly thanks to all the time spent coding. I feel like as a team we are really getting into a good rhythm so I hope we can keep it up for the rest of the week.


## Day 87
*20230614*

Today we split into two teams in order to work on the `NavBar` component and general styling for some of the components we have already finished using Material UI.

- In the stand-up we agreed that we would need some time to get to grips with MUI since it was not quite as simple as we had anticipated.
- Whilst we were working, one of the hiring partners popped into our room to get to know us and see how we were getting on with the project.
	- We all gave a 10-second intro before talking through our problem statement, our MVP, and some of the code we have written thus far.
	- The hiring partner was keen to hear about how we had planned out the project and the division of labour, and seemed impressed by our approach which is certainly encouraging.
	- I feel we all gave a good account of ourselves and it gave us some extra motivation to do a good rest of the day's work.
- I was part of the group that worked on the `NavBar`.
	- We managed to get it looking very close to our hi-fi wireframe, with a home button on the left and an account button on the right that brings up a drop-down menu when clicked.
	- We had issues importing a `.png` of our app's logo that is supposed to sit in the middle of the `NavBar` so we will have to sort that out tomorrow.
- In the retro we congratulated each other on a good day's work, and on making a good impression with the hiring partner we spoke to today.
- We also noted that quite a few of our unit tests had been broken when we switched over to using MUI code in the JSX for our components and we spent a lot of time fixing the unit tests so that they passed again.
	- I am not sure if this is normal or if this is a sign that our unit tests were written poorly in the first place.
	- Either way, I am glad that we are sticking to our manifesto and implementing testing, as I want all the practice I can get with it so that it gets ingrained as a habit early in my software development journey.

Today was tiring thanks to the constant issues with unit tests. On the other hand, we got some great work done on the `NavBar` and we added some great styling to our display cards which now look very similar to the versions on our hi-fi wireframe. It was also a pleasure to chat to a hiring partner today and I can't wait to talk to more!


## Day 88
*20230615*

Today we focused on adding responsiveness to our homepage so that it would look good on both mobile and desktop, as well as adding React Router to our app.

- In the stand-up we agreed that we needed to get the `NavBar` sorted and looking good for tomorrow's sprint demo.
- I was part of the team working on the `NavBar` and we started things off by importing a `.png` of our app logo and adding it to the centre of the `NavBar`.
	- We had an issue later in the day after merging where the border of the image was blocking part of the search bar so it could not be selected with the cursor.
	- Luckily, the fix was as simple as cropping down the `.png`.
- Nadeem popped into our breakout room at one point and asked how we had been getting on.
	- He seemed impressed that we had followed his advice and got continuous deployment working with Netlify.
	- He even tried to break the responsiveness (that the other sub-team had worked on) when we sent him the URL but he couldn't manage it!
- In the afternoon one of our team members talked us through React Router since she had used it in a previous hackathon.
	- It was surprisingly simple and I think I picked it up quite quickly.
	- The only issue we had was that when we first merged our work into `main`, the Netlify site would crash when we tried to add `/home` to the end of the URL (so that we could see the homepage, which is the only page we have worked on thus far).
	- It turned out that changing the path like this causes Netlify to not reference the `index.html` file anymore, so the solution was to make a file called `_redirects` and put it in the `public` folder.
	- We added a single line to said file which tells Netlify to always route to `index.html` (and give an HTTP status code of 200), irrespective of the path, and then React Router can take over from there:
```
/*    /index.html   200
```
- In our retro we reflected on the importance of only keeping a couple of tasks open at any one time so that we avoid having a whole load of half-finished tickets.

Today was hugely productive, and I was especially glad at how quickly we managed to get to grips with React Router. Tomorrow we have our sprint demo and I feel very confident considering we set out to deliver a working homepage as our feature for the week, and it already looks very similar to the hi-fi wireframe, whilst also being responsive.


## Day 89
*20230616*

Today we sorted out the `PopUp` component and then delivered our third sprint demo of the final project.

- In our stand-up we agreed that sorting out the `<Modal>` in the `PopUp` component was the top priority since that was the only part of the `HomePage` that did not yet look close to our hi-fi wireframe.
	- Having a working homepage that looks very close to our hi-fi wireframe was the feature that we set out to deliver at the start of the week so we wanted it to be the centrepiece of our sprint demo.
- We researched how to set up the MUI modal and got it looking very similar to our hi-fi wireframe in the morning.
- When we checked the Netlify site, we noticed a bug where clicking on the background (to quit the pop-up) made all of the "GET IT NOW" buttons unclickable.
- We solved the issue by adding a line to the function that is called `onClose` when the user clicks the background in order to quit the pop-up:
```tsx
const handleCloseModal = () => {
  setOpen(false);
  setGetItNowClicked(false);
};
```
- By setting `getItNowClicked` to `false`, the "GET IT NOW" buttons become clickable once more.
- In the afternoon, we did not leave enough time to practise our presentation so by the time the coaches came into our breakout room we did not feel very prepared.
	- Luckily, the presentation still went well, and we sent the Netlify URL in the chat to let the coaches test out our app and try to break its responsiveness which was definitely a good decision as it added some interactivity to our sprint demo.
- In our retro we talked about how impressed we all were with the code we wrote this week.
- We also noted that we were starting to take liberties in terms of how much time we dedicated to our stand-ups and retros so we looked back at our manifesto and agreed that we would try and nip things in the bud now so that our productivity does not worsen next week.
- Just after 17:00 I had a mentor meeting in which we talked about some of the work I did this week and had a look at some basic C# code so that I could get comfortable with getters, setters, constructors, etc.
	- This is all with a view to doing a TDD exercise in C# over the next few weeks in our meetings which I hope will really help me get used to incorporating TDD into my own projects.

Today was tiring and our preparation for the presentation was hectic to say the least. With that said, we have achieved so much this week and I can only see things getting even better from here, especially since we have made our reusable components now, so building the other pages for our site should not take too much time.


## Day 90
*20230617*

Today I read a couple of articles and then went through the codebase for our final project to make sure I understood how each file worked.

- I read an article titled [How Promises Work in JavaScript – A Comprehensive Beginner's Guide](https://www.freecodecamp.org/news/guide-to-javascript-promises/) in the morning.
	- It served as a good refresher on the `async`/`await` syntax that we have yet to use in our final project.
- I read another article from freeCodeCamp, this time on [different ways to style a React app](https://www.freecodecamp.org/news/how-to-style-a-react-app/).
	- There was a short section on Material UI that was relevant to our final project but some of the other sections, such as the one on Tailwind CSS, were new to me.
	- It would be worth trying these different styling options out in some practice projects just to get used to them.
- In the afternoon I went through all of the components that we have made so far in our final project just to make sure that I understand them fully in preparation for next week.
	- I found that I understood everything in terms of the logic of the code (functions, props, states, etc.) but did not immediately grasp what all of the Material UI styling meant.
	- Overall I was impressed at how much of it did just make sense straight away, which served as a testament to our communication between sub-teams before merges.

Today was fairly relaxed but that was exactly what was needed after a tiring week of coding. I expect that tomorrow I will spend some time editing my CV ready for job applications.


## Day 91
*20230618*

Today I made some edits to my CV and began reading *The Pragmatic Programmer*.

- In the morning I made a start on editing my CV by using [FlowCV](https://app.flowcv.com/).
	- I did not make any edits to the content but rather tried to make my CV a little more visually interesting.
	- I have heard conflicting advice in terms of whether to make your CV plain or playful, so I think it would be worth having two versions that I can choose between depending on the type of company I am applying to.
	- Down the line I will have to make a few changes such as adding a section on SoC but I will wait until we have actually finished our final project before I write it up.
- In the afternoon I began reading a book that I have seen recommended in a few different places as being great for new software developers, namely [The Pragmatic Programmer - 20th Anniversary Edition](https://www.goodreads.com/book/show/52715562-the-pragmatic-programmer).
- I am going to put my reading of *The Object-Oriented Thought Process* on hold for now as I feel that this new read will be more relevant for me as a junior, and I can always come back to *The Object-Oriented Thought Process* after the bootcamp has finished and I try to implement some OO principles into some of my own projects.

Today felt great as I finished a couple of books so I am well on my way to meeting my target of reading 52 books this year. I feel refreshed and ready to jump back into coding tomorrow, hopefully with an even better structure after our productive retro on Friday.


## Day 92
*20230619*

Today we integrated the `LandingPage` into our app, drew up our ERD, and made our Supabase project.

- In our stand-up one of the team members showed us the work she had done over the weekend on the `LandingPage` component (which she had started for us because she will be away for some of this week).
- After she had talked us through all of the code, we noticed one issue in which the `SearchBar` that was being rendered within `LandingPage` was smaller than the one on the homepage.
	- We discovered that this was due to the centring that had been applied to the search bar, "Get Started" button, and the Gif at the top of the page.
	- The solution was as simple as wrapping `<SearchBar />` inside a `<div>` and then applying in-line styling of `style={{width: "100%"}}` to said `<div>`.
- We then had a really engaging guest talk by SoC mentor Ira Rainey who talked about his journey into tech and how he went from leaving school with just one O-level to now being a senior engineer at Microsoft.
	- I asked a question about whether he has ever applied for a job without already knowing the language that he would be using were he to get the job and he said that he has done this countless times, and that as long as you can get across your passion and show your capacity to learn quickly, then it will not be a barrier for you.
- in the afternoon we built our ERD together before creating a Supabase project and creating a couple of tables (`users` and `items`) to test out some SQL commands and jog our memories when it comes to writing the different types of `JOIN` in PostgreSQL.
- That was all we had time for before our retro, in which we all agreed that our use of Trello had been much better today than it had been throughout the whole of the previous week, and that we all feel prepared for tomorrow and know what we need to work on.

Today was really reassuring as I was nervous about how long it would take us to set up the Supabase project. It turns out it was so much easier than I could have imagined and it has made me confident that we will make great progress this week.


## Day 93
*20230620*

Today we created the rest of our tables and then worked on writing a fetch request in our front-end to our Supabase project.

- In our stand-up we agreed that one team would handle the `AuthPage` component and the relevant Supabase set-up, whilst the other would work on creating a fetch request.
- Before we separated, we set up the integration of our back-end by creating a `.env.local` file and populating it with our `REACT_APP_SUPABASE_URL` and our `REACT_APP_SUPABASE_ANON_KEY`.
	- By having `.env.local` written in our `.gitignore` file, we could happily paste in the URL and ANON KEY without worrying about them being tracked by git (and as such visible on GitHub).
- We then had to create a file called `supabaseClient.tsx` and add the following code that referenced our environment variables:
```tsx
import {createClient} from '@supabase/supabase-js';
const supabaseUrl:string =  process.env.REACT_APP_SUPABASE_URL as string
const supabaseAnonKey:string = process.env.REACT_APP_SUPABASE_ANON_KEY as string
export default createClient(supabaseUrl,supabaseAnonKey)
```
- I was in the fetch request team, and we started our work off by writing an async function called `getItems()` which would be called by a `useEffect` which only runs on mount, because its dependency array is empty:
```tsx
useEffect(() => {
    getItems();
  }, []);
```
- We kept having issues with the Supabase syntax for writing a `JOIN` (as part of the data we wanted to pull was not available in the `items` table, but rather the `users` table).
	- It turned out that we had not yet set up reading permissions for the `users` table on our Supabase project which was a laughably simple solution to about an hour's confused frustration.
	- Even with this fix, the `JOIN` syntax was still not working for us so we settled on running two fetch requests (one for `items`, and one for `users`) and then combining the data we get from each by matching up the `user_id` value in each case (where `user_id` is the Primary Key of `users` and a Foreign Key of `items`).
	- We can always refactor our code later to try and get the `JOIN` to work.
- After logging the data to the console and confirming that we were getting what we expected, we passed it down as a prop through both `LandingPage` and `HomePage` to `ListDisplay` and got our site to display the actual database data instead of data from our local dummy `data.json` file which felt like a massive win after a hard day of coding!
- In our retro we talked about the roadblocks we had today in terms of getting to grips with Supabase but reflected that we had reached some crucial milestones, with the other team successfully getting a basic login page set up.

Today was definitely frustrating in terms of coding but rewarding at the same time. It has set us up well to continue on the back-end integration and I am cautiously optimistic about how much work we can get done this week.


## Day 94
*20230621*

Today we fixed our search functionality to work with the data fetched from our back-end and fleshed out the login and sign up functionality.

- In our stand-up we noted that the `SearchBar` component was not set up to interact with the new data fetched from the back-end and was instead still filtering the dummy data from our `data.json` file.
- We fixed this initially by having the search query used to filter down the `items` array.
- Unfortunately, this involved changing the state of `items`, which only fetches from the back-end one time (on mount), so as soon as `items` has been filtered once, all of the items no longer in the list are lost.
- We fixed this by creating a new state variable in `App.tsx`:
```tsx
const [filteredItems, setFilteredItems] = useState<ItemsTableResults[]>(items);
```
- This was combined with a `useEffect` in the same file to make sure that whenever `items` changes (i.e. whenever we fetch data), `filteredItems` copies the new state of `items`:
 ```tsx
 useEffect(() => {
    setFilteredItems(items);
  }, [items]);
 ```
 - We then passed the state variable down as a prop to `SearchBar` and rewrote the component so that it filtered down the `filteredItems` array without ever editing the original `items` array.
 - We rewrote `ListDisplay` to display the contents of the `filteredData` array and this fixed our issue, allowing the user to search, delete characters, and then search again for something else.
	- Our code for sanitising the user input still applied so there was no change to be made there.
- We merged our work on the search functionality into `main` before a couple of developers from one of the hiring partners popped into our room.
	- We talked about how our project was going so far and they seemed impressed, especially by our decision to go for a mobile-first design approach.
 	- They gave us some useful tips for the final presentation such as starting out in mobile mode before moving over to desktop and doing a full sign up in our demo to prove that the whole process works.
- In our retro we reflected that setting up new props can be a pain in TS since you know exactly what needs to change but still have to spend a while going through all the files and adding the new prop and changing the type definition.
	- Perhaps this shows one way in which we are misusing TS?

We made some good progress today, especially the other sub-team in terms of the `AuthPage` which was great to see. I feel like if we keep this up we will be almost done by the end of the week.


## Day 95
*20230622*

Today we set up an `images` bucket on Supabase and wrote the code that allows users to upload images to the database.

- In our stand-up we agreed that one team would work on bugs and fixes whilst another worked on the `MyAccountPage` component.
- I was on the `MyAccountPage` team which meant that we had to set up a bucket on Supabase that would store the images that users upload from the account page.
- We watched a video on [building an image gallery in Supabase](https://www.youtube.com/watch?v=8tfdY0Sf2rA&list=PPSV) before setting up our `images` bucket and adding policies to allow users to insert, select, update, and delete the images that are inside their folder, meaning that they have no access to other users' images.
- After making the bucket, we began writing the code to allow users to upload an image to our database.
- We got bogged down a few times but eventually got it working just before the end of the day with a `useEffect` that contains an async function:
```tsx
useEffect(() => {
    async function fetchUser() {
      const { data: { user } } = await supabase.auth.getUser();
      setUser(user);
      setIsUserLoaded(true);
    }
    fetchUser();
  }, []);
```
- In our retro we agreed that we need to get better at consulting the docs when we get stuck, since they so often contain exactly the answer we are looking for.
	- We also commented on how much smoother this week went in terms of sticking to our manifesto and following an Agile methodology.

Today was frustrating at times but overall very satisfying after we got the image upload working. We are very close to finishing up our MVP now and for that reason I cannot wait for our sprint demo tomorrow.


## Day 96
*20230623*

Today we did a code review to make sure that everyone understands the whole codebase going into the final week of the project, and we also delivered our fourth sprint demo.

- In the stand-up we agreed that we would do a code review together after finalising our presentation.
- We spent some time working out who would say what in the presentation before breaking off to write our individual slides.
- After we were all happy with what we were going to say, we came together for a big code review.
- Just before starting the code review, we tried to merge in the work that we had done on the `AccountPage` component in our separate branch.
	- Unfortunately, it turned out that for some reason this branch was behind `main`, which meant that we were going to have to solve a lot of merge conflicts (so many that GitHub said it could not display them all on the website).
	- Since we had only worked in the one file, we decided that, in the interest of time, we would just copy and paste our work on `AcountPage.tsx` into `main` and do a push.
	- In the future, it would be nice to try and learn a more robust way of dealing with such git issues.
- We spent the rest of the morning practising our presentation and getting the timings right.
- After, lunch it was time for our presentation.
	- It went well, thanks in no small part to our good preparation.
	- We got some helpful feedback, such as adding some functionality to the `Footer` component so that we actually get some practical use out of the space it occupies.
- We began writing the code for implementing the `token_count` column in our `users` table so that we can display the user's token count in the `NavBar` when they are logged in.
	- This proved more difficult than we had anticipated and we noticed ourselves getting bogged down and frustrated, so we decided to pivot and come back to it with fresh eyes on Monday.
- We spent the rest of the day fixing bugs and little issues we had noticed.
- In our retro we commented on how much we had achieved this week, especially considering the ambitious goals we had set for ourselves.

This week has been really enjoyable and I feel like we have worked more smoothly than ever as a team. I am nervous and excited in equal measure for the culmination of all our work next week!


## Day 97
*20230624*

Today I was not at home for most of the day so I only had a small window of time for programming.

- I watched the start of a new freeCodeCamp tutorial titled [Learn Supabase, an Open-Source Firebase Alternative](https://www.freecodecamp.org/news/learn-supabase-open-source-firebase-alternative/).
	- Hopefully this will help solidify my understanding of the platform and build on what I have done with Supabase thus far in our final project.
	- The tutorial itself is almost three hours long so I do not expect that I will be able to finish it by the end of our project but it will hopefully be useful for any of my own projects I work on after the bootcamp has ended.
- I then read an article that one of the coaches recommended on `useContext` titled [A Guide to React Context and useContext() Hook](https://dmitripavlutin.com/react-context-and-usecontext/).
	- I have not used this hook before but it seems simple enough, and we may well need it for some of the functionality in our project so it is definitely worth getting familiar with it now.

That was all I had time for today but I am happy enough with that after a long week working on our final project.


## Day 98
*20230625*

Today I went through the whole codebase for our final project to make sure I understand it all going into the final week.

- In the morning I stumbled across a book called  [Test-Driven Development in Go](https://www.goodreads.com/book/show/121382396-test-driven-development-in-go) by Adelina Simion.
	- This seems like a great book for me to read after the bootcamp as I both attempt to learn Go and also improve my understanding of TDD.
- In the afternoon I looked through our entire codebase for the final project to see if there were any gaps in my knowledge.
- Having done a code review at the end of last week, I was hopeful that it would all make sense to me and I was pleasantly surprised to discover that for the most part everything was either fairly self-explanatory or something that I remembered working on or being explained to me.
- A good example of some self-explanatory code is the way in which one of the sub-teams made a different gif appear on screen depending on the width of the user's screen:
```tsx
const isDesktop = useMediaQuery('(min-width: 768px)');

const landingPageGif = isDesktop ? landingpagegifdesktop : landingpagegif;
```
- The only parts of the codebase that I still found slightly confusing were the authentication sections, so hopefully the freeCodeCamp Supabase course I started going through yesterday can help with that.

Today was reassuring as I proved to myself that I do indeed understand our codebase and now I feel like I am in a great position to contribute to the team next week and add the finishing touches to our app!


## Day 99
*20230626*

Today we split our work for today and tomorrow and made good progress on the `MyAccountPage` component.

- In our stand-up, we decided that we would split into three teams:
	- One for planning our final presentation.
	- One for editing the Supabase tables such that when a user signs up, the UUID that gets created for them is added to the `users` table.
	- One for working on `MyAccountPage.tsx`.
- I was working on `MyAccountPage` which involved adding a `ListDisplay` to it that was slightly different to the ones that appear on the home page and the landing page.
	- In this case, the only items we want to show up are ones that have been listed by the currently logged in user, so we wrote some code to have the array of items filtered down by checking for a match between the `user_id` of each item and the UUID of the current user session:
```tsx
useEffect( () => {
    async function getUser() {
      const { data: { user } } = await supabase.auth.getUser()
      setCurrentUser(user);
    if(user) {
      setFilteredItems(items.filter(x => x.user_id === user?.id));
      setLoading(false);
    } else {
      console.error("User does not have a value.");
    };
    };
    getUser();
  }, [items, setFilteredItems] );
```
- After lunch, we wrote the code that allows the user to upload an item.
	- i.e. add a new row to the `items` table:
```tsx
if (user && title && uploadedFilePath) {
        const { data: insertData, error: insertError } = await supabase
          .from("items")
          .insert([{ title: title, user_id: user?.id, image: `https://xxxxxxxxxxxx.supabase.co/storage/v1/object/public/images/${uploadedFilePath}` }]);
          console.log("insertData variable from handleFormSubmit:", insertData);
```
- We found that the items were being uploaded to our bucket just fine, but this code that actually inserts a new row into the `items` table was not working.
- We solved this by adding console logs at various places, eventually discovering that the `title` variable was not updating as it should have done when the user typed into the input box.
	- For that reason, the value of `title` was always stuck at its initial `""` meaning `(user && title && uploadedFilePath)` was always evaluating to `false`, and our insert code was never even running.
	- After fixing the function that handled user input in the text box, the insert code worked straight away!
- In our retro we commented on a few bugs that we had noticed in our code and added them to Trello.

Today has been an excellent start to the week. We made great progress on the  `MyAccountPage` component and reached the milestone of finally having the user be able to upload an item to the database from our deployed front-end on Netlify.


## Day 100
*20230627*

Today marks 100 days of journaling my coding! We spent the day fixing bugs and adding a couple of features from our MVP specification that were still missing from our app.

- In our stand-up we agreed that we would be working in three teams of two today:
	- One for presentation prep and fixing small bugs.
	- One for back-end fixes and adding `claimed` functionality.
	- One for working on the  `MyAccountPage` component.
- I was part of the `MyAccountPage` team and we kicked things off by fixing a bug to do with going from the account page to the home page (by clicking the home icon).
	- The issue was that the items that would display on `/home` were the same ones being displayed on `/myaccount` (i.e. the ones listed by the currently logged in user) until you typed something into the search bar, which caused the value of `filteredItems` to be updated.
		- `filteredItems` was also being used on `/myaccount` which is why its effects persisted after the user moved to `/home`.
- We fixed the bug by resetting `filteredItems` to the value of `items` (i.e. what we fetched from Supabase when `App` first mounted) every time the home icon is clicked:
```tsx

<IconButton component = {Link} to = "/home" onClick={() => setFilteredItems(items)}>
    <HomeIcon sx={{ fontSize: isMobile ? "40px" : "50px", color: 'white'}}/>
</IconButton>)
```
- We also added an "unlist" button to each `DisplayCard` that only renders when the path is `/myaccount`, and we created a function called `handleUnlistButtonClick` which deletes the relevant item from our `items` table on Supabase:
```tsx
const handleUnlistButtonClick = async () => {
    if (tokenCount && tokenCount >= 1) {
      const { data: userData, error: userError } = await supabase.auth.getUser();
      const currentUserID = userData?.user?.id;
      if(userError) {
        console.error(userError);
      };
      if (currentUserID) {
        const { data: itemData, error: itemError } = await supabase
          .from("items")
          .select("user_id")
          .eq("item_id", id)
          .single();
        if (itemError) {
          console.error(itemError);
        }
        const itemUserID = itemData?.user_id;
        if (currentUserID === itemUserID) {
          await supabase.from("items").delete().eq("item_id", id);
          setFilteredItems(filteredItems.filter(x => x.item_id !== id));
          if (setTokenCount) {
            setTokenCount(tokenCount - 1);
          }
          const { error: updateError } = await supabase
          .from('users')
          .update({ token_count: tokenCount - 1 })
          .eq('user_id', currentUserID);
          if (updateError) {
            console.error('Error updating user token count:', updateError);
          }
        }   else {
          console.log("Permission denied. The current user is not the owner of the item.");
        }
      }
    }
    else {
      alert("You don't have enough tokens to unlist this item. You need at least 1 token to unlist an item. Please list an item to earn a token.")
    }
  };
```
- (I removed some console logs and comments to shorten the above code.)
- In our retro we talked about a few more bugs we had noticed and sorted out our Trello board ready for tomorrow.

I cannot quite believe that I have already written 100 entries of this coding journal. I threw my ramblings (excluding day 100) into LibreOffice Writer and it said that I had written 39,389 words (229,940 characters)! That's a small book! I guess it goes to show that a little can go a long way if you do it consistently. I feel like summarising what I have got up to each day has been rewarding and has helped clarify my thoughts on various coding (and non-coding) issues over these last few months, so I actually plan to continue. If anyone is reading this, I hope you might try journaling your coding activities too (and if you do, drop me an email at gregoraubrey@protonmail.com). I can say wholeheartedly that it has been worth the 5 to 10 minutes it has taken me each day, and if these entries serve as nothing more than a memento to look back on then it will have been worth my while. Until tomorrow!


## Day 101
*20230628*

Today we added the finishing touches to `MyAccountPage` and worked on our presentation.

- In our stand-up we agreed that we would all work together to add the final feature to our app that would complete the MVP.
- This involved making the "VIEW" button on the `/myaccount` page show the claimant's email address, username, and home address, or show an alert saying that the item had not yet been claimed if there was no claimant.
- This did not take too long although we did have an issue with our use of `useLocation()` in the `PopUp` component.
	- This was causing issues when our GitHub Actions attempted to build before we could merge to `main`.
	- It said that we could not have `useLocation()` inside a non-router component, so we solved the issue by passing down a prop that was either a string of `"homepage"` or a string of `"myaccount"` and then using that to determine what fields the `PopUp` should display.
- After merging our last piece of work into `main`, we spent the rest of the day working on our presentation and brainstorming our demo video.
- In our retro we agreed that we had done another good day's work and reflected on how strange it felt to actually have the code finished at last!

Today went really well, although I feel like we will have to move quickly tomorrow in order to get the video finished on time.


## Day 102
*20230629*

Today we finished off our presentation and recorded it before moving on to planning our demo video which we will make tomorrow.

- In the stand-up we agreed that we would each spend some time individually finalising our slides for the presentation and writing out a script.
- After we were all happy with what we were going to say, we did a couple of run-throughs and timed ourselves to see how we were doing.
- After a couple of run-throughs we were happy with what we wanted to say, and had managed to get the total time down to around 12 minutes which was perfect.
- We moved into a separate Zoom meeting so we could record our presentation and managed to get a good recording done at the first time of asking which was satisfying.
- We spent the afternoon planning out our 3-minute demo video which will introduce our app and its features.
- We recorded a few lines of voiceover and then it was time for our retro.
- In our retro we reflected on how happy we were to get the presentation recording done, and in good time too.
- All that we have left tomorrow is to add the finishing touches to our demo video, and then we will be done!

It feels very strange to be going into the final day of the course tomorrow (excluding demo day on the 5th of July). At the same time, I could not be prouder of how my teammates and I have worked together over these last five weeks and I really feel like we have not just produced a well-made app but learned so much about product engineering and the Agile workflow too.


## Day 103
*20230630*

Today was the last official day of the School of Code bootcamp Cohort 14 (excluding demo day next week)!

- In our stand-up I mentioned that I had noticed that our `README.md` was looking a bit barren so we updated it so that it served as a good introduction to our project.
- We knew exactly what we had to work on today and consequently spent the morning and most of the afternoon scripting and then recording our 3-minute video that will serve as a sort of advertisement for our app.
	- We recorded it using Canva which caused a couple of issues due to our inexperience with the software but we managed to get the recording exported in time and uploaded as an unlisted video on YouTube.
- At 15:30 we all came together in the main room and spent the remainder of the afternoon celebrating and playing some games like Kahoot which was a good laugh.
- I had my final mentor meeting just after 17:00 and expressed just how lucky I felt to have been paired up with someone so helpful and so experienced in the industry.
	- To my delight, my mentor expressed a similar sentiment and said he was glad to have had me as his mentee which was wonderful to hear.
	- He hammered home one last time the idea that in this industry you can progress as fast or as slow as you like, and that if you apply yourself and are constantly hungry to learn, there is no reason why you cannot soon be at the same level as colleagues 10 years your senior.

It feels strange to know that this was the last day of School of Code. I have the rehearsals and then demo day itself to look forward to so it has not really sunk in yet. For now, it is time to have a well-earned rest and then look over the codebase and prepare for our presentation next week.


## Day 104
*20230701*

Today I spent some time reading through our codebase to prepare for demo day next week.

- I started off by going through our component tree just to get an idea of how we had planned out the structure of our components.
	- It was interesting to see just how simple the tree makes everything look, when in reality by the end we had some components taking in six or seven props.
	- I guess it goes to show just how quickly complexity can creep into a project if you are not careful.
- Having gone through the tree, I made a start on `App.tsx` before moving on to the four different pages of our web app.
- Whenever there was a line of code that did not click straight away, pasting it into ChatGPT and asking for a breakdown was enough to jog my memory and get me back up to speed.

That was all I worked on today but I think a rest was well-deserved after five long weeks working on our final project! Tomorrow I will keep going through the codebase until I have checked through every file at least once.


## Day 105
*20230702*

Today I edited my CV and sent off my first few job applications.

- I started the day by editing my CV and adding sections both on School of Code and our 5-week final project.
	- There was something very fulfilling about committing all my hard work over these last 16 weeks to writing (even though I have been doing that every day here!).
- After getting my CV to a point where I was happy with it, I applied to some jobs that interested me that I had found through various platforms such as LinkedIn and Indeed.
- In the afternoon I spent some time reading *The Pragmatic Programmer*, which I had not picked up in a while.
	- I hope that since the bootcamp has now finished, I should be able to spend a lot more of my time reading programming books.
	- I have kept up my [personal reading habit](https://www.goodreads.com/user/show/109060712-gregor-aubrey) so I do not expect that it will be too much of a challenge to ramp up the time I spend reading technical books.

Today marks the start of my journey trying to find a job in tech! It felt great to finally send out some applications - I just hope I get some responses! Unfortunately I did not get the time to read through the rest of the codebase so I will have to spend some time on that tomorrow.


## Day 106
*20230703*

Today we had our rehearsals for demo day and I sent off some more job applications in the afternoon.

- We started the day by logging into [Kumospace](https://www.kumospace.com/) and finding our team's booth.
- After sorting out a few technical difficulties and getting everyone set up, we did a couple of run-throughs of our presentation.
	- These went well, with the only issues being that we could have been more explicit with our description of some of the app's features during the demo section of the presentation.
- After a while, the coaches visited our booth and we did our proper presentation rehearsal.
	- It went smoothly, thanks in no small part to our practice runs earlier in the day.
	- We got some useful feedback, such as demoing the app as if we were a user rather than just drily explaining each one of the features.
- In the afternoon I sent off some more job applications based on roles I had come across on LinkedIn and Indeed.

As a team we were all in agreement that today's rehearsal went well and we are all excited for Wednesday so we can finally show off our hard work to the hiring partners.


## Day 107
*20230704*

Today I took part in a hackathon for one of the School of Code hiring partners.

- One of our team members could not make it so we were in a team of three instead of four as had been planned.
- Our task was to come up with ideas for an app or website that the company could use to help reduce its carbon footprint.
	- We had free rein to take this in any direction we liked, so we came up with a huge variety of ideas.
	- We talked about a car pooling app, a system for using excess heat from PCs, and a pedometer app to name just a few of our ideas.
- We settled on an app that takes watts generated by using exercise machines in the company gym and gives them back to the grid.
	- The app will let users log in and see their wattage go up as they use a machine.
	- It will also let them see the leader board and any prizes up for grabs this month so they know who they need to beat!
- We made a manifesto, used Disney Ideation, wrote out some user stories, settled on the features for an MVP, chose a tech stack, and started work on a lo-fi wireframe before time was up.
- At the end of the day we gave a short presentation to some of the judges who seemed impressed with what we had achieved in the time.

All in all, I was surprised that there was no coding involved today but I expect they are more interested in our teamwork than our coding ability right now. It was certainly good practice and should set me in good stead for any future hackathons. Tomorrow is demo day, the culmination of all our hard work, and I cannot wait!


## Day 108
*20230705*

Today was demo day and our opportunity to showcase what we have learned in these last 16 weeks!

- We kicked things off with a brief pep talk from Chris who congratulated us all and said how well we had done to get to this point.
	- He gave some good advice for our presentations by saying that there was nobody in the world better equipped to present our work on our final project than us, and he recommended that we always think about making sure the audience enjoys themselves.
- We headed to Kumospace just before 10:00 to get ready for the hiring partners to come round and see us.
- We were a bit nervous before our first presentation but it went really well, which helped to settle the nerves.
- Throughout the whole day, the only issue we had was occasionally trying to claim an item that we had already claimed in a previous demo.
	- I alleviated this issue by listing a whole load of new items from my account on our site.
- All of the hiring partners were positive in their feedback and many of them reflected that it was seriously impressive to have produced a working MVP for a full-stack application in just 5 weeks.
- When all was said and done we had presented eight times, and were absolutely knackered!
- I spent some time mingling with fellow bootcampers from other groups to see how things had gone for them and to reflect on the last 16 weeks and how quickly they have gone by.

With demo day done and dusted, that marks the end of the bootcamp, and now all we have left are the employability sessions that start from next week. I had a whale of a time today and it felt wonderful to be acknowledged by industry professionals for our hard work and the progress we have made. I cannot thank my final project teammates and everyone at School of Code enough!


## Day 109
*20230706*

Today I reread a couple of articles that I had gone through in the last few weeks and sent off some more job applications.

- I began the day by reading some more of *The Pragmatic Programmer* which I am really enjoying.
	- I like the way the authors have structured the book into a series of short topics as it makes for easy reading and it feels like every paragraph contains a nugget of self-contained wisdom without having to contribute overly to an over-arching narrative flow.
- In the afternoon I read through some articles that I had saved to Reader but felt that I no longer really remembered.
	- One of these was an article on [promises in JavaScript](https://www.freecodecamp.org/news/guide-to-javascript-promises/) that I only read recently.
	- I am confident when it comes to `async/await` but the older promise syntax still confuses me somewhat, likely because I have not yet seen examples of it in use in an actual project.
- I sent off a few more job applications today, so hopefully I hear back soon.
	- I have already had a couple of rejections but I am unfazed as these were all for companies that were not explicitly looking for a first-role junior developer.

I got some good reading done today and I hope I can continue in the same vein tomorrow.


## Day 110
*20230707*

Today I attended an info session and Q and A run by one of the employer partners, and then set up a GitHub Actions workflow to update the word count of this file each time I push changes.

- The info session started off with an introduction from the company's head of engineering.
	- He introduced two former bootcampers who have been working with him for a year now, which is a good sign.
- I was impressed by the career development structure that was laid out in the presentation.
	- Knowing that the company has good opportunities for its employees' growth is a huge thing for me, so it was great to see it highlighted today.
- After the presentation, there was some time set aside for questions and answers.
	- I asked a question about why the company had chosen to go for JavaScript in both the front-end and the back-end and the head of engineering gave an informative answer about the practicality of trying to hire juniors who know other back-end languages versus simply JavaScript.
- When the info session was over, I spent some time writing a `.yml` file that would use `grep` to read the word count of this file, and `sed` to edit the word count figure on line 3 each time there was a push to `main`.
	- It took a while but eventually I got it working, and it should really motivate me to keep writing these journal entries.
```bash
WORD_COUNT=$(grep -o '\w*' README.md | wc -w)
FORMATTED_WORD_COUNT=$(printf "%'d" $WORD_COUNT)
sed -i "3s/.*/## Word Count: $FORMATTED_WORD_COUNT/" README.md
```

I really enjoyed the info session today, and was especially happy to get the `.yml` file working after a bit of trial and error. It feels great to have the confidence now to think of a coding idea and actually believe that I could execute on it.


## Day 111
*20230708*

Today I read some more of *The Pragmatic Programmer* and read over the codebase for our final project.

- I started the day by reading some of *The Pragmatic Programmer*.
	- My thoughts on the book from a few days ago still stand, and I feel like I am learning two or three really valuable nuggets of information each time I open up the book.
	- I hope to have the book finished within the next week or so.
- In the afternoon I was feeling quite tired so I decided that I would limit myself to simply looking through our codebase for the final project once more.
	- I had already brushed up on it recently in order to prepare for demo day but I decided that it would not hurt to check back in on it and see how much I remembered.
	- Luckily, everything made sense to me which is certainly a good sign.

Rereading the codebase for our final project felt a little like an exercise in futility after finding that I really did remember everything, but I suppose it cannot hurt. I am really enjoying *The Pragmatic Programmer* and am glad to have picked it out.


## Day 112
*20230709*

Today I got through some more of *The Pragmatic Programmer* and sent off some job applications.

- I read through a bit more of *The Pragmatic Programmer* and took some notes on the paragraphs that stood out to me.
	- I hope that coming back to these highlights and notes periodically will help keep me focused on writing clean code and maintaining best practices both at work and in my personal projects.
- I sent off quite a few job applications today for junior roles that I had come across on LinkedIn and Indeed.
	- Hopefully I will hear back soon from some of these companies and, if I am lucky, get an interview or two.
- I also did some research into pulling data from the [RAE](https://www.rae.es/) Spanish dictionary website so that I could easily look up Spanish vocabulary.
	- Perhaps I could build out a simple app to help me save some time each time I want to look up a word.

I did not do too much coding today but I got some good reading done which is always nice.


## Day 113
*20230710*

Today we had our first post-course employability session where we had a guest talk and worked on our CVs.

- We started the day by splitting up into groups and just having a chat about how we felt demo day had gone.
	- I mentioned how I was very happy with how our group had presented and the other people in the breakout room held a similar sentiment.
- Next up we had a guest talk by someone who was on cohort 13 of the bootcamp.
	- She talked about how anxious she had been during the bootcamp about her own coding abilities, considering herself one of the weakest coders out of her cohort.
	- Despite this, she ended up being the first one hired, so she talked about the soft skills that came across in the one interview she did and also about how she tackled the tech test she was set.
	- I asked a question about testing and she said that she wrote a few unit tests in Jest for her tech test but that these were written after the code they were designed to be testing, so it was not strictly TDD.
- For the rest of the session today we split off into our breakout rooms again and worked on our CVs together.
	- To be honest my group just spent most of the time chatting about the upcoming job hunt and what kinds of personal projects we might like to build.

It was really nice to see everyone's faces again today, even though it has only been a few days since last I saw them! I look forward to the next of these employability sessions on Wednesday and am really appreciative of the great support that the team at School of Code is lending us.


## Day 114
*20230711*

Today I made a start on a tech test and did some more research into TDD.

- In the morning I was sent a tech test for one of the hiring partners via GitHub Classrooms.
- I did not have much free time today so I just had a brief look over the test, tested out a quick `git push`, and then left it for tomorrow when I can focus on it 100%.
- Later on in the day I spent some brushing up on test-driven development so that I will be ready to follow TDD principles as I tackle the tech test on Wednesday.

I did not have much spare time today so I was glad to have got at least a little done, and confirmed that the tech test is all set up ready for me to work on it tomorrow.


## Day 115
*20230712*

Today we had an employability session featuring a guest talk, and I spent the afternoon working on the tech test I was given yesterday.

- For our employability session today we had a guest talk from Greg Morley.
	- He talked about "turning left" as it pertains to an unexpected change from the previous path you were on.
 	- My decision to leave my job and embark on the 16-week bootcamp is an example of this.
  	- He also spoke about the benefits of keeping a journal, which was music to my ears!
- In the afternoon I got to work on the tech test that I had been set yesterday.
	- I decided to go for a fully TDD approach, so I wrote my tests before writing the code that would make them pass.
	- The start of the test was easy enough but the second half really stumped me, and try as I might to break the problem down, I just could not make headway and the function I was being asked to write just seemed impossible due to the potential ambiguity of its parameter.
	- Nonetheless, I planned as best I could and wrote down all of my steps and my thoughts in a `plan.md` file.
	- I also set up a GitHub Actions workflow (using a `.yml` file) for automated building and running of the tests on each push or pull request to `main`.

The tech test today was tough but I feel like I approached it in the right way and followed good software development principles which I was very pleased with.
