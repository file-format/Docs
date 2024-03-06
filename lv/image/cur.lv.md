{
  "date": "2021-06-29",
  "keywords": [
"CUR",
"pagarinājumu",
"failu",
"formātā",
"attēlu",
"No ierīces neatkarīga bitkarte",
"Kursora faila formāts",
"Kursors",
"Windows",
"pieteikumu"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "CUR — kursora faila formāts",
  "description": "Uzziniet par CUR faila formātu un API, kas var izveidot un atvērt CUR failus.",
  "linktitle": "CUR",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-cu-lvr"
}
},
  "lastmod": "2021-06-29"
}

## Kas ir CUR fails? ##

CUR fails ir statisks Microsoft Windows kursora faila formāts. Būtībā tie ir stacionāri attēli, kas visos veidos, izņemot paplašinājumu, ir identiski ICO (ikonu) failiem. Gan CUR, gan [ICO](/image/ico/) ir izveidoti, pamatojoties uz Device Independent Bitmap [DIB](/image/dib/) (no ierīces neatkarīgās bitkartes) specifikāciju. Noklusējums, kā arī pielāgotais kursors, piemēram, Windows peles rādītājs operētājsistēmai Windows, tiek saglabāti CUR failos. Tā var būt bultiņa parastai lietošanai, rotējošs smilšu pulkstenis, lai parādītu gaidīšanas periodus, vai I-josla teksta rediģēšanai. CUR faili tiek piegādāti kopā ar pielāgoto darbvirsmas motīvu instalācijas pakotni, lai nodrošinātu, ka Windows kursors atbilst pielāgotajam darbvirsmas motīvam.

## Tehniskā specifikācija ##

CUR faili ir bināri sistēmas faili, kurus var atrast ierīcēs, kas darbojas operētājsistēmā Microsoft Windows. CUR rādītāja attēliem ir dažādi standarta izmēri, piemēram, 16 × 16, 32 × 32 utt. CUR faili ir ļoti līdzīgi ICO failiem; abas sastāv no maziem stacionāriem attēliem. Atšķiras tikai CUR un ICO failu paplašinājumi. Turklāt karstā punkta skaidrojums CUR faila galvenē atšķiras no ICO faila. Karstais punkts interpretē pikseļu nobīdi no augšējā kreisā stūra līdz vietai, kur pavērsiet peli. Windows sistēmas joprojām izmanto CUR failus, taču tagad animētajiem kursoriem parasti ir faila paplašinājums ANI, nevis CUR.

## Īsa vēsture ##

CUR fails ir izveidots no ICO faila. Pirmais CUR faila formāts tika iekļauts Microsoft Windows 1.0 operētājsistēmā 1981. gadā, lai atvieglotu komerciālo izmantošanu. Drīzumā tika ieviesti vairāk interaktīvu kursoru, kas lietotājiem ļāva mainīt kursora preferences no pieejamajām iepriekš instalētajām opcijām. Tomēr CUR failu ir viegli rediģēt pats, pat ja jums nav pietiekamas tehniskās zināšanas.


## CUR piemērs ##

CUR failus var atrast šeit: *C:\Windows\Cursors*:

{{< figure src="../cur.png" alt="CUR faila formāts" >}}

