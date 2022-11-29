{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PDF/VT-filformat",
  "description":"Läs mer om PDF/VT-filformat och API:er som kan skapa och öppna PDF/VT-filer.",
  "linktitle" : "PDF/VT",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# Vad är PDF/VT? #

PDF/VT, publicerad som [ISO 16612-2](https://www.iso.org/standard/46428.html) i augusti 2010 som standard, är utformad för att möjliggöra variabel dokumentutskrift (VDP) i en mängd olika miljöer. Standarden gör Variabel information och Transaktionell utskrift som grund för standarden. Variabel datautskrift används där en del av informationen är olika för varje mottagare av innehållet. Transaktionsutskriften inkluderar fakturor, kontoutdrag och andra dokument som kombinerar faktureringsinformation med marknadsföringsinformation. Detta resulterar i en blandning av förbättrad bearbetning av bilder, text och andra innehållstyper. PDF/VT möjliggör tillförlitlig och dynamisk hantering av sidor för HVTO-utskriftsdata (High Volume Transactional Output) genom att använda DPM-konceptet (Document Part Metadata). PDF/VT-filer kan öppnas i Adobe Acrobat Viewer utan att behöva lägga till någon annan komponent.

## Dokumentdelhierarki ##

Dokumentdelhierarkin (DPart) är som en trädstruktur av dokumentdelnoder som är baserad på alla sidor i dokumentet. Elementen i detta träd kallas DPart-noder. Varje intern nod innehåller andra DPart-noder och varje bladnod anger en eller flera sidor för en mottagare. I huvudsak specificerar DPart-hierarkin sekvensen och förhållandet mellan dokument eller dokument i en PDF/VT-fil. Trädstrukturen för DPart-noder representerar enkelt det interna innehållet i ett PDF/VT-dokument eftersom det kan innehålla underdokument för många mottagare och varje dokumentdel motsvarar sidorna för en enskild mottagare. DPart-hierarkin krävs i PDF/VT-filer.

## Document Part Metadata (DPM) ##

Document Part Metadata (DPM) är associerad med varje nod i dokumentdelhierarkin och kan användas för att kommunicera information om en viss mottagares underdokument och dess delar. I synnerhet kan DPM innehålla information om egenskaperna eller information om mottagarna i en kodad form.

## Överensstämmelsenivåer ##

PDF/VT tilldelas följande tre överensstämmelsenivåer. Dessa är alla baserade på [PDF](/sv/pdf/) 1.6.

* `PDF/VT-1` - Den är baserad på PDF/X-4 och innehåller alla resurser som krävs för att rendera ett PDF-dokument.
* `PDF/VT-2` - Designad för utbyte av flera filer, PDF/VT-2-dokument kan referera till externa utdata, externt innehåll eller båda. Ett PDF/VT-dokument och alla dess refererade PDF-filer och externa utdata kallas tillsammans en PDF/VT-2-filuppsättning. Acrobat 9 och stöder denna funktion.
* `PDF/VT-2s` - Stöder PDF/VT-2 livestreaming. Detta gör att segmenterade delar av data kan bearbetas.

## Referenser ##

* [PDF/VT - Av Wikipedia](https://en.wikipedia.org/wiki/PDF/VT)
* [ISO 16612-2 grafisk teknik](https://www.iso.org/standard/46428.html)

