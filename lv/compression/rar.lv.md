{
  "date": "2019-10-11",
  "keywords": [
"rar fails",
"rar faila formāts",
"kas ir rar fails",
"failu",
"rets piemērs",
"rar faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "RAR",
  "description": "Kas ir RAR faila paplašinājums un API, kas var izveidot un atvērt RAR failus.",
  "linktitle": "RAR",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-ra-lvr"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir RAR fails?

Faili ar paplašinājumu .rar ir arhīva faili, kas izveidoti informācijas glabāšanai saspiestā vai parastā formā. RAR, kas apzīmē Roshal ARchive faila formātu, ir patentēts faila formāts, ko 1995. gadā izveidoja Jevgeņijs Rošals, kurš bija krievu programmatūras inženieris. Formāts tiek izmantots, lai arhivētu failus ar dažādām metodēm, tostarp dažādām saspiešanas metodēm. Sistēmām Windows, Linux un MacOS ir pieejamas vairākas lietojumprogrammatūras RAR failu ieguvei. RARLab programmatūra WinRAR ir koplietošanas failu arhivēšanas utilīta (bezmaksas 40 dienas) Microsoft Windows platformai; programmatūru uz Linux (tikai kā ekstraktoru) pārnesa tas pats autors Jevgeņijs Rošals.

## RAR faila formāta versiju vēsture

* v1.3 (oriģināls, nav "Rar!" paraksta)

* v1.5

* v2.0 — izlaists ar WinRAR 2.0 un Rar operētājsistēmai MS-DOS 2.0

* v2.9 — izlaists WinRAR versijā 3.00

* v5.0 — atbalsta WinRAR 5.0 un jaunākas versijas


## RAR formāta galvenās iezīmes

RAR ir bijis šajā jomā diezgan ilgu laiku un ir bijis viens no iecienītākajiem arhivēšanas failu formātiem. Galvenās RAR formāta funkcijas ir šādas:

**`Augsta saspiešanas pakāpe:`** Labāka salīdzinājumā ar [ZIP](/compression/zip/), salīdzināma ar 7z un zipx formātu.

**`Spēcīga failu šifrēšana pēc dizaina:`** Šifrētie RAR4 arhīvi balstās uz AES-128 balstītu šifrēšanu, savukārt šifrētie RAR5 arhīvi paļaujas uz AES-256 šifrēšanu ar uzlabotu atslēgu plānošanu.

**`Papildu kļūdu labošanas un datu atkopšanas iespējas:`** izvēles atkopšanas ieraksti arhīva izveides laikā

**`Faila lielums:`** Vismaz 20 baiti un ne vairāk kā 2^63 baiti (8 eksabaiti no kopējā arhīva lieluma)

**`Daudzsējumu RAR arhīvi:`** Iespēja sadalīt lielus arhīvus vairākos mazākos failos, lai atvieglotu pārsūtīšanu tīklā. Šādā gadījumā failu paplašinājumi tiek palielināti par 1, lai attēlotu sadalītos sējumus

## RAR faila formāts

Pilnīgas RAR formāta specifikācijas nav pieejamas publiski, tāpēc informāciju par formātu nevar formulēt kodolīgi.

### Vispārējais arhīva izkārtojums

5.0 versijā ieviestā RAR faila formāta vispārīgais izkārtojums ir šāds:

|Faila formāts
---|
| Pašizvilkšanas modulis (pēc izvēles)
|RAR 5.0 Paraksts
|Arhīva šifrēšanas galvene (neobligāti)
|Galvenā arhīva galvene
|Arhīva komentāru pakalpojuma galvene (neobligāti)
Faila galvene 1
|Pakalpojumu galvenes (NTFS ACL, straumes utt.) iepriekšējam failam (neobligāti)
|...
|Faila galvene N
|Pakalpojumu galvenes (NTFS ACL, straumes utt.) iepriekšējam failam (neobligāti)
|Atkopšanas ieraksts (neobligāti)
|Arhīva beigu galvene

Informāciju par katru iepriekš minēto RAR faila sadaļu var atrast dokumentā [RAR 5.0 File Format specifications](https://www.rarlab.com/technote.htm#arcstruct).

#### Pašizvilkšanas RAR arhīvi

Ja pats RAR fails ir pašizvilkšanas process, pašizvilkšanas informācija atrodas faila sākumā pirms arhīva paraksta. Tā izmērs un saturs nav definēts.

#### RAR 5.0 paraksts

RAR paraksts ir 8 baitu galvene, kas sastāv no šāda maģiskā skaitļa:

0x 52 61 72 21 1A 07 00

kur

0x6152 — HEAD_CRC

0x72 — HEAD_TYPE

0x1A21 — HEAD_FLAGS

0x0007 — HEAD_SIZE

## Atsauces

* [RAR 5.0 arhīva formāts](https://www.rarlab.com/technote.htm)

* [RAR — Wikipedia](https://en.wikipedia.org/wiki/RAR_(file_format))


