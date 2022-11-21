{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CRL Dosyası - Sertifika İptal Listesi",
  "description":"CRL dosya formatı ve CRL dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "CRL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-01"
}

## CRL dosyası nedir?

Bir CRL (Sertifika İptal Listesi) dosyası, bir sertifika yetkilisinin (CA) atanan iptal tarihinden önce iptal ettiği X.509 dijital sertifikalarının kara listesidir. Güvenlik yöneticilerinin etkilenen dijital sertifikaları engellemesine olanak tanıyan sorun ve iptal tarihi hakkında bilgiler içerir. SİL, asıl amacı güvenilmeyen ve geçersiz sertifikaları bildirmek olduğu için süresi dolmuş sertifikaları içermez.

**CRL dosyalarını açabilen** uygulamalar arasında OpenSSL, Microsoft IIS Server ve Citrix NetScaler bulunur.

## CRL Dosya Biçimi - Daha Fazla Bilgi

CRL dosyaları, ortak anahtar bilgilerini paylaşmak için semantiğini de tanımlayan X.509 standardındaki bilgileri içerir. Bir CRL dosyasında yer alan diğer bilgiler, sertifikaların iptal edildiği süreyi, iptalin nedenini, iptal edilen sertifikanın seri numarasını ve zaman damgasını içerebilir.


### Sertifikaların CRL'ye Eklenmesinin Başlıca Nedenleri

Web sitenizin sertifikasının iptal edilmesinin ve CRL'ye eklenmesinin birkaç nedeni olabilir. Bazıları olabilir;

1. Sertifikanızın özel anahtarının güvenliği ihlal edildi
1. Sertifikanız geçerli değil veya CA tarafından yanlış verilmiş
1. Sertifikayla ilişkili kuruluş ayrıntıları değiştirilir ve CA yeni sertifika verir
1. Sertifikanın iptal edilmesine neden olan diğer kaçınılmaz nedenler

## Referanslar

* [Ulusal Standartlar ve Teknoloji Enstitüsü (NIST)](https://csrc.nist.gov/glossary/term/CRL)
* [Internet Engineering Task Force's (IETF) RFC 5280](https://tools.ietf.org/html/rfc5280)
* [Sertifika İptal Listesi](https://en.wikipedia.org/wiki/Certificate_revocation_list)

