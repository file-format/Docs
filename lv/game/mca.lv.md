{
  "date": "2022-12-13",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par MCA failu formātu un API, kas var izveidot un atvērt MCA failus.",
  "title": "MCA — Minecraft Anvil reģiona faila formāts",
  "linktitle": "MCA",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-mc-lva"
}
},
  "lastmod": "2022-12-13"
}

## Kas ir MCA fails?

Minecraft Anvil reģiona faila formāts ir datu uzglabāšanas formāts, kas tiek izmantots, lai populārajā videospēlē **Minecraft** saglabātu Minecraft pasaules reljefa gabalus. Minecraft pasaule sastāv no reģioniem, kur katrs reģions ir sadalīts gabalos. MCA faila formāts ļauj efektīvi uzglabāt lielu spēļu datu apjomu, piemēram, bloku un entītiju atrašanās vietu noteiktā spēļu pasaules daļā. MCA faili ir jāapvieno ar citiem MCA failiem, lai radītu visu pasauli.

Papildus spēļu datu glabāšanai Anvil reģiona faila formāts ietver arī dažādu citu datu veidu atbalstu, piemēram, spēlētāja datus un metadatus. Tas ļauj efektīvi uzglabāt visu informāciju, kas nepieciešama, lai pilnībā atjaunotu noteiktu spēles pasaules daļu, tostarp bloku, entītiju un citu spēles objektu atrašanās vietu.

## MCA faila formāts — vairāk informācijas

Anvil reģiona faila formāts ir NBT (Named Binary Tag) formāta variants, kas ir hierarhiska koka struktūra datu glabāšanai binārā failā. Tas ļauj efektīvi uzglabāt sarežģītas datu struktūras kompaktā un viegli lasāmā formātā.

### Daļas MCA failā

Minecraft gabals ir 16x16x16 bloka apgabals spēļu pasaulē, kas tiek ielādēts atmiņā un tiek atveidots spēlētāja ekrānā. Anvil reģiona faila formāts visus konkrētas daļas datus saglabā vienā failā, ko pēc tam vajadzības gadījumā var ātri ielādēt atmiņā. Tas nodrošina efektīvu glabāšanu un ātru piekļuvi spēles datiem, kas ir svarīgi, lai nodrošinātu vienmērīgu un nevainojamu spēļu pieredzi.

### Mazs MCA faila izmērs

Viena no Anvil reģiona faila formāta galvenajām iezīmēm ir tā saspiešanas izmantošana. Tas ļauj efektīvi uzglabāt lielu datu apjomu, nezaudējot datu kvalitāti vai ātrumu, ar kādu tiem var piekļūt. Tas tiek panākts, izmantojot dažādas metodes, piemēram, gzip saspiešanu un datu saspiešanu.

MCA failu saspiestais faila formāts padara to par svarīgu spēles datu uzglabāšanas un pārvaldības sistēmas sastāvdaļu. Tā efektīva saspiešanas izmantošana un atbalsts dažādiem datu tipiem ļauj efektīvi uzglabāt un ātri piekļūt spēles datiem, nodrošinot spēlētājiem vienmērīgu un nevainojamu spēļu pieredzi.

## MCA faila formāta struktūra

MCA failu iekšējā faila formāta struktūra sastāv no:
 * Galvene un a
 * Lietderīgā slodze

### MCA galvene

MCA reģiona faila galvene sākas ar 8KiB galveni, kas ir sadalīta divās 4KiB tabulās. Pirmajā tabulā ir ietvertas daļu nobīdes pašā reģiona failā, savukārt otrajā tabulā ir norādīti šo gabalu pēdējo atjauninājumu laikspiedoli.

### MCA kravnesība

MCA Payload sastāv no gabaliem, kur katrs gabala dati sākas ar (lielo) četru baitu garu lauku. Šis lauks norāda precīzu atlikušo datu daļu garumu baitos. Pēdējā gabala dati ir polsterēti, lai tie būtu 4096 B daudzkārtēji. Minecraft nepieņem failus, kuru pēdējā daļa nav polsterēta.

## Kā atvērt MCA failus

Varat atvērt un rediģēt MCA failus, izmantojot programmu MCEdit, kas ir bezmaksas Minecraft atvērtā koda redaktors. Varat [download MCEdit](https://www.mcedit.net/) no oficiālās vietnes un izmantot to, lai atvērtu un skatītu sava Anvil reģiona faila saturu.

Kad esat instalējis programmu MCEdit, varat atvērt Anvil reģiona failu, veicot šādas darbības:

 1. Palaidiet programmu MCEdit un noklikšķiniet uz pogas Atvērt loga augšējā kreisajā stūrī.

 1. Dialoglodziņā Atvērtā pasaule dodieties uz sava Anvil reģiona faila atrašanās vietu un atlasiet to.

 1. Noklikšķiniet uz pogas Atvērt, lai atvērtu failu programmā MCEdit.

 1. MCEdit ielādēs failu un parādīs tā saturu galvenajā logā. Pēc tam varat izmantot MCEdit rīkus un līdzekļus, lai skatītu, rediģētu un izvilktu datus no Anvil reģiona faila.

## Atsauces

* [Minecraft pasaules redaktors](https://www.mcedit.net/)

* [Par Minecraft](https://www.minecraft.net/)

* [Reģiona faila formāts](https://minecraft.fandom.com/wiki/Region_file_format)


