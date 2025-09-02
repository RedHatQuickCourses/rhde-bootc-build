# How to Create Interactive Quizes with Google Gemini

This `prompts` folder is outside of the Antora doc tree (the `modules` folder) on purpose. There's no need to the `antora*yaml`, `package.json`, nor GitHub actions. After you generate your interactive quiz with Gemini, it's just a static HTML file which you commit as part of your Antora documentation site, as an attachment file.

We keep this folder so you can reproduce, or re-generate, the interactive quizzes, to fix bugs, grammar mistakes, or when you need to update a quick course to a new product version.

* If you already have your quiz text, copy it to a markdown file with minimal formatting, and follow the template for questions and answers outlined in the `prompt-quiz.md` file.

* Remember to change any web links and other AsciiDoc or MarkDown formatting on your questions and answer file to use simple HTML tagging. Also, remember you CANNOT use Antora xref for images.

* Of course, you can use Gemini or any other LLM to generate questions from your content, but here we start with the assumption that you already wrote (or generated) and reviewed your questions, answers, and also already reviewed the feedback for correct and incorrect answers.

* Open Google Gemini and select "Canvas". Also select the "Pro" model for better results.

* Upload your questions file, and paste the contents of the prompt file to gemini. There is no need to tell it to keep the questions and answers as a JavaScript variable, for ease of maintenance. It will do that.

* Wait while Gemini "thinks"

* Test the quiz on the canvas preview, make sure it works as expected, the answers match each question, and each answer displays the correct feedback text.

* If all is fine, click the "Share" button to copy the contexts of the JavaScript application.

* Paste the contents of the quiz in a new HTML file, for example `s2-quiz.html` on the `attachments` directory of your chapter (which should be a sibbling of your `pages` directory).

* Create a passthrough HTML block on the place you want to display the interactive quiz. Remember to include titles, instructions, and other boilerplate text outside of the HTML block and its JavaScript application. You CANNOT use Antora xref: processing to generate the URL, but you can use a relative path to the `_attachments` directory of the same chapter which containers you page.

````
<iframe type="text/javascript" src='_attachments/s2-quiz.html' style="width: 768px; height: 532px" allowfullscreen webkitallowfullscreen mozAllowFullScreen allow="autoplay *; fullscreen *; encrypted-media *" frameborder="0"></iframe>
````

* You may have to tweak the iframe above, for example to make it larger or taller.

* Test the quiz on the local preview of your Antora course.

* Commit all files in the `prompts`, `attachments`, and `pages` directory and push them to GitHub.

* Test again that the quiz works well from your live Antora documentation site (or its preview in a PR).

* If you include an estimated reading time, sum the times of the .adoc file and the questions.md file. This does NOT take into account the time to click on answers and click "Next" to move to the next question, not the time to think about a question and its answers, but it is the best estimage we can do for now.

* If you had to add some tweaks to the prompt, or continue the conversation to tweak the generated JavaScript code, record all your prompts and messages (not answers, only your input to Gemini) in this `prompts` directory, and save it on your quick course project in GitHub.

* Review the Red Hat Brand portal https://www.redhat.com/en/about/brand/standards if you need to tweak the output to better align with the Red Hat brand.

* Do not be afraid of starting a new Gemini chat and discart the previous attempt. It creates small variations of layout for each run. Maybe a longer prompt could bring more consistency, but I'm happy with the results so far.