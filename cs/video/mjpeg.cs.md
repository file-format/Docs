{
  "date" : "2021-02-15",
  "keywords" :[ "MJPEG", "soubor", "přípona", "formát", "Motion JPEG", "komprese", "obrázek JPEG", "video"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MJPEG - formát souboru Motion JPEG",
  "description":"Další informace o formátu souboru MJPEG a rozhraních API, která mohou vytvářet a otevírat soubory MJPEG.",
  "linktitle" : "MJPEG",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## Co je soubor MJPEG? ##

Soubor s příponou .mjpeg (Motion JPEG) je soubor videa, který je vytvořen kompresí jednotlivého snímku videa jako obrázek JPEG. Liší se od standardních formátů souborů MPEG-1 a MPEG-2, kde je komprese interframes a rozhoduje se na základě predikce obsahu v následujících snímcích. MJPEG je podporován širokou škálou aplikací, které zahrnují webové prohlížeče, přehrávače médií, digitální fotoaparáty, webové kamery, streamovací servery. Zásuvné moduly jsou k dispozici pro aplikace, které chtějí využívat formát souboru MJPEG.

## Formát souboru MJPEG ##

MJPEG je založen na vyspělém kompresním standardu, tj. [JPEG](/cs/image/jpeg/), který má dobře definované knihovny. Nelze jej standardizovat podobně jako standardy jako MPEG-2 a není k dispozici žádná dokumentace, kterou by bylo možné označit za kompletní specifikace pro „Motion JPEG“. Pokud takový standard neexistuje, mohou výstupy od různých výrobců vyvolávat problémy s kompatibilitou. Společnosti jako Microsoft a Apple však zdokumentovaly, jak jsou soubory M-JPEG uloženy v jejich nativních formátech, jako je [AVI](/cs/video/avi/) a [QT](/cs/video/qt/). [rfc2435](https://tools.ietf.org/html/rfc2435) popisuje RTP Payload Format pro JPEG-komprimované video a lze jej použít jako referenční materiál.

## Reference ##

- [RFC2435 - RTP Payload Format for JPEG-Compressed Video](https://tools.ietf.org/html/rfc2435)
- [Motion JPEG - Wikipedia](https://en.wikipedia.org/wiki/Motion_JPEG)

