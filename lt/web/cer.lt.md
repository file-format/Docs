{
  "date": "2021-07-13",
  "keywords": [
"CER",
"pratęsimas",
"failą",
"formatu",
"žiniatinklio",
"sertifikatas",
"kalba"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "CER – sertifikato failo formatas",
  "description": "Sužinokite apie CER failo formatą ir API, kurios gali kurti ir atidaryti CER failus.",
  "linktitle": "CER",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ce-ltr"
}
},
  "lastmod": "2021-07-13"
}

## Kas yra CER failas? ##

A file with an extension .cer is responsible for storing some information about the owner certificate and the specific public key. This format of files cannot store the private keys and have the capacity to store only one certificate which is x509. Specialiai apsaugotos sertifikatų institucijos priklauso HTTPS – patikimam ir saugiam naršymo protokolui  
CER yra jūsų serverio sertifikatas. Paprastai jį gauna domeno sertifikatų institucija. CER dažniausiai laikomas tuo pačiu kaip [CRT](/web/crt/), nors abu yra to paties SSL sertifikato formato, tačiau skiriasi failo vardų plėtiniai.
Juos galima naudoti operacinėse sistemose tiesiog atidarius naršyklę ir patikrinus naudojamos naršyklės ar svetainės saugumą.

## Trumpa istorija ##

1995 m. Thawte tapo pirmąja sertifikavimo institucija, sprendžiančia viešųjų SSL (saugaus lizdo nuorodos) sertifikatų problemą iš JAV. Po to yra keletas tokių institucijų, kurios buvo įsteigtos 1995–2020 m.

## CER failo formatas ##

Šie failai gali būti paprasti
* PKC S#7 apima Base64 ASCII kodavimą
* Jo failų plėtiniai yra p7b arba p7cZ
* Dvejetainio turinio sertifikatas būtų DER arba pkcs12/pfx.
Yra daugybė sertifikatų failų tipų su tam tikromis unikaliomis specifikacijomis:
* .pem, kai organizacija usThawteificate grandine sujungia šį formatą, gerai žinoma, kad kuria sertifikatus
* Reikalingas .arm, kai sertifikato išgavimo būdas padeda pasirašyti savarankiškai, nurodytas formatas šiam tikslui yra .arm. Jis pavaizduotas base-64 ASCII koduotėje.
* .der, Jį sudaro dvejetainiai duomenys. Tai reiškia, kad jį galima naudoti tik vienam sertifikatui
* .pfx (PKC512), Jį sudaro privatus raktas, atitinkantis CA išduotą sertifikatą arba savarankiškai pasirašytas sertifikatas. Šis formatas gerai žinomas dėl vieno SSL diegimo konvertavimo į kitą.


