{
  "date": "2023-06-12",
  "keywords": [
"bak",
"bak failas",
"BAK Chromium žymės",
"kas yra bak failas",
"kaip atidaryti bak failą",
"failą",
"bak failo plėtinys",
"pratęsimas"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "BAK failo formatas – „Chromium Bookmarks“ atsarginė kopija",
  "description": "Sužinokite apie BAK Chromium žymių formatą ir API, kurios gali kurti ir atidaryti BAK failus.",
  "linktitle": "BAK Chromium Bookmarks",
  "menu": {
    "docs": {
      "identifier": "misc-bak-chromium-lt",
      "parent": "misc"
}
},
  "lastmod": "2023-06-12"
}

## Kas yra BAK failas?

.bak failas Chromium pagrindu veikiančiose žiniatinklio naršyklėse, pvz., Google Chrome ir Microsoft Edge, iš esmės yra jūsų žymių atsarginės kopijos failas. Šios žymės išsaugomos kaip paprasto teksto sąrašas, o naudojamas failo formatas yra JSON. Šių .bak failų paskirtis yra apsaugoti jūsų žymes suteikiant atsarginę kopiją, kurią galima atkurti atsitiktinai ištrynus arba pametus.

Chromium pagrįstos naršyklės, įskaitant Google Chrome, reguliariai kuria šiuos atsarginės kopijos failus ir paprastai suteikia jiems pavadinimą Bookmarks.bak. Jie iš esmės yra jūsų žymių momentinė nuotrauka tam tikru momentu.

## Kaip naudoti .bak failą žymėms atkurti

1. **Raskite atsarginės kopijos failą:** jis paprastai yra konkrečiame aplanke, susietame su jūsų Chromium profiliu. Tiksli vieta gali skirtis priklausomai nuo jūsų operacinės sistemos.

Windows sistemoje: ieškokite C:\Users\<YourUsername> \AppData\Local\Chromium\User Data\Default\Bookmarks.bak`.

MacOS: ieškokite ~/Library/Application Support/Chromium/Default/Bookmarks.bak.

Linux sistemoje: pažymėkite ~/.config/chromium/Default/Bookmarks.bak.

3. Įsitikinkite, kad Chromium naršyklė uždaryta.
4. Pervardykite failą Bookmarks.bak pašalindami plėtinį .bak, todėl jis tiesiog vadinamas Žymės.
5. Paleiskite Chromium.

Pervadinus .bak failą į Žymės, Chromium naudos jį kaip dabartinį žymių failą, o ankstesnės žymės turėtų būti atkurtos.

## „Chromium“ žymių atsarginė kopija

Chromium žymių atsarginių kopijų kūrimas yra protinga atsargumo priemonė, siekiant užtikrinti, kad neprarastumėte svarbių išsaugotų tinklalapių ir URL. Chromium yra atvirojo kodo naršyklė, kuri yra kitų naršyklių, tokių kaip Google Chrome ir Microsoft Edge, pagrindas. Norėdami sukurti atsarginę Chromium žymių kopiją, atlikite šiuos veiksmus:

## 1 būdas: rankinis atsarginis kopijavimas

1. **Atidaryti Chromium**: kompiuteryje paleiskite Chromium naršyklę.

2. **Access Bookmarks**: Click on the three vertical dots (menu icon) in the top-right corner of the browser window. From the dropdown menu, hover over "Bookmarks" to reveal the bookmarks submenu.

3. **Export Bookmarks**: In the bookmarks submenu, click on "Bookmark manager." This will open a new tab displaying your bookmarks.

4. **Export Bookmarks**: In the bookmark manager tab, click on the three vertical dots again (usually in the upper-right corner) to open the bookmarks manager menu. From this menu, select "Export bookmarks."

5. **Pasirinkite vietą**: pasirinkite, kur kompiuteryje norite išsaugoti eksportuotą žymių failą. Numatytasis failo pavadinimas yra bookmarks.html, bet jei norite, galite jį pakeisti. Išsaugokite jį toje vietoje, kurią prisiminsite.

6. **Išsaugoti**: spustelėkite mygtuką Išsaugoti arba Eksportuoti, kad išsaugotumėte žymes kaip HTML failą.

Dabar jūsų žymių atsarginė kopija sukurta kaip HTML failas. Galite nukopijuoti šį failą į išorinį diską arba debesies saugyklą, kad ją saugotumėte.

## 2 būdas: sinchronizuokite su „Google“ paskyra (jei taikoma)

Jei esate prisijungę prie Google paskyros naudodami Chromium, taip pat galite naudoti įtaisytąją sinchronizavimo funkciją, kad žymės būtų saugios ir sinchronizuojamos visuose įrenginiuose. Tokiu būdu jūsų žymių atsarginės kopijos bus automatiškai sukurtos jūsų Google paskyroje.

1. **Atidaryti Chromium**: paleiskite Chromium naršyklę ir įsitikinkite, kad esate prisijungę prie Google paskyros.

2. **Enable Sync**: Click on the three vertical dots (menu icon) in the top-right corner of the browser window and go to "Settings."

3. **Sinchronizavimas ir Google paslaugos**: skirtuke Nustatymai spustelėkite Sinchronizuoti ir Google paslaugos kairėje šoninėje juostoje.

4. **Sinchronizuokite duomenis**: skiltyje Sinchronizavimas įsitikinkite, kad įjungta parinktis Žymės. Taip bus sinchronizuojamos jūsų žymės su Google paskyra.

Dabar bus automatiškai sukurtos jūsų žymių atsarginės kopijos ir sinchronizuojamos su Google paskyra. Juos galite pasiekti prisijungę prie Google paskyros bet kuriame įrenginyje, kuriame yra Chromium arba kita naršyklė, palaikanti Google sinchronizavimą.

Nepamirškite periodiškai kurti atsargines žymių kopijas ir rankiniu būdu, ypač jei norite vietinės kopijos, kuri priklauso ne tik nuo Google paskyros sinchronizavimo.

## Kaip atidaryti BAK failą

Jei norite ištirti neapdorotus žymių atsarginės kopijos duomenis, galite atidaryti failą Bookmarks.bak naudodami įvairius teksto redaktorius, tokius kaip Microsoft Visual Studio Code (galima naudoti keliose platformose), Microsoft Notepad (Windows vartotojams), Apple TextEdit (Mac naudotojams) arba bet kuri kita jūsų pasirinkta teksto rengyklė. Tai padarę galėsite peržiūrėti faile esančias žymes ir metaduomenis.

Galite atidaryti failą Bookmarks.bak ir peržiūrėti jo turinį naudodami įvairią teksto redagavimo programinę įrangą ir kodų rengykles. Štai keletas dažniausiai naudojamų parinkčių:

1. Visual Studio kodas (VS kodas)
2. Užrašų knygelė (Windows)
3. Teksto redagavimas (Mac)
4. Prabangus tekstas
5. Notepad++
6. Atom
7. nano ir Vim (Linux)
8. WordPad (Windows)

## Kiti BAK failai

Štai kiti failų tipai, kuriuose naudojamas **.bak** failo plėtinys.

**Duomenų bazė**
- [BAK - Database Backup File](/database/bak/)
- [BAK - Swiftpage Act! Database Backup](/database/bak-act/)
- [BAK - Microsoft SQL Server Database Backup](/database/bak-sqlserver/)

**Žaidimas**
- [BAK - Terraria World or Player Backup](/game/bak-terraria/)

**Įvairūs**
- [BAK - Backup File](/misc/bak-backup/)
- [BAK - Finale 2012 Score Backup](/misc/bak-finale/)
- [BAK - MobileTrans Backup](/misc/bak-mobiletrans/)
- [BAK - VEGAS Video Project Backup](/misc/bak-vegas/)

**Nustatymai**
- [BAK - Holo Launcher Backup](/settings/bak-holo/)

## Nuorodos
* [Chromium Bookmarks](https://www.chromium.org/user-experience/bookmarks/)
