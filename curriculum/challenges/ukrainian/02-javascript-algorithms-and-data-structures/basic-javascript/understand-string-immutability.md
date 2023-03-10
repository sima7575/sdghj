---
id: 56533eb9ac21ba0edf2244ba
title: Розуміння нестійкості рядка
challengeType: 1
videoUrl: 'https://scrimba.com/c/cWPVaUR'
forumTopicId: 18331
dashedName: understand-string-immutability
---

# --description--

У JavaScript, `String` значення <dfn>immutable</dfn>, означає, що їх не можна буде змінити після створення.

For example, the following code will produce an error because the letter `B` in the string `Bob` cannot be changed to the letter `J`:

```js
let myStr = "Bob";
myStr[0] = "J";
```

Note that this does *not* mean that `myStr` could not be re-assigned. The only way to change `myStr` would be to assign it with a new value, like this:

```js
let myStr = "Bob";
myStr = "Job";
```

# --instructions--

Виправте призначення `myStr` так, щоб код містив рядок зі значенням `Hello World`, використовуючи підхід, показаний вище.

# --hints--

`myStr` має мати значення рядка `Hello World`.

```js
assert(myStr === 'Hello World');
```

Не слід змінювати код над зазначеним коментарем.

```js
assert(/myStr = "Jello World"/.test(code));
```

# --seed--

## --after-user-code--

```js
(function(v){return "myStr = " + v;})(myStr);
```

## --seed-contents--

```js
// Setup
let myStr = "Jello World";

// Only change code below this line
myStr[0] = "H"; // Change this line
// Only change code above this line
```

# --solutions--

```js
let myStr = "Jello World";
myStr = "Hello World";
```
