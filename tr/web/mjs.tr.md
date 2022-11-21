{
  "date" : "2021-07-20",
  "keywords" :["MJS", "Dosya", "Uzantı", "Dosya Biçimi", "Dosya Uzantısı", "Node.js ES Modül Dosyası"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MJS - Node.js ES Modül Javascript Dosyası",
  "description" :"MJS dosyasının ne olduğu ve MJS dosyasını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "MJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-20"
}

## Bir MJS dosyası nedir?

.mjs uzantılı bir dosya, Node.js uygulamalarında ECMA Modülü (ECMAScript Modülü) olarak kullanılan bir JavaScript kaynak kod dosyasıdır. Node.js'nin natvie modül sistemi, [JS](/tr/web/js/) kodunu düzenli tutmak için kodu farklı dosyalara bölmek için kullanılan CommonJS'dir. MJS, Node.js tarafından modülün CommonJS mi yoksa ES6 mı olduğunu belirlemek için kullanılan tek yoldur. ECMAScript modülleri, JavaScript kodunu yeniden kullanım için paketlemeye yönelik standart biçimdir. MJS dosyaları Atom, Vim, Apple xCode, Microsoft Visual Studio ve Notepad gibi metin editörlerinde açılabilir.

## MJS Dosya Biçimi - Daha Fazla Bilgi

MJS dosyaları, JavaScript sözdiziminde düz metin biçiminde diske kaydedilir. Bunlar herhangi bir metin düzenleyicide açılabilir ve insanlar tarafından okunabilir. 2018'den bu yana, neredeyse tüm büyük tarayıcılar artık ES modüllerini desteklemektedir.

## ES modülleri ile CommonJS arasındaki farklar

Peki MJS dosyalarını düz JS dosyalarından farklı kılan nedir? ES Modülleri ile CommonJS arasındaki fark şu şekilde özetlenebilir:

* Gerek yok, ihracat veya modül. ihracat
* \__filename veya \__dirname yok
* JSON Modülü Yüklemesi Yok
* Yerel Modül Yüklemesi Yok
* Çözüm gerektirmez
* NODE_PATH yok
* Uzantı gerekmez
* Önbellek gerektirmez

## Referanslar

* [Node.js ESM](https://nodejs.org/docs/latest/api/esm.html)
* [JS ve MJS Arasındaki Fark](https://nodejs.org/docs/latest/api/esm.html#esm_differences_between_es_modules_and_commonjs)

