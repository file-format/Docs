{
  "date": "2023-10-26",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CJS Faylı - CommonJS Kod Faylı",
  "description": ".cjs faylı nədir və onu necə açmaq olar?",
  "linktitle": "CJS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-cj-azs"
}
},
  "lastmod": "2023-10-26"
}

## CJS faylı nədir?

CommonJS (CJS) faylı CommonJS sintaksisində yazılmış JavaScript kodunu ehtiva edən fayldır. CommonJS qabaqcıl veb brauzerlərdən kənar mühitlərdə işləmək üçün nəzərdə tutulmuş modul sistemidir və o, tez-tez Node.js kimi server tərəfli JavaScript mühitlərində istifadə olunur.

## CJS Fayl Format - Ətraflı Məlumat

CJS faylları CommonJS sintaksisində yazılmışdır və Microsoft Notepad və ya Apple TextEdit kimi istənilən mətn redaktorunda redaktə edilə bilər. CommonJS modulları adətən ayrı-ayrı fayllarda saxlanılır və daha yaxşı təşkili və davamlılığı üçün kodu əhatə etmək və modullaşdırmaq üçün nəzərdə tutulub. Bu modullar asılılıqları idxal etmək üçün tələb funksiyasından, kodun digər hissələri tərəfindən istifadə oluna bilən dəyərləri və funksiyaları ifşa etmək üçün modul.exports və ya ixrac obyektindən istifadə edir.

### CJS kodu nümunəsi

CommonJS modulları digər modulların idxalı üçün tələb funksiyası və modul.moduldan dəyərləri, funksiyaları və ya obyektləri ixrac etmək üçün obyektləri ixrac edir və ya ixrac edir kimi xüsusiyyətləri özündə birləşdirən xüsusi sintaksis və struktura malikdir. Bu modullar böyük JavaScript kod bazalarını idarə etməyi və saxlamağı asanlaşdıran kod hissələrini əhatə etmək və ayırmaq üçün istifadə olunur. CommonJS modulunun əsas nümunəsi:

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

## İstinadlar

* [Visual Studio-da Dizayn Dərsləri](https://en.wikipedia.org/wiki/CommonJS)


