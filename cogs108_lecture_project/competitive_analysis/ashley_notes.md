# Research Notes
## Meta Information
- Topic: COGS108 Lecture Project
- Outline:
  - [X] Competitors
  - [X] Framework
  - [ ] Features

## Notes
### Competitors
- Wayground (formally Quizizz)
  - About
    - Link: https://wayground.com/
    - Purpose: This is a platform intended for teachers; think Kahoot but self-paced. Wayground appears to be made with K-12 in mind.
  - The Good
    - There's a good variety of question types such as multiple choice, math based (e.g. graphing), visual labeling, word clouds, etc.
    - Their site lists "anti-cheating" as a feature, whatever that means. If it relates to physical location, then that'd be good to verify students actually present in class.
    - Integrates with Canvas on the School/District plan.
  - The Meh
    - Gamification: probably can be a good motivator, but may be distracting from the point of the lecture(s).
    - AI features exist to create questions or provide student feedback. While, on paper, this is great- I feel it doesn't incentivize a personal discussion between the class and professor.
  - The Bad
    - Free plan is limited to 100 students (doesn't work for COGS108).
    - Reviews on Trustpilot say their customer support is terrible.
- Poll Everywhere
    - About
      - Link: https://www.polleverywhere.com/
      - Purpose: this is a tool to poll audiences live, specifically built for higher education and corporate in mind. 
  - The Good
    - Attendance is trackable.
    - LMS syncing (Canvas).
    - This has geofencing (checks physical location).
  - The Meh
    - Only has multiple choice and some open-ended word questions for word clouds. Good for what it is, but a bit limiting for what this project wants to achieve.
  - The Bad
    - Free plan is limiting (40 people); $10/mo for 700 people (there are more tiers).

### Framework
(Skipped)

### Features
- General
  - Feature 1: Google OAuth Sign-on
    - Purpose: For authentication and authorization; ideally this keeps students at the institution only participating in lecture
    - Additional info:
      - Not every student will have a `@ucsd.edu` email. However, this is probably a good enough start.
- Student-side
  - Feature 1: joining a class
    - Purpose: this allows a student to participate. On the screen, it would ideally say the name of the class e.g. "COGS 108" to inform the student that they are indeed answering for x class.
    - Additional info:
      - This can probably be simple like a class code to join. It could either be something random like "ABCDEF" or a hackable phrase like "ucsd-sp26-cogs108-a01".
- Professor/TA-side
  - Feature 1: session and question CRUD 
    - Purpose: the instructor(s) can create questions and perhaps even collections of questions for specific lectures. This is the crux of the app.
    - Additional info:
      - We could consider "sessions" akin to creating folders to organize questions e.g. you may have Lecture 1 with 10 questions, Lecture 2 with 4 questions, and so on.
      - Questions should be editable during the session in case a typo or error is noticed. This does not seem like it would be an MVP goal though.
      - The professor/TAs should be able to create a variety of questions e.g. multiple choice, enter a phrase (--> word cloud), or drawing.
      - It may be interesting to have multiple parts to a "live question" too. For example, you could have 2 multiple choice questions, 1 multiple choice and 1 drawing, etc.
  - Feature 2: create a class
    - Purpose: helps instructors keep track of their classes, especially if they teach multiple sections. Additionally, we want to create separate "rooms" such that students in Class A are participating for Class A and are not accidentally connected to Class B.
    - Additional info:
      - See Feature 1 under student side.
  - Feature 3: export participation data and/or participation summary
    - Purpose: if the instructor uses polling for participation grades, then this data will be useful for them to track grading.
    - Additional info:
      - Image data may be difficult.
  - Feature 4: viewing/displaying answers
    - Purpose: this can either be a small select random sample or a few the professor/TA chooses.