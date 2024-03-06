{
  "date": "2021-03-10",
  "keywords": [
"VP8",
"Fails",
"Pagarinājums",
"Faila formāts",
"Video formāts",
"TrueMotion video",
"WebRTC",
"WebM"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "VP8 — TrueMotion video fails",
  "description": "Uzziniet par VP8 faila formātu un API, kas var izveidot un atvērt VP8 failus.",
  "linktitle": "VP8",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-vp-lv8"
}
},
  "lastmod": "2021-03-27"
}

## Kas ir VP8 fails?

VP8 is announced by Google as one of the best video formats having the best picture quality data rate and encoding speed. The best advantage of VP8 is that its a royalty-free substitute of H.264. Tas ir īpašs formāts augstas kvalitātes video kodēšanai un dekodēšanai kā fails vai bitu straume. Tas ir bezmaksas, jo Google ir izlaidusi visus VP8 patentus saskaņā ar publisko licenci bez autoratlīdzības. Gandrīz 90% vai vairāk no visām WebRTC video sesijām izmanto VP8.

## VP8 faila formāts

VP8 was developed by On2 Technologies in 2008 and then, later owned by Google in 2010. VP8 video kodeka galvenā priekšrocība ir tā, ka tas ir bez autoratlīdzības saskaņā ar bezmaksas licenci. Tas ir izstrādāts, lai nodrošinātu augstas kvalitātes video tīmeklī un mobilajās ierīcēs. Pirmais VP8 audio-video konteiners bija WebM, un šis kodeks tika izvēlēts par WebRTC video kodeku 2011. gadā. Šis formāts ir atzīts daudzās rūpnieciskās lietojumprogrammās, piemēram, HTML5, tīmekļa reāllaika saziņā un video atskaņošanā dažādās pārlūkprogrammās. Tirgū ir pilns pieprasījums atbalstīt šo formātu Full HD izšķirtspējā. To izmanto dažādiem mērķiem, piemēram, video konferencēm, video apraidei un ierakstīšanai no mobilajām ierīcēm.

## Specifikācijas ##

### VP8 funkcijas
 
 *  Bezmaksas video kodeks
* Progresīvākais video faila formāts
* Uzlabota izturība pret rāmja zudumu
* Ātrgaitas video dekodēšana
* Viegli izdomāt aparatūras platformās
* Tam ir tīra ievada režīma funkcija, ti, tiek izmantoti tikai individuāli kodēti kadri bez secīgas prognozēšanas, lai nodrošinātu nejaušu piekļuvi tādās lietojumprogrammās kā video rediģēšana.
* libvpx ir vienīgā programmatūras bibliotēka, kas pārvalda VP8 video straumju kodēšanu
* VP8 tika īpaši izstrādāts, lai darbotos galvenokārt kvalitātes diapazonā
* Ir pieejams plašs klientu aparatūras klāsts, kas savienots ar tīmekli, sākot no mazjaudas mobilajām un implantētām ierīcēm līdz vismodernākajiem galddatoriem ar daudziem procesora kodoliem.
* 420 krāsu paraugu ņemšanu, 8 bitu krāsu dziļumu kanālā, progresīvo skenēšanu un attēla izmērus līdz pat lielākajam attēla formātam 16383x16383 pikseļi var vienkārši darbināt, izmantojot VP8
* Impulss uz saspiešanas spēju un dekodera vienkāršību zem šiem dizaina risinājumiem radīja vairākas unikālas tehniskās funkcijas VP8 salīdzinājumā ar citiem atzītiem video saspiešanas formātiem.
* VP8 izmanto trīs atsauces kadrus no daudzajām atsauces kustības kompensācijas shēmām, kas redzamas citos formātos
* VP8 nav ierobežots ar kadru ātrumu vai datu pārraides ātrumu. Tas izmanto 14 bitus gan platumam, gan augstumam, kas nodrošina augstāko izšķirtspēju 16384x16384 pikseļi

### VP8 ierobežojumi

VP8 ierobežojumi izšķirtspējas, datu pārraides ātruma un kadru ātruma ziņā ir šādi:

* VP8 izmanto 14 bitus platumam un augstumam, lai nodrošinātu maksimālo izšķirtspēju 16384 x 16384 pikseļi
* VP9 platumam un augstumam izmanto 16 bitus, lai nodrošinātu maksimālo izšķirtspēju 65536x65536 pikseļi
* Nav ierobežojumu attiecībā uz kadru ātrumu vai datu pārraides ātrumu
 
 
## Atsauces

 * [VP8 Wikipedia](https://en.wikipedia.org/wiki/VP8#:~:text=VP8%20was%20first%20released%20by,%2C%20replacing%20its%20prececessor%2C%20VP7.&text=On %20May%2019%2C%20at%20its,an%20neatsaucams%20free%20patent%20licence)
 * [Springer Link](https://link.springer.com/chapter/10.1007/978-81-322-1157-0_32)

