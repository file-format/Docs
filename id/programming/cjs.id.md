{
  "date" : "2023-10-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "File CJS - File Kode CommonJS",
  "description":"Apa itu file .cjs dan bagaimana cara membukanya?",
  "linktitle" : "CJS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2023-10-26"
}

## Apa itu berkas CJS?

File CommonJS (CJS) adalah file yang berisi kode JavaScript yang ditulis dalam sintaks CommonJS. CommonJS adalah sistem modul yang dirancang untuk bekerja di lingkungan di luar browser web frontend, dan sering digunakan di lingkungan JavaScript sisi server, seperti Node.js.

## Format File CJS - Informasi Lebih Lanjut

File CJS ditulis dalam sintaks CommonJS dan dapat diedit di editor teks apa pun seperti Microsoft Notepad atau Apple TextEdit. Modul CommonJS biasanya disimpan dalam file terpisah dan dimaksudkan untuk merangkum dan memodulasi kode untuk organisasi dan pemeliharaan yang lebih baik. Modul-modul ini menggunakan fungsi require untuk mengimpor dependensi dan objek module.exports atau ekspor untuk mengekspos nilai dan fungsi yang dapat digunakan oleh bagian lain dari kode.

## Contoh Kode CJS

Modul CommonJS memiliki sintaks dan struktur khusus yang mencakup fitur seperti fungsi require untuk mengimpor modul lain dan objek module.exports atau ekspor untuk mengekspor nilai, fungsi, atau objek dari modul. Modul-modul ini digunakan untuk merangkum dan memisahkan potongan kode, sehingga memudahkan pengelolaan dan pemeliharaan basis kode JavaScript yang besar. Berikut ini contoh dasar modul CommonJS:

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

## Referensi

* [Design Classes in Visual Studio](https://en.wikipedia.org/wiki/CommonJS)