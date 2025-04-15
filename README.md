# Lilypad DeepSeek R1 7B

Run [DeepSeek R1 Distill Qwen 7B](https://ollama.com/library/deepseek-r1) on Lilypad Network.

## Getting Started

```sh
export WEB3_PRIVATE_KEY=WEB3_PRIVATE_KEY

lilypad run github.com/Lilypad-Tech/lilypad-deepseek-r1-7b:<COMMIT> \
-i request="$(echo -n '{
  "model": "deepseek-r1:7b",
  "messages": [{
    "role": "system",
    "content": "you are a helpful AI assistant"
  },
  {
  "role": "user",
  "content": "what is the animal order of the frog?"
  }],
  "stream": false,
  "options": {
    "temperature": 1.0
  }
}' | base64 -w 0)"
```
