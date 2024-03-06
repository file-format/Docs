{
  "date": "2023-06-12",
  "keywords": [
"bak",
"bak fails",
"BAK Chromium grāmatzīmes",
"kas ir bak fails",
"kā atvērt bak failu",
"failu",
"bak faila paplašinājums",
"pagarinājumu"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "BAK faila formāts — Chromium grāmatzīmju dublējums",
  "description": "Uzziniet par BAK Chromium grāmatzīmju formātu un API, kas var izveidot un atvērt BAK failus.",
  "linktitle": "BAK Chromium Bookmarks",
  "menu": {
    "docs": {
      "identifier": "misc-bak-chromium-lv",
      "parent": "misc"
}
},
  "lastmod": "2023-06-12"
}

## Kas ir BAK fails?

.bak fails Chromium balstītu tīmekļa pārlūkprogrammu, piemēram, Google Chrome un Microsoft Edge, kontekstā būtībā ir jūsu grāmatzīmju dublējuma fails. Šīs grāmatzīmes tiek saglabātas kā vienkārša teksta saraksts, un izmantotais faila formāts ir JSON. Šo .bak failu mērķis ir aizsargāt jūsu grāmatzīmes, nodrošinot dublējumu, ko var atjaunot nejaušas dzēšanas vai pazaudēšanas gadījumā.

Pārlūkprogrammas, kuru pamatā ir Chromium, regulāri izveido šos dublējuma failus un parasti piešķir tiem nosaukumu Bookmarks.bak”. Tie būtībā ir jūsu grāmatzīmju momentuzņēmums noteiktā brīdī.

## Kā izmantot .bak failu, lai atjaunotu grāmatzīmes

1. **Atrodiet dublējuma failu:** tas parasti atrodas noteiktā mapē, kas saistīta ar jūsu Chromium profilu. Precīza atrašanās vieta var atšķirties atkarībā no operētājsistēmas.

Operētājsistēmā Windows: skatiet `C:\Users\<YourUsername> \AppData\Local\Chromium\User Data\Default\Bookmarks.bak`.

Operētājsistēmā macOS: meklējiet mapē ~/Library/Application Support/Chromium/Default/Bookmarks.bak.

Operētājsistēmā Linux: pārbaudiet ~/.config/chromium/Default/Bookmarks.bak”.

3. Pārliecinieties, vai pārlūkprogramma Chromium ir aizvērta.
4. Pārdēvējiet failu Bookmarks.bak, noņemot paplašinājumu .bak, tāpēc to vienkārši sauc par Grāmatzīmēm.
5. Sāciet Chromium.

Pārdēvējot .bak failu par Grāmatzīmes”, Chromium to izmantos kā pašreizējo grāmatzīmju failu, un jūsu iepriekšējās grāmatzīmes ir jāatjauno.

## Chromium grāmatzīmju dublēšana

Chromium grāmatzīmju dublēšana ir saprātīgs piesardzības pasākums, lai nepazaudētu svarīgās saglabātās tīmekļa lapas un vietrāžus URL. Chromium ir atvērtā pirmkoda pārlūkprogramma, kas kalpo par pamatu citām pārlūkprogrammām, piemēram, Google Chrome un Microsoft Edge. Lai dublētu Chromium grāmatzīmes, veiciet tālāk norādītās darbības.

## 1. metode: manuāla dublēšana

1. **Atvērt Chromium**: palaidiet Chromium pārlūkprogrammu savā datorā.

2. **Access Bookmarks**: Click on the three vertical dots (menu icon) in the top-right corner of the browser window. From the dropdown menu, hover over "Bookmarks" to reveal the bookmarks submenu.

3. **Export Bookmarks**: In the bookmarks submenu, click on "Bookmark manager." This will open a new tab displaying your bookmarks.

4. **Export Bookmarks**: In the bookmark manager tab, click on the three vertical dots again (usually in the upper-right corner) to open the bookmarks manager menu. From this menu, select "Export bookmarks."

5. **Izvēlēties atrašanās vietu**: izvēlieties, kur datorā vēlaties saglabāt eksportēto grāmatzīmju failu. Noklusējuma faila nosaukums ir bookmarks.html, taču varat to mainīt, ja vēlaties. Saglabājiet to vietā, kuru atcerēsities.

6. **Saglabāt**: noklikšķiniet uz pogas Saglabāt vai Eksportēt, lai saglabātu grāmatzīmes kā HTML failu.

Jūsu grāmatzīmes tagad ir dublētas kā HTML fails. Varat kopēt šo failu ārējā diskdzinī vai mākoņkrātuvē glabāšanai.

## 2. metode: sinhronizējiet ar Google kontu (ja piemērojams)

Ja pārlūkprogrammā Chromium esat pierakstījies Google kontā, varat arī izmantot iebūvēto sinhronizācijas funkciju, lai grāmatzīmes būtu drošībā un sinhronizētas dažādās ierīcēs. Tādā veidā jūsu grāmatzīmes tiks automātiski dublētas jūsu Google kontā.

1. **Atvērt Chromium**: palaidiet pārlūkprogrammu Chromium un pārliecinieties, ka esat pierakstījies savā Google kontā.

2. **Enable Sync**: Click on the three vertical dots (menu icon) in the top-right corner of the browser window and go to "Settings."

3. **Sinhronizācija un Google pakalpojumi**: cilnes Iestatījumi kreisajā sānjoslā noklikšķiniet uz Sinhronizēt un Google pakalpojumi.

4. **Sinhronizējiet savus datus**: sadaļā Sinhronizācija” pārbaudiet, vai ir ieslēgta opcija Grāmatzīmes. Tādējādi jūsu grāmatzīmes tiks sinhronizētas ar jūsu Google kontu.

Jūsu grāmatzīmes tagad tiks automātiski dublētas un sinhronizētas ar jūsu Google kontu. Varat tiem piekļūt, pierakstoties savā Google kontā jebkurā ierīcē ar Chromium vai citu pārlūkprogrammu, kas atbalsta Google sinhronizāciju.

Atcerieties periodiski arī manuāli dublēt savas grāmatzīmes, it īpaši, ja vēlaties lokālu kopiju, kas nav atkarīga tikai no jūsu Google konta sinhronizācijas.

## Kā atvērt BAK failu

Ja vēlaties izpētīt grāmatzīmju dublējuma neapstrādātos datus, varat atvērt failu Bookmarks.bak ar dažādiem teksta redaktoriem, piemēram, Microsoft Visual Studio Code (pieejams vairākās platformās), Microsoft Notepad (Windows lietotājiem), Apple TextEdit. (Mac lietotājiem) vai jebkuru citu teksta redaktoru pēc jūsu izvēles. To darot, varēsit skatīt failā esošās grāmatzīmes un metadatus.

Varat atvērt failu Bookmarks.bak un skatīt tā saturu, izmantojot dažādas teksta rediģēšanas programmatūras un kodu redaktorus. Šeit ir dažas biežāk izmantotās iespējas:

1. Visual Studio kods (VS kods)
2. Notepad (Windows)
3. TextEdit (Mac)
4. Cildens teksts
5. Notepad++
6. Atom
7. nano un Vim (Linux)
8. WordPad (Windows)

## Citi BAK faili

Šeit ir citi failu tipi, kas izmanto faila paplašinājumu **.bak**.

**Datu bāze**
- [BAK - Database Backup File](/database/bak/)
- [BAK - Swiftpage Act! Database Backup](/database/bak-act/)
- [BAK - Microsoft SQL Server Database Backup](/database/bak-sqlserver/)

**Spēle**
- [BAK - Terraria World or Player Backup](/game/bak-terraria/)

**Dažādi**
- [BAK - Backup File](/misc/bak-backup/)
- [BAK - Finale 2012 Score Backup](/misc/bak-finale/)
- [BAK - MobileTrans Backup](/misc/bak-mobiletrans/)
- [BAK - VEGAS Video Project Backup](/misc/bak-vegas/)

**Iestatījumi**
- [BAK - Holo Launcher Backup](/settings/bak-holo/)

## Atsauces
* [Chromium Bookmarks](https://www.chromium.org/user-experience/bookmarks/)
