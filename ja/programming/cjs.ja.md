{
  "date" : "2023-10-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "CJS ファイル - CommonJS コード ファイル",
  "description":".cjs ファイルとは何ですか?またそれを開く方法は?",
  "linktitle" : "CJS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2023-10-26"
}

## CJS ファイルとは何ですか?

CommonJS (CJS) ファイルは、CommonJS 構文で記述された JavaScript コードを含むファイルです。 CommonJS は、フロントエンド Web ブラウザーを超えた環境で動作するように設計されたモジュール システムであり、Node.js などのサーバーサイド JavaScript 環境でよく使用されます。

## CJS ファイル形式 - 詳細情報

CJS ファイルは CommonJS 構文で記述されており、Microsoft メモ帳や Apple TextEdit などのテキスト エディタで編集できます。 CommonJS モジュールは通常、別個のファイルに保存され、コードをカプセル化してモジュール化して編成と保守性を向上させることを目的としています。 これらのモジュールは、require 関数を使用して依存関係をインポートし、module.exports または exports オブジェクトを使用して、コードの他の部分で使用できる値と関数を公開します。

## CJS コード例

CommonJS モジュールには、他のモジュールをインポートするための require 関数や、モジュールから値、関数、またはオブジェクトをエクスポートするための module.exports またはエクスポート オブジェクトなどの機能を含む、特定の構文と構造があります。 これらのモジュールは、コードの一部をカプセル化して分離するために使用され、大規模な JavaScript コードベースの管理と保守が容易になります。 CommonJS モジュールの基本的な例を次に示します。

```
// Module definition in a file named "myModule.js"
const someValue = 42;

function add(a, b) {
  return a + b;
}

module.exports = {
  someValue,
  add,
};

// Using the module in another file
const myModule = require('./myModule');
console.log(myModule.someValue); // 42
console.log(myModule.add(10, 20)); // 30
```

## 参考文献

* [Design Classes in Visual Studio](https://en.wikipedia.org/wiki/CommonJS)