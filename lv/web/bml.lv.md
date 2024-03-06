{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "BML faila formāts — pupiņu iezīmēšanas valodas fails",
  "description": "Uzziniet par BML failu formātu un API, kas var izveidot un atvērt BML failus.",
  "linktitle": "BML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-bm-lvl"
}
},
  "lastmod": "2021-08-12"
}

## Kas ir BML fails?

Fails ar paplašinājumu .bml ir pupiņu iezīmēšanas valodas fails, kurā tiek saglabātas Java klases Java programmu atbalstam. Tas ļauj piekļūt Java objektiem un metodēm, un nav jāizveido jauna funkcionalitāte, izmantojot Java klases. Tas norāda, kā komponenti ir savienoti viens ar otru, lai veiktu noderīgus uzdevumus. BML izstrādāja IBM alphaWorks, lai aprakstītu struktūras un komponentu attiecības. BML failus var atvērt un skatīt, izmantojot jebkuru teksta redaktoru, piemēram, Web Browsers, Microsoft Notepad un Notepad++.

## BML faila formāts

IBM alphaworks vietne ir nodrošinājusi divas BML ieviešanas. Pirmā ieviešana ir tulks, kas atskaņo BML skriptu, lai ģenerētu vēlamo pupiņu hierarhiju. Otrais variants ir kompilators, kas kompilē jebkuru BML skriptu Java kodā bez refleksijas. Tas ir izdevīgi tādā ziņā, ka ļauj uztvert lietojumprogrammas starpkomponentu struktūru, izmantojot valodu, kas ir paredzēta šim konkrētajam mērķim, ar papildu iespēju to apkopot parastā” Java kodā.

## BML tagi

Tālāk ir sniegts dažu BML valodā izmantoto tagu skaidrojums.

### The<bean> tags:

The<bean> elements tiek izmantots, lai izveidotu jaunas pupiņas vai meklētu pupiņas pēc nosaukuma. The<bean> tagam ir šāds formāts:
```
<bean class = "classname or serialized file" [id = "name"]>
</bean>
```
Tagā esošais id ir saistīts ar JavaBean objektu reģistru.

### The<string> tagu

Virknes tagu var izmantot divos veidos:

 1. Lai izveidotu virkni, kas nav tukša:

```
<string [value = "value of string"]> [value of string]
</string>
```
 2. Lai izveidotu tukšu virkni:

```
<string/>
```
## Atsauces

* [Object-Oriented Messaging with XML](https://docs.oracle.com/cd/A87860_01/doc/appdev.817/a86030/adx16nt5.htm)
* [Fiziskā iezīmēšanas valoda] (http://web.mit.edu/mecheng/pml/standards.htm)



