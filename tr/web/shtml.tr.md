{
  "date" : "2021-05-20",
  "keywords" :[ "shtml","shtml dosyası", "shtml dosya biçimi", "shtml dosya türü", "dosya", "tür", "shtml dosyası nedir" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHTML - Sunucu Tarafı HTML Dosyasını Dahil Et",
  "description":"SHTML dosya formatı ve SHTML dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "SHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## SHTML dosyası nedir?

.shtml uzantılı bir dosya, [HTML](/tr/web/html/) ile yazılmış ve sunucu talimatlarını içeren bir web sayfasıdır. Daha hızlı yükleme için ASP dosyalarına benzer sunucu tarafı içerikleri de içerebilir. Sunucu tarafı dosyaları, sunucunun normalden daha yavaş yüklenmesine neden olabilen yürütülebilir kod da içerebilir. SHTML dosyaları HTML'ye benzer, ancak basit sunucu komutlarının kullanılmasına da izin verir. Bu sunucu komutları, Sunucu Tarafı İçeriği (SSI) adı verilen basit bir bilgisayar programlama dilinde gerçekleştirilir. SHTML'nin yerini büyük ölçüde [PHP](/tr/programming/php/) gibi diğer sunucu tarafı programlama dilleri almıştır.

## SHTML Dosya Biçimi

SHTML dosyaları düz metin olarak yazılır ve sunucu tarafında yürütülen [SSI komutlarını](https://www.w3.org/Jigsaw/Doc/User/SSI.html) kullanır. Bu sunucu tarafı komutları, veritabanı sürücülerini kullanarak veritabanına bağlanmak ve tablolardan kullanıcı verilerini almak için bile kullanılabilir.

## SHTML Örneği

Sunucu tarafı talimatları, sayfa ziyaretçi sayacı veya web sayfası takvimi gibi uygulamalarda kullanılır. Aşağıdaki örnek, kullanıcı veri tabanının ilk üç satırının ilk dört sütununu göstermektedir.

```
<!--#jdbc name="result2" select="SELECT * FROM users"
          user="bmahe" password=""
          url="jdbc:msql://www43.inria.fr:4333/users"
          driver="com.imaginary.sql.msql.MsqlDriver"  -->

      <table border=2>
        <!--#cpt name="cpt1" init="0" -->
          <tr><td><b>Name </td><td><b>Login</td>
              <td><b>Email</td><td><b>Age  </td></tr>
          <!--#loop name="loop2" -->

          <!--#jdbc name="result2" next="true" -->

          <tr>
            <td>
              <!--#jdbc name="result2" column="1" -->
            </td><td>
              <!--#jdbc name="result2" column="2" -->
            </td><td>
              <!--#jdbc name="result2" column="3" -->
            </td><td>
              <!--#jdbc name="result2" column="4" -->
            </td>
          </tr>

          <!--#cpt name="cpt1" incr="1" -->
          <!--#exitloop name="loop2" command="cpt" var="cpt1" equals="3" -->
          <!--#endloop name="loop2" -->

      </table>

      counter value : <!--#cpt name="cpt1" value="true" -->
```
## Referanslar

* [Sunucu Tarafı İçeriği](https://en.wikipedia.org/wiki/Server_Side_Includes)

