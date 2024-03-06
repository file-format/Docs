{
  "date": "2019-10-11",
  "keywords": [
"JAR",
".jar",
"kas ir jar fails",
"kā atvērt jar failu",
"pagarinājumu",
"failu",
"jar fails",
"jar faila formātā",
".jar paplašinājums"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "JAR — Java arhīva faila formāts",
  "description": "Uzziniet par JAR faila formātu un API, kas var izveidot un atvērt JAR failu.",
  "linktitle": "JAR",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-ja-lvr"
}
},
  "lastmod": "2020-09-10"
}

## Kas ir JAR fails?

Fails ar paplašinājumu .jar ir Java arhīva fails, kurā kā viens fails ir daudz dažādu ar lietojumprogrammu saistītu failu. Šis faila formāts tika izveidots, lai samazinātu lejupielādētās Java sīklietotnes ielādes ātrumu pārlūkprogrammā, izmantojot HTTP darījumu, izvairoties no vairāku HTTP savienojumu izveides. Vienā JAR failā var būt Java klases faili ([.class](/programming/class/)), [images](/image/) un [sounds](/audio/). Lietojumprogrammas izstrādātājs var digitāli parakstīt atsevišķus vienumus JAR failā, lai autentificētu to izcelsmi. JAR faili tiek regulāri izmantoti, lai izveidotu funkcionālas API, kurās ir noteiktas ar šo API saistītas funkcijas.

## JAR faila formāts

JAR files are based on the popular [ZIP file format](/compression/zip/) that archives its individual content files in a single file. JAR file format supports compressions, resulting in a smaller file size for downloading and hence further improves the download time. The [JAR file specifications](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) artilce by Oracle gives complete details about the internal specifications of JAR files.

### Manifesta fails

Kad tiek izveidots JAR fails, tajā tiek automātiski izveidots manifesta fails, kas satur metadatu informāciju par JAR faila saturu. Šis fails parāda saturu, kas ir iesaiņots JAR failā. Tipisks manifesta fails izskatās šādi, kas parāda JAR failā iekļautās mapes un klases.

```
META-INF/
META-INF/MANIFEST.MF
pack/
pack/class1.class
pack/class2.class
..
..
```

#### Manifesta specifikācijas

Manifesta specifikācijas Oracle nosaka šādi.

`manifesta fails`: galvenās sadaļas jaunā rindiņa \*individual-section

`galvenā sadaļa`: versijas informācijas jaunā rindiņa \*galvenais atribūts

`version-info`: manifesta versija : versijas numurs

`versijas numurs` : cipars+{.cipars+}*

main-attribute: (jebkurš likumīgs galvenais atribūts) jauna rindiņa

individual-section: nosaukums : vērtība jaunā rindiņa \*perentry-atribūts

perentry-attribute: (jebkurš likumīgs perentry atribūts) jaunā rindiņa

`jaunā rindiņa` : CR LF | LF | CR (neseko LF)

cipars: {0-9}

### Izpildāmais JAR

JAR faili var ietvert arī lietojumprogrammu, ko Java virtuālā mašīna (JVM) var izpildīt līdzīgi jebkurai citai lietojumprogrammai Microsoft Windows operētājsistēmā. Šajā gadījumā JVM ir jāzina par lietojumprogrammas ieejas punktu, kas ir jebkura klase ar publisko statisko tukšumu galveno metodi. Manifesta fails identificē šādu klasi ar galveni Main-Class šādā formātā:

```
Main-Class: com.example.MyClassName
```



## Atsauces

 * [JAR File Overview](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jarGuide.html)
 * [JAR faila formāts](https://en.wikipedia.org/wiki/JAR_(file_format))

