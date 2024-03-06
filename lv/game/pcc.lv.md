{
  "date": "2021-09-08",
  "keywords": [
"pcc fails",
"pcc faila formātā",
"kas ir pcc fails",
"failu",
"pcc piemērs",
"pcc faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par Mass Effect PCC faila formātu un API, kas var izveidot un atvērt PCC failus.",
  "title": "PCC — Mass Effect pakotnes fails",
  "linktitle": "PCC",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-pc-lvc"
}
},
  "lastmod": "2021-09-08"
}

## Kas ir PCC fails?

Fails ar .pcc ir [Mass Effect Game](https://www.ea.com/games/mass-effect/mass-effect-3) fails, kurā ir spēļu dati, lai mainītu spēles saturu, piemēram, modeļus, tekstūras un telpas. Mass Effect 2 un 3 ir pirmās šāvēja spēles, kuru pamatā ir Unreal Engine 3 spēļu dzinējs. Spēli sākotnēji izstrādāja [Bioware](https://www.bioware.com/about/), kurš lielāko daļu spēļu resursu saglabāja savā patentētajā PCC faila formātā. Bioware iegādājās Electronic Arts, pasaules vadošais interaktīvās izklaides izdevējs.

## PCC faila formāts — vairāk informācijas

PCC faili satur saspiestas un/vai nesaspiestas struktūras, kas veicina kopējo failu organizēšanu.

### Saspiesta PCC struktūra

Saspiests PCC fails sastāv no tabulām un datiem, kas ir segmentēti gabalos. Katrs gabals satur mainīgu skaitu saspiestu bloku.

 * Chunks Header — 16 baitu kopējā galvene, kas satur informāciju par gabaliem.
 * Daļas galvene — 16 baitu galvene, kurā ir informācija par neapstrādātiem saspiestiem datiem, kas ietverti bloka formā.

### Nesaspiesta PCC struktūra

Nesaspiesti PCC faili ir sadalīti šādās piecās daļās.

 * Galvene - satur pamatinformāciju par PCC faila struktūru.
 * Nosaukumu tabula — satur nosaukumu, kas atrodams pakotnē, tostarp importēšanas klases, eksportēšanas un eksportēšanas rekvizītus.
 * `Importa tabula` - satur visas PCC importētās klases un objektus.
 * `Eksportēt tabulu` - satur visus pakotnē saglabātos objektus. Katrs eksports var atšķirties pēc izmēra.

## Atsauces

 * [Me3Explorer — PCC faila formāts](https://me3explorer.fandom.com/wiki/PCC_File_Format)
 * [Spēle Mass Effect](https://www.ea.com/games/mass-effect/mass-effect-3)
 * [Bioware](https://www.bioware.com/about/)

