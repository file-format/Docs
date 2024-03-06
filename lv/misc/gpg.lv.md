{
  "date": "2022-02-17",
  "keywords": [
"gpg failu",
"gpg faila formātā",
"kas ir gpg fails",
"failu",
"gpg piemērs",
"gpg faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GPG fails — GNU Privacy Guard publiskā atslēgu piekariņa fails",
  "description": "Uzziniet par GPG failiem un API, kas var izveidot un atvērt GPG failus.",
  "linktitle": "GPG",
  "menu": {
    "docs": {
      "parent": "misc",
      "identifier": "misc-gp-lvg"
}
},
  "lastmod": "2022-02-17"
}

## Kas ir GPG fails?

GPG fails ir šifrēšanas/atšifrēšanas atslēgas fails, ko izmanto GNU Privacy Guard (GnuPG) šifrēšanas programma. Pati GnuPC programma ir balstīta uz OpenPGP standartu, kā definēts RFC4880, un to sauc arī par PGP. Veiksmīgas GPG izmantošanas atslēga mūsdienu operētājsistēmā ir tās daudzpusīgā atslēgu pārvaldības sistēma. GPG komandrindas utilīta ļauj to viegli integrēt ar citām lietojumprogrammām.

## GPG faila formāts

GPG faili tiek saglabāti kā šifrēti bināri faili, un, protams, tie nav lasāmi cilvēkiem. Lai atšifrētu šifrētu GPG failu, jums ir jāizmanto tā pati drošā atslēga. Un tāpēc šo failu iekšējais faila formāts nav zināms.

## Šifrējiet un atšifrējiet failus, izmantojot GPG operētājsistēmā Linux

GPG komandrindas utilītu var izmantot, lai šifrētu un atšifrētu failus operētājsistēmā Linux.

### Faila šifrēšana

Failu var šifrēt, izmantojot komandu gpg ar opciju -c (izveidot), kā parādīts zemāk.

```
gpg -c file1.txt
```
Palaižot šo komandu, tiek prasīta atslēgas frāze, ar kuru šifrēt sākotnējā faila `file1.txt` saturu. Tā rezultātā tiek izveidots šifrēts fails file1.txt.gpg.

### Faila atšifrēšana un izvilkšana

Lai atšifrētu un izvilktu šifrētu failu, var izmantot šādu komandu.

```
gpg cfile.txt.gpg
```

## Atsauces

* [GNUPG](https://gnupg.org/)

* [HDF — Wikipedia](https://en.wikipedia.org/wiki/Hierarchical_Data_Format)


