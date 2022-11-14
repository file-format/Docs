{
  "date" : "2021-06-09",
  "keywords" :[ "m4p", "mp3", "bestand", "extensie", "formaat", "wat is m4p-bestandsformaat", "muziek", "m4p-bestandsformaat", "M4b vs MP3", "specificatie van het m4p-bestandsformaat "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over M4P-bestandsindeling en API's die M4P-bestanden kunnen maken, converteren en openen.",
  "title" :"M4P - MPEG-4 Audioboek-bestandsindeling",
  "linktitle" : "M4P",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## Wat is een M4P-bestand?
Het bestand met de extensie .m4p is een audiobestand dat meestal te downloaden is in de Apple iTunes Store. Met andere woorden, we kunnen zeggen dat M4P een AAC-bestand is, maar beveiligd tegen kopiëren met behulp van Digital Rights Management (DRM). Dit betekent dat M4P-bestanden alleen kunnen worden afgespeeld op geautoriseerde systemen of apparaten. Meestal zijn M4P-bestanden specifiek voor Apple multimedia-apparaten. Deze bestanden kunnen dus alleen worden afgespeeld op Apple macbooks, podcasts, smartphones zoals iPhone 6 of iPhone 7.

## M4P-bestandsindeling
De M4P staat voor MPEG 4 Protected (audio) en codeert de audio met geavanceerde audiocodec (AAC) en beschermt het bestand tegen ongeoorloofd gebruik van het bestand. Dit bestandsformaat wordt meestal beschouwd als het audiobestandsformaat van een iTunes Music Store. Apple gebruikt zijn FairPlay Digital Rights Management (DRM) -systeem om M4P-bestanden te beschermen. FairPlay DRM is gebaseerd op technologie die is ontwikkeld door Veridisc. Het beveiligingsmechanisme werkt door de AAC-audiostream te coderen met behulp van de AES-codering. De gebruiker ontvangt een hoofdsleutel die is toegewezen aan zijn account voor decodering. Dit bestandsformaat is geïntroduceerd als vervanging van het MP3-bestandsformaat, omdat de MP3 oorspronkelijk niet bedoeld was als audiobestand, maar als laag III in een MPEG 1 of 2 videobestand.


## Specificaties M4P-bestandsindeling

Net als bij [M4A](/nl/audio/m4a/), bestaan de M4P-bestanden ook uit opeenvolgende chunks. Elke chunk heeft een header van 8 bytes en is onderverdeeld als:
- Brokkengrootte van 4 bytes (big-endian, eerst hoge byte)
- 4-byte chunk-type - een van de vooraf gedefinieerde handtekeningen: "mdat", "moov", "pnot", "moof", "udta", "uuid", "free", "skip", "ftyp", "jP2", "wide", "load", "imap", "matt", "chap", "kmat", "clip", "crgn", "sync", "tmcd", "PICT", "scpt ", "ctab", "ssrc".

Net als bij M4A is de eerste chunk in M4P van het type "ftype" en heeft een subtype op offset 8. De M4P gedefinieerd door subtype dat "M4P_" moet zijn.

Het herhalen van chunks, totdat een onbekend type wordt gedetecteerd, zal het een M4P-bestand (MPEG-4 Audio) samenstellen.

## Referenties ##

* [MPEG-4 Deel 14 - Door Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [MPEG-4 Part 14 Audio (M4A,M4B,M4P) Format & Recovery-voorbeeld](https://www.file-recovery.com/m4a-signature-format.htm)

