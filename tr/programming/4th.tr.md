
{
  "date" : "2023-02-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"4. Dosya - Dördüncü Dil Dosya Formatı",
  "description":"4. dosyaları oluşturup açabilen örnek ve API'ler ile .4. dosya formatının ne olduğunu öğrenin.",
  "linktitle" : "4th",
  "menu" : {
    "docs" : {
      "identifier":"programming-4th",
      "parent" : "programming"
}
},
  "lastmod" : "2023-02-09"
}

## 4. dosya nedir?

.4th dosya uzantısına sahip bir dosya **Dördüncü Programlama Dili** için oluşturulmuş bir programlama dosyasıdır. Forth programlama dilinde yazılan programların kaynak kodunu içerir ve program çalıştırıldığında çıktı üretir. Bu, [C](/tr/programming/c/) ve [C++](/tr/programming/cpp/) kaynak dosyasına benzeyen başka bir programlama dili dosyasıdır.

## 4. Dosya Formatı - Daha Fazla Bilgi


### 4. Programlama Dili Kod Örneği

Belirli bir sayının faktöriyelini hesaplayan, Forth'ta yazılmış basit bir program örneği:

```
: factorial ( n -- n! )
   dup 0=
   if
      drop 1
      exit
   then
   1
   swap
   begin
      dup 1-
      dup 0=
      if
         drop
         exit
      then
      swap
      *
   repeat
;

```

Bu örnekte, faktöriyel sözcüğü tek bir n argümanını alır ve onun faktöriyelini döndürür. Dup sözcüğü yığının üstündeki değeri çoğaltır, drop yığının üstündeki değeri atar ve * yığının üstündeki iki değeri çarpar. If ve begin/until yapıları programın akışını kontrol eder.

Bu programı kullanmak için, tanımı Forth yorumlayıcısına girersiniz ve ardından faktöriyel kelimesini, faktöriyelini bulmak istediğiniz sayıyla çağırırsınız:

```
10 factorial .
```
Bu, 10'un faktöriyeli olan 3628800 çıktısıyla sonuçlanacaktır.

## Referanslar

* [Dördüncü Programlama Dili](https://en.wikipedia.org/wiki/Forth_(programming_language))

