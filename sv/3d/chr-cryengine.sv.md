{
"datum":"2023-10-11",
   "keywords":[
"chr",
"chr-fil",
"chr cryengine teckenfil",
"hur man öppnar en chr-fil",
"fil",
"chr filtillägg",
"förlängning",
"fil"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"utkast":"falskt",
"toc":true,
"title":"CHR-filformat - CryENGINE-teckenfil",
   "description":"Läs mer om CHR CryENGINE Character-filformat och API:er som kan skapa och öppna CHR-filer.",
"linktitle":"CHR CryENGINE",
   "menu":{
      "docs":{
         "identifier":"3d-chr-cryengine",
         "parent":"3d"
}
},
"lastmod":"2023-10-11"
}

## Vad är en CHR fil?

CHR-fil i CryENGINE-sammanhang hänvisar till en **CryENGINE Character File**. CryENGINE är en spelmotor utvecklad av Crytek och dessa filer används för att lagra karaktärsmodeller och tillhörande data för användning i videospel och andra realtidsapplikationer.

## CryENGINE karaktärsfil

En CryENGINE-teckenfil innehåller vanligtvis följande komponenter:

1. **Teckenmodell**: Detta är en 3D-modell av karaktär, inklusive dess geometri, texturer och animationer. Dessa modeller skapas ofta med programvara som Autodesk Maya eller Blender och importeras sedan till CryENGINE.
    




















2. **Animationsdata**: CryENGINE stöder komplexa animationer för karaktärer, så ".chr"-filen kan innehålla olika animationer som att gå, springa, hoppa och mer. Dessa animationer lagras vanligtvis som nyckelbilddata.
    




















3. **Riggningsinformation**: Riggning avser processen att skapa skelettstruktur för karaktärsmodell, vilket gör att animationer kan appliceras på modellen. ".chr"-filen kan innehålla information om benhierarki och hur karaktärens mesh är kopplat till detta skelett.
    




















4. **Material- och texturdata**: Information om material som används på karaktärsmodeller och tillhörande texturkartor kan inkluderas i ".chr"-filen. CryENGINE stöder fysiskt baserad rendering, så dessa material kan vara ganska detaljerade.
    




















5. **Fysikdata**: Om karaktären är avsedd att interagera med spelvärlden kan ".chr"-filen innehålla fysikdata som kollisionsformer eller begränsningar för ragdoll-fysik.
    




















6. **Konfigurationsinställningar**: Olika konfigurationsinställningar relaterade till karaktärens beteende i spelvärlden, såsom AI-beteende eller skriptade händelser, kan också vara en del av ".chr"-filen.

## CryENGINE

CryENGINE är en kraftfull spelmotor utvecklad av Crytek, tyskt videospelsföretag. Det är känt för sina banbrytande grafikmöjligheter och har använts för att skapa några visuellt fantastiska och tekniskt avancerade videospel. Här är några viktiga funktioner och information om CryENGINE:

1. **Grafik och rendering**: CryENGINE är känt för sina avancerade grafikfunktioner. Den stöder funktioner som global belysning i realtid, högkvalitativ dynamisk belysning och skuggor, fysiskt baserad rendering (PBR) och högupplösta texturer. Dessa funktioner bidrar till att skapa visuellt fantastiska och realistiska spelvärldar.
    




















2. **Physics Engine**: CryENGINE inkluderar en inbyggd fysikmotor som möjliggör realistiska interaktioner mellan objekt i spelvärlden. Den stöder funktioner som stel kroppsfysik, mjuk kroppsfysik och ragdoll-fysik, vilket gör den lämplig för att skapa dynamiska och uppslukande miljöer.
    




















3. **Terräng och vegetation**: CryENGINE tillhandahåller verktyg för att skapa stora och detaljerade utomhusmiljöer. Den stöder terrängredigering, vegetationsplacering och dynamiska vädersystem, vilket gör att utvecklare kan skapa expansiva och realistiska utomhusmiljöer.
    




















4. **Teckenanimering**: CryENGINE innehåller robusta verktyg för karaktärsanimering. Den stöder komplexa karaktärsriggar, ansiktsanimationer och blandningsträdsystem som gör det möjligt för utvecklare att skapa verklighetstrogna karaktärsrörelser och animationer.
    




















5. **AI-system**: Motorn har ett AI-system som gör det möjligt att skapa intelligenta NPC:er (icke-spelare) och fiendens AI. Utvecklare kan skriva AI-beteende och interaktioner för att skapa utmanande och uppslukande spelupplevelser.
       





















6. **Skript**: CryENGINE använder skriptspråk som kallas "Schematyc" som låter utvecklare skapa spellogik och interaktioner. Dessutom stöder den C++ för mer avancerade programmeringsbehov.

## Filformat som används av CryENGINE

Här är några vanliga filtyper associerade med CryENGINE:

1. **cryproj**: CryENGINE-projektfiler. Dessa filer lagrar projektspecifika inställningar och konfigurationer för ett visst spelprojekt.
    




















2. **.nivå**: Nivåfiler innehåller 3D-spelvärldsdata, inklusive terräng, objekt, belysning och andra nivåspecifika inställningar. Nivåer är en grundläggande del av speldesign i CryENGINE.
    




















3. **.cgf**: Teckengeometriformat. Dessa filer innehåller 3D-modelldata för karaktärer, objekt och andra speltillgångar. CGF-filer kan innehålla geometri, texturer och animationsdata.
    




















4. **.chrparams**: Filer med teckenparametrar. Dessa filer lagrar inställningar och konfigurationer för karaktärsmodeller och deras animationer.
    




















5. **.dds**: DirectX Texture Format. CryENGINE använder vanligtvis DDS-filer för att lagra texturer, inklusive diffusa kartor, normala kartor och andra texturtyper.
    




















6. **.cryshader**: CryENGINE Shader-filer. Dessa filer definierar hur material och objekt renderas i spelvärlden, och specificerar shaders, materialegenskaper och mer.
    




















7. **.crytif**: Texturinformationsfil. Dessa filer lagrar ytterligare information om texturer, såsom komprimeringsinställningar, mipmaps och andra texturrelaterade detaljer.
    




















8. **.cdf**: Teckendefinitionsfil. CDF-filer används för att definiera karaktärstillgångar och deras egenskaper, inklusive bilagor, animeringstillstånd och karaktärsrelaterade inställningar.
    




















9. **.dds**: CryENGINE använder även DDS-filer (DirectDraw Surface) för olika texturkartor, såsom normala kartor, spegelkartor och diffusa kartor.
    




















10. **.anim**: Animationsfiler. Dessa filer lagrar animationsdata för karaktärer och objekt, inklusive nyckelbildrutor, benpositioner och animationssekvenser.
    




















11. **.xml**: XML-filer kan användas för olika konfigurationer och datadefinitioner inom CryENGINE, såsom spellogik, AI-beteende och mer.
    




















12. **.pak**: [PAK-filer](/sv/game/pak/) är arkivfiler som används för att paketera speltillgångar och -resurser, vilket gör det mer effektivt för speldistribution och -laddning.

## Hur öppnar man filen CHR?

Program som öppnar CHR-filer inkluderar

- **Crytek CryENGINE SDK** (gratis testversion) för Windows

**SubTyp:** 3D-bildfiler

## Andra CHR-filer

Här är andra filtyper som använder filtillägget **.chr**.

**3D**
- [CHR - CryENGINE Character File](/sv/3d/chr-cryengine/)
- [CHR - 3ds Max Characters File](/sv/3d/chr-3ds/)

**Teckensnitt och spel**
- [CHR - Borland Character Set](/sv/font/chr/)
- [CHR - Doki Doki Litteraturklubb! Karaktärsfil](/sv/game/chr-doki/)

## Referenser
- [CryEngine](https://en.wikipedia.org/wiki/CryEngine)

