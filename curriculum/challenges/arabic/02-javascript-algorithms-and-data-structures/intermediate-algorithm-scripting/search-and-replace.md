---
id: a0b5010f579e69b815e7c5d6
title: البحث والاستبدال
challengeType: 1
forumTopicId: 16045
dashedName: search-and-replace
---

# --description--

قم بإجراء بحث واستبدال علي الجملة باستخدام الوسيطات المقدمة و ارجع الجملة الجديدة.

الوسيطة الأولى هي الجملة التي سيجري البحث والاستبدال عليها.

الوسيطة الثانية هي الكلمة التي سيتم استبدالها.

أما الوسيطة الثالثة فهي ما ستحل محل الوسيطة الثانية.

**ملاحظة:** احتفظ بحالة الحرف الأول في الكلمة الأصلية عند استبدالها. على سبيل المثال إذا كنت تقصد استبدال كلمة `Book` بكلمة `dog`، ينبغي استبدالها كـ `Dog`

# --hints--

`myReplace("Let us go to the store", "store", "mall")` يجب أن يعيد السلسلة النصية `Let us go to the mall`.

```js
assert.deepEqual(
  myReplace('Let us go to the store', 'store', 'mall'),
  'Let us go to the mall'
);
```

`myReplace("He is Sleeping on the couch", "Sleeping", "sitting")` يجب أن يعيد السلسلة النصية `He is Sitting on the couch`.

```js
assert.deepEqual(
  myReplace('He is Sleeping on the couch', 'Sleeping', 'sitting'),
  'He is Sitting on the couch'
);
```

`myReplace("I think we should look up there", "up", "Down")` يجب أن يعيد السلسلة النصية `I think we should look down there`.

```js
assert.deepEqual(
  myReplace('I think we should look up there', 'up', 'Down'),
  'I think we should look down there'
);
```

`myReplace("This has a spellngi error", "spellngi", "spelling")` يجب أن يعيد السلسلة النصية `This has a spelling error`.

```js
assert.deepEqual(
  myReplace('This has a spellngi error', 'spellngi', 'spelling'),
  'This has a spelling error'
);
```

`myReplace("His name is Tom", "Tom", "john")` يجب أن يعيد السلسلة النصية `His name is John`.

```js
assert.deepEqual(
  myReplace('His name is Tom', 'Tom', 'john'),
  'His name is John'
);
```

`myReplace("Let us get back to more Coding", "Coding", "algorithms")` يجب أن يعيد السلسلة النصية `Let us get back to more Algorithms`.

```js
assert.deepEqual(
  myReplace('Let us get back to more Coding', 'Coding', 'algorithms'),
  'Let us get back to more Algorithms'
);
```

# --seed--

## --seed-contents--

```js
function myReplace(str, before, after) {
  return str;
}

myReplace("A quick brown fox jumped over the lazy dog", "jumped", "leaped");
```

# --solutions--

```js
function myReplace(str, before, after) {
  if (before.charAt(0) === before.charAt(0).toUpperCase()) {
    after = after.charAt(0).toUpperCase() + after.substring(1);
  } else {
    after = after.charAt(0).toLowerCase() + after.substring(1);
  }
  return str.replace(before, after);
}
```
