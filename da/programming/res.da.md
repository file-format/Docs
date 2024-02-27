{
  "date": "2021-04-23",
  "keywords": [
"RES fil",
"hvordan man åbner en res-fil",
"hvad er en res-fil",
"udvidelse",
"format",
"RES filformat"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "RES - C++ kompileret ressourcescript",
  "description": "Lær om RES filformat med RES eksempel og API'er, der kan oprette og åbne RES filer.",
  "linktitle": "RES",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-re-das"
}
},
  "lastmod": "2021-04-23"
}

## Hvad er RES fil?
Filen med .res suffiks eller filtypenavn kan tilhøre mange filformatkategorier. Her diskuterer vi RES-filformatet, som er et C++ Compiled Resource Script; en binær fil oprettet af Microsoft Resource Compiler (rc), der indeholder ressourcedata; baseret på ressourcedefinitionsfilens indhold; relevant for dets overordnede softwareprojekt. .res-filen omformateres normalt til en ressourceobjektfil for at linke den til den eksekverbare fil i et program.

## RES filformat
RES-filformatet tilhører Microsoft Resource Compiler (rc). Ressourcekompileren er et værktøj, der kompilerer ressourcer såsom markører, ikoner, menuer og dialogbokse, som din applikation bruger. Ressourcefilerne har normalt filtypenavnet .res; indeholder ressourcer, såsom markører, billeder og versionsoplysninger. En RES-fil kunne være en 16- eller 32-bit ressourcefil.
## Ressourcefilstruktur
En ressourcefil indeholder en række forskellige ressourceposter. Hver post indeholder en ressourceoverskrift og relevante data. En ressourceheader er normalt DWORD-justeret i filen og indeholder følgende:

- Et **DWORD** for at angive størrelsen på ressourcehovedet
- Et **DWORD** for at angive størrelsen af ressourcedataene
- Ressourcetypen
- Ressourcenavnet
- Yderligere ressourceoplysninger

The resource header structure defines the format of the RES file. The data for the resource follows the resource header. Some resources also add a resource-specific group header pattern to provide information about a group of resources. Following are some of the resource entry types and their description:

### Acceleratortabelressourcer
En acceleratortabel er en ressourcepost i en RES-fil uden en gruppeoverskrift. **ACCELTABLEENTRY**-mønsteret definerer hver indtastning i acceleratortabellen. En RES-fil kan have flere acceleratortabeller.

### Cursor- og ikonressourcer
Selvom systemet betragter hvert ikon og markør som en enkelt fil, men disse er gemt i RES-filer som en gruppe af ikonressourcer eller en gruppe af markørressourcer. Filformaterne for ikon- og markørressourcer er de samme. En ressourcegruppeoverskrift følger alle de individuelle ikon- eller markørgruppekomponenter i .res-filen.

### Dialogboksressourcer
En dialogboks er også realiseret som en ressourcepost i RES-filen. Den indeholder et **DLGTEMPLATE**-dialogboksoverskriftsmønster og et **DLGITEMTEMPLATE**-mønster for hver specifik kontrol i dialogboksen. **DLGTEMPLATEEX** og **DLGITEMTEMPLATEEX** mønstrene forklarer formatet af udvidede dialogboksressourcer.

### Fontressourcer
En menuressource indeholder et **MENUHEADER** mønster efterfølgende et eller flere **NORMALMENUITEM** eller **POPUPMENUITEM** mønstre, et for hvert menupunkt i menuskabelonen. Mønstrene **MENUEX_TEMPLATE_HEADER** og **MENUEX_TEMPLATE_ITEM** forklarer formatet af udvidede menuressourcer.

### Ressourcer til meddelelsestabel
En meddelelsestabel består af formateret tekst til visning som en fejlmeddelelse eller i en meddelelsesboks. Hovedmønsteret i en meddelelsestabelressource er strukturen **MESSAGE_RESOURCE_DATA**.

### Versionsressourcer
Hovedmønsteret i en versionsressource er **VS_FIXEDFILEINFO**. Yderligere mønstre omfatter **VarFileInfo** til lagring af sproginformationsrelaterede data og **StringFileInfo** til brugerdefinerede strengoplysninger.




## Referencer

 * [Resource File Formats](https://learn.microsoft.com/en-us/windows/win32/menurc/resource-file-formats)
 
 

