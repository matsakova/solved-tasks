# solved-tasks
### Powers of 2
```javascript
function powersOfTwo(n){
let arr = [];
  for (let i = 0; i <= n; i++) {
  arr.push(Math.pow(2, i));
  }
  return arr;
}
```

### Power of two
```javascript
function isPowerOfTwo(n){
  return Math.log(n / 2)/Math.log(2) % 1 === 0;
}
```

### Odd or Even?
```javascript
function oddOrEven(array) {
   if (!array.length) return "even";
   let sum = 0;
   for (let i = 0; i < array.length; i++) {
   sum += array[i];
   }
   return sum % 2 === 0 ? "even" : "odd";
}
```