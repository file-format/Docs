{
   "date":"2023-07-18",
   "keywords":[
"PAR",
"PAR fil",
"hvordan man åbner en par fil",
"fil",
"PAR filtypenavn",
"udvidelse",
"fil"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"PAR-filformat - Parchive Index File",
   "description":"Lær om PAR-format og API'er, der kan oprette og åbne PAR-filer.",
   "linktitle":"PAR",
   "menu":{
      "docs":{
         "identifier":"compression-par-da",
         "parent":"compression"
}
},
   "lastmod":"2023-07-18"
}

## Hvad er PAR fil?

I Parchive (PAR)-arkiver refererer en .par-fil til en indeksfil, der indeholder en gruppe paritetsvolumener eller paritetsblokke. Denne indeksfil bruges til fejlfinding og gendannelsesformål, når en eller flere filer i arkivet går tabt eller beskadiges.

Et arkivarkiv består typisk af både de originale datafiler og de tilsvarende paritetsvolumener. Paritetsvolumener oprettes ved hjælp af Reed-Solomon fejlkorrektionsalgoritmer. Disse paritetsvolumener indeholder redundant information, der kan bruges til at gendanne de originale datafiler.

.par-filen, også kendt som et paritetsvolumensæt, indeholder oplysninger om strukturen og placeringen af paritetsvolumenerne i arkivet. Det fungerer som et indeks eller et kort for gendannelsesprocessen. Ved at bruge .par-filen kan specialiseret PAR-software bestemme, hvilke paritetsvolumener der er nødvendige, og hvordan de skal bruges til at rekonstruere de manglende eller beskadigede filer.

Når en eller flere filer i Parchive-arkivet bliver utilgængelige eller korrupte, kan .par-filen bruges sammen med de tilgængelige paritetsvolumener til at gendanne de tabte data. PAR-softwaren læser .par-filen, identificerer de manglende eller beskadigede filer og bruger paritetsvolumener til at rekonstruere dem.

## Hvordan åbner jeg filen PAR?

For at åbne og bruge .par-filer skal du have specialiseret PAR-software. Her er et par populære softwaremuligheder, der kan håndtere .par-filer:

- **QuickPar:** QuickPar er en meget brugt PAR-software til Windows. Det giver dig mulighed for at oprette, verificere og reparere PAR-filer. Du kan åbne en .par-fil i QuickPar for at bekræfte dens integritet eller bruge den til at reparere beskadigede eller manglende filer i et Parchive-arkiv.

- **MultiPar:** MultiPar er en anden populær PAR-software tilgængelig til Windows. Det understøtter både PAR- og PAR2-filformater og giver avancerede funktioner til oprettelse, verifikation og reparation af arkiver. MultiPar kan åbne .par-filer og udføre fejlfinding og gendannelsesoperationer baseret på de angivne paritetsvolumener.

- **MacPAR deLuxe:** MacPAR deLuxe er en PAR-software designet specielt til macOS. Det understøtter PAR- og PAR2-filformater og giver lignende funktionalitet som QuickPar og MultiPar. MacPAR deLuxe kan åbne .par-filer og hjælpe med at verificere arkiver og gendanne beskadigede eller manglende filer.

## PAR-filformat - flere oplysninger

PAR-filformatet, almindeligvis omtalt som Parchive, er et specifikt filformat, der bruges til at skabe paritetsdata og udføre fejlfinding og -gendannelse i filarkiver. PAR-filformatet består typisk af tre typer: PAR, PAR2 og PAR3.

- **PAR:** Det originale PAR-filformat, også kendt som PAR1, blev udviklet af Parchive-projektet. Det inkluderer paritetsdata genereret fra de originale datafiler. PAR-filer giver et grundlæggende niveau for fejlfinding og -gendannelse, men har begrænsninger med hensyn til fejlkorrektionsmuligheder.

- **PAR2:** PAR2 er en forbedret version af PAR-filformatet. Det tilbyder mere avancerede fejlkorrektionsfunktioner og forbedrede gendannelsesfunktioner. PAR2-filer bruges typisk til at skabe paritetsdata, der kan gendanne tabte eller beskadigede filer i et arkiv. PAR2-filer giver bedre beskyttelse mod datakorruption og bruges i vid udstrækning til filarkivering.

- **PAR3:** PAR3 is the latest version of the PAR file format and provides further improvements in error correction and recovery. It offers even higher levels of redundancy and error correction capabilities compared to PAR2. PAR3-filer er designet til at give mere robuste beskyttelses- og gendannelsesmuligheder for data, der er gemt i arkiver.

Både PAR2- og PAR3-filformater understøttes bredt af PAR-software og giver mulighed for at verificere integriteten af filer i et arkiv og gendanne tabte eller beskadigede data. PAR- og PAR2-filer er stadig almindeligt anvendte, mens PAR3-filer gradvist er ved at blive adopteret på grund af deres forbedrede fejlrettelsesmuligheder.

## Referencer
* [Parchive](https://en.wikipedia.org/wiki/Parchive)


