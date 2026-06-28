# Pages

There will be three categories of pages. Universal refers to pages that exist for both instructors and students. Student view refers to pages that only students will see. Innstructor view refers to pages that only instructors will see.

## Universal 
- Home / login page: this is a pretty simple page with the app name and something like "Sign-in with Google."
- App settings page: the user can configure things like change the theme, accessibility settings, view app information (e.g. "Hi, we're open source" or app version information), etc.


## Student View
Once logged in, the student will be greeted by their **home / "Your Classes" screen**. Imagine this like Canvas's home screen. There should be a button that says "add a class" where it will prompt the student to enter in a class code shared by the instructor.

When a user clicks on a class, there should be three pages:
- Answering area: a page that listens and waits for live questions to be sent out from the instructor. If there is no question live, the app will say so. On the other hand, when there is a question live, then the student will have their multiple choice options and perhaps even the question reiterated on the screen (screen size permitting). The student should be able to change their answer until the instructor locks the question.
- Your gradebook: a page to check how many questions the student has answered (perhaps broken down by day and/or week in a table-like format).
- Class settings: a page where the student can modify information like adding a student ID or removing the class from their class list (this should bring up an "Are you sure?" prompt).


## Instructor View
Once logged in, the instructor will be at their **home / "Your Classes" screen**, where it lists the classes they currently are in charge or a part of. This should have a "create a class" button.

When an instructor clicks on a class, there should be _ pages:
- Questions: this is a page where there are tabs sectioned off like the `<details>/<summary>` tags in HTML. For example, an instructor may be interested in breaking down their questions by day, so there may be a tab for `July 28 2026` or `July 30 2026`, etc. Here, the instructor can create/edit tabs, create/edit questions, etc. 
  - Editing questions should be its own page. Note that when editing, changes should only be made upon "Save and Apply Changes."
- Live session: this is the page where the instructor can start polling questions. First, the page should have the status like "A question is live" or "There is no question live" as an informative measure.
  - If there is nothing live, then the instructor can select one of the question tabs they have created to use for the day. Once selected, the instructor can preview the questions and answers (and maybe even edit if necessary), start a session, or even skip to another question, which they can preview.
    - If answers *have* been received, then the instructor can open the histogram in a new tab to share with the class for discussion sake. Note that this can't happen until all answers are received. The idea behind this is to prevent instructors from sharing results live and influencing student results based off what other students vote.
  - If there is a question live, the instructor can see answers come in live with some basic information like an answer distribution histogram (for the sake of our MVP, we're starting multiple choice) and the percentage of connected students that have answered e.g. 65% of connected students have answered. The instructor can also stop incoming answers.
- Class settings: this is an area where they can:
  - Change the class name
  - View the class join code to share with students
  - View the student roster and their participation stats
  - Export student participation data for gradebook usage
  - Import/export question sets 

