{
  "date" : "2021-05-20",
  "keywords" :[ "stml","stml dosyası", "stml dosya biçimi", "stml dosya türü", "dosya", "tür", "stml dosyası nedir" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"STML - SSI HTML Dosyası",
  "description":"STML dosya formatı ve STML dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "STML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## STML dosyası nedir?

.stml uzantılı bir dosya, bir kullanıcı sayfayı web tarayıcısına yüklediğinde yürütülen sunucu tarafı talimatlarına sahip bir web sayfasıdır. STML sayfaları, düz HTML ile elde edilmesi mümkün olmayan görevleri gerçekleştirmek için sunucu tarafı içeriklerini içeren sunucu tarafı kodunu içerir. [HTML](/tr/web/html/) ile benzer olsa da STML, Sunucu Tarafı İçeriği (SSI) olarak da adlandırılan sunucu üzerinde komutları çalıştırarak daha fazla güç sunar. PHP gibi sunucu tarafı komut dosyasına sahip yeni programlama dillerinin kullanıma sunulmasıyla birlikte, tüm sunucu tarafı teknolojileri tarafından hala desteklenmesine rağmen, STML kullanımı azaltılmıştır. STML dosyaları herhangi bir metin düzenleyicide açılabilir ve komutları güncellemek için düzenlenebilir.

## STML Dosya Biçimi

STML, insan tarafından okunabilen düz ascii metin dosyası biçimini temel alır. Ancak, sunucu tarafında yürütülen [SSI komutları](https://www.w3.org/Jigsaw/Doc/User/SSI.html) kullanılarak tanımlanan ve uygulanan sözdizimini takip eder. Diğer herhangi bir sunucu tarafı komut dosyası dili gibi, STML de sunucu tarafı komutlarını sayfa ziyaretçi sayacı, web sayfası takvimi, veritabanından kayıt alma ve benzerleri gibi görevleri gerçekleştirmek için kullanabilir.

## STML Örneği

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

