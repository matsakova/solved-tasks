# solved-tasks
### Factorial
```javascript
function factorial(n){
  let i = 1;
  let a = 1;
  
  while(i <= n) {
    a *= i;
    i++;
  }
  return a;
}
```
### No zeros for heros
```javascript
function noBoringZeros(n) {
  while (n % 10 === 0 && n !==  0) {
  n /= 10;
  }
  return n;
}
```
### Difference Of Squares
```javascript
function differenceOfSquares(n){
let a = 0;
let b = 0;


  for (let i = 0; i <= n; i++) {
  a += i;
  b += Math.pow(i, 2);
  }
  return Math.pow(a, 2) - b;
}
```