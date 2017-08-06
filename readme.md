# Dob &middot; [![CircleCI Status](https://img.shields.io/travis/ascoders/dob/master.svg?style=flat)](https://travis-ci.org/ascoders/dob) [![npm version](https://img.shields.io/npm/v/dob.svg?style=flat)](https://www.npmjs.com/package/dob)

Dob is a tool for monitoring object changes. Using [Proxy](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Proxy).

## Examples

There are some [demo](https://jsfiddle.net/1q772uL0/17/) on fiddle. Here's the simplest:

```typescript
import { observable, observe } from "dob"

const obj = observable({ a: 1 })

observe(() => {
    console.log("obj.a has changed to", obj.a)
}) // <· obj.a has changed to 1

obj.a = 2 // <· obj.a has changed to 2
```

You can enjoy the benefits of proxy, for example `obj.a = { b: 5 }` is effective.

## Installation

Dob is available as the `dob` package on [npm](https://www.npmjs.com/package/dob). It is also available on a [CDN](https://unpkg.com/dob@2.2.5/built/bundle.js).

```bash
npm i dob
```

## Apis

You can read [Quick start](./docs/mutable-quick-start.md) first, then read them:

- [observable, observe](./docs/observable.md)
- [unobserbe](./docs/unobserve.md)
- [Action](./docs/action.md)

## Combination

### Combining dynamic-react

[Quick start](./docs/dynamic-react.md)

Here is a basic [demo](https://jsfiddle.net/yp90Lep9/20/), and here is a [demo](https://jsfiddle.net/g19ehhgu/9/) with fractal.

### Combining dependency-inject

Here is a basic [demo](https://jsfiddle.net/bmea0pat/21/), and here is a [demo](https://jsfiddle.net/ppt3ztx7/3/) with fractal and dependency-inject.

### Combining react-redux

Here is a basic [demo](https://jsfiddle.net/56saqqvw/7/)

- [createReduxStore](./docs/createReduxStore.md)
- [task](./docs/task.md)

You can clone this project, and run `npm start` to see [redux todoMVC demo](./src/demo/todo-mvc).

## Inspired

- [mobx](https://github.com/mobxjs/mobx)
- [nx-js](https://github.com/nx-js/observer-util)
