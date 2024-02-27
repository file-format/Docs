{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PDF/VT filformat",
  "description": "Lær om PDF/VT-filformat og API'er, der kan oprette og åbne PDF/VT-filer.",
  "linktitle": "PDF/VT",
  "menu": {
    "docs": {
      "parent": "pdf",
      "identifier": "pdf-v-dat"
}
},
  "lastmod": "2019-09-10"
}

# Hvad er PDF/VT? #

PDF/VT, udgivet som [ISO 16612-2](https://www.iso.org/standard/46428.html) i august 2010 som standard, er designet til at muliggøre variabel dokumentudskrivning (VDP) i en række forskellige miljøer. Standarden gør Variable information and Transactional printing som grundlag for standarden. Udskrivningen af variable data bruges, hvor en del af informationen er forskellig for hver modtager af indholdet. Transaktionsudskrivningen inkluderer fakturaer, kontoudtog og andre dokumenter, der kombinerer faktureringsoplysninger med markedsføringsoplysninger. Dette resulterer i en blanding af forbedret behandling af billeder, tekst og andre indholdstyper. PDF/VT muliggør pålidelig og dynamisk styring af sider til HVTO-udskriftsdata (High Volume Transactional Output) ved at bruge DPM-konceptet (Document Part Metadata). PDF/VT-filer kan åbnes i Adobe Acrobat viewer uden behov for at tilføje nogen anden komponent.

## Dokumentdel hierarki ##

Document Part (DPart) Hierarkiet er som en træstruktur af dokumentdel noder, der er baseret på alle sider i dokumentet. Elementerne i dette træ kaldes DPart noder. Hver intern node indeholder andre DPart noder, og hver bladnode specificerer en eller flere sider for en modtager. I det væsentlige specificerer DPart-hierarkiet rækkefølgen og forholdet mellem dokumenter eller klapper af dokumenter i en PDF/VT-fil. Træstrukturen af DPart-noder repræsenterer nemt det interne indhold af et PDF/VT-dokument, da det kan indeholde underdokumenter for mange modtagere, og hver dokumentdel svarer til siderne for en enkelt modtager. DPart-hierarkiet er påkrævet i PDF/VT-filer.

## Document Part Metadata (DPM) ##

Document Part Metadata (DPM) er knyttet til hver node i dokumentdelhierarkiet og kan bruges til at kommunikere information om en bestemt modtagers underdokument og dets dele. DPM kan især indeholde information om egenskaberne eller information om modtagerne i en kodet form.

## Overensstemmelsesniveauer ##

PDF/VT er tildelt følgende tre overensstemmelsesniveauer. Disse er alle baseret på [PDF](/pdf/) 1.6.

* `PDF/VT-1` - Den er baseret på PDF/X-4 og indeholder alle de ressourcer, der kræves for at gengive et PDF-dokument.

* `PDF/VT-2` - Designet til udveksling af flere filer, PDF/VT-2-dokumenter kan referere til eksterne output-hensigter, eksternt indhold eller begge dele. Et PDF/VT-dokument og alle dets refererede PDF-filer og eksterne output-hensigter kaldes samlet et PDF/VT-2-filsæt. Acrobat 9 og understøtte denne funktion.

* `PDF/VT-2s` - Understøtter PDF/VT-2 live streaming. Dette gør det muligt at behandle segmenterede dele af data.


## Referencer ##

* [PDF/VT - Af Wikipedia](https://en.wikipedia.org/wiki/PDF/VT)

* [ISO 16612-2 grafisk teknologi](https://www.iso.org/standard/46428.html)


