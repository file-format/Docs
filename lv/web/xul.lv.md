{
  "date": "2021-05-24",
  "keywords": [
"xul",
"Fails",
"Pagarinājums",
"Faila formāts",
"Faila paplašinājums",
"XML lietotāja interfeisa valoda"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XUL — XML lietotāja interfeisa valodas fails",
  "description": "Uzziniet par XUL failu formātu un API, kas var izveidot un atvērt XUL failus.",
  "linktitle": "XUL",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-xu-lvl"
}
},
  "lastmod": "2021-05-24"
}

## Kas ir XUL fails?

Fails ar paplašinājumu .xul ([XUL](https://wiki.mozilla.org/XUL:Home_Page) apzīmē XML lietotāja interfeisa valodu) ir uz [XML](/web/xml/) balstīts iezīmēšanas valodas fails lietotāja saskarņu izveidei. Mozilla to izstrādāja izstrādātājiem, lai izveidotu grafiskos lietotāja interfeisa elementus, kas līdzīgi citām iezīmēšanas valodām, ko izmanto tīmekļa lapu izveidei. Mozilla XUL plaši izmanto savā Firefox pārlūkprogrammā, kur tā izmantoja Mozilla kodu bāzi. XUL renderēšana tiek veikta, izmantojot
{{HIPERSAITE1}}). Firefox dakšas, piemēram, Pale Moon, Basilisk un Waterfox, saglabā atbalstu XUL papildinājumiem. XUL faili tiek identificēti ar MIME veidu: application/vnd.mozilla.xul+xml.

## XUL faila formāts

XUL faili ir rakstīti vienkāršā tekstā, pamatojoties uz XML faila formātu, un tiek atveidoti, izmantojot Gecko dzinēju. Trīs galvenās XUL struktūras daļas ir:

 * Saturs — tas ietver loga deklarācijas un tajās ietvertos lietotāja interfeisa elementus.
 * Āda — tajā ir iekļautas visas stila lapas, attēli un citi ar tēmām saistīti faili. Loga izskats ir aprakstīts stilu lapās.
 * `Locale` — logā redzamais teksts tiek glabāts atsevišķi, un lietotāji var izmantot vairākas valodu failu kopas.

### XUL piemērs

Nākamajā piemērā ir izveidotas trīs pogas, kas ir sakrautas viena virs otras vertikālā virzienā.

```
<?xml version="1.0"?>
<?xml-stylesheet href="chrome://global/skin/" type="text/css"?>

<window id="vbox example" title="Example 3...."
xmlns="http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul">
  <layout>
    <button id="yes1" label="Yes"/>
    <button id="no1" label="No"/>
    <button id="maybe1" label="Maybe"/>
  </layout>
</window>
```

## Atsauces

* [XUL — Wikipedia](https://en.wikipedia.org/wiki/XUL)

* [XUL arhivētā dokumentācija — Mozilla](https://wiki.mozilla.org/XUL:Home_Page)


