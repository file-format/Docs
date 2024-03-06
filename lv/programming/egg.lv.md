{
  "date": "2022-03-15",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EGG faila formāts — Python izplatīšanas fails",
  "description": "Uzziniet par EGG faila formātu un API, kas var izveidot un atvērt EGG failus.",
  "linktitle": "EGG",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-eg-lvg"
}
},
  "lastmod": "2022-03-15"
}

## Kas ir EGG fails?

EGG fails, kas pazīstams arī kā Python eggs, ir vecāks Python izplatīšanas formāts. Tas ir [ZIP](/compression/zip/) saspiests arhīvs ar paplašinājumu .egg un satur Python lietojumprogrammas avota failus, kā arī meta informāciju par izplatīšanu. EGG faili ir alternatīva Windows izpildāmajam failam [EXE](/executable/exe/), taču tie ir vairāku platformu faili. Šis vecākais Python izplatīšanas formāts ir aizstāts ar jaunāku Wheel (WHL) faila formātu 2010. gada sākumā.

## EGG faila formāts

EGG faili tiek saglabāti kā saspiesti ZIP arhīvi. Tas nozīmē, ka, aizstājot paplašinājumu .egg ar .zip, varēsit to atvērt ar standarta dekompresijas utilītiem, piemēram, Corel WinZIP, Microsoft Explorer vai RARLAB WinRAR.

EGG failus var izveidot, izmantojot Python pieejamo pakotni **distutils**. Vēl viens rīks, ar kuru var izveidot un atvērt EGG failus, ir **SetupTools**. EGG failus var instalēt kā pakotni, izmantojot **easy_install**.

`PIEZĪME — EGG faila formāts ir novecojis par labu jaunajam riteņa WHL faila formātam.`

## Atsauce Nr.

* [Python EGGs](https://python101.pythonlibrary.org/chapter38_eggs.html)


