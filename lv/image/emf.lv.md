{
  "date": "2019-10-11",
  "keywords": [
"emf fails",
"emf faila formāts",
"kas ir emf fails",
"failu",
"emf piemērs",
"emf faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EMF — uzlabots metafaila formāts",
  "description": "Uzziniet par EMF failu formātu un API, kas var izveidot un atvērt EMF failus.",
  "linktitle": "EMF",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-em-lvf"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir EMF fails?

**Uzlabotais metafaila formāts (EMF)** grafiskos attēlus saglabā neatkarīgi no ierīces. EMF metafaili sastāv no mainīga garuma ierakstiem hronoloģiskā secībā, kas var atveidot saglabāto attēlu pēc parsēšanas jebkurā izvades ierīcē. Šie mainīga garuma ieraksti var būt slēgto objektu definīcijas, zīmēšanas komandas un grafiskie rekvizīti, kas ir svarīgi attēla precīzai renderēšanai. Kad ierīce atver EMF metafailu, izmantojot savu grafikas vidi, oriģinālā attēla proporcijas, izmēri, krāsas un citas grafiskās īpašības paliek nemainīgas neatkarīgi no ierīces atvēršanas platformas.

## Īsa vēsture ##

1990. gadā Microsoft izstrādāja attēla faila formātu Windows Metafile ([WMF](/image/wmf/)) operētājsistēmai Microsoft Windows. Windows metafaili ir 16 bitu formāts, kas var saturēt dažus bitkartes komponentus. WMF var sastāvēt no vektorgrafikas un ir paredzēts, lai tos varētu pārnēsāt dažādās lietojumprogrammās. 1993. gadā Win32/GDI paziņoja par Enhanced Metafile (EMF), jaunāku versiju ar uzlabotu elastību un mērogojamību. EMF izmanto arī kā grafikas valodas komandas, lai palaistu printera draiverus. Microsoft tagad iesaka uzlaboto metafailu formātu (EMF), nevis Windows formātu (WMF). Kad tika ieviesta sistēma Windows XP, tika izlaista Enhanced Metafile Format Plus (EMF+) versija. Šī jaunākā versija atrod savu ceļu, serializējot GDI+ API zvanus, tāpat WMF/EMF ieraksta zvanus uz GDI. Pastāv gzip saspiesta EMF versija, kas pazīstama kā EMZ.

## EMF metafaila formāts ##

Tālāk ir norādīti būtiski uzlabotā metafaila formāta elementi.

* EMR_HEADER (versija, izmērs, attēla izšķirtspēja izveides brīdī)

* Tabula GDI objektiem

* Rezervēta palete (pēc izvēles)

* Metafailu ieraksti, kas sakārtoti masīva struktūrā (īpašuma iestatījumi, definēti objekti, zīmēšanas komandas)

* EMR_EOF ieraksts (pēdējais ieraksts EMF metafailā)


## EMF versijas ##
* **Oriģināls**: sākotnējā versijā ir norādīts ieraksts, kas nepieciešams, lai saglabātu sākotnējo attēlu un nodrošinātu tā neatkarību no ierīces. Turklāt atbalsta ierakstu, kas satur grafikas objektus un komandas zīmēšanai.

* **1. versija**: otrā EMF versija uzlaboja elastību un ierīces neatkarību, pievienojot pikseļu formāta ierakstu un iespēju izmantot OpenGL komandu.

* **2. versija**: trešā versija uzlaboja precizitāti, pievienojot metrisko sistēmu, lai mērītu ierīces virsmas attālumus, padarot ierakstu mērogojamāku.


## Uzlabotie metafailu ieraksti ##

Metafailu ieraksti tiek sakārtoti masīva veidā. Šiem ierakstiem ir ENHMETARECORD struktūra un mainīgs garums. ENHMETARECORD norāda datus, kas nosaka GDI funkcijas, lai izveidotu attēlu, izmantojot uzlabotu metafaila formātu. **ENHMETAHEADER** struktūra vienmēr ir pirmais ieraksts šajā formātā. Šajā EMF galvenē ir šāda informācija.

Every record of enhanced metafile has two members of EMR (provides the base structure) in the beginning. The first member recognizes GDI function (parameters are used in record) which determines the type of record and is known as iType. The other member nSize define the size of each record. Remaining parameters (if any) and additional data arranged immediately below nSize. Immediately following the header an optional text description may present. The name of picture and author is recorded in that text description. The palette whose presence is an option specifies the colors used in enhanced metafile creation. The other records used to specify the GDI function which is essential in picture creation.

Katrā metafailā ir jābūt vismaz vienam EMF ierakstam. Informācijas pārvietošana no viena ieraksta uz otru ir atkarīga no EML ierakstiem, tāpēc šie ieraksti ir jāsakārto blakus. Jebkurā konkrētajā metafaila ierakstā, izņemot EOF_record, šī konkrētā ieraksta garums ir noteikts, lai pārietu uz nākamo ierakstu.

## Uzlabota metafailu izveide ##

Funkcija **CreateEnhMetaFile** tiek izmantota, lai izveidotu uzlabotu metafailu. Šīs funkcijas argumenti tiek izmantoti attēla izmēriem un uzglabāšanai diskā/atmiņā. Turklāt šai funkcijai ir nepieciešams tās ierīces izmērs, kurā attēls parādījās pirmais (atsauces ierīce), un atsauces ierīces (DC) konteksts. Tātad, izsaucot funkciju **CreateEnhMetaFile**, ir jānorāda argumenti, lai apstrādātu šo DC. Funkcijas sintakse ir šāda:
```
HDC CreateEnhMetaFileExample(

  HDC        hdc,

  LPCSTR     lptoFilename,

  const OVAL *lprc,

  LPCSTR     lpDesc

);
```
**HDC:** rokturis ar atsauces ierīci.

**lptoFilename:** rādītājs uz faila nosaukumu.

**lprc:** Rādītājs uz ovālu struktūru norāda attēla izmērus mm.

**lpDesc:**  a pointer to a string for the title of picture and application name that created the picture.

## Uzlabotas metafailu darbības ##

Tālāk ir norādīti darbi, kurus var veikt, izmantojot uzlabotā metafaila rokturi.

* Parādīt un rediģēt saglabāto attēlu.

* Izveidojiet uzlabotas metafailu kopijas.

* Retrieve the copy of an EMF header, optional description and binary version of an enhanced metafile
* Apkopojiet krāsas paletē.


## Grafiskie objekti ##

Zīmēšanas un gleznošanas operācijās grafikas objektus var izveidot ar objektu izveides ierakstiem un saglabāt tālākai lietošanai. Ieraksts EMR_SELECTOBJECT” var izgūt šos grafikas objektus, izmantojot atskaņošanas ierīces kontekstu. Pildspalvas, paletes, otas, krāsu telpas, fonti un krājuma objekti ir daži atkārtoti lietojamu objektu veidi.

## Baitu secība ##

Little-endian formāts tiek izmantots datu glabāšanai metafailu ierakstos.

## Versija ##

The EMF file format has been revised twice. The changed versions are original, extension 1, and extension 2. Paplašinātajās versijās ir paredzēti OpenGL ieraksti un izvēles deskriptors iekšējam pikseļu formātam. Parādītajiem izmēriem ir pievienota mērīšanas iekārta mililitros.

## Atsauces Nr.

* [Uzlabota formāta metafaili | Microsoft dokumenti](https://learn.microsoft.com/en-us/windows/desktop/gdi/enhanced-format-metafiles)

* [Uzlabots metafaila formāts un specifikācijas](https://msdn.microsoft.com/en-us/library/cc230514.aspx)


