### isReallyNaN
```javascript
const isReallyNaN = (val) => {
if (Number.isNaN(val)) return true;
else return false;
};
```

### Filter the number
```javascript
var FilterString = function(value) {
  let str = '';
  
  for (let i = 0; i < value.length; i++) {
    if (isNaN(value[i]) === false) {
    str += value[i];
  }
  }
  return +str;
}
```

###Find the next perfect square!
```javascript
function findNextSquare(sq) {
  let a = Math.sqrt(sq);
  
  if (Number.isInteger(a) === false) return -1;
  else return Math.pow(a + 1, 2); 
}
```

### You're a square!
```javascript
var isSquare = function(n){
let a = Math.sqrt(n);
  return Number.isInteger(a);
}
```

### Squares sequence
```javascript
function squares(x, n) {
let arr = [x];
if (n <= 0) return [];
else {
  for (let i = 2; arr.length < n; i *= 2) {
    arr.push(Math.pow(x, i));
  }
  }
return arr;

}
```
###Enumerable Magic #3 - Does My List Include This?
```javascript
function include(arr, item){
  for (let i = 0; i < arr.length; i++) {
  if (arr[i] === item) return true;
  }
  return false;
}
```

### Total amount of points
```javascript
function points(games) {
let sum = 0;
  for (let i = 0; i < games.length; i++) {
    if (games[i][0] > games[i][2]) sum += 3;
    else if (games[i][0] < games[i][2]) sum += 0;
    else sum += 1;
  }
  return sum;
}
```

### Find the first non-consecutive number
```javascript
function firstNonConsecutive (arr) {
  for (let i = 0; i < arr.length - 1; i++) {
    if (arr[i + 1] !== arr[i] + 1) return arr[i + 1];
    
  }
    return null;
}
```

### Santa's Naughty List
```javascript
function findChildren(santasList, children) {
  let arr = santasList.filter(el => children.includes(el)).sort();
  return arr2 = arr.filter((x, i, arr) => arr.indexOf(x) === i);
}
```

### filterEvenLengthWords
```javascript
function filterEvenLengthWords(words) {
  return arr = words.filter(el => el.length % 2 === 0);
}
```

### Find how many times did a team from a given country win the Champions League?
```javascript
function countWins(winnerList, country1) {
  let k = 0;
  for (let i = 0; i < winnerList.length; i++) {
    if (winnerList[i].country === country1) k++;
  }
  return k;
}
```

### Remove First and Last Character Part Two
```javascript
function array(s){
let arr1 = s.split(',');
if (arr1.length === 0 || arr1.length === 1 || arr1.length === 2) return null;
else {
  return arr1.slice(1, -1).join(' ');
}
}
```

### Array plus array
```javascript
function arrayPlusArray(arr1, arr2) {
  return arr1.reduce((acc, curr) => acc + curr, 0) + arr2.reduce((acc, curr) => acc + curr, 0);
}
```

### Beginner - Reduce but Grow
```javascript
function grow(x){
  return x.reduce((acc, curr) => acc * curr, 1);
}
```
### Thinking & Testing : Something capitalized
```javascript
function testit(s){
let str = '';
for (let i = 0; i < s.length; i++) {
  if (s[i + 1] === ' ' || i === s.length - 1) str += s[i].toUpperCase();
  else str += s[i];
}
return str;
}
```

### Find the capitals
```javascript
var capitals = function (word) {
let arr = [];
	for (let i = 0; i < word.length; i++) {
    if (word[i].toUpperCase() === word[i]) arr.push(i);
  }
  return arr;
};
```

### Can Santa save Christmas?
```javascript
function determineTime(d){
let sumH = 0;
let sumM = 0;
let sumS = 0;
for (let i = 0; i < d.length; i++) {
 
  sumH += Number(d[i].split(':')[0]);
  sumM += Number(d[i].split(':')[1]);
  sumS += Number(d[i].split(':')[2]);
  }

console.log(sumH);
return (sumH + sumM / 60 + sumS / 360) <= 24;
}
```

