{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TEX filformat",
  "description": "Lær om TEX-filformat og API'er, der kan oprette og åbne TEX-filer.",
  "linktitle": "TEX",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-te-dax"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en TEX-fil? ##

**TeX** er et sprog, der består af programmering samt mark-up funktioner, der bruges til at sætte dokumenter på. Donald Knuth fra Stanford University, er skaberen af dette ressourcestærke sættesystem. Over hele verden er TeX det ultimative valg blandt forfattere og udgivere til at producere tekniske dokumenter af høj kvalitet. TeX udfører et fremragende stykke arbejde med at formatere komplekse matematiske udtryk. Sammen med en fotosætter af høj kvalitet konkurrerer TeX om resultaterne, der genereres af de bedste traditionelle sættesystemer. Derfor betragtes som de mest klassiske digitale typografiske systemer.

TeX-inputfiler er baseret på ASCII-kode, hvilket giver mulighed for manuskriptdeling mellem forfattere, forlagsledere og kritikere. En bred vifte af computermiljøer, næsten alle moderne platforme og mange ældre platforme understøtter TeX. Desuden er TeX en gratis software, tilgængelig for en bred vifte af forbrugere. Mange UNIX-installationer bruger både UNIX troff og TeX som deres formateringssystem til forskellige formål. Andre typesætningsopgaver udføres enormt i form af LaTeX, ConTeXt og andre makropakker.

## Kort historie ##

TeX was designed and written by Donald Knuth in 1978. Guy Steele fra Massachusetts Institute of Technology reviderede input/output af TeX for at få det til at køre under det inkompatible operativsystem som Timesharing System (ITS). Den første version af TeX blev udviklet under Stanfords WAITS-operativsystem i programmeringssproget (SAIL) og testet til at køre på en PDP-10. Knuth introducerede ideen om læsefærdig programmering til avancerede versioner. Litterær programmering er en måde at generere kompilerbar kildekode og typesæt (i TeX) til tværbundet dokumentation ved hjælp af den originale fil. Sproget, der bruges til at udvikle disse avancerede versioner af TeX, kaldes WEB, en blanding af DEC PDP-10 Pascal-programmer for at sikre portabilitet.

A revised new version of TeX published in 1982 and was called TeX82. Den største ændring er udskiftningen af den originale orddelingsalgoritme med den nyskrevne algoritme af Frank Liang. For at sikre portabilitet på tværs af forskellige platforme, i stedet for at bruge flydende komma, bruger TeX82 aritmetik med fast punkt sammen med et ægte, turing-komplet programmeringssprog. I 1989 blev en ny version af TeX og Metafont udgivet. Så version 3.0 af TeX letter 8-bit input, hvilket tillader 256 forskellige tegn i teksten. Efter version 3 er opdateringer angivet ved at tilføje et ekstra ciffer i slutningen af decimalen, f.eks. er den aktuelle version af TeX angivet som 3.14159265. Denne version blev sidst opdateret 12-1-2014.

## TeX-input ##

En inputfil til TEX kan udarbejdes med en teksteditor ved brug af almindelig tekst. I modsætning til en typisk tekstbehandler tillader denne inputfil usynlige kontroltegn. En fil kan indlejres i en anden fil, der indeholder makrodefinitioner og hjælpedefinitioner, der forbedrer TeX's muligheder. Hvis en TeX-installation leveres med makrofiler, viser de lokale oplysninger om TeX brugen af makrofiler. Standardformen af TeX, integrerer en kombination af makroer og andre definitioner kendt som almindelig TEX.

På grundlag af præcis viden om størrelsen af alle tegn og symboler, beregner den den optimale organisering af bogstaver pr. linje og linjer pr. side. På tidspunktet for dokumentbehandlingen produceres en .dvi-fil, hvor dvi står for enhedsuafhængig. Enhedsdriverprogrammer er nødvendige for at udskrive eller se et eksempel på dokumentet med en dvi-udvidelse. I dag omgås dvi-generering af en almindeligt brugt pdf-TeX. Ingen forhåndskendskab til skrifttyper er tilgængelig inden for TeX-installation, så eksterne skrifttypefiler, som er en del af det lokale TeX-miljø, bruges til at indhente information til dokument.

## Sættesystem ##

Omkring 300 primitiver (kommandoer) kan forstås af basis TeX-systemet. Primitiver er kommandoer på lavt niveau, derfor brugte en almindelig bruger dem sjældent direkte, og den meste funktionalitet udføres af formatfiler. Disse formatfiler er forudindlæste hukommelsesbilleder af TeX, som efterfølges af indlæsning af store makrosamlinger. Det originale standardformat for sproget, dvs. almindelig TeX, tilføjer omkring 600 kommandoer.

En omvendt skråstreg grupperet med krøllede klammeparenteser angiver starten af TeX-kommandoer. Da TeX er et makro- og tokenbaseret sprog, kan næsten alle TeX's syntaktiske karakteristika ændres under kørsel, inklusive brugerdefinerede, undtagen uudvidelige tokens, som derefter udføres. Selve udvidelsen er praktisk talt problemfri. Nogle kommandoer skal komme efter et argument, der hjælper med at forklare en kommandos funktion. For eksempel dirigerer kommandoen \vskip TEX til at springe ned/op på siden efterfulgt af et argument, der bestemmer, hvor meget plads der skal springes over.

## Versioner ##

LaTeX er det mest brugte format, som oprindeligt er udviklet af Leslie Lamport. LaTeX integrerer forskellige dokumentstile til filer, breve, bøger og dias og tilbyder referencer og automatisk nummerering for forskellige sektioner og matematiske udtryk. AMS-TeX er et andet populært format, udviklet af American Mathematical Society.

AMS-TeX tilbyder meget mere brugervenlige kommandoer, som kan omdefineres af journaler, så de passer til deres lokale stil. LaTeX kan udnytte fordelene ved AMS-TeX ved at bruge AMS pakkerne, som så betegnes som AMS-LaTeX. ConTeXt er et andet format skrevet af Hans Hagen, der hovedsageligt bruges til desktop publishing.

TeX-softwaren tilbyder adskillige funktioner, der var utilgængelige eller af lavere kvalitet i andre sætningssystemer på tidspunktet for dens oprettelse. Nogle af de innovative egenskaber ved dette sprog er baseret på interessante algoritmer udledt af afhandlinger fra Knuths elever. Mens andre sætningsprogrammer nu inkorporerer nyttige funktioner fra TeX i deres programmer.

## Referencer ##

* [TeX-typeindstillingssystem](https://en.wikipedia.org/wiki/TeX)


