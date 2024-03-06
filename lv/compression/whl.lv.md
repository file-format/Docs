{
  "date": "2022-06-29",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WHL faila formāts — Python Wheel pakotnes fails",
  "description": "Uzziniet par WHL failu formātu un API, kas var izveidot un atvērt WHL failus.",
  "linktitle": "WHL",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-wh-lvl"
}
},
  "lastmod": "2022-06-29"
}

## Kas ir WHL fails?

WHL (Wheel) fails ir izplatīšanas pakotnes fails, kas saglabāts Python riteņa formātā. Tā ir Python izplatījumu standarta formāta instalācija, un tajā ir visi instalēšanai nepieciešamie faili un metadati. WHL failā ir arī informācija par Python versijām un platformām, kuras atbalsta šis riteņa fails. Līdzīgi kā [MSI](/executable/msi/) iestatīšanas failam, arī WHL faila formāts ir gatavs instalēšanai, kas ļauj palaist instalācijas pakotni, neveidojot avota izplatīšanu.

## WHL faila formāts

WHL faila formāts ir [ZIP](/compression/zip/) (.zip) arhīvs, kurā ir visi instalācijas faili un metadati, kas instalētājiem nepieciešami pakotnes instalēšanai. Šos WHL failus var iegūt, izmantojot unzip opciju vai standarta dekompresijas programmatūras lietojumprogrammas, piemēram, WinZIP un WinRAR.

### WHL failu nosaukumu konvencija

WHL fails tiek nosaukts saskaņā ar šādu vienošanos.

```
{dist}-{version}(-{build})?-{python}-{abi}-{platform}.whl
```

WHL faila nosaukuma piemērs ir šāds.

```
cryptography-2.9.2-cp35-abi3-macosx_10_9_x86_64.whl
```

 * kriptogrāfija ir pakotnes nosaukums.
 * 2.9.2” ir kriptogrāfijas pakotnes versija. Versija ir ar PEP 440 saderīga virkne, piemēram, 2.9.2, 3.4 vai 3.9.0.a3.
 * cp35 ir Python tags un apzīmē Python ieviešanu un versiju, kas nepieciešama ritenim.
 * abi3” ir ABI tags. ABI apzīmē lietojumprogrammu bināro interfeisu.
 * `macosx_10_9_x86_64' ir platformas tags, kas mēdz būt diezgan garšīgs.

## Atsauces

* [Kas ir Python riteņi un kāpēc jums tas būtu jārūpējas?](https://realpython.com/python-wheels/)

* [Python Wheel](https://pypi.org/project/wheel/)


