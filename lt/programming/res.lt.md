{
  "date": "2021-04-23",
  "keywords": [
"RES failas",
"kaip atidaryti res failą",
"kas yra res failas",
"pratęsimas",
"formatu",
"RES failo formatas"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "RES – C++ sudarytas išteklių scenarijus",
  "description": "Sužinokite apie RES failo formatą naudodami RES pavyzdį ir API, kurios gali kurti ir atidaryti RES failus.",
  "linktitle": "RES",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-re-lts"
}
},
  "lastmod": "2021-04-23"
}

## Kas yra RES failas?
Failas su .res priesaga arba plėtiniu gali priklausyti daugeliui failo formatų kategorijų. Čia mes aptariame RES failo formatą, kuris yra C++ sudarytas išteklių scenarijus; dvejetainis failas, sukurtas Microsoft Resource Compiler (rc), kuriame yra išteklių duomenų; remiantis išteklių apibrėžimo failo turiniu; susijusios su pirminės programinės įrangos projektu. .res failas paprastai performatuojamas į išteklių objekto failą, kad susietų jį su vykdomuoju programos failu.

## RES failo formatas
RES failo formatas priklauso Microsoft Resource Compiler (rc). Išteklių kompiliatorius yra įrankis, kompiliuojantis tokius išteklius kaip žymekliai, piktogramos, meniu ir dialogo langeliai, kuriuos naudoja jūsų programa. Išteklių failai paprastai turi .res plėtinį; yra išteklių, tokių kaip žymekliai, vaizdai ir versijos informacija. RES failas gali būti 16 arba 32 bitų išteklių failas.
## Išteklių failo struktūra
Išteklių faile yra įvairių išteklių įrašų serija. Kiekviename įraše yra išteklių antraštė ir atitinkami duomenys. Išteklių antraštė faile paprastai yra suderinta pagal DWORD ir joje yra:

- **DWORD**, kad nurodytumėte išteklių antraštės dydį
- **DWORD**, kad nurodytumėte išteklių duomenų dydį
- Ištekliaus tipas
- Ištekliaus pavadinimas
- Papildoma informacija apie išteklius

The resource header structure defines the format of the RES file. The data for the resource follows the resource header. Some resources also add a resource-specific group header pattern to provide information about a group of resources. Following are some of the resource entry types and their description:

### Greitintuvo lentelės ištekliai
Greitintuvo lentelė yra išteklių įrašas RES faile be grupės antraštės. **ACCELTABLEENTRY** modelis apibrėžia kiekvieną greitintuvo lentelės įrašą. RES faile gali būti kelios greitintuvo lentelės.

### Žymeklio ir piktogramos ištekliai
Nors sistema kiekvieną piktogramą ir žymeklį laiko vienu failu, tačiau jie saugomi RES failuose kaip piktogramų išteklių grupė arba žymeklio išteklių grupė. Piktogramų ir žymeklio išteklių failų formatai yra vienodi. Išteklių grupės antraštė yra po visų atskirų piktogramų arba žymeklio grupės komponentų .res faile.

### Dialogo lango ištekliai
Dialogo langas taip pat realizuojamas kaip išteklių įrašas RES faile. Jame yra vienas dialogo lango **DLGTEMPLATE** antraštės šablonas ir vienas **DLGITEMPLATE** šablonas kiekvienam konkrečiam dialogo lango valdikliui. **DLGTEMPLATEEX** ir **DLGITEMTEMPLATEEX** modeliai paaiškina išplėstinio dialogo lango išteklių formatą.

### Šrifto ištekliai
Meniu šaltinyje yra **MENUHEADER** šablonas, vėliau vienas ar daugiau **NORMALMENUITEM** arba **POPUPMENUITEM** šablonų, po vieną kiekvienam meniu šablono meniu elementui. Šablonai **MENUEX_TEMPLATE_HEADER** ir **MENUEX_TEMPLATE_ITEM** paaiškina išplėstinių meniu išteklių formatą.

### Pranešimų lentelės ištekliai
Pranešimų lentelę sudaro suformatuotas tekstas, skirtas rodyti kaip klaidos pranešimas arba pranešimų laukelyje. Pagrindinis šablonas pranešimų lentelės šaltinyje yra **MESSAGE_RESOURCE_DATA** struktūra.

### Versijos ištekliai
Pagrindinis versijos šaltinio modelis yra **VS_FIXEDFILEINFO**. Papildomi šablonai apima **VarFileInfo**, skirtą su kalbos informacija susijusiems duomenims saugoti, ir **StringFileInfo**, skirtą pasirinktinei eilutės informacijai.




## Nuorodos

 * [Resource File Formats](https://learn.microsoft.com/en-us/windows/win32/menurc/resource-file-formats)
 
 

