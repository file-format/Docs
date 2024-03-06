{
  "date" : "2023-01-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Uzziniet par Age of Empires 2 Expansion Replay MGX faila formātu un API, kas var izveidot un atvērt MGX failus.",
  "title" : "MII fails — Wii virtuālā iemiesojuma faila formāts",
  "linktitle" : "MII",
  "menu" : {
    "docs" : {
      "identifier":"game-mii-lv",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-15"
}

## Kas ir MII fails?

MII fails ir virtuālā iemiesojuma faila formāts, ko izmanto virtuālo iemiesojumu glabāšanai Nintendo Wii spēļu konsolē. Šajos failos ir ietverta tāda informācija kā iemiesojuma izskats, kustības un animācijas. Tos var izmantot spēlēs, sociālo tīklu lietojumprogrammās un citā Wii programmatūrā. MII failā ir arī citi iemiesojuma elementi, piemēram, dzimums, matu krāsa, ādas krāsa, sejas vaibsti un acu tips.

Varat atvērt MII failu, izmantojot [My Avatar Editor](https://rc24.xyz/goodies/mii/).

## MII faila formāts

MII faila formāts ir detalizēti definēts vietnē [Wii Brew](https://wiibrew.org/wiki/Mii_data). Virknes MII failā tiek glabātas Unicode formātā (UTF-16), big-endian.

### MI bloks

MII faila dati tiek glabāti Wiimote divos blokos. Katra bloka garums ir 750 baiti ar 2 baitu CRC, kas kopā veido 752 baitus. Katrs bloks sākas ar 4 baitu vērtību ('RNCD'), kas, šķiet, ir maģiskais skaitlis MII faila formātam.

## Kā izveidot MII failus?

Ir daži dažādi veidi, kā izveidot Nintendo Wii iemiesojumus:

1. `Izmantojot Wii iebūvēto Mii kanālu:` Šis kanāls ļauj izveidot pielāgotus iemiesojumus, izmantojot dažādus rīkus, tostarp sejas vaibstus, ķermeņa formu un apģērbu. Kad esat izveidojis savu iemiesojumu, varat to saglabāt kā Mii failu un izmantot spēlēs un citā Wii programmatūrā.

1. Lietotnes Mii Maker izmantošana Nintendo 3DS: lietotne Mii Maker ļauj izveidot pielāgotus iemiesojumus, izmantojot Nintendo 3DS skārienekrānu un kameru. Kad esat izveidojis savu iemiesojumu, varat to saglabāt kā Mii failu un pārsūtīt uz savu Wii, izmantojot bezvadu savienojumu.

1. `Trešās puses programmatūras izmantošana:` Daži izstrādātāji ir izveidojuši programmatūru, kas ļauj izveidot Wii pielāgotus iemiesojumus. Šī programmatūra parasti ir paredzēta lietošanai datorā, un, lai pārsūtītu iemiesojumu uz Wii, var būt nepieciešamas papildu darbības.

1. Izmantojot iepriekš izveidotus iemiesojumus: dažām spēlēm un citai Wii programmatūrai var būt pievienoti iepriekš izveidoti iemiesojumi, kurus varat izmantot.

Visos gadījumos jums ir nepieciešams Nintendo konts, lai izveidotu un saglabātu savu iemiesojumu Wii.

## Atsauces

* [Mana iemiesojuma redaktors](https://rc24.xyz/goodies/mii/)

* [Wii Brew](https://wiibrew.org/wiki/Mii_data)