### makeBackronym
```javascript
//preload variable: dict

var makeBackronym = function(string){
  let newStr = '';
  for (let i = 0; i < string.length; i++) {
    newStr += dict[string[i].toUpperCase()] + ' ';
  }
  return newStr.trimRight();
};
```

### Every possible sum of two digits
```javascript
function digits(num){
  let arr = num.toString().split('');
  console.log(arr);
  let newArr = [];
  
  for (let i = 0; i < arr.length; i++) {
    for (let j = 0; j < arr.length; j++) {
      if (i !== j && i < j) newArr.push(+arr[i] + +arr[j]);
    }
  }
  return newArr;
}
```

###  Exclamation marks series #2: Remove all exclamation marks from the end of sentence
```javascript
function remove(s){
 return s.replace(/!+$/, '');
  
}
```

### What is my name score? #1
```javascript
function nameScore(name){
let sum = 0;
let obj = {};
  for(let key in alpha) {
    for (let i = 0; i < name.length; i++) {
      if (key.includes(name[i].toUpperCase())) sum = sum + alpha[key];
    }
  }
  obj[name] = sum;
  return obj;
}
```

### Coding Meetup #5 - Higher-Order Functions Series - Prepare the count of languages
```javascript
function countLanguages(list) {
  let obj = {};
   for (let i = 0; i < list.length; i++) {
   if (obj[list[i].language]) obj[list[i].language] += 1;
   else obj[list[i].language] = 1;
   }
  return obj;
}
```

### Job Matching #1
```javascript
function match(candidate, job) {
  if (candidate.minSalary !== undefined && job.maxSalary !== undefined) {
  return candidate.minSalary - 0.1 * candidate.minSalary <= job.maxSalary;
  }
 else return error;
}
```

### The Office II - Boredom Score
```javascript
function boredom(staff){
  const obj = {
    accounts: 1,
    finance: 2,
    canteen: 10,
    regulation: 3,
    trading: 6,
    change: 6,
    IS: 8,
    retail: 5,
    cleaning: 4,
    'pissing about': 25,
  };
  let sum = 0;
  for (let key in obj) {
    for (let el in staff){
    if (key === staff[el]) sum += obj[key]; 
  }
  }
  if (sum <= 80) return 'kill me now';
  else if (sum < 100 && sum > 80) return 'i can handle this';
  else return 'party time!!';
}
```

### Permute a Palindrome
```javascript
function permuteAPalindrome (input) { 
  let obj = {};
   if (input.length === 0 || input.length === 1) return true;
   else if (input.length === 2 && input[0] === input[1]) return true;
   else if (input.length === 2 && input[0] !== input[1]) return false;
   else {
     for (let i = 0; i < input.length; i++){
       if (obj[input[i]]) obj[input[i]] += 1;
       else obj[input[i]] = 1;
     }
   }
   let countOdd = 0;
   for (let key in obj) {
    if (obj[key] % 2 === 1) countOdd += 1;
  }
   if (countOdd === 1 || countOdd === 0) return true;
   else return false;
}
```


### Most valuable character
```javascript
function solve(st) {
  let obj = {};
  for (let i = 0; i < st.length; i++) {
    obj[st[i]] = st.lastIndexOf(st[i]) - st.indexOf(st[i]);
  }
  let arr1 = Object.values(obj);
  let v = Math.max(...arr1);
  let arr2 = [];
  for (let key in obj){
    if (obj[key] === v) arr2.push(key);
  }
  let arr3 = arr2.sort();
  return arr3[0];
}
```

### How many days are we represented in a foreign country?
```javascript
function daysRepresented(trips){
   let arr = [];
   for (let i = 0; i < trips.length; i++) {
     for (let j = trips[i][0]; j <= trips[i][1]; j++) {
       arr.push(j);
     }
   }
  let arr1 = arr.sort();
  let l = arr1.length;
  for (let z = 0; z < arr1.length - 1; z++) {
    if (arr1[z] === arr1[z+1]) l -= 1;
  }
  return l;
}
```

### Beginner Series #2 Clock
```javascript
function past(h, m, s){
  return s * 1000 + m * 60000 + h * 3600000;
}
```

### Find the Slope
```javascript
function slope(points){
  if (points[0] === points[2]) return 'undefined';
  else return String((points[3] - points[1]) / (points[2] - points[0]));
}
```


### Miles per gallon to kilometers per liter
```javascript
function converter (mpg) {
  let a = Number(((mpg * 1.609344) / 4.54609188).toFixed(2));
  if ((a * 10) % 1 === 0) return Number(a.toFixed(1));
  else return a;
}
```

### Training JS #7: if..else and ternary operator
```javascript
function saleHotdogs(n){
  return n < 5 ? n * 100 : (n >= 5 && n < 10) ? n * 95 : n * 90;
}
```

### Is this a triangle?
```javascript
function isTriangle(a,b,c) {
  if ((a + b) > c && (a + c) > b && (b + c) > a) return true;
  else return false;
}
```

### Make a function that does arithmetic!
```javascript
function arithmetic(a, b, operator){
  const obj = {
  add: a + b,
  subtract: a - b,
  multiply: a * b,
  divide: a / b,
  };
  return obj[operator];
}
```

### Welcome!
```javascript
function greet(language) {
const obj = {
english: 'Welcome',
czech: 'Vitejte',
danish: 'Velkomst',
dutch: 'Welkom',
estonian: 'Tere tulemast',
finnish: 'Tervetuloa',
flemish: 'Welgekomen',
french: 'Bienvenue',
german: 'Willkommen',
irish: 'Failte',
italian: 'Benvenuto',
latvian: 'Gaidits',
lithuanian: 'Laukiamas',
polish: 'Witamy',
spanish: 'Bienvenido',
swedish: 'Valkommen',
welsh: 'Croeso',
};

return obj[language] || obj.english;
}
```

### simple calculator
```javascript
function calculator(a,b,sign){
  if (typeof(a) !== 'number' || typeof(b) !== 'number') return 'unknown value';
  else if (sign !== '+' && sign !== '-' && sign !== '*' && sign !== '/') return "unknown value";
  else {
    switch(sign) {
      case '+': return a + b;
      break;
      case '-': return a - b;
      break;
      case '*': return a * b;
      break;
      case '/': return a / b;
    }
  }
}
```
 ### Get Planet Name By ID
 ```javascript
function getPlanetName(id){
  var name;
  switch(id){
    case 1:
      name = 'Mercury';
      break;
    case 2:
      name = 'Venus';
      break;
    case 3:
      name = 'Earth';
      break;
    case 4:
      name = 'Mars';
      break;
    case 5:
      name = 'Jupiter';
      break;
    case 6:
      name = 'Saturn';
      break;
    case 7:
      name = 'Uranus';
      break;
    case 8:
      name = 'Neptune'
  }
  
  return name;
}
```

### Mumbling
```javascript
function accum(s) {
let s1 = '';
	for (let i = 0; i < s.length; i++) {
      if (i === s.length - 1) {
        s1 += s[i].toUpperCase() + s[i].toLowerCase().repeat(i);
      } else {
        s1 += s[i].toUpperCase() + s[i].toLowerCase().repeat(i) + '-';
      }
    }
  return s1;
}
```

