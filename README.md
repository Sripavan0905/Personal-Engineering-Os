# Personal Engineering OS

A zero-build, responsive learning experience for engineering students. Open `index.html` in a browser, or serve this folder locally:

```bash
python3 -m http.server 4173
```

Then visit `http://localhost:4173`.

## Included

- Start-learning and returning-student entry paths
- Theme and four-step text sizing controls
- Local persistence of user profile, course board, course progress, and UI preferences
- Curriculum-driven course discovery - including all 45 programme pathways from the supplied master curriculum - filters, course hierarchy, and cascading progress UI
- Focus timer, ambient selection controls, flashcard, sandbox, project hub, and assessment flow

## Production integration

The demo intentionally uses browser `localStorage`; no user information is sent anywhere. To deploy it, replace the local calls in `app.js` (`loadState`, `saveState`, `handleLogin`, `handleTopic`, and `gradeQuiz`) with authenticated API requests. The data shapes map directly to `Users_Master`, `Course_Progress`, `Login_Logs`, and `Assessment_Scores` from the product brief. Keep Gmail / WhatsApp dispatch server-side so credentials never reach the browser.
