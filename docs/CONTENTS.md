# KahootJS2023! Docs

## Joining Live Games
KahootJS2023! keeps in functionality to join a live game. You'll need to create a [`Kahoot.Client`](#kahootclient) object.
Here's a small script that answers the first question:
```js
let Kahoot = require('kahootjs2023')
let client = new Kahoot.Client();
client.connect(4810269, 'kahootjs2023')
client.on('question', question => {
  if(question.type == 'quiz') {
    if(question.maxAnswers == 1) {
      question.answer(0)
    } else {
      question.answer([0])
    }
});


## API Reference

### Kahoot.Client
