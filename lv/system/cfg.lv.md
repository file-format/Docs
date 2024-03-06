{
  "date": "2021-06-29",
  "keywords": [
"CFG",
"pagarinājumu",
"failu",
"formātā",
"sistēma",
"konfigurācija",
"iestatījumi",
"programmas",
"dators",
"pieteikumu"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "CFG — faila formāts",
  "description": "Uzziniet par CFG failu formātu un API, kas var izveidot un atvērt CFG failus.",
  "linktitle": "CFG",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-cf-lvg"
}
},
  "lastmod": "2021-06-29"
}

## Kas ir CFG fails? ##

Fails ar paplašinājumu .cfg ir iestatījumu” faila veids. Tas ir plaši izmantots faila tips, ko izmanto, lai saglabātu informāciju par datorprogrammu konfigurāciju un iestatījumiem. Lielākā daļa CFG failu veidu tiek glabāti teksta formātā, un tos nevajadzētu atvērt manuāli, tā vietā tie ir jāatver, izmantojot teksta redaktoru. Tomēr ir dažādi CFG failu veidi, kas atšķiras pēc informācijas glabāšanas formāta. Funkcijas, ko piedāvā CFG faili, dažādās lietojumprogrammās atšķiras. Dažas datoru lietojumprogrammas ļauj lietotājiem modificēt vai izstrādāt konfigurācijas failu sintaksi, izmantojot grafiskus traucējumus, savukārt citas pieļauj tikai izmaiņas, izmantojot teksta redaktoru. Pēc šo failu modificēšanas lietotāji var uzdot lietojumprogrammai vēlreiz izlasīt šos failus un lietot izmaiņas sistēmā.


## CFG faila formāts ##

CFG files are supported by various operating systems such as Unix and Unix-like operating systems, MS-DOS, macOS, Microsoft Windows, and IBM OS/2. Šo failu glabāšanas un izmantošanas formāts katrā no šīm operētājsistēmām atšķiras. Lielākā daļa sistēmu izmanto un glabā šos failus cilvēkiem lasāmā un rediģējamā teksta formātā, savukārt citas glabā tajā sarežģītāku formātu atkarībā no failu lietojuma un operētājsistēmas prasībām.

Unix un Unix līdzīgās operētājsistēmās lielākajā daļā CFG failu tiek izmantoti dažādi CFG failu formāta stili, tomēr visizplatītākais formāts ir viegli lasāms vienkārša teksta formāts, un gandrīz visi formāti ļauj komentēt un rediģēt. Šajās operētājsistēmās visizplatītākie CFG failu paplašinājumi ir CNF, CONF, CF un INI.

MS-DOS operētājsistēmā sākotnēji bija tikai viens konfigurācijas faila formāts, proti, vienkāršs teksts, taču MS-DOS 6 atnesa INI konfigurācijas faila formāta ieviešanu.

MacOS izmanto standarta rekvizītu saraksta formāta stila konfigurācijas failu.

Operētājsistēmā Microsoft Windows Vienkāršā teksta INI stila konfigurācijas faili bija nozīmīgs informācijas glabāšanas un rediģēšanas avots, tomēr 1993. gadā tika ieviesta jauna datu bāzes sistēma, kas pēc 1993. gada izraisīja konfigurācijas failu izmantošanas samazināšanos sistēmā Microsoft Windows.


## CFG piemērs ##

CFG faila paraugu var redzēt zemāk:

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

## Citi CFG faili

Šeit ir citi failu tipi, kas izmanto faila paplašinājumu **.cfg**.

**Iestatījumi**
- [CFG - Celestia Configuration File](/settings/cfg-celestia/)
- [CFG - Citrix Server Connection File](/settings/cfg-citrix/)
- [CFG - MAME Configuration File](/settings/cfg-mame/)
- [CFG - LightWave Configuration File](/settings/cfg-lightwave/)

**Spēle**
- [CFG - Wesnoth Markup Language File](/game/cfg-wesnoth/)
- [CFG - M.U.G.E.N Configuration File](/game/cfg-mugen/)
- [CFG - Source Engine Configuration File](/game/cfg-sourceengine/)

**Sistēma un citi**
- [CFG - CFG File](/system/cfg/)
- [CFG - Cal3D Model Configuration File](/misc/cfg-cal3d/)

