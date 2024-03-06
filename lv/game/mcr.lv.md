{
  "date": "2022-12-13",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par MCR failu formātu un API, kas var izveidot un atvērt MCR failus.",
  "title": "MCR - Minecraft reģiona faila formāts",
  "linktitle": "MCR",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-mc-lvr"
}
},
  "lastmod": "2022-12-14"
}

## Kas ir MCR fails?

Minecraft MCR faila formāts ir datu formāts, ko Minecraft izmanto, lai saglabātu Minecraft pasaules reljefa gabalus. Tas ir balstīts uz NBT (Named Binary Tag) formātu, kuru izstrādāja populārā atvērtā pirmkoda spēļu dzinēja Minecraft Forge izstrādātāji. MCR faila tips tika ieviests pašā sākumā un vēlāk tika aizstāts ar [MCA file format](/game/mca/).

## MCR faila formāts

MCR faila formāts ir strukturēts kā virkne nosauktu bināru tagu, no kuriem katrs satur noteikta veida datus. Augstākā līmeņa tags ir Līmeņa tags, kurā ir visi dati par vienu spēles līmeni. Tagā Level ir vairāki citi nosaukti tagi, kas glabā dažāda veida datus, piemēram, tags Data, kas glabā informāciju par spēļu pasauli, un tagi Entities un TileEntities, kas glabā datus par attiecīgi spēļu objekti un flīžu entītijas pasaulē.

## Kas atrodas MCR faila formātā?

Minecraft MCR faila formātā reģions ir 32x32 bloka apgabals spēļu pasaulē. MCR formāts sadala spēļu pasauli reģionos, lai efektīvāk pārvaldītu datus un ļautu ātrāk ielādēt un saglabāt spēles līmeņus. Katrs reģions tiek glabāts atsevišķā failā, un MCR faila formāts izmanto koordinātu sistēmu, lai noteiktu katra reģiona atrašanās vietu spēles pasaulē. Reģiona koordinātas nosaka apgabala apakšējā kreisā stūra bloka koordinātas. Piemēram, reģions ar koordinātām (-1,0) atrastos vienu reģionu pa kreisi un nulles reģionu uz leju no spēles pasaules sākuma.

## MCR faila formāta specifikācijas

MCR faila formāta specifikācijas ir publiski pieejamas. NBT formāta specifikācijas, uz kurām ir balstīts MCR formāts, ir pieejamas Minecraft Forge vietnē. Turklāt [Minecraft Wiki](https://minecraft.fandom.com/wiki/Region_file_format) ir arī detalizēta informācija par MCR faila formātu, tostarp tā struktūru un dažādiem datu veidiem, ko tas atbalsta.

### Saspiesti dati MCR failos

Minecraft MCR faila formāts atbalsta saspiešanu. MCR faila formāts ir balstīts uz [NBT format](https://minecraft.fandom.com/wiki/NBT_format), kas ļauj saglabāt datus saspiestā formā. Tas palīdz samazināt MCR failu lielumu un padarīt tos efektīvākus pārsūtīšanai un uzglabāšanai. Šī ir svarīga MCR faila formāta funkcija, jo tā ļauj spēlētājiem koplietot lielus Minecraft World reljefa datus ar citiem.

## Atsauces

* [Minecraft pasaules redaktors](https://www.mcedit.net/)

* [Par Minecraft](https://www.minecraft.net/)

* [Reģiona faila formāts](https://minecraft.fandom.com/wiki/Region_file_format)

* [NBT formāts](https://minecraft.fandom.com/wiki/NBT_format)


