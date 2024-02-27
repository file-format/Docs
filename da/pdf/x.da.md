{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PDF/X filformat",
  "description": "Lær om PDF/X-filformat og API'er, der kan oprette og åbne PDF/X-filer.",
  "linktitle": "PDF/X",
  "menu": {
    "docs": {
      "parent": "pdf",
      "identifier": "pdf--dax"
}
},
  "lastmod": "2019-09-10"
}

# Hvad er PDF/X-fil? #

PDF/X er en ISO 15930-standard udgivet i 2001 med en undergruppe af PDF-funktionalitet. Standarden blev etableret og udgivet på baggrund af specifikke krav fra trykkeri- og forlagsindustrien. Kravene til denne standard blev alle udformet i henhold til de forskellige behov i trykkeri- og forlagsindustrien. PDF/X kræver, at de overensstemmende filer er fuldstændige, dvs. selvstændige. Dette kræver, at elementer som skrifttyper, der bruges på siden, skal være en del af dokumentet. Indhold såsom 3D eller video kan ikke være en del af PDF/X-dokument. Oplysningerne i PDF/X-dokumentet kræver, at de er nøjagtige.

## PDF/X-standarder og revisioner ##

PDF/X-familien af standarder består af flere versioner, der hver er designet til et specialiseret resultat. Udviklingen af disse standarder havde til formål at imødekomme de mange forskellige behov i trykkeri- og forlagsindustrien.

* `PDF/X-1a` - Også kendt som den første standard i PDF/X-familien, kræver PDF/X-1a, at alt indhold er en del af PDF-dokumentet for at kunne udskrives. Dokumentelementer såsom skrifttyper, formularer, adgangskodebeskyttelse og synlige anmærkninger er ikke tilladt. PDF/X-1a har sine egne specifikke krav såvel som dem, der vedrører gennemsigtighed, og lag er tilladt. Disse kræver også, at printelementer kun bruger CMYK, gråtoner eller staffagefarver, hvilket resulterer i ingen brug af RGB eller enhedsuafhængige farverum. er til udvekslinger, hvor alle filer skal leveres i CMYK (og/eller staffagefarver), uden RGB eller farvestyrede data. PDF/X-1a omtales også som komplet udveksling på grund af fuldstændigheden af de oplysninger, der kræves af

* `PDF/X-3` - blev introduceret i 2002 og ophævede mange begrænsninger for PDF/X-1a. Dette gjorde det muligt for grafik i en PDF/X-3 at bruge CMYK, grescale, RGB, Lab og ICC-baserede farverum. Det er faktisk baseret på PDF-standarder 1.3 med [ICC-profil](https://en.wikipedia.org/wiki/ICC_Profile). Det omtales også som farvestyring på grund af den fleksibilitet og regler, det introducerer i forbindelse med farver, der er inkluderet i et PDF-dokument.

* `PDF/X-4` - understøtter transparenter, så PDF-X/4 indeholder alle data, der kræves til output uden at udfladning.

* `PDF/X-5` - er baseret på PDF/X-4, der tilføjer understøttelse af ekstern grafik via reference XObjects, såvel som eksterne n-farvestof profiler til gengivelse. Brug den til delvis udveksling af printdata ved hjælp af PDF-version 1.6


## Referencer ##

* [PDF/X - Af Wikipedia](https://en.wikipedia.org/wiki/PDF/X)


