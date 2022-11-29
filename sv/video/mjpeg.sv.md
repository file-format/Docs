{
  "date" : "2021-02-15",
  "keywords" :[ "MJPEG", "fil", "tillägg", "format", "Motion JPEG", "komprimering", "JPEG-bild", "video"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MJPEG - Motion JPEG File Format",
  "description":"Läs mer om MJPEG-filformat och API:er som kan skapa och öppna MJPEG-filer.",
  "linktitle" : "MJPEG",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## Vad är en MJPEG fil? ##

En fil med filtillägget .mjpeg (Motion JPEG) är en videofil som skapas genom att komprimera en enskild videoram som en JPEG-bild. Det skiljer sig från standardfilformaten MPEG-1 och MPEG-2 där komprimeringen är interframes och bestäms baserat på förutsägelse av innehåll i efterföljande bildrutor. MJPEG stöds av ett brett utbud av applikationer som inkluderar webbläsare, mediaspelare, digitalkameror, webbkameror, streamingservrar. Insticksprogram är tillgängliga för program som vill använda filformatet MJPEG.

## MJPEG-filformat ##

MJPEG är baserad på den mogna komprimeringsstandarden, dvs [JPEG](/sv/image/jpeg/) som har väldefinierade bibliotek. Det kunde inte standardiseras på samma sätt som standarder som MPEG-2 och det finns ingen tillgänglig dokumentation som kan hänvisas till som fullständiga specifikationer för "Motion JPEG". I avsaknad av en sådan standard kan utdata från olika tillverkare leda till kompatibilitetsproblem. Företag som Microsoft och Apple har dock dokumenterat hur M-JPEG-filerna lagras i sina ursprungliga format som [AVI](/sv/video/avi/) och [QT](/sv/video/qt/). [rfc2435](https://tools.ietf.org/html/rfc2435) beskriver RTP-nyttolastformatet för JPEG-komprimerad video och kan konsulteras som referensmaterial.

## Referenser ##

- [RFC2435 - RTP-nyttolastformat för JPEG-komprimerad video](https://tools.ietf.org/html/rfc2435)
- [Motion JPEG - Wikipedia](https://en.wikipedia.org/wiki/Motion_JPEG)

