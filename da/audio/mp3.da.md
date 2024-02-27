{
  "date": "2019-12-13",
  "keywords": [
"MP3",
"fil",
"udvidelse",
"format",
"Lyd",
"MPEG"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om MP3-filformater og API'er, der kan åbne og oprette MP3-filer.",
  "title": "MP3 - lydfilformat",
  "linktitle": "MP3",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-mp-da3"
}
},
  "lastmod": "2020-09-04"
}

## Hvad er en MP3-fil?

Filer med filtypenavnet .mp3 er digitalt kodede filformater til lydfiler, der formelt er baseret på MPEG-1 Audio Layer III eller MPEG-2 Audio Layer III. Det er udviklet af Moving Picture Experts Group (MPEG), der bruger Layer 3-lydkomprimering. Komprimering opnået med MP3-filformat er 1/10 af størrelsen af .WAV- eller .AIF-filer. Formatet giver fordele ved at streame sådanne lydfiler over internettet for at lytte online, hvilket tidligere ikke var muligt på grund af de store filstørrelser af lydfiler. Lydkvaliteten af en MP3-lydfil kan styres af parameterindstillinger såsom bitrate, sample rate, joint eller normal stereo.

## Kort historie om MP3-filformat

MP3-formatet blev opfundet og udviklet af et tysk firma, Fraunhofer-Gesellshart. Algoritmen har licenseret patenter for komprimeringsteknologi, den bruger. Her er en praktisk tidslinje for MP3:

• **1987** - Fraunhofer Instituttet i Tyskland begyndte at forske i højkvalitets lydkodning med lav bithastighed. Det blev kaldt EUREKA-projektet EU147, Digital Audio Broadcasting.

• **Januar 1988** - Moving Picture Experts Group, eller MPEG, blev etableret.

• **April 1989** - Fraunhofer modtog patent i Tyskland for MP3.

• **1992** - Dieter Seitzer, der hjalp med Fraunhofer med dens forskning, integrerede sin lydkodning med MPEG-1.

• **1993** - MPEG-1-standarden blev offentliggjort.

• **1994** - MPEG-2-standarden blev udviklet og udgivet et år senere.

• **nov. 26, 1996** - Det amerikanske patent for MP3 blev udstedt.

• **September 1998** - Fraunhofer begyndte at håndhæve patentrettigheder. Den, der brugte MP3-lydkodningen, betalte et licensgebyr til Fraunhofer.

• **Februar 1999** - SubPop, et pladeselskab, distribuerede musik i MP3-formatet, det første af disse firmaer til at gøre det.

• **1999** - De første bærbare MP3-afspillere dukker op.

## MP3 filformat

En MP3-fil består af MP3-rammer, hvor hver frame består af en header og en datablok. Rammerne er ikke uafhængige og kan normalt ikke udtrækkes ved vilkårlige rammegrænser. Filens datablokke indeholder information om lyden med hensyn til frekvenser og amplituder. Synkroniseringsordet i headeren identificerer begyndelsen af en gyldig ramme. Dette efterfølges af 3 bit, hvor den første bit viser, at det er en MPEG-standard, og de resterende 2 bit viser, at lag 3 er brugt; derfor MPEG-1 Audio Layer 3 eller MP3. Herefter vil værdierne variere afhængigt af MP3-filen.

[ISO](https://en.wikipedia.org/wiki/International_Organization_for_Standardization)/[IEC](https://en.wikipedia.org/wiki/International_Electrotechnical_Commission) 11172-3 definerer værdiintervallet for hver sektion af overskriften sammen med specifikationen af overskriften. De fleste MP3-filer i dag indeholder [ID3](https://en.wikipedia.org/wiki/ID3) [metadata](https://en.wikipedia.org/wiki/Metadata), som går forud for eller efter MP3-frames, som angivet i diagrammet. Datastrømmen kan indeholde en valgfri kontrolsum.

## Referencer ##

* [MP3 - af Wikipedia](https://en.wikipedia.org/wiki/MP3)


