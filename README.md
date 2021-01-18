![front and back](https://content.codecademy.com/courses/server-side-web-dev/FrontEndCut_v1.mp4)

![The Web Server](https://content.codecademy.com/courses/updated_images/NodeBackEndFrontEnd_Update_1.gif)

![So What is the Back-end?](https://content.codecademy.com/courses/updated_images/Node_3_v2_text_Updated_1.svg)

![Storing Data](https://content.codecademy.com/courses/updated_images/Node_4_v4_Updated_1.svg)

![What is an API?](https://content.codecademy.com/courses/updated_images/Node_5v2__Updated_1.gif)

![Authorization and Authentication](https://content.codecademy.com/courses/server-side-web-dev/NodeAnimation_6.gif)

![Different Back-end Stacks](https://content.codecademy.com/courses/updated_images/Coders-2_Updated_1.gif)

# Running a Program with Node


`let noun1 = 'mike';`
`let adjective = 'silly';`
`let noun2 = 'owino';`
`let verb = 'sing';`
`let noun3 = 'okumu';`


`console.log(`The world's first ${noun1} was a very ${adjective} ${noun2} who loved to ${verb} while eating ${noun3} for every meal.`);`

### _RUN_ `node app.js`
### **OUTPUT** ![](https://github.com/MikeOwino/nodejs/blob/main/Screenshot%202021-01-18%20173921.jpg)

# Accessing the Process Object


`let initialMemory = process.memoryUsage().heapUsed;`
`let word = process.argv[2];`

`console.log(`Your word is ${word}`)`

`// Create a new array`
`let wordArray = [];`

`// Loop 1000 times, pushing into the array each time `
`for (let i = 0; i < 1000; i++){`
  `wordArray.push(`${word} count: ${i}`)`
`}`

`console.log(`Starting memory usage: ${initialMemory}. \nCurrent memory usage: ${process.memoryUsage().heapUsed}. \nAfter using the loop to add elements to the array, the process is using ${process.memoryUsage().heapUsed - initialMemory} more bytes of memory.`)`

### _OUTPUT_ ![](https://github.com/MikeOwino/nodejs/blob/main/Screenshot%202021-01-18%20174349.jpg)

# Core Modules and Local Modules

`let initialMemory = process.memoryUsage().heapUsed;`
`let word = process.argv[2];`

`console.log(`Your word is ${word}`)`

`// Create a new array`
`let wordArray = [];`

`// Loop 1000 times, pushing into the array each time `
`for (let i = 0; i < 1000; i++){`
  `wordArray.push(`${word} count: ${i}`)`
`}`

`console.log(`Starting memory usage: ${initialMemory}. \nCurrent memory usage: ${process.memoryUsage().heapUsed}. \nAfter using the loop to add elements to the array, the process is using ${process.memoryUsage().heapUsed - initialMemory} more bytes of memory.`)`


# Event-Driven Architecture
`// Here we require in the 'events' module and save a reference to it in an events variable`
`let events = require('events');`

`let listenerCallback = (data) => {`
    `console.log(`Celebrate ${data}`);`
`}`

`// Here we create an instance of the EventEmitter class`
`let myEmitter = new events.EventEmitter();`

`// Here we subscribe to 'celebration' events and provide a callback function which will be passed the event's data`
`myEmitter.on('celebration', listenerCallback);`

`// Here we emit an event, we pass the event type, 'celebration', as the first argument, and the event data as the second`
`myEmitter.emit('celebration', 'good times, come on!');`

# Asynchronous JavaScript with Node.js
![](https://content.codecademy.com/courses/updated_images/EventLoop_Update_1.gif)


# User Input/Output
`let {testNumber} = require('./game.js');`

`process.stdout.write("I'm thinking of a number from 1 through 10. What do you think it is? \n(Write \"quit\" to give up.)\n\nIs the number ... ");`

`let playGame = (userInput) => {`
  `let input = userInput.toString().trim();`
	`testNumber(input);`
`};`

`process.stdin.on('data', playGame);`

# Errors

`const api = require('./api.js');`

`// Not an error-first callback`
`let callbackFunc = (data) => {`
   `console.log(`Something went right. Data: ${data}\n`);`
`};`
  
`try {`
  `api.naiveErrorProneAsyncFunction('problematic input', callbackFunc);`
`} catch(err) {`
  `console.log(`Something went wrong. ${err}\n`);`
`}`


# Filesystem
`const fs = require('fs');`

`let secretWord = null;`

`let readDataCallback = (err, data) => {`
  `if (err) {`
    `console.log(`Something went wrong: ${err}`);`
  `} else {`
    `console.log(`Provided file contained: ${data}`);`
  `}`
`};`

`//fs.readFile('./fileOne.txt', 'utf-8', readDataCallback);`
`//fs.readFile('./anotherFile.txt', 'utf-8', readDataCallback);`
`fs.readFile('./finalFile.txt', 'utf-8', readDataCallback);`

`secretWord = "cheeseburgerpizzabagels"`

# Readable Streams
`const readline = require('readline');`
`const fs = require('fs');`

`let settings = {`
  `input: fs.createReadStream('shoppingList.txt')`
`};`

`const myInterface = readline.createInterface(settings);`

`const printData = (data) => {`
  `console.log(`Item: ${data}`);`
`};`

`myInterface.on('line', printData);`