### Vowel Count
```javascript
function getCount(str) {
  let vowelsCount = 0;
  let vowels = 'aeiou';
  for (let i = 0; i < str.length; i++) {
  if (vowels.includes(str[i])) vowelsCount += 1;
  }
  
  
  return vowelsCount;
}
```
 ### Rock Paper Scissors!
 ```javascript
const rps = (p1, p2) => {
  if (p1 === p2) return 'Draw!';
  else if (p1 === 'rock' && p2 === 'scissors') return 'Player 1 won!';
  else if (p1 === 'scissors' && p2 === 'paper') return 'Player 1 won!';
  else if (p1 === 'paper' && p2 === 'rock') return 'Player 1 won!';
  else if (p1 === 'scissors' && p2 === 'rock') return 'Player 2 won!';
  else if (p1 === 'paper' && p2 === 'scissors') return 'Player 2 won!';
  else if (p1 === 'rock' && p2 === 'paper') return 'Player 2 won!';
};
```
 ### The Office I - Outed
 ```javascript
function outed(meet, boss){
let sum = 0;
let count = 0;
  for(let key in meet) {
   if (key === boss) sum = sum + meet[key] + meet[boss];
   else sum = sum + meet[key];
   count += 1;
  }
  return (sum / count <= 5) ? 'Get Out Now!' : 'Nice Work Champ!';
}
```

### Converting Measures
```javascript
function convertRecipe(recipe){
  const arr = recipe.split(' ');
  let full;
  for (let i = 1; i < arr.length; i++) {
    if (arr[i-1].includes('/')) {
      let n = arr[i-1].split('/')[0];
      let m = arr[i-1].split('/')[1];
      full = +n/+m;
    } else full = +arr[i-1];
    if (arr[i] === 'tbsp') {
      arr[i] = arr[i] + ` (${Math.ceil(full * 15)}g)`;
    } else if (arr[i] === 'tsp') {
      arr[i] = arr[i] + ` (${Math.ceil(full * 5)}g)`;
    }
  }
  return arr.join(' ');
}
```

### Convert string to camel case
```javascript
function toCamelCase(str){
let arr = str.split(/[^a-zA-Z]/g);
  for (let i = 1; i < arr.length; i++) {
     arr[i] = arr[i][0].toUpperCase() + arr[i].slice(1);
   }
   return arr.join('');
}
```


### Duck Duck Goose
```javascript
function duckDuckGoose(players, goose) {
  while (players.length < goose) {
  goose = goose - players.length;
  }
  return players[goose - 1].name;
}
```

### Vowel remover
```javascript
function shortcut(string){
let vowels = 'aeiou';
let newStr = '';
  for (let i = 0; i < string.length; i++) {
    if (!(vowels.includes(string[i]))) newStr += string[i];
  }
  return newStr;
}
```
### Check three and two
```javascript
function checkThreeAndTwo(array) {
let count = 0;
for (let i = 0; i < array.length; i++) {
  for (let j = 0; j < array.length; j++) {
    if ((array[i] === array[j]) && i < j) count += 1;
  }
}
if (count === 4) return true;
  else return false;
}
```

### Double Char
```javascript
function doubleChar(str) {
  let newStr = '';
  for (let i = 0; i < str.length; i++) {
    newStr += str[i] +str[i];
  }
  return newStr;
}
```

### Get the Middle Character
```javascript
function getMiddle(s)
{
 for (let i = 0; i < s.length; i++) {
 if (s.length % 2 === 0) return s[s.length/2 - 1] + s[s.length/2];
 else return s[Math.floor(s.length / 2)];
 }
}
```

### Square Every Digit
```javascript
function squareDigits(num){
  let str = num.toString();
  let newStr ='';
  
  for (let i = 0; i < str.length; i++) {
    newStr += Math.pow(str[i], 2);
  }
  return +newStr;
}
```

### Exes and Ohs
```javascript
function XO(str) {
let countX = 0;
let countO = 0;
  for (let i = 0; i < str.length; i++) {
    if (str[i].toLowerCase() === 'x') countX += 1;
    else if (str[i].toLowerCase() === 'o') countO += 1;
  }
  return countX === countO ? true : false;
}
```


