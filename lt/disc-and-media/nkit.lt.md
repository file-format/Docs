{
  "date": "2022-04-01",
  "keywords": [
"nkit failą",
"nkit failo formatas",
"kas yra nkit failas",
"failą",
"nkit pavyzdys",
"nkit failo plėtinys",
"pratęsimas",
"formatu",
"nkit poraštė",
"nkit failo formatas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie NKIT failo formatą ir API, kurios gali kurti ir atidaryti NKIT failus.",
  "title": "NKIT – disko vaizdo failo formatas",
  "linktitle": "NKIT",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-nki-ltt"
}
},
  "lastmod": "2022-04-01"
}

## Kas yra NKIT failas?

NKIT failas yra duomenų, gautų iš NintendoWii ir GameCube žaidimų, vaizdas diske. NKIT skirtas Nintendo Toolkit formatui. Gautame suspaudimo faile [ISO](/compression/iso/) naudojami pagrindiniai šių žaidimų duomenys, kuriuos galima paleisti su emuliatoriaus programomis, tokiomis kaip Dolphin, Swiss ir Nintendont. NKit yra neapdorotų (iso) ir suspaustų (gcz) failų formatų, kurie buvo sukurti atsižvelgiant į vaizdo grojamumą ir dydį.

## NKIT failo formatas

NKit failo formatas yra neprarandantis formatas ir naudojamas Nintendo Wii ir GameCube vaizdams mažinti ir atkurti. Formatai yra ISO ir GCZ failų formatai kiekvienam GameCube ir Wii žaidimui.

|Sistema |Formatas |Palaikoma aparatinė įranga |Palaikoma delfinų |Atkuriama 1:1 |Pastabos|
---|---|---|---|---|---|
|GameCube| nkit.iso| Taip |Taip| Taip |Tas pats kaip kompaktinis GameCube iso|
|GameCube| nkit.gcz| Ne| Taip| Taip |GCZ yra paties Dolphin bloko ieškomas glaudinimo formatas|
|Wii| nkit.iso| Ne Taip| Taip| RVT-H formatą galima žaisti tik Dolphin|
|Wii| nkit.gcz| Ne Taip| Taip| RVT-H GCZ, galima žaisti tik Dolphin|

### NKIT antraštė

NKIT failo formato antraštė yra tokia.

|Poslinkis |Ilgis |Vardas|
---|---|---|
|0x200 |0x4 |NKit antraštė 'NKIT'|
|0x204 |0x4 |NKit versija ' v01'|
|0x208 |0x4 |Originalinis vaizdas CRC32|
|0x20C |0x4 |NKit CRC – NKit failas CRC32 lygus šaltinio CRC 0x208 (0x4 GCZ)|
|0x210 |0x4 |Šaltinio vaizdo ilgis|
|0x214 |0x4 |Priverstinis šlamšto ID (kai disko ID skiriasi – retai – tik GameCube)|
|0x218 |0x4 |Wii Atnaujinkite CRC32 skaidinį, jei pašalinsite konvertuojant|

## Nuorodos Nr.

* [NKIT failo formatas – gbatemp](https://wiki.gbatemp.net/wiki/NKit/NKitFormat)


