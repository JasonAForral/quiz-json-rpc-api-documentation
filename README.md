### quiz-json-rpc-api-documentation

#### Request new question:

```json
{
  "jsonrpc": "2.0",
  "method": "getQuestion",
  "id": 1
}
```

#### Response from server:

```json
{
  "json": "2.0",
  "result": {
    "question": {
      "id": 1,
      "text": "What is a hat?"
    },
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
    ]
  },
  "id": 1
}
```

#### Request answer question:

```json
{
  "jsonrpc": "2.0",
  "method": "answerQuestion",
  "params": {
    "questionId": 1,
    "answerId": 1
  },
  "id": 1
}
```

#### Response answer question:

```json
{
  "jsonrpc": "2.0",
  "result": {
    "correct": false,
    "answerId": 2
  },
  "id": 1
}
```