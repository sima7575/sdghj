---
id: 587d7fb6367417b2b2512c07
title: モデルを作成する
challengeType: 2
forumTopicId: 301535
dashedName: create-a-model
---

# --description--

**C**RUD パート I - 作成する

First of all, we need a Schema. 各スキーマは、MongoDB コレクションにマップされます。 スキーマにより、コレクション内のドキュメントの形状を定義します。 Schemas are building blocks for Models. They can be nested to create complex models, but in this case, we'll keep things simple. モデルにより、ドキュメントと呼ばれるオブジェクトのインスタンスを作成できます。

Replit is a real server, and in real servers, the interactions with the database happen in handler functions. これらの関数は、何らかのイベントが発生した時に実行されます (たとえば、誰かが API 上のエンドポイントにアクセスしたとき)。 演習でも同じアプローチに従います。 `done()` 関数は、挿入、検索、更新または削除などの非同期操作を完了した後に処理を続行できることを示すコールバック関数です。 Node の規約に従い、成功時には `done(null, data)` を呼び出し、エラー時には `done(err)` を呼び出します。

警告 - リモートサービスとのやり取りではエラーが発生する可能性があります！

```js
/* Example */

const someFunc = function(done) {
  //... do something (risky) ...
  if (error) return done(error);
  done(null, result);
};
```

# --instructions--

次のプロトタイプを持つ `personSchema` というパーソンスキーマを作成してください。

```markup
- Person Prototype -
--------------------
name : string [required]
age :  number
favoriteFoods : array of strings (*)
```

Mongoose の基本的なスキーマタイプを使用してください。 フィールドを追加したい場合は、required や unique といった単純なバリデーターを使用し、デフォルト値を設定してください。 <a href="https://www.freecodecamp.org/news/introduction-to-mongoose-for-mongodb-d2a7aa593c57/" target="_blank" rel="noopener noreferrer nofollow">Mongoose の記事</a>を参照してください。

次に、`personSchema` から `Person` というモデルを作成してください。

# --hints--

Mongoose スキーマからインスタンスを正しく作成する必要があります。

```js
(getUserInput) =>
  $.post(getUserInput('url') + '/_api/mongoose-model', {
    name: 'Mike',
    age: 28,
    favoriteFoods: ['pizza', 'cheese']
  }).then(
    (data) => {
      assert.equal(data.name, 'Mike', '"model.name" is not what expected');
      assert.equal(data.age, '28', '"model.age" is not what expected');
      assert.isArray(
        data.favoriteFoods,
        '"model.favoriteFoods" is not an Array'
      );
      assert.include(
        data.favoriteFoods,
        'pizza',
        '"model.favoriteFoods" does not include the expected items'
      );
      assert.include(
        data.favoriteFoods,
        'cheese',
        '"model.favoriteFoods" does not include the expected items'
      );
    },
    (xhr) => {
      throw new Error(xhr.responseText);
    }
  );
```

# --solutions--

```js
/**
  Backend challenges don't need solutions, 
  because they would need to be tested against a full working project. 
  Please check our contributing guidelines to learn more.
*/
```
