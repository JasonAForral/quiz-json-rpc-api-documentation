### quiz-json-rpc-api-documentation

#### Request quizzes available:

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "getQuizzes"
}
```

#### Response from server:

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "result": {
    "quizzes": [
      {
        "id": 1,
        "text": "State Capitals"
      },
      {
        "id": 2,
        "text": "Atomic Numbers"
      }
    ]
  }
}
```

#### Request new question:

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "getQuestion",
  "params": {
    "quizId": 1
  }
}
```

#### Response from server:

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "result": {
    "answers": [
      {
        "id": 1,
        "text": "A type of dog."
      },
      {
        "id": 2,
        "text": "Something you wear on your head."
      },
      {
        "id": 3,
        "text": "Something you eat."
      },
      {
        "id": 4,
        "text": "A type of tree."
      }
    ],
    "question": {
      "id": 1,
      "text": "What is a hat?"
    }
  }
}
```

#### Request answer question:

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "method": "answerQuestion",
  "params": {
    "guessId": 1,
    "questionId": 1
  }
}
```

#### Response answer question:

```json
{
  "id": 1,
  "jsonrpc": "2.0",
  "result": {
    "correctId": 2
  }
}
```