{
  "date" : "2022-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"PYC dosya formatı ve PYC dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"PYC Dosya Biçimi- Python Derlenmiş Dosyası",
  "linktitle" : "PYC",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2022-05-09"
}

## .pyc dosyası nedir?

PYC dosyası, Python programlama dilinde yazılmış kaynak kodundan oluşturulan derlenmiş bir çıktı dosyasıdır. PY dosyası Python yorumlayıcı kullanılarak çalıştırıldığında, yürütme için bayt koduna dönüştürülür. Aynı zamanda, derlenen bayt kodu, gerektiğinde daha sonra önbellekten yeniden kullanılmak üzere .pyc dosyası olarak da kaydedilir.

## PYC Dosya Biçiminin Yapısı

PYC dosyaları bayt kodundadır ve dosya formatı özellikleri herkese açık değildir. Ancak, bazı kaynaklar tarafından yapılan araştırmalar, [bir PYC dosyasının yapısının](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html) şunlardan oluşur:

* `Dört baytlık sihirli bir sayı`r - Sıralama kodundaki her değişiklikle değişen yalnızca iki bayt ve ardından iki bayt 0d0a.
* `Dört baytlık bir değişiklik zaman damgası` - .pyc dosyasını oluşturan kaynak dosyanın Unix değişiklik zaman damgası, böylece kaynak değişirse dosya yeniden derlenebilir.
* `Bir sıralanmış kod nesnesi` - kaynak dosyanın derlenmesinin bir sonucu olan kod nesnesinin marshal.dump çıktısı.

## Referanslar

* [.pyc dosyalarının yapısı](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html)

