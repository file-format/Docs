{
  "date": "2023-05-24",
  "keywords": [
"cba fails",
"kas ir cba fails",
"kā izveidot CBA failu",
"ko satur CBA fails",
"kāds ir cba faila formāts",
"failu",
"cba faila paplašinājums",
"pagarinājumu"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "CBA faila formāts — komiksu grāmatu arhīvs",
  "description": "Uzziniet par CBA formātu un API, kas var izveidot un atvērt CBA failus.",
  "linktitle": "CBA",
  "menu": {
    "docs": {
      "identifier": "compression-cba-lv",
      "parent": "compression"
}
},
  "lastmod": "2023-05-24"
}

## Kas ir CBA fails?

Komiksu grāmatu arhīva (CBA) fails, kas pazīstams arī kā komiksu grāmatu arhīvs vai komiksu lasītāja fails, ir populārs formāts, ko izmanto digitālo komiksu grāmatu glabāšanai un izplatīšanai. Tas parasti satur atsevišķu komiksu lapu vai attēlu kolekciju, kas apvienotas vienā failā, lai to būtu viegli sakārtot un lasīt.

Viens no izplatītākajiem komiksu grāmatu arhīva failu izveides formātiem ir TAR (lentes arhīva) formāts. TAR ir failu arhivēšanas formāts, ko izmanto Unix un Linux vidēs. Tas apvieno vairākus failus vienā failā, ko bieži izmanto dublēšanai.

## Kā izveidot CBA failu?

Lai izveidotu komiksu grāmatu arhīva failu, izmantojot TAR arhivēšanas rīku, parasti jāveic šādas darbības:

1. Apkopojiet visas komiksu lapas vai attēlus, kurus vēlaties iekļaut arhīvā.
2. Atveriet komandu uzvedni vai termināļa logu.
3. Dodieties uz direktoriju, kurā atrodas komiksu lapas/attēli.
4. Lai izveidotu arhīvu, izmantojiet komandu TAR ar atbilstošām opcijām. Piemēram, komanda var izskatīties šādi:

```
tar -cf comicbook.cbt page1.jpg page2.jpg page3.jpg
```

Šajā piemērā opcija -c liek TAR izveidot jaunu arhīvu, bet opcija -f norāda izvades faila nosaukumu (šajā gadījumā comicbook.cbt). Pēc opciju norādīšanas norādiet to failu nosaukumus, kurus vēlaties iekļaut arhīvā (page1.jpg, page2.jpg, page3.jpg).

5. Pēc komandas izpildes TAR rīks izveidos komiksu grāmatu arhīva failu (šajā piemērā comicbook.cbt) pašreizējā direktorijā.

Kad esat ieguvis komiksu grāmatu arhīva failu, varat izmantot dažādas komiksu lasītāju programmatūras vai lietojumprogrammas, lai datorā vai ierīcē atvērtu un lasītu komiksu grāmatu. Šīs lietojumprogrammas parasti nodrošina tādas funkcijas kā lapas navigācija, tālummaiņa un grāmatzīmju pievienošana, lai uzlabotu lasīšanas pieredzi.

## Ko satur CBA fails?

Komiksu grāmatu arhīva (CBA) failā, kas izveidots, izmantojot TAR arhivēšanas rīku, ir atsevišķu komiksu lapu vai attēlu kolekcija, kas apvienota vienā failā. Konkrētais arhīva saturs ir atkarīgs no iesaiņotās komiksu grāmatas.

Parasti komiksu grāmatu arhīva failā ir iekļauts:

- **Komiksu lapas:** Arhīva galvenais saturs ir pašas komiksu lapas. Šīs lapas parasti tiek saglabātas kā atsevišķi attēlu faili, piemēram, JPEG vai PNG, kas attēlo katru komiksu grāmatas lapu. Lapas ir sakārtotas noteiktā secībā, lai saglabātu komiksa stāstījuma plūsmu.
- **Metadata:** Some Comic Book Archive formats may include metadata about the comic book, such as the title, author, publisher, publication date, and description. This information helps identify and categorize the comic book.
- **Papildu faili:** papildus komiksu lapām un metadatiem arhīvā var būt arī citi ar komiksu saistīti papildu faili. Šie faili var ietvert vāka noformējumu, reklāmas attēlus, papildu saturu vai teksta failus, kas sniedz papildu informāciju vai komentārus.

## Kāds ir CBA faila formāts?

Komiksu arhīva (CBA) faila formāts, kas izveidots, izmantojot TAR arhivēšanas rīku, parasti ir TAR formātā. TAR, saīsinājums no Tape Archive, ir failu arhivēšanas formāts, ko parasti izmanto Unix un Linux sistēmās. Tas nav paredzēts komiksu grāmatām, bet ir vispārējs arhivēšanas formāts.

TAR formāts ir vienkāršs veids, kā apvienot vairākus failus vienā arhīva failā. Tas pats par sevi nenodrošina saspiešanu, tāpēc iegūtais TAR fails var būt liels salīdzinājumā ar citiem saspiestiem formātiem, piemēram, ZIP vai RAR. Tomēr TAR failus var saspiest, izmantojot papildu rīkus vai kombinēt ar saspiešanas algoritmiem, piemēram, gzip vai bzip2, lai samazinātu faila lielumu.

TAR formāts saglabā iekļauto failu failu struktūru, failu atļaujas un laikspiedolus. Tas saglabā failus secīgi arhīvā, ļaujot viegli iegūt atsevišķus failus vai visu arhīvu.

## Atsauces
* [Komiksu grāmatu arhīvs](https://en.wikipedia.org/wiki/Comic_book_archive)


