{
   "date":"2023-10-11",
   "keywords":[
"chr",
"chr filen",
"chr cryengine karakterfil",
"hvordan man åbner en chr fil",
"fil",
"chr filtypenavn",
"udvidelse",
"fil"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"CHR-filformat - CryENGINE-tegnfil",
   "description":"Lær om CHR CryENGINE Character-filformat og API'er, der kan oprette og åbne CHR-filer.",
   "linktitle":"CHR CryENGINE",
   "menu":{
      "docs":{
         "identifier":"3d-chr-cryengine-da",
         "parent":"3d"
}
},
   "lastmod":"2023-10-11"
}

## Hvad er CHR fil?

CHR-fil i sammenhæng med CryENGINE refererer til en **CryENGINE Character File**. CryENGINE er spilmotor udviklet af Crytek, og disse filer bruges til lagring af karaktermodeller og tilhørende data til brug i videospil og andre realtidsapplikationer.

## CryENGINE-karakterfil

En CryENGINE Character File indeholder typisk følgende komponenter:

1.  **Karaktermodel**: Dette er en 3D-model af karakter, inklusive dens geometri, teksturer og animationer. Disse modeller er ofte skabt ved hjælp af software som Autodesk Maya eller Blender og derefter importeret til CryENGINE.
    
2.  **Animationsdata**: CryENGINE understøtter komplekse animationer til karakterer, så .chr-filen kan indeholde forskellige animationer såsom at gå, løbe, hoppe og mere. Disse animationer gemmes typisk som keyframe-data.
    
3.  **Rigging Information**: Rigging refererer til processen med at skabe skeletstruktur til karaktermodel, som gør det muligt at anvende animationer på modellen. .chr-filen kan indeholde information om knoglehierarki og hvordan karakterens mesh er forbundet med dette skelet.
    
4.  **Materiale- og teksturdata**: Oplysninger om materialer brugt på karaktermodeller og tilhørende teksturkort kan være inkluderet i .chr-filen. CryENGINE understøtter fysisk baseret gengivelse, så disse materialer kan være ret detaljerede.
    
5.  **Fysikdata**: Hvis karakteren er beregnet til at interagere med spilverdenen, kan .chr-filen indeholde fysikdata såsom kollisionsformer eller begrænsninger for ragdoll-fysik.
    
6.  **Konfigurationsindstillinger**: Forskellige konfigurationsindstillinger relateret til karakterens adfærd i spilverdenen, såsom AI-adfærd eller scriptede hændelser, kan også være en del af .chr-filen.

## CryENGINE

CryENGINE er en kraftfuld spilmotor udviklet af Crytek, tysk videospilfirma. Det er kendt for sine avancerede grafikmuligheder og er blevet brugt til at skabe nogle visuelt betagende og teknologisk avancerede videospil. Her er nogle nøglefunktioner og oplysninger om CryENGINE:

1.  **Grafik og gengivelse**: CryENGINE er kendt for sine avancerede grafikfunktioner. Den understøtter funktioner som global belysning i realtid, dynamisk belysning af høj kvalitet og skygger, fysisk baseret gengivelse (PBR) og højopløselige teksturer. Disse funktioner bidrager til at skabe visuelt betagende og realistiske spilverdener.
    
2.  **Physics Engine**: CryENGINE inkluderer en indbygget fysikmotor, der giver mulighed for realistiske interaktioner mellem objekter i spilverdenen. Den understøtter funktioner som stiv kropsfysik, blød kropsfysik og ragdoll-fysik, hvilket gør den velegnet til at skabe dynamiske og fordybende miljøer.
    
3.  **Terræn og vegetation**: CryENGINE giver værktøjer til at skabe store og detaljerede udendørsmiljøer. Det understøtter terrænredigering, vegetationsplacering og dynamiske vejrsystemer, hvilket giver udviklere mulighed for at skabe ekspansive og realistiske udendørs omgivelser.
    
4.  **Karakteranimation**: CryENGINE indeholder robuste værktøjer til karakteranimation. Det understøtter komplekse karakterrigger, ansigtsanimation og blandingstræsystem, der gør det muligt for udviklere at skabe naturtro karakterbevægelser og animationer.
    
5.  **AI-system**: Motoren har et AI-system, der giver mulighed for at skabe intelligente NPC'er (ikke-spillerfigurer) og fjendens AI. Udviklere kan skrive AI-adfærd og interaktioner for at skabe udfordrende og fordybende spiloplevelser.
       
6.  **Scripting**: CryENGINE bruger scriptsprog kaldet Schematyc, der giver udviklere mulighed for at skabe gameplaylogik og interaktioner. Derudover understøtter den C++ til mere avancerede programmeringsbehov.

## Filformater brugt af CryENGINE

Her er nogle af de almindelige filtyper forbundet med CryENGINE:

1.  **cryproj**: CryENGINE-projektfiler. Disse filer gemmer projektspecifikke indstillinger og konfigurationer for et bestemt spilprojekt.
    
2.  **.niveau**: Niveaufiler indeholder 3D-spilverdendata, inklusive terræn, objekter, belysning og andre niveauspecifikke indstillinger. Niveauer er grundlæggende komponent i spildesign i CryENGINE.
    
3.  **.cgf**: Karaktergeometri-format. Disse filer indeholder 3D-modeldata for karakterer, objekter og andre spilaktiver. CGF-filer kan omfatte geometri, teksturer og animationsdata.
    
4.  **.chrparams**: Karakterparameterfiler. Disse filer gemmer indstillinger og konfigurationer for karaktermodeller og deres animationer.
    
5.  **.dds**: DirectX teksturformat. CryENGINE bruger almindeligvis DDS-filer til at gemme teksturer, herunder diffuse kort, normale kort og andre teksturtyper.
    
6.  **.cryshader**: CryENGINE Shader-filer. Disse filer definerer, hvordan materialer og objekter gengives i spilverdenen, og specificerer shaders, materialeegenskaber og mere.
    
7.  **.crytif**: Teksturinformationsfil. Disse filer gemmer yderligere oplysninger om teksturer, såsom komprimeringsindstillinger, mipmaps og andre tekstur-relaterede detaljer.
    
8.  **.cdf**: Karakterdefinitionsfil. CDF-filer bruges til at definere karakteraktiver og deres egenskaber, herunder vedhæftede filer, animationstilstande og karakterrelaterede indstillinger.
    
9.  **.dds**: CryENGINE bruger også DDS-filer (DirectDraw Surface) til forskellige teksturkort, såsom normale kort, spejlende kort og diffuse kort.
    
10.  **.anim**: Animationsfiler. Disse filer gemmer animationsdata for karakterer og objekter, herunder keyframes, knoglepositioner og animationssekvenser.
    
11.  **.xml**: XML-filer kan bruges til forskellige konfigurationer og datadefinitioner i CryENGINE, såsom spillogik, AI-adfærd og mere.
    
12.  **.pak**: [PAK files](/game/pak/) er arkivfiler, der bruges til at pakke spilaktiver og -ressourcer, hvilket gør det mere effektivt til spildistribution og -indlæsning.

## Hvordan åbner jeg filen CHR?

Programmer, der åbner CHR filer inkluderer

- **Crytek CryENGINE SDK** (gratis prøveversion) til Windows

## Andre CHR filer

Her er andre filtyper, der bruger filtypen **.chr**.

**3D**
- [CHR - CryENGINE Character File](/3d/chr-cryengine/)
- [CHR - 3ds Max Characters File](/3d/chr-3ds/)

**Skrifttype og spil**
- [CHR - Borland Character Set](/font/chr/)
- [CHR - Doki Doki Literature Club! Character File](/game/chr-doki/)

## Referencer
- [CryEngine](https://en.wikipedia.org/wiki/CryEngine)

