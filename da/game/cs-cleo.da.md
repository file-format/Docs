{
   "date":"2023-01-04",
   "keywords":[
"cs",
"cs fil",
"cs cleo brugerdefineret script",
"hvordan man åbner en cs-fil",
"fil",
"cs filtypenavn",
"udvidelse",
"fil"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"CS-filformat - CLEO Custom Script",
   "description":"Lær om CS CLEO Custom Script-format og API'er, der kan oprette og åbne CS-filer.",
   "linktitle":"CS CLEO",
   "menu":{
      "docs":{
         "identifier":"game-cs-cleo-da",
         "parent":"game"
}
},
   "lastmod":"2023-01-04"
}

## Hvad er en CS fil?

En .CS-fil i sammenhæng med CLEO (forkortelse for CLEO Library) refererer typisk til en brugerdefineret scriptfil, der bruges i Grand Theft Auto (GTA)-serien af videospil. CLEO er et populært modding-framework, der giver spillere mulighed for at oprette og tilføje brugerdefinerede scripts til GTA-spil, så de kan ændre gameplay, tilføje nye funktioner og forbedre den overordnede spiloplevelse.

## Oversigt over CS-fil

Her er en grundlæggende oversigt over, hvad en .cs-fil i CLEO kan indeholde:

1.  **Scriptkode**: En .cs-fil indeholder scriptkode skrevet i CLEO-scriptsprog. Dette scriptsprog er specifikt for CLEO og bruges til at definere opførsel af brugerdefinerede scripts i spillet. Koden kan skrives ved hjælp af en teksteditor, og den følger typisk en bestemt syntaks.
    
2.  **Modifications**: CLEO scripts can make various modifications to game such as changing behavior of in-game objects, creating custom missions, adding new vehicles, weapons and more. The possibilities are extensive and depend on creativity and programming skills of script author.
    
3.  **Triggere**: CLEO-scripts inkluderer ofte triggere, der bestemmer, hvornår og hvordan tilpasset script skal køre. Disse udløsere kan være baseret på begivenheder i spillet, spillerhandlinger eller specifikke forhold.
    
4.  **Variabler og funktioner**: CLEO-scripts kan bruge variabler til at gemme og manipulere data, samt funktioner til at indkapsle og genbruge kode. Disse variabler og funktioner bruges til at kontrollere scriptets adfærd.

## Eksempel på CS-fil

Her er et simpelt eksempel på et CLEO .cs-script, der ændrer vejret i spillet:

```
{$CLEO .cs}

03A4: name_thread 'WEATHER'

:WEATHER_LOOP
    // Change the weather to sunny
    0085: 0@ = 11 // Weather ID for sunny weather
    00D8: mission_cleanup
    0051: return 0@ // Exit the script

// Add more code and conditions as needed
```

## CLEO bibliotek

**CLEO Library**, ofte blot omtalt som CLEO, er en populær og kraftfuld modding-ramme for Grand Theft Auto (GTA)-serien af videospil. Det giver spillere og moddere mulighed for at oprette og tilføje brugerdefinerede scripts til GTA-spil, så de kan ændre gameplay, tilføje nye funktioner og forbedre den overordnede spiloplevelse. CLEO er især kendt for sin fleksibilitet og brugervenlighed i GTA modding-fællesskabet.

Her er nogle nøglefunktioner og aspekter af CLEO Library:

1.  **Scriptsprog**: CLEO introducerer sit scriptsprog, som er specifikt for modding framework. Scriptsproget er designet til at være relativt nemt at forstå og arbejde med at gøre det tilgængeligt for både nybegyndere og erfarne moddere.
    
2.  **Tilpassede scripts**: Med CLEO kan du oprette brugerdefinerede scripts, der kan udføre en lang række funktioner i spilverdenen. Disse scripts kan ændre adfærd i spillet, tilføje nye missioner, introducere nye køretøjer eller våben, ændre spillets fysik og meget mere.
    
3.  **Triggere og begivenheder**: CLEO-scripts kan udløses af forskellige begivenheder i spillet, spillerhandlinger eller specifikke forhold. Dette giver modders mulighed for at skabe dynamisk og interaktivt indhold i spillet.
    
4.  **Support for Multiple GTA Versions**: CLEO has versions tailored to different GTA games, including GTA III, GTA Vice City, GTA San Andreas, GTA IV and others. This means that modders can create and share their custom scripts for different GTA titles.

## Filformater brugt af CLEO Library

I CLEO modding til Grand Theft Auto (GTA) spil bruges flere filformater almindeligvis til at oprette og installere mods. Disse filformater tjener forskellige formål fra at indeholde egentlige scripts til at gemme yderligere ressourcer såsom teksturer, modeller eller lyd. Her er nogle af de vigtigste filformater, der bruges i CLEO modding:

1.  **.cs (Custom Script)**: CLEO .cs-filer er brugerdefinerede script-filer skrevet i CLEO-scriptsprog. Disse filer indeholder kode, der definerer adfærd og funktionalitet af mod. .cs-filer er kernen i CLEO-modding og udføres af spil for at implementere brugerdefinerede funktioner.
    
2.  **.csa (Custom Script Archive)**: .csa-filer er arkiver, der kan gemme flere .cs-scriptfiler. De bruges ofte til at pakke relaterede scripts sammen for lettere installation og administration.
    
3.  **.fxt (tekstfiler)**: .fxt-filer er tekstfiler, der kan bruges til at lokalisere eller levere tekstoversættelser til CLEO-mods. De indeholder tekststrenge, der kan vises i spillet, hvilket gør mods tilgængelige for spillere på forskellige sprog.
    
4.  **[.bmp](/image/bmp/), [.png](/image/png/), [.jpg](/image/jpeg/) (Billedformater)**: Disse billedformater bruges til at gemme teksturer og billeder til mods. De kan bruges til brugerdefinerede skins, køretøjsteksturer, HUD-elementer og mere. Afhængigt af spil kan forskellige billedformater foretrækkes.

## Hvordan åbner jeg filen CS?

For at åbne og se indholdet af en CLEO .cs (Custom Script) fil, kan du bruge en teksteditor eller kodeeditor efter eget valg. Fælles valg omfatter:

- **Notesblok**: En simpel teksteditor, der leveres forudinstalleret med Windows.
- **Notesblok++**: En mere funktionsrig teksteditor designet til kodning og scripting.
- **Visual Studio Code**: En populær, gratis og meget udvidelsesbar kodeeditor.
- **Sublim tekst**: Endnu en kodeeditor kendt for sin hastighed og alsidighed.
- **Atom**: En åben kildekode-editor udviklet af GitHub.

## Andre CS-filer

Her er andre filtyper, der bruger filtypen **.cs**.

**Datafiler og spil**
- [CS - ColorSchemer Studio Color Scheme](/data/cs-colorschemer/)
- [CS - CLEO Custom Script](/game/cs-cleo/)

**Programmering**
- [CS - CSharp Code File](/programming/cs/)

## Referencer
* [CLEO-bibliotek](https://cleo.li/)


