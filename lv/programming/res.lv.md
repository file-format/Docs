{
  "date": "2021-04-23",
  "keywords": [
"RES fails",
"kā atvērt res failu",
"kas ir res fails",
"pagarinājumu",
"formātā",
"RES faila formāts"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "RES — C++ kompilētais resursa skripts",
  "description": "Uzziniet par RES faila formātu, izmantojot RES piemēru un API, kas var izveidot un atvērt RES failus.",
  "linktitle": "RES",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-re-lvs"
}
},
  "lastmod": "2021-04-23"
}

## Kas ir RES fails?
Fails ar .res sufiksu vai paplašinājumu var piederēt daudzām failu formātu kategorijām. Šeit mēs apspriežam RES faila formātu, kas ir C++ apkopotā resursa skripts; binārais fails, ko izveidojis Microsoft Resource Compiler (rc), kas satur resursu datus; pamatojoties uz resursa definīcijas faila saturu; attiecas uz tā mātes programmatūras projektu. .res fails parasti tiek atkārtoti formatēts resursa objekta failā, lai saistītu to ar lietojumprogrammas izpildāmo failu.

## RES faila formāts
RES faila formāts pieder Microsoft Resource Compiler (rc). Resursu kompilators ir rīks, kas apkopo resursus, piemēram, kursorus, ikonas, izvēlnes un dialoglodziņus, ko izmanto jūsu lietojumprogramma. Resursu failiem parasti ir .res paplašinājums; satur resursus, piemēram, kursorus, attēlus un informāciju par versiju. RES fails var būt 16 vai 32 bitu resursa fails.
## Resursu faila struktūra
Resursu failā ir virkne dažādu resursu ierakstu. Katrā ierakstā ir resursa galvene un attiecīgie dati. Resursa galvene failā parasti ir līdzināta ar DWORD, un tajā ir:

- **DWORD**, lai norādītu resursa galvenes lielumu
- **DWORD**, lai norādītu resursa datu lielumu
- Resursa veids
- Resursa nosaukums
- Papildu informācija par resursiem

The resource header structure defines the format of the RES file. The data for the resource follows the resource header. Some resources also add a resource-specific group header pattern to provide information about a group of resources. Following are some of the resource entry types and their description:

### Akseleratora tabulas resursi
Akseleratora tabula ir resursa ieraksts RES failā bez grupas galvenes. Modelis **ACCELTABLEENTRY** nosaka katru akseleratora tabulas ierakstu. RES failam var būt vairākas paātrinātāju tabulas.

### Kursoru un ikonu resursi
Lai gan sistēma katru ikonu un kursoru uzskata par vienu failu, bet tie tiek saglabāti RES failos kā ikonu resursu grupa vai kursora resursu grupa. Ikonu un kursora resursu failu formāti ir vienādi. Resursu grupas galvene seko visām atsevišķajām ikonām vai kursoru grupas komponentiem .res failā.

### Dialoglodziņa resursi
Dialoglodziņš tiek realizēts arī kā resursa ieraksts RES failā. Tajā ir viens **DLGTEMPLATE** dialoglodziņa galvenes raksts un viens **DLGITEMTEMPLATE** raksts katrai konkrētai vadīklai dialoglodziņā. Modeļi **DLGTEMPLATEEX** un **DLGITEMTEMPLATEEX** izskaidro paplašināto dialoglodziņu resursu formātu.

### Fontu resursi
Izvēlnes resurss satur **MENUHEADER** modeli, pēc tam vienu vai vairākus **NORMALMENUITEM** vai **POPUPMENUITEM** modeļus, pa vienam katram izvēlnes vienumam izvēlnes veidnē. Modeļi **MENUEX_TEMPLATE_HEADER** un **MENUEX_TEMPLATE_ITEM** izskaidro paplašināto izvēlnes resursu formātu.

### Ziņojumu tabulas resursi
Ziņojumu tabula sastāv no formatēta teksta, kas tiek parādīts kā kļūdas ziņojums vai ziņojuma lodziņā. Ziņojumu tabulas resursa galvenais modelis ir **MESSAGE_RESOURCE_DATA** struktūra.

### Versiju resursi
Galvenais versijas resursa modelis ir **VS_FIXEDFILEINFO**. Papildu modeļi ietver **VarFileInfo**, lai saglabātu ar valodu saistītus datus, un **StringFileInfo** pielāgotai virknes informācijai.




## Atsauces

 * [Resource File Formats](https://learn.microsoft.com/en-us/windows/win32/menurc/resource-file-formats)
 
 

