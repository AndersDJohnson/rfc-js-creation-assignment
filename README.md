# rfc-js-creation-assignment
A proposal for JS assignment to objects on creation.

A terse, declarative syntax to annotate objects/arrays/functions with an additional property on creation.

Could be useful within large configuration objects, not having to break up into multiple statements, just to add additional flags to tell a helper to treat an array or function differently than usual.

```js
const options = [
  'thing',
  2
].also = true

const options2 = {
  some: 'thing',
  plus: 2
}.also = true
```

equivalent to:

```js
const options = [
  'thing',
  2
]

options.also = true

const options2 = {
  some: 'thing',
  plus: 2,
  also: true
}
```

or:

```js
const options = [
  'thing',
  2
]

options.also = true

const options2 = {
  some: 'thing',
  plus: 2
}

options2.also = true
```
