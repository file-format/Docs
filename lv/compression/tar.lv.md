{
  "date": "2019-10-11",
  "keywords": [
"tar fails",
"tar faila formāts",
"kas ir tar fails",
"failu",
"darvas piemērs",
"tar faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TAR — Unix arhīva faila formāts",
  "description": "Uzziniet, kas ir TAR fails un API, kas var izveidot un atvērt TAR failus.",
  "linktitle": "TAR",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-ta-lvr"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir TAR fails?

Faili ar paplašinājumu .tar ir arhīvi, kas izveidoti ar Unix utilītu viena vai vairāku failu apkopošanai. Vairāki faili tiek glabāti nesaspiestā formātā ar atbalstu failu un mapju pievienošanai arhīvam. TAR utilīta operētājsistēmā Unix ir balstīta uz komandām, taču līdz ar to izveidotos failus atbalsta lielākā daļa failu arhivēšanas sistēmu gandrīz visās operētājsistēmās. Pirmo reizi to 1979. gadā izveidoja AT&T Bell Laboratories, un laika gaitā tika publicētas turpmākās versijas.

## TAR faila formāts

TAR is an open file format with full specifications available for developer's reference. Its file structure was standardized in POSIX.1-1988 and later in POSIX.1-2001. Ar tar izveidotās datu kopas saglabā informāciju par failu sistēmas parametriem, piemēram:

* Vārds

* Laika zīmogi

* Īpašumtiesības

* Failu piekļuves atļaujas

* Direktoriju organizācija


TAR failam nav nekāda maģiskā numura. Tas satur virkni bloku, kur katrs bloks ir BLOCKSIZE baiti.

Katrs arhivētais fails ir attēlots ar galvenes bloku, kas apraksta failu, kam seko nulle vai vairāki bloki, kas norāda faila saturu. Arhīva faila beigās ir divi 512 baitu bloki, kas ir aizpildīti ar binārām nullēm kā faila beigu marķieri. Saprātīgai sistēmai šāds faila beigu marķieris ir jāraksta arhīva beigās, taču tā nedrīkst pieņemt, ka šāds bloks pastāv, lasot arhīvu. Jo īpaši GNU tar vienmēr izdod brīdinājumu, ja tā nesaskaras ar to.

Bloki var tikt bloķēti fiziskām I/O operācijām. Katrs n bloku ieraksts (kur n ir iestatīts ar bloķēšanas koeficientu = 512 izmēra opciju uz tar) tiek ierakstīts ar vienu write()” darbību. Magnētiskajās lentēs šādas rakstīšanas rezultāts ir viens ieraksts. Rakstot arhīvu, pēdējais bloku ieraksts jāraksta pilnā izmērā, bloki aiz nulles bloka ietverot visas nulles. Lasot arhīvu, saprātīgai sistēmai pareizi jāapstrādā arhīvs, kura pēdējais ieraksts ir īsāks par pārējo vai kurā pēc nulles bloka ir atkritumu ieraksti.

### TAR faila galvene

Tāpat kā jebkura cita failu galvene, arī tar faila galvenes ieraksts satur metadatus par failu, un tas ir parādīts nākamajā tabulā.

|Lauka nobīde|Lauka lielums (baiti)|Lauks
---|---|---|
|0|100|Faila nosaukums
|100|8|Faila režīms
|108|8|Īpašnieka skaitliskais lietotāja ID
|116|8|Grupas lietotāja ID
|124|12|Faila lielums baitos (oktālā bāze)
|136|12|Pēdējās modifikācijas laiks ciparu Unix laika formātā (oktāls)
|148|8|Galvenes ieraksta kontrolsumma
|156|1|Saites indikators (faila tips)
|157|100|Saistītā faila nosaukums

Neizmantotie lauki ir aizpildīti ar NUL baitiem. Galvene sastāv no 257 baitiem, kas ir papildināti ar NUL baitiem, lai to aizpildītu līdz 512 baitu ierakstam.

## Kā izveidot TAR failu

### Izveidojiet TAR failu operētājsistēmā Windows

Operētājsistēmā Windows varat izmantot Windows apakšsistēmu operētājsistēmai Linux (WSL) vai trešo pušu rīkus, piemēram, 7-Zip, lai izveidotu TAR failus. Lūk, kā to izdarīt, izmantojot WSL:

 1. Instalējiet WSL, ja vēl neesat to izdarījis. Varat to instalēt, izmantojot Windows funkciju iestatījumus.

 1. Atveriet WSL termināli un izmantojiet to pašu tar komandu kā Linux vai Unix sistēmās, lai izveidotu TAR failu.

### Izveidojiet TAF failu operētājsistēmā Linux no komandrindas

Lai izveidotu TAR failu, izmantojot komandrindu Linux vai Unix sistēmās, atveriet termināli un izmantojiet tar komandu. Varat izveidot TAR failu dažādos saspiešanas formātos (piemēram, .tar.gz, .tar.bz2, .tar.xz), bet šeit mēs izveidosim vienkāršu .tar failu:

Lai izveidotu TAR failu no viena faila vai direktorija, izmantojiet šo komandu:

```
tar -cvf archive.tar file_or_directory
```

## Kā atvērt TAR failu

### Atveriet TAR failu operētājsistēmā Windows

Operētājsistēmā Windows ir jāinstalē dekompresijas utilīta, piemēram, 7-Zip. Tā ir bezmaksas arhivēšanas utilīta, ko var izmantot dažādu saspiestu failu formātu izveidošanai un izvilkšanai. Ar peles labo pogu noklikšķiniet uz sava TAR faila un atlasiet opciju **Izvilkt**.

### Atveriet TAR failu operētājsistēmā Mac

Mac datorā vienkārši veiciet dubultklikšķi uz faila TAR, TGZ vai TAR.GZ, lai to izsaiņotu.

### Atveriet TAR failu operētājsistēmā Linux

Ja izmantojat Linux vai Mac Terminal lietotni, izmantojiet tar -xvf TAR failiem vai tar -xvzf failiem, kas beidzas ar TGZ vai TAR.GZ.

## Atsauces Nr.

* [TAR — Wikipedia](https://en.wikipedia.org/wiki/Tar_(computing))

* [TAR pamatformāts](https://www.gnu.org/software/tar/manual/html_node/Standard.html)


