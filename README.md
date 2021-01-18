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