### Shortest Word
```javascript
function findShort(s){
const array = s.split(' ');
const newArray = [];

 for (let i = 0; i < array.length; i++) {
   newArray.push(array[i].length);
 }
  newArray.sort(function(a,b) {return a - b;});
  return newArray[0];

}
```

### Friend or Foe?
```javascript
function friend(friends){
  const arr = [];
  for (let i = 0; i < friends.length; i++) {
    if (friends[i].length === 4 && typeof(friends[i]) === 'string') arr.push(friends[i]);
  }
  return arr;
}
```

### Isograms
```javascript
function isIsogram(str){
const arr = str.split('');
  for (let i = 0; i < arr.length; i++) {
   for (let y = 0; y < arr.length; y++) {
     if (arr[i].toLowerCase() === arr[y].toLowerCase() && i !== y) return false;
   }
  }
  return true;
}
```

### Categorize New Member
```javascript
function openOrSenior(data){
const arr = [];
  for (let i = 0; i < data.length; i++) {
    if (data[i][0] >= 55 && data[i][1] > 7) arr.push('Senior');
    else arr.push('Open');
  }
  return arr;
}
```

### Two to One
```javascript
function longest(s1, s2) {
  const arr = (s1 + s2).split('');
  const newArr = arr.sort();
  const array = newArr.filter((el, i) => newArr.indexOf(el) === i);
  
  return array.join('');
}
```

### Jaden Casing Strings
```javascript
String.prototype.toJadenCase = function () {
  const array = this.split(' ');
  for (let i = 0; i < array.length; i++) {
    array[i] = array[i][0].toUpperCase() + array[i].slice(1);
  } 
  return array.join(' ');
};
```

### Will there be enough space?
```javascript
function enough(cap, on, wait) {
  return (cap - (on + wait)) >= 0 ? 0 : Math.abs(cap - (on + wait));
}
```

### Is the string uppercase?
```javascript
String.prototype.isUpperCase = function() {
  for (let i = 0; i < this.length; i++) {
    if (this[i].toUpperCase() !== this[i]) return false;
  }
  return true;
}
```

### Twice as old
```javascript
function twiceAsOld(dadYearsOld, sonYearsOld) {
  if(sonYearsOld * 2 === dadYearsOld) return 0;
  else return Math.abs(dadYearsOld - sonYearsOld * 2);
}
```

### Opposites Attract
```javascript
function lovefunc(flower1, flower2){
  if (flower1 % 2 === 0 && flower2 % 2 === 1) return true;
  else if (flower1 % 2 === 1 && flower2 % 2 === 0) return true;
  else return false;
}
```

### Are You Playing Banjo?
```javascript
function areYouPlayingBanjo(name) {
  if (name[0].toLowerCase() === 'r') return `${name} plays banjo`;
  else return `${name} does not play banjo`;
}
```

### Transportation on vacation
```javascript
function rentalCarCost(d) {
  if (d >= 7) return d * 40 - 50;
  else if(d < 7 && d >= 3) return d * 40 - 20;
  else return d * 40;
}
```

### Training JS #6: Basic data types--Boolean and conditional statements if..else
```javascript
function trueOrFalse(val){
  if (Boolean(val) == true) return 'true';             
  else return 'false';
}
```

### Fix the Bugs (Syntax) - My First Kata
```javascript
function myFirstKata(a,b) {
  if (typeof(a) !== "number" || typeof(b) !== "number") {
    return false;
  } else {
    return a % b + b % a;
  }
}
```

### All Star Code Challenge #22
```javascript
function toTime(seconds) {
  let h = Math.floor(seconds / 3600);
  let min = Math.floor((seconds / 3600 - h) * 60);
  return `${h} hour(s) and ${min} minute(s)`;
}
```

### Exclamation marks series #11: Replace all vowel to exclamation mark in the sentence
```javascript
function replace(s){
  return s.replace(/[aeiouAEIOU]/gi, '!');
}
```





















