{
  "date": "2023-06-08",
  "keywords": [
"crx failu",
"kas ir crx fails",
"Kā instalēt crx failu pārlūkā Google Chrome",
"kā atvērt crx failu",
"ko satur crx fails",
"kāds ir crx faila formāts",
"failu",
"crx faila paplašinājums",
"pagarinājumu"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "CRX faila formāts — Google Chrome paplašinājums",
  "description": "Uzziniet par CRX formātu un API, kas var izveidot un atvērt CRX failus.",
  "linktitle": "CRX",
  "menu": {
    "docs": {
      "identifier": "misc-crx-lv",
      "parent": "misc"
}
},
  "lastmod": "2023-06-08"
}

## Kas ir CRX fails?

CRX faila formāts ir saistīts ar Google Chrome pārlūkprogrammas paplašinājumiem. CRX fails būtībā ir saspiesta pakotne, kurā ir nepieciešamie faili un metadati paplašinājumam, ko instalēt un palaist pārlūkā Google Chrome. Tas uzlabo tīmekļa pārlūkprogrammas funkcionalitāti vai izskatu, nodrošinot papildu funkciju vai motīvu.

Kad pārlūkprogrammā Google Chrome tiek lejupielādēts un instalēts CRX fails, pārlūkprogramma pārbauda paplašinājuma integritāti, izmantojot publisko atslēgu un parakstu. Ja verifikācija ir veiksmīga, Chrome izvelk CRX faila saturu un instalē paplašinājumu, padarot to pieejamu lietošanai. Lietotāji var pārvaldīt savus paplašinājumus, izmantojot Chrome paplašinājumu lapu, kas ļauj iespējot, atspējot vai noņemt instalētos paplašinājumus.

## Kā instalēt CRX failu pārlūkprogrammā Google Chrome?

Lai pārlūkprogrammā Google Chrome instalētu CRX failu, varat veikt šādas darbības:

1. Atveriet pārlūkprogrammu Chrome.
2. Adreses joslā ierakstiet chrome://extensions” un nospiediet taustiņu Enter.
3. Iespējojiet Izstrādātāja režīma” pārslēgšanas slēdzi, kas atrodas paplašinājumu lapas augšējā labajā stūrī.
4. Noklikšķiniet uz pogas Ielādēt neizpakoto.
5. Atrodiet un atlasiet mapi, kurā ir izvilkts CRX faila saturs (vai vienkārši atlasiet pašu CRX failu).
6. Noklikšķiniet uz Atvērt, lai instalētu paplašinājumu.

## Ko satur CRX fails?

CRX fails satur nepieciešamos failus un metadatus, kas nepieciešami Google Chrome paplašinājumam. Šeit ir CRX failā atrastā tipiskā satura sadalījums:

- **Manifest file (manifest.json):** This file is a JSON-formatted file that includes information about extension such as its name, version, description, permissions and background scripts. It defines the structure and behavior of extension.
- **JavaScript faili:** šajos failos ir kods, kas nosaka paplašinājuma funkcionalitāti. Tie var ietvert skriptus notikumu apstrādei, tīmekļa lapu pārveidošanai vai mijiedarbībai ar Chrome API.
- **HTML, CSS un attēlu faili:** paplašinājumos bieži ir iekļauti lietotāja interfeisa elementi, piemēram, uznirstošie logi vai opciju lapas. HTML faili nosaka šo saskarņu struktūru, savukārt CSS faili kontrolē to izskatu. Attēlu faili tiek izmantoti ikonām vai citiem grafiskiem līdzekļiem.
- **Neobligātie resursu faili:** paplašinājumos var būt iekļauti papildu resursi, piemēram, lokalizācijas faili vairāku valodu atbalstam. Šajos failos ir ietverti paplašinājuma lietotāja saskarnē izmantotā teksta tulkojumi.
- **Fona skripti:** ja paplašinājumam ir fona procesi vai skripti, kas darbojas neatkarīgi no aktīvās tīmekļa lapas, šie skripti tiks iekļauti CRX failā.
- **Satura skripti:** satura skripti ir skripti, kurus var ievadīt tīmekļa lapās, lai mainītu to darbību vai mijiedarbotos ar to saturu. Ja paplašinājums izmanto satura skriptus, šiem skriptiem nepieciešamie faili būs pieejami CRX failā.
- **Citi līdzekļi:** atkarībā no īpašām paplašinājuma prasībām var tikt iekļauti papildu faili, piemēram, audio vai video faili, fonti vai datu faili.

CRX faila formāts būtībā ir saspiesta pakotne, kas satur visus šos failus un mapes strukturētā veidā. Kad pārlūkprogrammā Google Chrome ir instalēts CRX fails, pārlūkprogramma izvelk saturu un ievieto to atbilstošās vietās, ļaujot paplašinājumam ielādēt un palaist pārlūkprogrammā.

## Kāds ir CRX faila formāts?

CRX faila formāts ir īpašs Google Chrome paplašinājumu iesaiņošanas un izplatīšanas formāts. Tas būtībā ir saspiests ZIP arhīvs ar dažādu faila paplašinājumu. CRX faila pamatstruktūra ir šāda:

- **Faila paraksts:** pirmajos 4 faila baitos ir maģiskais numurs Cr24 (heksadecimāls: 43 72 32 34), kas kalpo kā paraksts, lai identificētu failu kā CRX failu.
- **Versijas numurs:** nākamie 4 baiti apzīmē CRX formāta versijas numuru.
- **Publiskās atslēgas garums:** tālāk norādītie 4 baiti norāda paplašinājuma paraksta pārbaudei izmantotās kodētās publiskās atslēgas garumu.
- **Paraksta garums:** nākamie 4 baiti norāda paplašinājuma paraksta garumu.
- **Publiskā atslēga:** šajā sadaļā ir ietverta kodētā publiskā atslēga, ko izmanto paplašinājuma integritātes pārbaudei.
- **Paraksts:** šajā sadaļā ir ietverts paplašinājuma paraksts, kas tiek ģenerēts, parakstot paplašinājuma saturu, izmantojot privāto atslēgu, kas atbilst iepriekš minētajai publiskajai atslēgai.
- **ZIP arhīvs:** atlikušie CRX faila baiti ietver saspiestu ZIP arhīvu. Šajā arhīvā ir visi nepieciešamie paplašinājumu faili un mapes, tostarp manifesta faili, JavaScript faili, HTML faili, CSS faili, attēli un citi resursi.

## Atsauces
* [CRX formāta specifikācija](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/K3YIsNL_Et4)


