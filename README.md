## Checklist

- `rm -r .git`
- `git init`
- package.json
    - name
    - description
    - keywords

## <library name>
[![Build Status](https://travis-ci.org/rafaelkallis/<library name>.svg?branch=master)](https://travis-ci.org/rafaelkallis/<library name>)
[![npm version](https://badge.fury.io/js/<library name>.svg)](https://badge.fury.io/js/<library name>)
[![GitHub version](https://badge.fury.io/gh/rafaelkallis%2F<library name>.svg)](https://badge.fury.io/gh/rafaelkallis%2F<library name>)

<library description>

- Simplest approach possible
- Express-like path parameters
- Custom HTTP methods if needed
- Use with `koa-compose` for seamless modularization
- Typescript definitions included

### Usage

#### Installation

```bash
npm install --save <library package>
# or
yarn add <library name>
```

#### Example 1 (Basic)
```js
const { GET } = require("<library name>");
const Koa = require("koa");

const app = new Koa();

app.use(GET("/foo")(async ctx => {
    ctx.body = "Hello World!";
}));

app.listen(3000);
```