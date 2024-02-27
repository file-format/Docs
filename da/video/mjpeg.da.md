{
  "date": "2021-02-15",
  "keywords": [
"MJPEG",
"fil",
"udvidelse",
"format",
"Motion JPEG",
"komprimering",
"JPEG billede",
"video"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MJPEG - Motion JPEG-filformat",
  "description": "Lær om MJPEG-filformat og API'er, der kan oprette og åbne MJPEG-filer.",
  "linktitle": "MJPEG",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-mjpe-dag"
}
},
  "lastmod": "2021-02-16"
}

## Hvad er en MJPEG fil? ##

En fil med filtypenavnet .mjpeg (Motion JPEG) er en videofil, der oprettes ved at komprimere en individuel videoramme som et JPEG-billede. Det er forskelligt fra standard MPEG-1 og MPEG-2 filformater, hvor komprimeringen er interframes og bestemmes baseret på forudsigelse af indhold i efterfølgende frames. MJPEG understøttes af en lang række applikationer, der inkluderer webbrowsere, medieafspillere, digitale kameraer, webkameraer, streamingservere. Plug-ins er tilgængelige for programmer, der ønsker at gøre brug af MJPEG-filformatet.

## MJPEG filformat ##

MJPEG er baseret på den modne komprimeringsstandard, dvs. [JPEG](/image/jpeg/), der har veldefinerede biblioteker. Det kunne ikke standardiseres i lighed med standarder som MPEG-2, og der er ingen tilgængelig dokumentation, der kan omtales som komplette specifikationer for Motion JPEG. I mangel af en sådan standard kan output fra forskellige producenter rejse kompatibilitetsproblemer. Virksomheder som Microsoft og Apple har dog dokumenteret, hvordan M-JPEG-filerne gemmes i deres oprindelige formater såsom [AVI](/video/avi/) og [QT](/video/qt/). [rfc2435](https://tools.ietf.org/html/rfc2435) beskriver RTP nyttelastformatet for JPEG-komprimeret video og kan konsulteres som referencemateriale.

## Referencer ##

- [RFC2435 - RTP Payload Format for JPEG-Compressed Video](https://tools.ietf.org/html/rfc2435)
- [Motion JPEG - Wikipedia](https://en.wikipedia.org/wiki/Motion_JPEG)

