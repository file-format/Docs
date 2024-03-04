{
  "date": "2020-11-11",
  "keywords": [
"ACCDT",
"pratęsimas",
"failą",
"Dokumento formatas",
"Duomenų bazės failo tipas",
"Duomenų bazės failo formatas",
"Duomenų bazės failai"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie ACCDT failo formatą ir API, kurios gali kurti ir atidaryti ACCDT failus.",
  "title": "ACCDT – „Microsoft Access 2007“ šablonų duomenų bazės failo formatas",
  "linktitle": "ACCDT",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-accd-ltt"
}
},
  "lastmod": "2020-11-12"
}

## Kas yra ACCDT failas?

A file with .accdt extension is a Microsoft Access database template file that contains pre-defined database elements. These elements are a collection of structures that define a database applications such as database schemas for storing data, layout description for views of the data, and metadata describing the database. Being template files, ACCDT files can be used to create databases based on the template settings available in these. Resultant database files are saved as [ACCDB](/database/accdb/) files and populated with data in tables. Microsoft Access 2007 and onwards can open ACCDT files.

## ACCDT failo formatas

ACCDT šablonų failai yra pagrįsti Office Open XML specifikacijomis, o visi duomenys yra ZIP pakete. Duomenų bazės struktūros ir turinio informacija yra [XML](/web/xml/) failuose ir tekstiniuose failuose ir yra susieta viena su kita per ryšius. Galite pervardyti ACCDT failą į [.zip](/compression/zip/) plėtinį ir naudoti bet kokią glaudinimo programinę įrangą, kad ištrauktumėte ZIP archyvo turinį.

### Failo struktūra

ACCDT failai yra paketai, kuriuose yra susijusių dalių rinkinys. Kiekvienoje ** dalyje** saugoma informacija apie duomenų bazės programos turinį naudojant XML, teksto ir dvejetainius formatus, įskaitant:

 * Duomenų bazės objektai
 * Susiję metaduomenys
 * Pakuotės struktūra

#### Paketas

Paketas yra [ZIP](/compression/zip/) archyvas, kurį sudaro kelios dalys ir kuris atitinka atvirojo pakavimo konvencijas, nurodytas [ISO/IEC-29500-2](https://www.iso.org/standard/51459.html). ACCDT failuose turi būti bent viena šablono metadaa dalis, kuri turėtų būti santykio tikslas. Šie šablono metaduomenys yra pradinė ACCDT failo dalis.

#### Dalis

Dalis yra baitų srautas, turintis susietą tipą, nurodantį joje saugomo turinio pobūdį ir tipą. Dalių sąrašas nurodo galiojančias dalis, galiojančius turinio tipus ir būtinus ryšius tarp visų paketo dalių.

#### Santykiai

Paketo ryšys – kai tikslas yra dalis, o šaltinis yra paketas kaip visuma.

Part-to-Part Relationship – kai tikslas yra dalis, o šaltinis yra paketo dalis.

Aiškus ryšys – kai šaltinis nurodomas iš šaltinio dalies turinio, nurodant ryšio elementą pagal jo ID atributo vertę.

Numanomas ryšys' – santykiai, kurie nėra aiškūs.

Vidinis ryšys – kai tikslas yra paketo dalis.

Išorinis ryšys – tai išorinis šaltinis, kurio nėra pakete.

## Nuorodos Nr.

* [Access Template File Format](https://learn.microsoft.com/en-us/openspecs/sharepoint_protocols/ms-accdt/0a4a68d7-7a85-4a27-ad74-730db57862d7)

