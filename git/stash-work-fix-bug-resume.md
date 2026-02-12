# Stash Work Fix Bug Resume

> **Company:** Kraken | **Difficulty:** Medium

---

#### **Scenario**

You have a Git repository at `/home/interview/repo` where you are working on a new feature on the `feature-login` branch with uncommitted changes in `login.js`. A fix is needed on the `dev` branch: `app.js` contains a JavaScript syntax error that can be identified by running `node app.js`.

#### **Task**

Stash your current changes to clean the working directory, switch to the `dev` branch, fix the syntax error in `app.js`, commit the fix using the commit message `Fix syntax error in app.js`, then return to your `feature-login` branch, merge the fix from `dev`, and restore your stashed work.
