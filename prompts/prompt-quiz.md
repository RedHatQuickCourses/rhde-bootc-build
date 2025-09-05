# Initial prompt

Create a JavaScript application that displays an interactive quiz, one question and all its answers at a time, from the provided questions and answers file.

Display each answer with a checkbox, which when clicked displays the explanation for why the answer is either correct or incorrect.

After clicking an answer, change its color to success-green-50 (#63993d) , if it is correct, and to danger-orange-50 (#f0561d), if it is incorrect. Color the explanation the same way. Also change the checkbox to a checked mark for correct (OK) answers, and for a crossed mark, for incorrect (NOT OK) answers.

The questions file follows the format:

---
Q[number]: [question text]

A: [answer text]
Correct: [explanation for correct answer]

A: [answer text]
Incorrect: [explanation for incorrect answer]
---

Explanation text for correct and incorrect answers might include basic HTML formatting and HTML links, which must be preserved.

There can be more than one correct answer. All answers can be correct or incorrect. There can be more than two answers per question.

Do not include any title for the quiz, because it will be used as an iframe in a larger HTML page. Use minimum styling to not interfere with the sorounding web site. Include only the introduction text which preceedes all quesitons on the questions file, and keep that introduction text visible as the quiz navigates to the next question. Color the introduction text with color red-50 (#ee0000).

For each question, include buttons to move to the Next and Previous questions. After the last question, include a button to restart the quiz. The Next question buttons should use color interaction-blue-50 (#0066cc), the Previous question button should use color gray-70 (#383838), and the button to Restart the quiz should use color red-50 (#ee0000).

Use the "Red Hat Display" font famility for all text in the JavaScript application. Do not put any background color nor border around the JavaScript application, so it fits nicely as part of a larger web page.

# Follow-up prompt

The JavaScript application looks nice and works as expected. Change it so there is a line of text, between the introduction text and the question text, which indicates the sequential number of the current questions and the total number of questions, for example: "Question 2 of 4". Color that text as gray-70 (#383838).