> Fast, unopinionated, minimalist web framework for Deno Deploy 🦕

Kyuko is an ultra-light framework for [Deno Deploy](https://deno.com/deploy) scripts.

It aims to provide a similar experience to developing a server with
[express](https://expressjs.com/).

Kyuko (急行) is a word for *express* trains in Japanese railway systems 🚃

# Usage

```ts
const app = new Kyuko();

app.get('/', () => {
  return new Response('Hello World!');
});

app.get('/:name', (req) => {
  return new Response(`Hello ${req.params.name}!`);
});

// json request bodies are loaded into req.requestBody by default
app.post('/', (req) => {
  const { name } = req.requestBody;
  const greetings = `Hello ${name}!`;
  return new Response(greetings);
});

app.listen();
```
