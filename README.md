# portfolio-generator

## Introduction

 You'll be creating a generator that dynamically produces a high-quality README file directly from the command line.

## Acceptance Criteria

In order to succeed in this Challenge, you’ll apply the following skills:

Modularize your code into multiple files

Write your code using ES6+ concepts, such as let, const, and arrow functions

Use npm (Node Package Manager) to initialize a project and install and import Node.js modules

Build an interactive command-line application that processes user input using a third-party Node.js module

Use string literals to dynamically generate markdown from the command line

## Comprehensive Flow of Project Coding Development

1) We start by asking the user for their information with Inquirer prompts; this returns all of the data as an object in a Promise.

2) The promptProject() function captures the returning data from promptUser() and we recursively call promptProject() for as many projects as the user wants to add. Each project will be pushed into a projects array in the collection of portfolio information, and when we're done, the final set of data is returned to the next .then().

3) The finished portfolio data object is returned as portfolioData and sent into the generatePage() function, which will return the finished HTML template code into pageHTML.

4) We pass pageHTML into the newly created writeFile() function, which returns a Promise. This is why we use return here, so the Promise is returned into the next .then() method.

5) Upon a successful file creation, we take the writeFileResponse object provided by the writeFile() function's resolve() execution to log it, and then we return copyFile().

6) The Promise returned by copyFile() then lets us know if the CSS file was copied correctly, and if so, we're all done!