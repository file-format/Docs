{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EML — e-pasta ziņojums",
  "description": "Uzziniet par EML failu formātu un API, kas var izveidot un atvērt EML failus.",
  "linktitle": "EML",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-em-lvl"
}
},
  "lastmod": "2019-09-16"
}

## Kas ir EML fails?

EML faila formāts ir e-pasta ziņojumi, kas saglabāti, izmantojot Outlook un citas atbilstošas lietojumprogrammas. Gandrīz visi e-pasta klienti atbalsta šo faila formātu, lai tas atbilstu RFC-822 interneta ziņojumu formāta standartam. Microsoft Outlook ir noklusējuma programmatūra EML ziņojumu veidu atvēršanai. EML failus var izmantot gan saglabāšanai diskā, gan izsūtīšanai adresātiem, izmantojot sakaru protokolus.

## Īsa EML vēsture

EML faila formāta specifikācijas ir pieejamas [RFC 822](https://www.ietf.org/rfc/rfc0822.txt) standarta formātā. Pirms RFC-822, RFC-733 regulēja tīkla ziņojumu apmaiņas noteikumus, līdz 1982. gadā pirmais tika izveidots kā sānu uzlabojums, izveidojot ARPA standartus. Tajā pašā laikā Microsoft izveidoja savus COM moduļus sava e-pasta klienta, ti, Outlook Express, izstrādei. RFC-822 tika izveidots kā patentēts formāts, kad Microsoft novirzījās no atvērtā standarta un izveidoja [PST](/email/pst/) faila formātu, kurā e-pasta ziņojumi tiek saglabāti ļoti strukturētā datu bāzes formātā. Tas radīja problēmas lietotājiem, kas nav Microsoft e-pasta klienti, kad e-pasta ziņojumi tika pārsūtīti no Microsoft Outlook.

Tas notika 2001. gadā, kad standarts 822 tika uzlabots līdz 2822 — interneta ziņojumu formātam, kas pašlaik tiek izmantots, lai izveidotu, lasītu un nosūtītu EML ziņojumus MIME RFC-822 formātā.

## EML faila formāta specifikācijas

EML faili sastāv no divām atšķirīgām sadaļām:

* **Galvenes** — satur informāciju par ziņojuma galveni

* **Ziņojuma pamatteksts** — satur virkni informācijas, kas var ietvert ziņojuma saturu, iegultos attēlus un pielikumus


### Galvenes informācija ###

EML fails sastāv no galveņu informācijas un pēc izvēles ziņojuma pamatteksta. Katrai EML galvenes rindai ir divas daļas, kas atdalītas ar kolu :. Pirmo sauc par galvenes nosaukumu, bet pēc kola ir virsraksta pamatteksts. Piemēram, šādas galvenes ietver:

* Sūtītāja e-pasta adrese

* Saņēmēja e-pasta adrese

* E-pasta tēma

* Ziņojuma laika un datuma zīmogs


**Galvenes piemērs**

```
From: <John@bmw.eml.light.com>

To: <Andy@fileformat.com>

Date: Thu, 8 Mar 2018 10:43:37 +0100

Subject: bmw eml light
```

### Ziņojuma pamatteksts ###

EML ziņojuma pamatteksts satur primāro e-pasta informāciju teksta, hipersaišu un pielikumu veidā. E-pasta pamattekstā var būt vienkāršs lasāms teksts, taču tas nav nepieciešams. Šajā gadījumā ziņojuma pamatteksts var būt tukšs vai tajā var būt kodēti pielikumu dati.

Ziņojuma pamatteksta saturu apraksta tā satura veids, kas ļauj lasīšanas lietojumprogrammām lasīt informāciju attiecīgajos formātos. Tas faktiski atspoguļo dokumenta būtību un formātu. MIME tipa vai satura tipa struktūra ir ļoti vienkārša; tas sastāv no tipa un apakštipa, divām virknēm, kas atdalītas ar '/'. Vieta nav atļauta. Tips apzīmē kategoriju un var būt diskrēts vai vairāku daļu veids. Apakštips ir raksturīgs katram veidam. Satura veida kategorijā ietilpstošo veidu saraksts ir garš, taču daži svarīgi satura veidi ir šādi:


|**Veids**|**Apraksts**|**Apakštipu piemērs**
---|---|---|
|text|Apzīmē formātu, kas ir cilvēkiem lasāms|teksts/vienkāršs, teksts/html, teksts/css, teksts/javascript
|image|Attēlo jebkura veida attēlu, izņemot videoklipus|attēls/bmp, attēls/png, attēls/jpg, attēls/gif
|audio|Attēlo jebkuru audio faila formātu|audio/mdi, audio/wav
|aplikācija|Apzīmē jebkāda veida bināros datus|application/octet-stream, application/vnd.mspowerpoint, application/xhtml+xml, application/xml, application/pdf

### Pieķeršanās attēlojums EML pamattekstā

EML pamattekstā ir ietvertas robežas katram saturam, ko tas satur. Pielikums ziņojuma pamattekstā tiek identificēts pēc tā satura veida un satura izvietojuma, kā parādīts šajā piemērā:

Satura veids: teksts/vienkāršs; rakstzīmju kopa #windows-1252; name#apple app store.txt
Saturs-Izkārtojums: pieķeršanās; faila nosaukums#apple app store.txt
Satura pārsūtīšana-kodēšana: base64
X pielikuma ID: f_jkhztmd02

Kā redzams, satura izvietojums, kas iestatīts uz pielikumu, ļauj lasīšanas lietojumprogrammām iegūt pielikuma informāciju, piemēram, pielikuma faila nosaukumu un pārsūtīšanas kodējumu. Pielikuma galvenes informācijai seko kodēts pielikuma saturs, kas ir jālasa.

#### Izklājlapas kā pielikuma piemērs

Satura veids: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet; name#english_spodr.xlsx
Saturs-Izkārtojums: pieķeršanās; faila nosaukums#english_spodr.xlsx
Satura pārsūtīšana-kodēšana: base64
X pielikuma ID: f_jkhztmd43

## Kā atvērt EML failu

EML failus var atvērt, izmantojot dažādas e-pasta programmas, piemēram:

 * **Apple Mail operētājsistēmā macOS**
 * **Mozilla Thunderbird**
 * **Microsoft Outlook**

EML faili tiek saglabāti vienkārša teksta formātā, un jūs varat arī atvērt šos EML failus ar populāriem teksta redaktoriem, piemēram, **TextEdit** operētājsistēmā MacOS un **Microsoft Notepad** operētājsistēmā Windows.

## Kā konvertēt EML failu

Varat konvertēt EML failus vairākos citos formātos, izmantojot tādas lietojumprogrammas kā Apple Mail un Microsoft Outlook.

Piemēram, Microsoft Outlook var pārvērst EML failu šādos formātos:

**[.MSG](/eml/msg/)** — Microsoft Outlook ziņojuma formāts
**[.PDF](/pdf/)** — Protable Document Format

## Atsauces

* [RFC 822](https://www.ietf.org/rfc/rfc0822.txt)


