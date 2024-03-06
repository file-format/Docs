{
  "date": "2019-12-12",
  "keywords": [
"PLY",
"failu",
"pagarinājumu",
"formātā",
"3D faila formāts"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par PLY faila formātu un API, kas var izveidot un atvērt PLY failus.",
  "title": "PLY — daudzstūra 3D faila formāts",
  "linktitle": "PLY",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-pl-lvy"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir PLY fails?

PLY, daudzstūra faila formāts, ir 3D faila formāts, kas glabā grafiskos objektus, kas aprakstīti kā daudzstūru kolekcija. Šī faila formāta mērķis bija izveidot vienkāršu un vienkāršu faila tipu, kas ir pietiekami vispārīgs, lai būtu noderīgs plašam modeļu klāstam. PLY faila formāts ir pieejams kā ASCII, kā arī binārais formāts kompaktai glabāšanai un ātrai saglabāšanai un ielādei. Faila formātu izmanto dažādas lietojumprogrammas, kas nodrošina 3D failu lasīšanas atbalstu.

Objektus PLY formātā apraksta virsotņu, seju un citu elementu kolekcija, kā arī īpašības, piemēram, krāsa un parastais virziens, ko var pievienot šiem elementiem. Citi rekvizīti, kurus var arī saglabāt kopā ar objektu, ir:

* Virsmas normāli

* tekstūras koordinātas

* caurspīdīgums

* diapazona datu ticamība

* rekvizīti daudzstūra priekšpusei un aizmugurei


Objekts, kas attēlots ar PLY formātu, var būt dažādu avotu rezultāts, piemēram, ar roku digitalizēti objekti, daudzstūru objekti no modelēšanas lietojumprogrammām, diapazona dati, trīsstūri no maršējošiem kubiem, reljefa dati un radiositātes modeļi.

## Īsa vēsture

PLY formātu 1990. gados izstrādāja Gregs Turks un citi Stenfordas grafikas laboratorijā, un tāpēc to sauc arī par Stenfordas trīsstūra formātu. Kopš tā laika faila formātam ir versija 1.0, un turpmākas izmaiņas netika veiktas.

## PLY faila formāts

Vienkāršs PLY objekts sastāv no elementu kolekcijas objekta attēlošanai. Tas sastāv no virsotņu (x,y,z) trīskāršu saraksta un to seju saraksta, kuras faktiski ir virsotņu saraksta indeksi. Virsotnes un sejas ir divi elementu piemēri, un lielākā daļa PLY faila sastāv no šiem diviem elementiem. Var izveidot arī jaunus rekvizītus un pievienot tiem objekta elementiem, taču tie jāpievieno tā, lai vecās programmas nesabojātos, saskaroties ar šiem jaunajiem rekvizītiem. No šādām īpašībām var atteikties, lasot arī lietojumprogrammas. Turklāt ar šo elementu var izveidot jaunus elementus un definēt īpašības.

### Faila struktūra

PLY faila formāta faila struktūra ir šāda:

|Lauks
---|
|Faila galvene
|Vertex saraksts
|Seju saraksts
|Citu elementu saraksts

#### Struktūras piemērs

Mēs izmantosim tālāk sniegto piemēru mūsu turpmākajā diskusijā par dažādām PLY faila formāta daļām.

```
ply
format ascii 1.0           { ascii/binary, format version number }
comment made by Greg Turk  { comments keyword specified, like all lines }
comment this file is a cube
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
element face 6             { there are 6 "face" elements in the file }
property list uchar int vertex_index { "vertex_indices" is a list of ints }
end_header                 { delimits the end of the header }
0 0 0                      { start of vertex list }
0 0 1
0 1 1
0 1 0
1 0 0
1 0 1
1 1 1
1 1 0
4 0 1 2 3                  { start of face list }
4 7 6 5 4
4 0 4 5 1
4 1 5 6 2
4 2 6 7 3
4 3 7 4 0
```

#### Faila galvene

PLY faila formāta galvene sastāv no ASCII teksta gan ASCII, gan binārajam formātam. Galvenes sadaļas sākumu un beigas identificē ar slāņa un beigu galvenes atslēgvārdiem. Galvenes sākumā ir burvju vārds ply, ko izmanto, lai lasītāji atpazītu PLY faila formātu. Nākamajā rindā ir parādīts šī faila versijas numurs. Komentāri PLY faila formātā sākas ar komentāra atslēgvārdu katras komentāra rindiņas sākumā.

#### Elementa atslēgvārds

Pēc tam elementa atslēgvārds norāda, kas atrodas failā. Tam seko rekvizīti konkrētajam elementa tipam, kur katram rekvizītam ir savs rekvizītu tips un secība, kā norādīts tālāk:

```
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
```

Šajā konkrētajā piemērā konkrētajam virsotnes elementam ir 3 peldošā tipa rekvizīti ar norādīto secību.

#### Datu tipu veidi

Īpašumam var būt divu veidu datu veidi.

Skalārs: Skalāro datu veidi ir šādi:

|#Vārds|#Tips|#Baitu skaits
|rakstzīme|rakstzīme|1
|uchar|neparakstīta rakstzīme|1
|īss|īss vesels skaitlis|2
|ushort|neparakstīts īss vesels skaitlis|2
|int|Vesels skaitlis|4
|uint|neparakstīts vesels skaitlis|4
|pludiņš|vienas precizitātes pludiņš|4
|dubultais|dubultās precizitātes pludiņš|8

Saraksts: ir īpaša rekvizītu definīciju forma, kas izmanto saraksta datu tipu. Piemērs tam ir no iepriekš esošā kuba faila:

īpašumu saraksts uchar int vertex_index.

Tas nozīmē, ka rekvizīts vertex_index vispirms satur neparakstītu simbolu, kas norāda, cik indeksu rekvizīts satur, un pēc tam sarakstu, kurā ir tik daudz veselu skaitļu. Katrs vesels skaitlis šajā mainīgā garuma sarakstā ir virsotnes indekss.

## Atsauces Nr.

* [PLY faila formāts](http://paulbourke.net/dataformats/ply/)

* [PLY — Wikipedia](https://en.wikipedia.org/wiki/PLY_(file_format))


