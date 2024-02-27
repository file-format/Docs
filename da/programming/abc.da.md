
{
  "date": "2021-12-14",
  "keywords": [
".abc-fil",
"udvidelse",
"format",
"ActionScript bytekodefil",
"hvordan man åbner en .abc-fil",
"abc filformat"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ABC - ActionScript Byte Code File",
  "description": "Lær om, hvad der er ABC-filformat med eksempler og API'er, der kan oprette og åbne ABC-filer.",
  "linktitle": "ABC",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-ab-dac"
}
},
  "lastmod": "2021-12-14"
}

## Hvad er ABC fil?

En fil med filtypen .abc er en ActionScript-bytekodefil, der er oprettet af Flash-kompileren som et resultat af kompilering af ActionScript-scriptfilerne. Bytekoden, der er indeholdt i ABC-filen, udføres af ActionScript Virtual Machine (AVM og AVM2). Bytekoden består af konstante data, instruktioner fra AVM2-instruktionssættet og forskellige slags metadata. Når en ABC-fil indlæses i AVM eller AVM2, gennemgår den verifikation. Hvis den ikke er i overensstemmelse med AVM2-oversigten, afvises den. ABC-filer kan åbnes i Adobe Flash Player, der er udgået for længe siden.

## ABC-filformat - flere oplysninger

ABC-filer gemmes på disk i binært filformat, der kan læses af AVM eller AVM2 virtuelle maskiner. Dens interne filstruktur repræsenterer eksekverbar kodeblok med alle dens konstante data, typebeskrivelser, kode og metadata.

## ABC-filstruktur

ABC-filstrukturen er som vist nedenfor.

```
abcFile  
{
           u16        minor_version                
           u16        major_version                
           cpool_info        constant_pool                
           u30        method_count                
           method_info        method[method_count]                
           u30        metadata_count                
           metadata_info        metadata[metadata_count]                
           u30        class_count                
           instance_info        instance[class_count]                
           class_info        class[class_count]                
           u30        script_count                
           script_info        script[script_count]               
           u30        method_body_count                
           method_body_info        method_body[method_body_count]        
}
```

### ABC-filfelter

|Feltnavn|Beskrivelse|
---|---|
|minor_version, major_version|Værdierne for major_version og minor_version er de større og mindre versionsnumre i abcFile-formatet.|
|constant_pool|Konstant_puljen er en struktur med variabel længde sammensat af heltal, doubler, strenge, navnerum, navnerumssæt og multinavne.|
|method_count, method|Værdien ofmethod_count er antallet af indtastninger i metodearrayet. Hver indgang i metodearrayet er en method_info-struktur med variabel længde.|
|metadata_count, metadata|Værdien af metadata_count er antallet af poster i metadataarrayet. Hver metadataindgang er en metadata_infostruktur, der knytter et navn til et sæt strengværdier. |
|class_count, instans, class|Værdien af class_count er antallet af poster i instansen og klasse-arrays. |
|script_count, script|Værdien af script_count er antallet af poster i script-arrayet. Hver scriptindgang er en script_info-struktur, der definerer karakteristikaene for et enkelt script i denne fil. |
|method_body_count, method_body|Værdien af method_body_count er antallet af poster i method_body-arrayet. Hver method_bodyentry består af en method_body_info-struktur med variabel længde, som indeholder instruktionerne for en individuel metode eller funktion.|

## Referencer

 * [Robust ABC (ActionScript Bytecode) [Dis-]Assembler - Github](https://github.com/CyberShadow/RABCDAsm)

