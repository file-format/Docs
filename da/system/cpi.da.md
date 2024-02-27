{
   "date":"2023-10-18",
   "keywords":[
"cpi",
"cpi fil",
"cpi kodetabel informationsfil",
"hvordan man åbner en cpi-fil",
"fil",
"cpi filtypenavn",
"udvidelse",
"fil"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"CPI-filformat - kodetabelinformationsfil",
   "description":"Lær om CPI Codepage Information filformat og API'er, der kan oprette og åbne CPI filer.",
   "linktitle":"CPI",
   "menu":{
      "docs":{
         "identifier":"system-cpi-da",
         "parent":"system"
}
},
   "lastmod":"2023-10-18"
}

## Hvad er en CPI fil?

En `.cpi`-fil i forbindelse med Microsoft Windows- og DOS-operativsystemer er typisk **Kodesideinformationsfil.** Disse filer indeholder oplysninger om tegntabel, der bruges til tekstkodning og tegnsættilknytning. Kodesider er afgørende for visning og behandling af tekst på forskellige sprog og tegnsæt.

I sammenhæng med Windows og DOS bruges tegntavler til at definere, hvordan tegn repræsenteres og kodes på forskellige sprog og områder. Disse kodesider bestemmer, hvordan tegn gemmes i hukommelsen og vises på skærmen. Hver tegntabel har en unik identifikator, og `.cpi`-filer gemmer oplysninger om disse kodesider, herunder detaljer som tegntilknytninger og skrifttypeoplysninger.

`.cpi`-filer findes almindeligvis i Windows- eller DOS-systemmapper, og de spiller en afgørende rolle for at gøre det muligt for operativsystemet at vise tekst korrekt for forskellige lokaliteter og tegnsæt. De hjælper systemet med at forstå, hvordan man fortolker og gengiver tegn fra forskellige sprog og kodninger.

## Kodesideinformationsfiler

Lad os se nærmere på Code Page Information Files (.cpi), og hvordan de fungerer inden for rammerne af MS-DOS og tidligere iterationer af Microsoft Windows:

1.  **Tegnkodning og kodesider**: Kodesider er en kritisk komponent i, hvordan tekst kodes og vises på computeren. De definerer tegnkodning for specifikt sprog eller tegnsæt. Hver tegntabel tildeler numeriske værdier (kodepunkter) til tegn, så computeren kan repræsentere og vise dem. For eksempel bruges tegntabel 437 almindeligvis i USA og Vesteuropa, mens tegntabel 850 bruges til Latin-1-kodning.
    
2.  **Systeminitialisering**: Under systeminitialisering (når computeren starter), vil MS-DOS og ældre versioner af Windows læse `.cpi`-filer for at bestemme, hvilke kodesider der skal understøttes. Disse oplysninger var afgørende for tekstgengivelse, tastaturinput og tegnsætkonverteringer.
    
3.  **Skærm- og tastaturunderstøttelse**: Disse filer giver information om, hvordan tegn skal vises på skærmen, og hvilke tegnsæt eller tegntavler, der skal understøttes til tastaturinput. Forskellige kodesider definerer forskellige tegnsæt, så disse filer hjælper operativsystemet med at vide, hvordan man håndterer brugerinput og viser tekst korrekt.
    
4.  **Lokalisering**: `.cpi`-filer er afgørende for lokalisering af operativsystemet. De gør det muligt for systemet at tilpasse sig forskellige sprog, regioner og tegnsæt, hvilket gør det muligt for brugere over hele verden at bruge MS-DOS eller Windows på deres foretrukne sprog.
    
5.  **Flere `.cpi`-filer**: På computere med flersproget understøttelse kan du finde flere `.cpi`-filer, der svarer til forskellige kodesider. For eksempel kan systemet have `437.cpi` for USA, `850.cpi` for Latin-1, `852.cpi` for Centraleuropa og så videre. Den relevante fil indlæses baseret på brugerens lokalitet eller valgte tegntabel.
    
6.  **Skrifttypeoplysninger**: Ud over tegntilknytninger kan disse filer indeholde skrifttypeoplysninger, der angiver, hvilke skrifttyper der skal bruges til hver tegntabel. Dette er vigtigt for at gengive tekst i passende stil og størrelse.
    
7.  **Ældre systemer**: `.cpi`-filer var mere almindelige i ældre versioner af MS-DOS og Windows. Moderne Windows-versioner (såsom Windows 10 og nyere) bruger typisk Unicode til tekstkodning, som understøtter en bred vifte af tegn og sprog. Unicode forenkler tekstbehandling til flersprogede miljøer og er standard for moderne software.

## Hvordan åbner jeg filen CPI?

Åbning af .CPI (Code Page Information) fil er ikke typisk brugerhandling, og disse filer er generelt ikke beregnet til at blive åbnet manuelt. De bruges af operativsystemet til at administrere tekstkodning og tegnsæt, og deres indhold tilgås og bruges automatisk af systemet.

Men hvis du er interesseret i at se indholdet af .CPI-filen til informationsformål, kan du prøve at åbne den med teksteditor eller hexadecimal viewer. Sådan kan du forsøge at åbne .CPI-filen:

1.  **Teksteditor**: Du kan bruge teksteditor som Notesblok (på Windows) eller enhver almindelig teksteditor på andre operativsystemer til at åbne og se .CPI-fil. Husk, at indholdet af .CPI-filer ikke er beregnet til at være læseligt af mennesker, og du kan se serier af tegn, der er svære at fortolke.
    
2.  **Hexadecimal Viewer**: En hexadecimal viewer eller hex-editor kan bruges til at åbne og inspicere indholdet af .CPI-filen i dens rå binære form. Hex-editorer giver en mere detaljeret visning af filens data, hvilket kan være nyttigt, hvis du forsøger at forstå dens struktur. Eksempler på sådan software omfatter HxD, Hex Fiend (til macOS) og 010 Editor.

## Andre CPI-filer

Her er andre filtyper, der bruger filtypen **.cpi**.

**Video og system**
- [CPI - AVCHD Video Clip Information](/video/cpi/)
- [CPI - Codepage Information File](/system/cpi/)

## Referencer
* [Kodeside](https://en.wikipedia.org/wiki/Code_page)


