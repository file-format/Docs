{
  "date" : "2022-11-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "BIF fails — Ventana visa slaida attēla formāts",
  "description":"Uzziniet par BIF faila formātu un API, kas var izveidot un atvērt BIF failus.",
  "linktitle" : "BIF",
  "menu" : {
    "docs" : {
      "identifier":"image-bif-lv",
      "parent" : "image"
}
},
  "lastmod" : "2022-11-17"
}

## Kas ir BIF fails?

BIF fails ir rastra attēla fails, kas satur slaida parauga attēlu. Tas sastāv no vairākiem TIFF attēliem, kurus slaidu skatīšanas lietojumprogrammas apvieno vienā saliktā attēlā. BIF failus veido Ventana Medical Systems digitālais slaidu skeneris, un tie pilnībā atbilst [TIFF](/image/tiff/) v6.0 definīcijas BigTIFF variantam.

## BIF faila formāts

BIF fails tiek saglabāts kā binārs attēla fails, un tas sastāv no 200 000 x 200 000 pikseļiem. Tas var radīt lielus failu izmērus, pārkāpjot 4 GB lieluma ierobežojumu, ko nosaka 32 bitu faila norādes, ko nosaka TIF standarts. Tomēr, izmantojot 64 bitu faila norādes, šo faila lieluma barjeru pārvar TIFF standarta BigTIFF variants.

### Kas izmanto BIF failu?

BIF failus izmanto digitālie priekšmetstikliņu skeneri, lai skenētu un izveidotu priekšmetstikliņu paraugu digitālās kopijas. Ja esat patologs, varat atvērt šos BIF failus slaidu skatīšanas lietojumprogrammās. Pateicoties lielam detaļu līmenim un augstas izšķirtspējas datiem, varat tuvināt un tālināt slaida attēlu, lai skatītu paraugu sekcijas vairāk vai mazāk detaļās. Šajos failos esošais metadatu fails [XML](/web/xml/) nosaka, kā attēli ir jāapvieno, un attēlu, kas jāizmanto kā faila sīktēls.

## Kā atvērt BIF failu?

BIF failus var atvērt, izmantojot:

 * OpenSlide (vairāku platformu)
 * ImageJ (vairāku platformu)
 * NetScope Viewer (Windows)

## Atsauces Nr.

 * [Roche Digital Pathology BIF Whitepaper](https://diagnostics.roche.com/content/dam/diagnostics/Blueprint/en/pdf/rmd/Roche-Digital-Pathology-BIF-Whitepaper.pdf)

