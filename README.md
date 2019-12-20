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