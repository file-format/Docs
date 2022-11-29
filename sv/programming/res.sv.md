{
  "date" : "2021-04-23",
  "keywords": [ "RES File", "how to open a res file", "what is a res file", "extension", "format", "RES file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RES - C++ Compiled Resource Script",
  "description":"Lär dig om RES-filformat med RES-exempel och API:er som kan skapa och öppna RES-filer.",
  "linktitle" : "RES",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## Vad är RES fil?
Filen med .res suffix eller filtillägg kan tillhöra många filformatkategorier. Här diskuterar vi RES-filformatet som är ett C++ Compiled Resource Script; en binär fil skapad av Microsoft Resource Compiler (rc) som innehåller resursdata; baserat på resursdefinitionsfilens innehåll; relevant för dess moderprogramvaruprojekt. .res-filen formateras vanligtvis om till en resursobjektfil för att länka den till den körbara filen i ett program.

## RES filformat
RES-filformatet tillhör Microsoft Resource Compiler (rc). Resurskompilatorn är ett verktyg som kompilerar resurser som markörer, ikoner, menyer och dialogrutor som din applikation använder. Resursfilerna har vanligtvis filnamnstillägget .res; innehåller resurser, såsom markörer, bilder och versionsinformation. En RES-fil kan vara en 16- eller 32-bitars resursfil.
## Resursfilstruktur
En resursfil innehåller en serie olika resursposter. Varje post innehåller en resursrubrik och relevant data. En resursrubrik är vanligtvis DWORD-justerad i filen och innehåller följande:

- Ett **DWORD** för att ange storleken på resurshuvudet
- Ett **DWORD** för att ange storleken på resursdata
- Resurstypen
- Resursnamnet
- Ytterligare resursinformation

Resurshuvudstrukturen definierar formatet för RES-filen. Data för resursen följer resurshuvudet. Vissa resurser lägger också till ett resursspecifikt grupprubrikmönster för att ge information om en grupp av resurser. Följande är några av resursposttyperna och deras beskrivning:

### Acceleratortabellresurser
En acceleratortabell är en resurspost i en RES-fil utan grupphuvud. Mönstret **ACCELTABLEENTRY** definierar varje post i acceleratortabellen. En RES-fil kan ha flera acceleratortabeller.

### Markör- och ikonresurser
Även om systemet betraktar varje ikon och markör som en enda fil, men dessa lagras i RES-filer som en grupp av ikonresurser eller en grupp av markörresurser. Filformaten för ikon- och markörresurser är desamma. En resursgrupprubrik följer alla individuella ikon- eller markörgruppskomponenter i .res-filen.

### Resurser för dialogrutan
En dialogruta realiseras också som en resurspost i RES-filen. Den innehåller ett **DLGTEMPLATE**-dialogrutahuvudmönster och ett **DLGITEMMALL**-mönster för varje specifik kontroll i dialogrutan. Mönstren **DLGTEMPLATEEX** och **DLGITEMTEMPLATEEX** förklarar formatet för utökade dialogrutaresurser.

### Font Resources
En menyresurs innehåller ett **MENUHEADER**-mönster och därefter ett eller flera **NORMALMENUITEM**- eller **POPUPMENUITEM**-mönster, ett för varje menyalternativ i menymallen. Mönstren **MENUEX_TEMPLATE_HEADER** och **MENUEX_TEMPLATE_ITEM** förklarar formatet för utökade menyresurser.

### Meddelandetabellresurser
En meddelandetabell består av formaterad text för visning som ett felmeddelande eller i en meddelanderuta. Huvudmönstret i en meddelandetabellresurs är strukturen **MESSAGE_RESOURCE_DATA**.

### Versionsresurser
Huvudmönstret i en versionsresurs är **VS_FIXEDFILEINFO**. Ytterligare mönster inkluderar **VarFileInfo** för att lagra språkinformationsrelaterad data och **StringFileInfo** för anpassad stränginformation.




## Referenser

* [Resursfilformat](https://docs.microsoft.com/en-us/windows/win32/menurc/resource-file-formats)
 


 



