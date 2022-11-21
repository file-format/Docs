{
  "date" : "2021-07-29",
  "keywords" :[ "md5 dosyası", "md5 dosya biçimi", "md5 dosyası nedir", "dosya", "md5 örneği", "md5 dosya uzantısı","uzantı", "biçim" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MD5 - MD5 Sağlama Toplamı Dosyası",
  "description":"MD5 dosyası ve MD5 dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "MD5",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2021-07-29"
}

## MD5 dosyası nedir?

Bir MD5 dosyası, bir dosyanın bütünlüğünün doğrulanması için kullanılan bir sağlama toplamı dosyasıdır. İlişkili dosya için bir parmak izine benzer ve dosyadaki bit sayısını kullanan bir algoritma kullanılarak benzersiz bir şekilde oluşturulur. Dosyayı [md5sum](http://www.gnu.org/software/coreutils/manual/html_node/md5sum-invocation.html) gibi yazılımlarla doğrulamak için kullanılır. MD5 dosyalarını kullanmanın bir avantajı, indirilen dosyaların bozuk olmadığını doğrulamaktır.

## MD5 Dosya Biçimi - Daha Fazla Bilgi

Genellikle bir MD5 dosyası, orijinal dosya adıyla aynı adla ancak .md5 uzantısıyla kaydedilir. Örneğin, ilişkili dosya adı "abc_987_123456.grb" ise karşılık gelen MD5 dosya adı "abc_987_123456.grb.md5" olacaktır. MD5 dosyaları, alınan veya indirilen bir dosyanın bozulmadığını veya kötü amaçlı içerikten etkilenmediğini belirlemeye yardımcı olur. Kısacası, MD5 dosyaları bir dosyanın bütünlüğünü garanti eder.


## MD5 Sağlama toplamı nasıl kontrol edilir?

Aşağıdaki gibi [md5sum](https://en.wikipedia.org/wiki/Md5sum) aracı kullanılarak tek bir dosya MD5 için kontrol edilebilir/doğrulanabilir.

```
md5sum -c abc_987_123456.grb.md5
```

## Referanslar

* [md5sum - Wikipedia](https://en.wikipedia.org/wiki/Md5sum)

