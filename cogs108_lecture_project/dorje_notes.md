# Research Notes

# Competitors

## Top Hat

https://tophat.com/

**Purpose:** Top Hat is a "classroom response and student engagement platform" built mainly for higher education. Teachers can ask live questions, run discussions, track attendance, present lecture content, and review student responses in real time.

### The Good

Top Hat is probably one of the closest competitors because it is built specifically around in-class participation rather than just quizzes or polls.

It supports many question types:
- multiple choice 
- numeric answers 
- word answers
- long answers
- matching 
- sorting
- click-on-target
- discussion-style responses.

Most importantly for this project, Top Hat appears to support **drawing responses** in discussion questions. Students can use a drawing canvas in the Top Hat mobile app and submit that drawing as a reply.

Top Hat also has attendance tracking, including location-related attendance features on phones, which could be useful(?)

It integrates with Canvas for roster and grade syncing, which is useful if participation needs to connect back to the course LMS.

### The Meh

Top Hat may be more “institutional” than what this project needs. It does a lot: 
- lectures
- textbooks
- attendance
- gradebook syncing
- AI tools
- student engagement

That makes it powerful, but probably too heavy than what Prof is looking for. It also seems more structured around formal course participation than spontaneous classroom discussion.

### The Bad

**Pricing!!!** Top Hat lists student purchase options, which is kind of out of the question I think.

Another downside is that the drawing feature seems attached to discussion-style responses.



## Nearpod

**Link:** https://nearpod.com/

**Purpose:** Nearpod is "an interactive lesson platform where teachers can create live or self-paced lessons with activities, quizzes, polls, collaborative boards, open-ended questions, and drawing activities." Its used more heavily in K-12, but the interaction model is relevant.

### The Good

The teacher controls the lesson, students join on their own devices, and responses can be reviewed during or after the session.

The most relevant feature is that Nearpod supports drawing activities. 

Teachers can add:
- quizzes
- drawing
- open-ended questions
- polls
- collaborative boards

Nearpod also really seems to emphasize real-time insights into student understanding, which fits the professor’s goal of asking a question, collecting answers, and reviewing them with the class.

Nearpod supports Google Classroom integration and lets teachers assign lessons and review lesson results through that workflow. That is not Canvas, but it shows that LMS-style integration is part of the product direction.

### The Meh

Nearpod is more of a lesson delivery platform than a simple classroom response app. The professor would likely need to build the activity into a Nearpod lesson rather than just quickly ask a spontaneous question.

It also feels more K-12 oriented than college lecture oriented. That does not make it bad, but for COGS108, the tone might be off.

### The Bad

Nearpod also feels too heavy. If the professor just wants to ask, “Draw a bike,” collect drawings, and discuss them, Nearpod could feel like using a whole lesson platform for one simple interaction.


# Features

## General

### Feature 1: Google OAuth Sign-on

**Purpose:** Authentication and authorization. Ideally, this limits participation to students from the institution.

**Additional info:** Not every student may have a `@ucsd.edu` email, but Google sign-in is probably a good starting point. If 1% or less of the class has this issue, probably not a big concern. Later, the app could support professor-created invite links or class codes if it comes up.


### Feature 2: Join Code / Session Link

**Purpose:** Students need a fast way to join the correct lecture session.

**Additional info:** This could work like Kahoot or Top Hat: professor starts a session, students enter a short code, and then they can answer active questions.



### Feature 3: Anonymous vs. Named Mode

**Purpose:** Some questions work better when students are anonymous. Others require names for participation credit.

**Additional info:** The professor could choose per question or per session:

- Anonymous responses
- Visible to professor only
- Fully named responses
- Names hidden during projection

This matters because students may draw or answer more honestly if they are not immediately exposed to the whole room.



## Student-side

### Feature 1: Drawing Response

**Purpose:** Students can draw an answer directly on their phone, tablet, or laptop.

**Additional info:** Should probably be a core features since the professor specifically asked for it.

- Pencil
- Eraser
- Clear canvas
- Undo
- Submit button

Later features could include colors, shapes, image upload, or professor-provided backgrounds.



### Feature 2: Confidence Rating

**Purpose:** Students can answer with a numeric or visual confidence level before and/or after drawing. (might be funny to see if their confidence wavers after drawing lol)

**Additional info:** For the bike example, the professor might ask:

> “How confident are you that you can draw a bike accurately?”

Then students could answer:

- 1 to 5 scale
- Slider
- Multiple choice

Then they draw the bike and the professor can see the visuals as well as their confidence answer. Then they can be displayed to the class.



### Feature 3: Text Response

**Purpose:** Students can answer open-ended questions in words.

**Additional info:** This should be included because not every classroom prompt needs a drawing. It also gives the app more flexibility for general lecture use.



### Feature 4: Mobile-Friendly Interface

**Purpose:** Students should be able to answer quickly from their phones without downloading an app.

**Additional info:** This is important. Requiring app downloads would create friction, especially for one-off use in a lecture.


## Professor / TA-side

### Feature 1: Session and Question CRUD

**Purpose:** The instructor can create, edit, delete, and organize questions.

**Additional info:** Sessions could work like folders:

- Lecture 1
- Lecture 2
- Midterm Review
- Perception Activity
- Drawing Exercise

Each session could contain multiple questions.

For MVP, editing questions during a live session might be optional. But eventually it would be useful in case the professor notices a typo.


### Feature 2: Create a Class

**Purpose:** Helps instructors keep track of different classes or sections.

**Additional info:** This prevents students from joining the wrong room. For example:

- COGS108 Section A
- COGS108 Section B
- COGS108 Discussion 1

This also makes participation tracking cleaner.



### Feature 3: Live Response Dashboard

**Purpose:** The professor can view incoming answers in real time.

**Additional info:** For drawings, this could be a gallery/grid view. For confidence ratings, this could be a chart or average score. For text answers, this could be a list or word cloud.

This is one of the most important professor-side features.



### Feature 4: Select Answers to Display

**Purpose:** The professor can choose specific student answers to show on the projector or on student devices.

**Additional info:** This is key for classroom discussion. The professor may not want to show every response. They may want to select:

- A strong example
- A funny example
- A common misconception
- Two contrasting answers
- A drawing that reveals an interesting assumption

This feature could make the app feel much more discussion-driven than typical polling tools.


### Feature 6: Export Participation Data

**Purpose:** If the professor uses this for participation grades, they need records.

**Additional info:** Export options could include:

- CSV of students who participated
- Question-by-question response status
- Confidence ratings
- Text answers
- Links or filenames for drawings

Image data may be harder, but maybe the school database could store that info.