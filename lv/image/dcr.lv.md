{
  "date" : "2021-26-08",
  "keywords" : [ "dcr file", "dcr file format", "what is a dcr file", "file", "dcr example", "dcr file extension","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" : "DCR — digitālās kameras RAW attēla fails",
  "description":"Uzziniet par DCR faila formātu un API, kas var izveidot un atvērt DCR failus.",
  "linktitle" : "DCR",
  "menu" : {
    "docs" : {
      "identifier":"image-dcr-lv",
      "parent" : "image"
}
},
  "lastmod" : "2021-26-08"
}

## Kas ir DCR fails? ##
Fails ar paplašinājumu dcr satur digitālās fotogrāfijas saturu, kas saglabāts Kodak Digital Camera RAW (DCR) formātā. DCR ir saīsinājums no **Digital Camera Raw**; satur nesaspiestu un bezzudumu attēlu datu versiju, kas uzņemta ar Kodak digitālo kameru. Profesionāliem fotogrāfiem patīk izmantot šos failus, jo tie saglabā attēlus augstākā kvalitātē nekā zemas kvalitātes saspiesto attēlu formāti.

## DCR faila formāts
DCR ir patentēts formāts, ko izstrādājusi Eastman Kodak Company; sauc vienkārši par Kodak. Digital Camera Raw (DCR) attēla fails satur minimāli apstrādātus datus no attēla sensora un digitālās kameras. Šie faili vēl nav apstrādāti un tāpēc nav gatavi drukāšanai vai rediģēšanai ar bitkartes grafikas redaktoru.
Parasti neapstrādāts pārveidotājs apstrādā attēlu plašas gammas iekšējā krāsu telpā, kur var veikt precizitāti un pilnveidošanu pirms pārvēršanas rastra faila formātā, piemēram, TIFF vai JPEG, lai tos uzglabātu, drukātu vai veiktu turpmākas manipulācijas.
### Faila saturs
Neapstrādātu failu struktūra bieži atbilst vispārīgam modelim:
- Īsa faila galvene, kas satur faila baitu secības indikatoru.
- Kameras sensora metadati, kas nepieciešami, lai interpretētu sensora attēla datus, tostarp CFA atribūtus, sensora izmēru un krāsu profilu.
- Attēlu metadati, kas var būt noderīgi iekļaušanai jebkurā CMS vidē vai datu bāzē. Dažos neapstrādātos failos ir standartizēta metadatu sadaļa ar datiem Exif formātā.
- attēla sīktēls.
- Pilna izmēra attēla JPEG konvertēšana, ko izmanto, lai priekšskatītu failu kameras LCD panelī.
- Kinofilmu skenēšanas gadījumā laika kods, atslēgas kods vai kadra numurs faila secībā, kas apzīmē kadru secību skenētajā rullī.
- Sensora attēla dati
### Sensora attēla dati
Neapstrādātajam failam ir tāda pati loma digitālajā fotogrāfijā kā fotofilmai filmu fotogrāfijā. Neapstrādāti faili, tādējādi satur pilnus izšķirtspējas datus, kas nolasīti no katra kameras attēla sensora pikseļa. Kameras sensors gandrīz pastāvīgi tiek pārklāts ar CFA (krāsu filtru masīvu. To var izmantot augsta dinamiskā diapazona attēlveidošanas pārveidošanai, ja ir pieejami neapstrādāta formāta dati; kā vienkāršāku alternatīvu vairāku ekspozīciju HDI pieejai trīs atsevišķu attēlu uzņemšanai.


## Atsauces Nr.

* [Neapstrādāta attēla formāts — Wikipedia](https://en.wikipedia.org/wiki/Raw_image_format)

* [Kas ir DCR fails](https://expertphotography.com/dcr-file/)


