# Quiz App Demo

## What is this?

This demo showcases the framework for a quiz app, showing off how a quiz would work with the given code. The user presses the start button and begins answering some questions, while being told after they've selected an answer if it is right or wrong. The user is then given a final score and the option to take the quiz again.

## How does it work?

This demo has a lot of functional features, including:

- A button that awaits user input to start the quiz
- An interactive display for each question
  - A variety of answers for each question with visual indicators that let the user know if they selected the correct one
  - A timer that counts down to zero, shutting off all user interaction with the answers after this occurs. This timer also stops once a user selects an answer
  - A counter letting the user know how many questions they've answered as well as the total amount of questions
  - Another button allowing the user to continue to the next question
- A quiz completion screen that gives the user multiple options, either to replay the quiz or go back to the starting page

## Is it structurally sound?

Yes! All the files are correctly linked to each other in a way that should cause no issues with any download. 

The CSS and JS files are all linked to index.html in the head section, and the JS files work off of each other while placing content into "index.html". The file "questions.js" is indexed multiple times in the file "quizApp.js", and "quizApp.js" dynamically places content into "index.html" by way of div, span, and p tags.

## What do the different files do?

Going in a logical order, we'll start with questions.js:

questions.js creates an array of objects called "questions", which has all the info in it relating to the content displayed, such as the question number, the answer options, the correct answer, and the question itself.

quizApp.js:
- quizApp.js starts by declaring all the necessary variables from index.html it needs to use in itself. 
- It then moves to declaring local variables and setting up functionality for non-question-related buttons.
- The file also imports the questions and potential answers from the array in questions.js and adds them to the empty div in index.html.
- Next, it checks if the user got the question right or wrong and updates the page accordingly.
- This file also dictates what content should be on the results page depending on the user did.
- Finally, quizApp.js adds the timer functionality to the program.

style.css adds all the necessary styling content to make the program more visually appealing and readable than it would be without any CSS styling.

index.html is the foundation for this app, creating all the static content needed for the webpage. It contains the initial page with the start button, the rules page before the quiz begins, and the buttons and other elements on the results page. It also contains multiple empty classes that are eventually filled with content from quizApp.js.