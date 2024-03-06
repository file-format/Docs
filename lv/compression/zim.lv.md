{
  "date": "2019-12-09",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ZIM faila formāts - OpenZIM arhīva fails",
  "description": "Uzziniet par ZIM failu formātu un API, kas var izveidot un atvērt ZIM failus.",
  "linktitle": "ZIM",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-zi-lvm"
}
},
  "lastmod": "2019-12-09"
}

## Kas ir ZIM fails? ##

Faili ar paplašinājumu .zim ir arhīvi, kas izveidoti Wiki satura glabāšanai bezsaistē. Tas tiek uzskatīts par vispiemērotāko atvērtā faila formātu Wikipedia glabāšanai USB. Tas saglabā vietnes saturu kompaktā formātā. Tā nosaukums cēlies no Zeno IMproved, kas bija agrākais Zeno faila formāts. ZIM uztur [openZIM ](https://openzim.org/)projekts, kuru sponsorē Wikimedia CH un atbalsta Wikimedia Foundation. ZIM failus var atvērt ar tādām lietojumprogrammām kā Kiwix un ZIMReader. OpenZIM projekts ir uzņēmis ZIM faila formāta ieviešanu vietnē [Github](https://github.com/openzim), lai sniegtu ieguldījumu no OpenSource kopienas.

## ZIM faila formāta specifikācijas

ZIM faila formāts tika izstrādāts, izmantojot [Zeno file format](https://openzim.org/wiki/Zeno_file_format), un tas nav saderīgs ar atpakaļejošu spēku. ZIM faila formāta formāta specifikācijas ir OpenZIM [available online](https://openzim.org/wiki/ZIM_file_format) izstrādātāja uzziņai. OpenZIM ir nodrošinājis C++ atvērtā pirmkoda ieviešanu [LibZim](https://openzim.org/wiki/Zimlib) ZIM failu lasīšanai un rakstīšanai.

ZIM faila formāts izmanto LZMA2 saspiešanu, lai padarītu saturu kompaktu.

{{< figure src="../ZIM_File_Format.jpeg" alt="ZIM faila formāts" >}}


### ZIM galvene

A ZIM file starts with a header that is at offset 0. Visas sastāvdaļas ir balstītas uz little-endian, un visi veselie skaitļi ir veseli skaitļi bez paraksta, ti, uint_16, uint_32, uint_64.

|Lauka nosaukums |Tips| Nobīde| Garums| Apraksts|
---|---|---|---|---|
|magicNumber| vesels skaitlis| 0| 4| Burvju skaitlim, lai atpazītu faila formātu, ir jābūt 72173914 (0x44D495A)|
|majorVersion| vesels skaitlis| 4| 2| ZIM faila formāta galvenā versija (5 vai 6)|
|minorVersion| vesels skaitlis| 6| 2| ZIM faila formāta neliela versija|
|uuid| vesels skaitlis| 8| 16| šī zim faila unikālais ID|
|articleCount| vesels skaitlis| 24| 4| kopējais rakstu skaits|
|clusterCount| vesels skaitlis| 28| 4| kopējais klasteru skaits|
|urlPtrPos| vesels skaitlis| 32| 8| direktoriju rādītāju saraksta pozīcija, kas sakārtota pēc URL|
|titlePtrPos| vesels skaitlis| 40| 8| direktoriju rādītāju saraksta pozīcija, kas sakārtota pēc Title|
|clusterPtrPos| vesels skaitlis| 48| 8| klastera rādītāju saraksta pozīcija|
|mimeListPos| vesels skaitlis| 56| 8| MIME tipu saraksta pozīcija (arī galvenes izmērs)|
|galvenā lapa| vesels skaitlis| 64| 4| galvenā lapa vai 0xffffffff, ja nav galvenās lapas|
|izkārtojumsLapa| vesels skaitlis| 68| 4| izkārtojuma lapa vai 0xffffffffff, ja nav izkārtojuma lapas|
|checksumPos| vesels skaitlis| 72| 8| norādiet uz šī faila md5kontrolsummu bez pašas kontrolsummas. Tas vienmēr norāda 16 baitus pirms faila beigām.|

## Atsauces Nr.

* [OpenZIM](https://openzim.org/)

* [C++ LibZim](https://openzim.org/wiki/Zimlib)


