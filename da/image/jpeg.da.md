{
  "date": "2019-11-25",
  "keywords": [
"jpeg-fil",
"jpeg filformat",
"hvad er en jpeg-fil",
"fil",
"jpeg eksempel",
"jpeg filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "JPEG - billedfilformat",
  "description": "Lær om JPEG-filformat og API'er, der kan oprette og åbne JPEG-filer.",
  "linktitle": "JPEG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-jpe-dag"
}
},
  "lastmod": "2020-08-08"
}

## Hvad er en JPEG-fil? ##

En JPEG er en type billedformat, der gemmes ved hjælp af metoden med tabskomprimering. Outputbilledet, som et resultat af komprimering, er en afvejning mellem lagerstørrelse og billedkvalitet. Brugere kan justere komprimeringsniveauet for at opnå det ønskede kvalitetsniveau og samtidig reducere lagerstørrelsen. Billedkvaliteten påvirkes ubetydeligt, hvis der anvendes 10:1-komprimering på billedet. Jo højere komprimeringsværdien er, desto højere er forringelsen af billedkvaliteten.

## Filformatspecifikationer ##

JPEG-billedfilformatet blev standardiseret af Joint Photographic Experts Group og dermed navnet JPEG. Formatet har været valget mellem at gemme og sende fotografiske billeder på nettet. Næsten alle operativsystemer har nu fremvisere, der understøtter visualisering af JPEG-billeder, som ofte også gemmes med JPG-udvidelse. Selv webbrowsere understøtter visualisering af JPEG-billeder. Før du går ind i JPEG-filformatspecifikationerne, skal den overordnede proces af trin involveret i JPEG-oprettelse nævnes.

### JPEG-komprimeringstrin ###

**Transformation:** Farvebilleder omdannes fra RGB til et luminans/krominansbillede (øjet er følsomt over for luminans, ikke krominans, så den krominansdel kan miste mange data og kan derfor være meget komprimeret.

**Nedsampling:** Nedsamplingen udføres for farvet komponent og ikke for luminanskomponent. Nedsampling udføres enten i forholdet 2:1 horisontalt og 1:1 lodret (2h 1 V). Således reduceres billedet i størrelse, da 'y'-komponenten ikke berøres, og der er intet mærkbart tab af billedkvalitet.

**Organisering i grupper:** Pixels for hver farvekomponent er organiseret i grupper på 8×2 pixels kaldet dataenheder, hvis antallet af rækker eller kolonner ikke er et multiplum af 8, er den nederste række og kolonnerne længst til højre duplikeret.

**Diskret cosinustransformation:** Diskret cosinustransformation (DCT) anvendes derefter på hver dataenhed for at skabe 8×8 kort over transformerede komponenter.DCT indebærer noget tab af information på grund af computeraritmetikkens begrænsede præcision. Det betyder, at selv uden kortet vil der være et vist tab af billedkvalitet, men det er normalt lille.

**Kvantisering:** Hver af de 64 transformerede komponenter i dataenheden er divideret med et separat tal kaldet dens 'Quantization Coefficient (QC)' og derefter afrundet til et heltal. Det er her information går tabt uigenkaldeligt, store QC forårsager mere tab. Generelt tillader de fleste JPEG-redskaber brug af QC-tabeller anbefalet af JPEG-standarden.

**Kodning:** De 64 kvantiserede transformerede koefficienter (som nu er heltal) for hver dataenhed er kodet ved hjælp af en kombination af RLE- og Huffman-kodning.

**Tilføjelse af header:** Det sidste trin tilføjer header og alle de anvendte JPEG-parametre og udlæser resultatet.

JPEG-dekoderen bruger trinnene omvendt til at generere det originale billede fra det komprimerede.

### Filstruktur ###

Et JPEG-billede er repræsenteret som en sekvens af segmenter, hvor hvert segment begynder med en markør. Hver markør starter med 0xFF byte efterfulgt af markørflag for at repræsentere typen af markør. Nyttelasten efterfulgt af markør er forskellig afhængig af markørtype. Almindelige JPEG-markørtyper er som angivet nedenfor:

|Kort navn|Bytes|Nyttlast|Navn|Kommentarer
---|---|---|---|---|
|SOI|0xFF, 0xD8|ingen|Start af billede|
|S0F0|0xFF, 0xC0|variabel størrelse|Start af ramme|
|S0F2|0xFF, 0xC2|variabel størrelse|Start for ramme|
|DHT|0xFF, 0xC4|variabel størrelse|Definer Huffman-tabeller|
|DQT|0xFF, 0xDB|variabel størrelse|Definer kvantiseringstabell(er)|
|DRI|0xFF, 0xDD|4 bytes|Definer genstartsinterval|
|SOS|0xFF, 0xDA|variabel størrelse|Start af scanning|
|RSTn|0xFF, 0xD//n//(//n//#0..7)|ingen|Genstart|
|APPn|0xFF, 0xE//n//|variabel størrelse|Applikationsspecifik|
|COM|0xFF, 0xFE|variabel størrelse|Kommentar|
|EOI|0xFF, 0xD9|ingen|Slut på billede|

Inden for de entropikodede data, efter enhver 0xFF byte, indsættes en 0x00 byte af indkoderen før den næste byte, så der ikke ser ud til at være en markør, hvor ingen er tilsigtet, hvilket forhindrer rammefejl. Dekodere skal springe denne 0x00 byte over. Denne teknik, kaldet [byte stuffing](https://en.wikipedia.org/wiki/Byte_stuffing) (se JPEG-specifikationsafsnit F.1.2.3), anvendes kun på de entropikodede data, ikke til at markere nyttelastdata. Bemærk dog, at entropikodede data har et par egne markører; specifikt Reset-markørerne (0xD0 til 0xD7), som bruges til at isolere uafhængige bidder af entropikodede data for at tillade parallel afkodning, og indkodere kan frit indsætte disse Reset-markører med regelmæssige intervaller (selvom ikke alle indkodere gør dette).

