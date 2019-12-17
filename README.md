# solved-tasks
### The wheat/rice and chessboard problem
```javascript
function squaresNeeded(grains){
if (grains === 0) return 0;
else return Math.floor(Math.log(grains) / Math.log(2) + 1);
}
```

### Sum of the first nth term of Series
```javascript
function SeriesSum(n)
{
   let sum = 0;
  for(i = 0; i < n; i++){
    sum += (1/(1 + i * 3));
  }
  return sum.toFixed(2);
}
```

### Power
```javascript
function numberToPower(number, power){
 let m = 1;
 for (let i = 0; i < power; i++) {
 m *= number;
 }
 return m;
}
```
