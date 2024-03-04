{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MBOX – el. pašto dėžutės failas",
  "description": "Sužinokite apie MBOX failo formatą ir API, kurios gali kurti ir atidaryti MBOX failus.",
  "linktitle": "MBOX",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-mbo-ltx"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra MBOX failas?

MBox failo formatas yra bendras terminas, reiškiantis elektroninio pašto pranešimų rinkimo konteinerį. Pranešimai saugomi konteinerio viduje kartu su jų priedais. Pranešimai iš viso aplanko išsaugomi viename duomenų bazės faile, o nauji pranešimai pridedami prie failo pabaigos. Daugybė programų ir API palaiko MBox failų formatus, tokius kaip Apple Mail ir Mozilla Thunderbird.

## MBOX failo formatas ##

The MBox file format remained non-standardized for quite long time until 2005 when the application/mbox  was standardized as [RFC 4155.](https://tools.ietf.org/rfc/rfc4155.txt) Messages, in RFC 2822 format, are concatenated inside MBox file format one after another. Each message begins with a separator line that identifies the message sender, and also identifies the date and time at which the message was received by the final recipient (either the last-hop system in the transfer path, or the system which serves as the recipient's mailstore). Each message is typically terminated by an empty line. The end of the database is usually recognized by either the absence of any additional data, or by the presence of an explicit end-of-file marker.

## Pranešimo skaitymas iš MBox failo Nr.

Skaitytojas nuskaito mbox failą ieškodamas eilučių From_. Bet kuri eilutė From_ žymi pranešimo pradžią. Skaitytojas neturėtų bandyti pasinaudoti tuo, kad kiekviena From_ eilutė (už failo pradžios) yra tuščia eilutė. Skaitytojas, radęs pranešimą, iš eilutės From_ ištraukia (galbūt sugadintą) voko siuntėją ir pristatymo datą. Tada jis skaitomas iki kitos From_ eilutės arba failo pabaigos, atsižvelgiant į tai, kas įvyksta anksčiau. Ji pašalina paskutinę tuščią eilutę ir ištrina citatas >Iš_ eilučių ir >>Iš_ eilučių ir pan. Rezultatas yra RFC 822 pranešimas.

## Kodavimo svarstymai ##

MBox failo turinys gali negrįžtamai susimaišyti, kai gautame el. laiške yra Mbox failas kaip priedas ir jis išsaugomas kitame Mbox faile. Kad to išvengtų, pranešimų sistemos turi užkoduoti mbox duomenų bazę su neskaidria perdavimo koduota (pvz., BASE64 arba Quoted-Printable), kai toks objektas perduodamas naudojant pranešimų siuntimo protokolus. Diegėjai taip pat turėtų būti pasirengę užkoduoti mbox duomenis vietoje, jei gaunami neatitinkantys duomenų.

## Nuorodos Nr.

* [MBox – RFC4155](https://tools.ietf.org/rfc/rfc4155.txt)

* [Mbox – Vikipedija](https://en.wikipedia.org/wiki/Mbox)


