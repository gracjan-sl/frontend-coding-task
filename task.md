# Front-end coding task
Welcome to Sauce Labs front-end coding task.

![Jigsaw](https://i.pinimg.com/474x/5b/a8/3d/5ba83d0d5c438ae9a081631541ffe4f1.jpg)

## The task
We're asking you to create a quiz game in the form of a browser application.
The goal of the game is to gather as many points as possible before making 3 mistakes.
The player answers questions one by one, gettings points and losing chances until they're out of chances.

The API is available at `GET https://eok9ha49itquif.m.pipedream.net` and returns questions in the following format:
```json
{
  "questions": [
    {
      "answerSha1": "5c8452354c261b52e6dcf7f94b80ea5a7bceb677",
      "question": "What do people mean when type the letters 'SMH' in a message on the internet?"
    },
    {
      "answerSha1": "088e4a2e6f0c20048cd3e53c639c7092bffb8524",
      "question": "Which country's flag can be described as 'Green with a vertical white band on the left side. The green section contains a white crescent and star.'?"
    },
    {
      "answerSha1": "b79445b10bd5bc34cbebf63355101dbdb420aa0e",
      "question": "Which director directed Gangs of New York?"
    }
    {
      "answerSha1": "fd26fb6ff5aa10eaddad0b2c832139dbe052c9d7",
      "question": "Which philosopher famously said 'This is patently absurd; but whoever wishes to become a philosopher must learn not to be frightened by absurdities'?"
    },
    {
      "answerSha1": "e8002c169040af08d8b4ed2f0d636b840f335f9b",
      "question": "What is Xylology the study of?"
    }
  ]
}
```

You can find specific acceptance criteria below.

### Acceptance Criteria
1. On the main screen of the game, a single question is displayed, followed by a text input to enter the answer, and a button. On the side, the player can see their current score and chances left.
1. No question may repeat within a single game.
1. The API returns questions in batches of 5. The total pool of question is much bigger. For each call, a random subset of questions is returned.
    1. Questions fetched from the API may contain duplicates. It's up to you to filter them out.
    1. The API returns a JSON array of objects, each of which has a plaintext `question` and expected `answerSha1`, hashed with SHA1.
    1. All answers were lowercased before hashing. You'll have to do the same in order to verify answers.
1. The button triggers answer verification.
    1. After successful verification, the player gets one point and next question is displayed.
    1. After a wrong answer, one chance is deducted and:
        1. if the player has any chances left, the next question is displayed,
        1. otherwise, a final screen is displayed, showing the number gathered points and showing a button that starts a new game.
1. The application runs in newest versions of modern browsers (Firefox, Chrome, Safari).
1. No console errors or warnings.
1. Day & night mode, toggled via a button click.
1. Critical parts of the application should be unit tested.
1. Include a `README.md` file, explaining how to run the app in a browser.
1. Production build is not necessary.
1. The visual design of the application doesn't have to be exquisite, but it should not upset the eye. Simple and clean is what we're looking for.

## Ground rules
1. The solution can be coded in Javascript or TypeScript. Your choice. Styling should be done in raw CSS.
1. Put the code on your GitHub account or send it to the recruiter in an archive file.
1. You don't need to add any extra features or improvements not listed in the Acceptance Criteria. There are no bonus points for it.
1. You can use React or an alternative library if it makes your job easier (but you don't have to).
1. You can use other external libraries to speed up your work.
1. You can use a styling framework (Material UI, Bootstrap, or other) for quick and consistent styling.
1. If you're not able to implement all parts of the task, partial submissions are welcome.

## Tips
1. You can use a cookie cutter utility like [Create React App](https://create-react-app.dev/) to quickly set up the application.
1. Simplicity is highly valued in this exercise.
