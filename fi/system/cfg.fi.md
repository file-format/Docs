{
  "date": "2021-06-29",
  "keywords": [
"CFG",
"laajennus",
"tiedosto",
"muoto",
"järjestelmä",
"kokoonpano",
"asetukset",
"ohjelmia",
"tietokone",
"sovellus"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "CFG - tiedostomuoto",
  "description": "Opi CFG-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata CFG-tiedostoja.",
  "linktitle": "CFG",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-cf-fig"
}
},
  "lastmod": "2021-06-29"
}

## Mikä on CFG-tiedosto? ##

Tiedosto, jonka tunniste on .cfg, on asetus-tiedosto. Se on yleisesti käytetty tiedostotyyppi, ja sitä käytetään tallentamaan tietoja tietokoneohjelmien määrityksistä ja asetuksista. Useimmat CFG-tiedostotyypit on tallennettu tekstimuodossa, eikä niitä tule avata manuaalisesti, vaan ne tulee avata tekstieditorilla. On kuitenkin olemassa erilaisia CFG-tiedostoja, jotka eroavat tietojen tallennusmuodosta. CFG-tiedostojen tarjoamat ominaisuudet vaihtelevat sovelluksista riippuen. Jotkut tietokonesovellukset antavat käyttäjien muokata tai kehittää asetustiedostojensa syntaksia käyttämällä graafisia häiriöitä, kun taas toiset sallivat muutokset vain tekstieditorilla. Näiden tiedostojen muokkauksen jälkeen käyttäjät voivat ohjeistaa sovelluksen lukemaan nämä tiedostot uudelleen ja soveltamaan muutokset järjestelmään.


## CFG-tiedostomuoto ##

CFG files are supported by various operating systems such as Unix and Unix-like operating systems, MS-DOS, macOS, Microsoft Windows, and IBM OS/2. Muoto, jossa nämä tiedostot tallennetaan ja käytetään kussakin näistä käyttöjärjestelmistä, vaihtelee. Useimmat järjestelmät käyttävät ja tallentavat näitä tiedostoja ihmisen luettavassa ja muokattavassa tekstimuodossa, kun taas toiset tallentavat siihen monimutkaisemmassa muodossa tiedostojen käytöstä ja käyttöjärjestelmän tarpeista riippuen.

Unix- ja Unix-tyyppisissä käyttöjärjestelmissä useimmissa CFG-tiedostoissa käytetään useita eri muototyylejä CFG-tiedostoille, mutta yleisin muoto on helposti luettava tekstimuoto, ja lähes kaikissa muodoissa on mahdollista kommentoida ja muokata. CFG-tiedostojen yleisimmät tiedostopäätteet näissä käyttöjärjestelmissä ovat CNF, CONF, CF ja INI.

MS-DOS-käyttöjärjestelmässä oli alun perin vain yksi konfiguraatiotiedostomuoto, nimittäin pelkkä teksti, mutta MS-DOS 6 toi mukanaan INI-konfiguraatiotiedostomuodon käyttöönoton.

macOS käyttää tavallista ominaisuusluettelomuodon tyylimääritystiedostoa.

Microsoft Windowsissa Plain text INI -tyyliset konfiguraatiotiedostot olivat tärkeä tiedon tallennus- ja muokkauslähde, mutta vuonna 1993 otettiin käyttöön uusi tietokantajärjestelmä, mikä johti konfiguraatiotiedostojen käytön vähenemiseen Microsoft Windowsissa vuoden 1993 jälkeen.


## CFG-esimerkki ##

Esimerkki CFG-tiedostosta näkyy alla:

```
#########################
## Settings
##

genome_dir = ~/genome/hg18/

> reads_list1
fastq_100k_1_1.txt
fastq_100k_3_1.txt
<

> reads_list2
fastq_100k_1_2.txt
fastq_100k_3_2.txt
<

read_format = FASTQ
quality_format = phred-33
mapper = bowtie
annotations = all.gene.refFlat.txt
out_path = output
max_intron = 400000
max_multi_hit = 10

```

## Muut CFG-tiedostot

Tässä on muita tiedostotyyppejä, jotka käyttävät **.cfg**-tiedostotunnistetta.

**Asetukset**
- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}

**Peli**
- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}

**Järjestelmä ja muut**
- {{HYPERLINKKI1}}
- {{HYPERLINKKI}}

