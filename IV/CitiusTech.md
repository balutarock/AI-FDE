
JS: 
1. Closure
2. Event loop
3. promise methods(promiss.all, promise.resolve etc)
4. shallow, deep copy(In background memory level what happen?)
5. Hoising concepts()
6. Scopes

Nodejs: 
1. readFile, write, Stream
2. Middleware
3. 

Coding Questions: provide optimal solution

Find the output:
```
 console.log("A");
 setTimeout(() => { console.log("B"); }, 1000);
 hello().then(() => { console.log("C"); });
 console.log("E");
 async function hello() {
   console.log("D");
   return Promise.resolve();
 }
```
Output: 
```
// A 
// E
// C
// D
// B
```

Find the output 2: 
```
// setTimeout(() => {
//     console.log('T1');
//     process.nextTick(() => console.log('nextTick inside T1'));
// }, 0);
// process.nextTick(() => console.log('N1'));
// Promise.resolve().then(() => console.log('P1'));
// setImmediate(() => console.log('I1'));
```
Outpu: 
```
```

Solve in one loop
1. Combination of target number
```
// Coding Question : 
let target =10 
let data = [0,2,4,6,8,10,1,3,5,7,9]   
// Pair of numbers whose sum is == target. Create an array of pairs.


function sum(arr, target) {
    let res = [];
    let arrSet = new Set();
    for (const i of arr) {
        if (!arrSet.has(i)) {
            arrSet.add(i);
        }
        if (arrSet.has(target - i)) {
            res.push([i, target - i]);
        }
    }
    console.log(res);
}
 
sum(data, target);
```
output: 
```
[[1,9], [4,6]] 
```

2. Palindrom : solve it in optimize 
```
```