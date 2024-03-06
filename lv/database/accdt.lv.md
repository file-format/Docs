{
  "date": "2020-11-11",
  "keywords": [
"ACCDT",
"pagarinājumu",
"failu",
"faila formātā",
"Datu bāzes faila tips",
"Datu bāzes faila formāts",
"Datu bāzes faili"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par ACDT faila formātu un API, kas var izveidot un atvērt ACCDT failus.",
  "title": "ACCDT — Microsoft Access 2007 veidņu datu bāzes faila formāts",
  "linktitle": "ACCDT",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-accd-lvt"
}
},
  "lastmod": "2020-11-12"
}

## Kas ir ACDT fails?

A file with .accdt extension is a Microsoft Access database template file that contains pre-defined database elements. These elements are a collection of structures that define a database applications such as database schemas for storing data, layout description for views of the data, and metadata describing the database. Being template files, ACCDT files can be used to create databases based on the template settings available in these. Resultant database files are saved as [ACCDB](/database/accdb/) files and populated with data in tables. Microsoft Access 2007 and onwards can open ACCDT files.

## ACDT faila formāts

ACCDT veidņu faili ir balstīti uz Office Open XML specifikācijām, un visi dati ir ietverti ZIP pakotnē. Informācija par datubāzes struktūru un saturu ir ietverta [XML](/web/xml/) failos un teksta failos un ir savstarpēji saistīta, izmantojot attiecības. Varat pārdēvēt ACCDT failu uz paplašinājumu [.zip](/compression/zip/) un izmantot jebkuru saspiešanas programmatūru, lai izvilktu ZIP arhīva saturu.

### Faila struktūra

ACCDT faili ir pakotnes, kurās ir saistītu daļu kolekcija. Katrā **daļā** tiek glabāta informācija par datu bāzes lietojumprogrammas saturu, izmantojot XML, teksta un bināros formātus, tostarp:

 * Datu bāzes objekti
 * Saistītie metadati
 * Iepakojuma struktūra

#### Iepakojums

Package ir [ZIP](/compression/zip/) arhīvs, kurā ir vairākas daļas un kas atbilst atvērtā iepakojuma konvencijām, kas norādītas [ISO/IEC-29500-2](https://www.iso.org/standard/51459.html). ACCDT failos ir jābūt vismaz vienai Veidnes metadaa daļai, kurai vajadzētu būt attiecības mērķim. Šie veidnes metadati ir ACCDT faila sākuma daļa.

#### Daļa

Daļa ir baitu straume, kurai ir saistīts tips, lai norādītu tajā saglabātā satura veidu un veidu. Daļu uzskaitījums norāda derīgas daļas, derīgus satura tipus un vajadzīgās attiecības starp visām pakotnes daļām.

#### Attiecības

`Pakotnes saistība` — kur mērķis ir daļa un avots ir pakotne kopumā.

Daļēja daļa — kur mērķis ir pakotnes daļa un avots ir daļa.

Izteikta saistība — kur uz resursu ir atsauce no avota daļas satura, atsaucoties uz attiecību elementu pēc tā ID atribūta vērtības.

`Implicit Relationship` - attiecības, kas nav izteiktas.

`Iekšējās attiecības` — kur mērķis ir pakotnes daļa.

`Ārējās attiecības` — kur mērķis ir ārējs resurss, kas nav pakotnē.

## Atsauces Nr.

* [Access Template File Format](https://learn.microsoft.com/en-us/openspecs/sharepoint_protocols/ms-accdt/0a4a68d7-7a85-4a27-ad74-730db57862d7)

