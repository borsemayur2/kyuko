> Fast, unopinionated, minimalist web framework for Deno Deploy 🦕

Kyuko is an ultra-light framework for API servers hosted on [Deno Deploy](https://deno.com/deploy).

It aims to provide a similar experience to developing API servers with [Express](https://expressjs.com/).

Latest deno doc available [here](https://doc.deno.land/https/deno.land/x/kyuko/mod.ts)

# Hello World

Deployed at https://kyuko.deno.dev

```ts
import { Kyuko } from 'https://deno.land/x/kyuko@v0.1.0';

const app = new Kyuko();

app.get('/', (req, res) => {
  res.send('Hello World!');
});

app.get('/:name', (req, res) => {
  res.send(`Hello ${req.params.name}!`);
});

app.listen();

```

# Usage

To run your Kyuko app locally using `deployctl`

```sh
deployctl run --libs="" your_kyuko_app.ts
```
