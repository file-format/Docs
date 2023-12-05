{
"tarih": "2023-03-01",
  "keywords": [
"çip dosyası",
"çip dosyası nedir",
"dosya",
"chip dosyası nasıl açılır",
"çip dosya uzantısı",
"eklenti"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "CHIP Dosya Formatı - Mikrodizi Ek Açıklama Dosyası",
  "description":"CHIP dosya formatı ve CHIP dosyalarını oluşturup açabilen API'ler hakkında bilgi edinin.",
"linktitle" : "CHIP",
  "menu": {
    "docs": {
      "identifier": "spreadsheet-chip",
      "parent": "spreadsheet"
}
},
"sonmod": "2023-03-01"
}

## .CHIP dosyası nedir?

CHIP dosyası bir mikrodizi ek açıklama dosyasıdır ve Gen Seti Zenginleştirme Analizi (GSEA) yazılımıyla ilgilidir. GSEA, önceden tanımlanmış bir gen kümesinin (bir gen kümesi), sağlıklı ve hastalıklı doku veya ilaçla tedavi edilmiş ve tedavi edilmemiş hücreler gibi iki biyolojik durum arasında istatistiksel olarak anlamlı farklılıklar gösterip göstermediğini değerlendiren hesaplamalı bir yöntemdir. GSEA'yı gerçekleştirmek için bir gen ifadesi veri kümesine ve bir gen kümesi veritabanına ihtiyacınız vardır. Gen seti veritabanı, gen setlerindeki genler hakkında, bunların fonksiyonu, yolu veya dokuya özgü ekspresyonu gibi bilgileri içerir.

CHIP dosyası, GSEA tarafından kullanılan belirli bir tür gen seti veritabanıdır. Deneyde kullanılan mikrodizi platformuyla ilgili genler ve gen setleri hakkında bilgi içerir. CHIP dosyası, mikrodizideki her prob için gen sembolü, gen adı, gen tanımı ve kromozomal konum gibi ek açıklamalar sağlar. Bu bilgi, probları gen ekspresyonu veri setindeki genlerle eşleştirmek ve bunları GSEA analizi için uygun gen setlerine atamak için kullanılır.

GSEA'da bir CHIP dosyası kullanmak için, onu yazılıma aktarmanız ve mikrodizi veri kümenize bağlamanız gerekir. GSEA, çeşitli mikrodizi platformlarını destekler ve birçoğu için önceden oluşturulmuş CHIP dosyaları sağlar. Ancak, NCBI veya Ensembl gibi harici kaynaklardan alınan açıklama veritabanlarını kullanarak kendi CHIP dosyanızı da oluşturabilirsiniz.

## Daha fazla bilgi

CHIP dosyası bir e-tablo değildir ancak Microsoft Excel veya Google E-Tablolar gibi bir e-tablo programında açılabilir ve düzenlenebilir. CHIP dosyası, sekmeyle ayrılmış veriler içeren ve görüntüleme ve düzenleme amacıyla bir elektronik tablo programına kolayca aktarılabilen bir metin dosyası türüdür.

Bir elektronik tablo programında, mikrodizi üzerindeki genler ve gen kümeleri için ek açıklamalar eklemek, kaldırmak veya değiştirmek için CHIP dosyasındaki verileri değiştirebilirsiniz. Örneğin, orijinal CHIP dosyasında yer almayan genler için özel açıklamalar eklemek veya farklı kaynaklardan birden fazla CHIP dosyasını tek bir dosyada birleştirmek için bir elektronik tablo programı kullanabilirsiniz.

Ancak bir CHIP dosyasının, GSEA yazılımıyla uyumluluk için korunması gereken belirli bir formata ve yapıya sahip olduğunu unutmamak önemlidir. Bir CHIP dosyasının içeriğini bir elektronik tablo programında değiştirirseniz, değişikliklerin dosya formatını veya içeriğini GSEA analizinin doğruluğunu veya geçerliliğini etkileyebilecek şekilde değiştirmediğinden emin olmalısınız.

## CHIP dosyası nasıl açılır?

CHIP dosyası sekmeyle ayrılmış veriler içerdiğinden, elektronik tablo verilerini görüntülemek istiyorsanız onu Microsoft Excel'de açabilirsiniz.

## Referanslar
* [GSEA](https://en.wikipedia.org/wiki/Gene_set_enrichment_analysis)
