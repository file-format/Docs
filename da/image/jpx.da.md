{
  "date": "2021-02-10",
  "keywords": [
"jpx fil",
"jpx filformat",
"hvad er en jpx-fil",
"fil",
"jpx eksempel",
"jpx filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "JPX - Billedfilformat",
  "description": "Lær om JPX-filformat og API'er, der kan oprette og åbne JPX-filer.",
  "linktitle": "JPX",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-jp-dax"
}
},
  "lastmod": "2021-02-10"
}

## Hvad er en JPX fil? ##

En fil med filtypenavnet .jpx er en filtypenavn til JPEG 2000-filformatet. Den bruger primært JPEG 2000-komprimering og giver også avancerede funktioner såsom flere lag til et billede, forskellige farverum, opacitet og fragmenterede kodestrømme. JPX tillader også andre komprimeringer såsom JBIG, CCITT Group3, CCITT Group4 osv. ud over JPEG 2000-komprimeringen. JPX-filformatet blev godkendt som [ISO/IEC 15444-2](https://www.iso.org/standard/33160.html)-standard, men kunne ikke modtage en varm modtagelse på grund af den omfattende brug af filformatet [JPEG](/image/jpeg/). Programmer, der kan åbne JPX-filer, omfatter Corel PaintShop Pro, Adobe Photoshop 2020, Adobe Illustrator 2020 og CorelDraw Graphics Suite 2020.

## Kort historie

In 2000, the Joint Photographic Experts Group committee designed JP2 with the objective to improve their own discrete cosine transform-based JPEG standard with this new wavelet-based method. The JPEG committee aimed to provide their baseline methods free of license fees.in the JP2 license gaining competition among 20 companies, they won by a whisker. JPEG 2000 has been declared as an ISO standard, though most web browser are not ready to give a hand to JPEG 2000 since 2017. I 2004 blev ISO/IEC 15444-2-formatet offentligt accepteret som udvidelse til JP2-filformatet.

## JPX filformat

JPX-filformatet blev formuleret til at opfylde kravene til applikationer, der havde behov for datastrukturer ud over den funktionalitet, der er defineret af filformatet [JP2](/image/jp2/). En JP2-fil med ikke-kompatible udvidelser kan føre til forvirring på markedet, hvor nogle læsere kan fortolke nogle JP2-filer, men ikke andre. JPX er svaret på at undgå sådanne problemer i applikationer.

### Filidentifikation

JPX-filer gemmes som [JPF](/image/jpf/), når de gemmes i et traditionelt computerfilsystem. Det er grunden til, at JPX-udtrykket er mindst almindeligt brugt sammenlignet med JPF. En JPX-fil begynder med følgende bytes:

`00 00 00 0c 6a 50 20 20 0d 0a 87 0a ?? ?? ?? ?? 66 74 79 70 6a 70 78 20`

### Filorganisation

I lighed med JP2 er en JPX-fil en samling af kasser med en binær struktur med kasserne arrangeret i en sammenhængende rækkefølge. Den første boks giver starten på filen med dens første byte, og den sidste byte i den sidste boks repræsenterer den sidste byte af filen.
Den binære struktur af en boks i en JPX-fil er identisk med den, der er defineret i filformatet [JP2](/image/jp2/).

### Lagring af CodeStream i JPX

JPX-filformatet gør det muligt at opdele billedkodestrømmen i fragmenter. Dette gør det muligt at ændre en enkelt flise af billedet og skrive den modificerede flise til slutningen af filen uden at omskrive hele filen. Det originale [JP2](/image/jp2/)-filformat begrænser hele kodestrømmen til at blive lagret i en sammenhængende del af filen, hvilket kan være problematisk for billedredigeringsprogrammer, der kan ønske at ændre en enkelt flise af billedet og opnå ovenstående understøttelse af JPX filformat. Fragmenteringen af billedkodestrømmen gør JPX-filformatet overlegent i forhold til JP2-filformatet. Derudover tillader JPX-filformatet, at flere kodestrømme kan kombineres og producere gengivet resultat. Codestreams kan kombineres som sammensætning og animation.

## Referencer ##

* [Oversigt over JPEG 2000](https://jpeg.org/jpeg2000/)


