```Example Formate
### Event bubbling
#### Definition
#### Diagram
#### Example
##### Output:
```

### Event loop
#### Definition
The Event Loop is a mechanism that continuously monitors the Call Stack and task queues. When the Call Stack becomes empty, it first executes all tasks from the Microtask Queue and then executes tasks from the Macrotask Queue, enabling asynchronous behavior in JavaScript.
#### Diagram
```
          JavaScript Engine
                |
          +------------+
          | Call Stack |
          +------------+
                ^
                |
          Event Loop
                |
      +------------------+
      | Microtask Queue  |  ← Promises
      +------------------+
                |
      +------------------+
      | Macrotask Queue  |  ← setTimeout, Events
      +------------------+
                ^
                |
         Browser / Node APIs
```
#### Example
```
console.log("1");

setTimeout(() => console.log("2"), 0);

Promise.resolve().then(() => console.log("3"));

queueMicrotask(() => console.log("4"));

console.log("5");
```
##### Output:
```
1
5
3
4
2
```

### Event bubbling
#### Definition
#### Diagram
#### Example
##### Output: