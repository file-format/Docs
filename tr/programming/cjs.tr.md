{
  "date" : "2023-10-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "CJS Dosyası - CommonJS Kod Dosyası",
  "description":".cjs dosyası nedir ve nasıl açılır?",
  "linktitle" : "CJS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2023-10-29"
}


## CJS dosyası nedir?

CommonJS (CJS) dosyası, CommonJS sözdiziminde yazılmış JavaScript kodunu içeren bir dosyadır. CommonJS, ön uç web tarayıcılarının ötesindeki ortamlarda çalışmak üzere tasarlanmış bir modül sistemidir ve genellikle Node.js gibi sunucu tarafı JavaScript ortamlarında kullanılır.

## CJS Dosya Formatı - Daha Fazla Bilgi

CJS dosyaları CommonJS sözdiziminde yazılmıştır ve Microsoft Notepad veya Apple TextEdit gibi herhangi bir metin düzenleyicide düzenlenebilir. CommonJS modülleri genellikle ayrı dosyalarda depolanır ve daha iyi organizasyon ve bakım kolaylığı için kodu kapsülleme ve modülerleştirme amacı taşır. Bu modüller, bağımlılıkları içe aktarmak için gerekli işlevi kullanır ve kodun diğer bölümleri tarafından kullanılabilecek değerleri ve işlevleri ortaya çıkarmak için module.exports veya Exports nesnesini kullanır.

## CJS Kodu Örneği

CommonJS modülleri, diğer modülleri içe aktarmak için gerekli işlev ve bir modülden değerleri, işlevleri veya nesneleri dışa aktarmak için module.exports veya Exports nesneleri gibi özellikleri içeren belirli bir sözdizimine ve yapıya sahiptir. Bu modüller kod parçalarını kapsüllemek ve ayırmak için kullanılır, böylece büyük JavaScript kod tabanlarının yönetimini ve bakımını kolaylaştırır. Aşağıda CommonJS modülünün temel bir örneğini bulabilirsiniz:

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

## Referanslar

* [Design Classes in Visual Studio](https://en.wikipedia.org/wiki/CommonJS)
