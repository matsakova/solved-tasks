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