{
  "date": "2019-10-11",
  "keywords": [
"xaml",
"xaml failu",
"xaml faila formātā",
"xaml faila tips",
"failu",
"veids",
"kas ir xaml fails"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XAML — uz XML balstīta iezīmēšanas valoda",
  "description": "Uzziniet par XAML failu formātu un API, kas var izveidot un atvērt XAML failus.",
  "linktitle": "XAML ",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-xam-lvl"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir XAML fails?

XAML, Extensible Application Markup Language, paplašinājumu faili apraksta lietotāja interfeisa elementus lietojumprogrammām, kuru pamatā ir Windows prezentācijas fonds (WPF). Lai gan tā ir valoda, tā nav jāprogrammē, jo tā ir balstīta uz standarta formātu **[XML](/web/xml/)**, kas ir viegli lietojams un saprotams. XAML (izrunā kā zammel) izstrādāja Microsoft ar īpašu mērķi izveidot lietotāja saskarnes. Tā akronīma oriģināls apzīmēja Extensible Avalon Markup Language, kur Avalon bija WPF koda nosaukums. XAML faili dažreiz tiek saglabāti arī ar XOML paplašinājumu.

## XAML lietojumprogrammas

XAML ir izvēle lietošanai .NET Framework 3.0 un .NET Framework 4.0 tehnoloģijās, piemēram, WPF, Silverlight, Windows Workflow Foundation (WF) un dažās citās. UI elementi, datu saistījumi, notikumi un citi līdzekļi tiek definēti ar XAML formām WPF. Līdzīgi, WF darbplūsmas var definēt, izmantojot XAML. Tas ir viegli apstrādājams ar rīkiem, jo tas ir balstīts uz XML. Tā kā tā ir deklaratīva valoda un tai nav nepieciešama kompilācija, tiek parādīti daudzi produkti, kuru pamatā ir XAML lietojumprogrammas. Jebko, kas ir izveidots vai ieviests XAML, var izteikt, izmantojot tradicionālāku .NET valodu, piemēram, C# vai Visual Basic .NET.

## XAML faila formāts

XAML is totally based on the XML format. The initial specifications of [XAML Object Mapping](https://download.microsoft.com/download/0/A/6/0A6F7755-9AF5-448B-907D-13985ACCF53E/%5BMS-XAML%5D.pdf) were published in 2006, followed by another [version](https://download.microsoft.com/download/0/A/6/0A6F7755-9AF5-448B-907D-13985ACCF53E/%5BMS-XAML-2009%5D.pdf) published in 2009. Šīs specifikācijas nosaka divus abstraktas informācijas modeļus:

* XAML shēmas informācijas kopas modelis

* XAML informācijas kopas modelis


Xaml informācijas kopa (īsumā Xaml Infoset) nosaka informācijas struktūru, ko var attēlot Xaml instance. Xaml shēmas informācijas kopa ļauj definēt noteiktas Xaml vārdnīcas. Šī specifikācija definē arī noteikumu kopumu XML dokumenta pārveidošanai par Xaml informācijas kopu. XML ir izplatīts Xaml formāts. (Termins Xaml dokuments attiecas uz XML dokumentu, kas attēlo Xaml informācijas kopu.) Bet, lai gan šī specifikācija nedefinē citus attēlojumus, var izmantot jebkuru fizisko attēlojumu, ja vien tas var attēlot informāciju Xaml informācijas komplektā. .

## Atsauces

* [XAML — Wikipedia](https://en.wikipedia.org/wiki/Extensible_Application_Markup_Language)

* [XAML faila formāta specifikācijas](https://download.microsoft.com/download/0/A/6/0A6F7755-9AF5-448B-907D-13985ACCF53E/%5BMS-XAML-2009%5D.pdf)


