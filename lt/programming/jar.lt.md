{
  "date": "2019-10-11",
  "keywords": [
"JAR",
".stiklainis",
"kas yra jar failas",
"kaip atidaryti jar failą",
"pratęsimas",
"failą",
"jar failas",
"jar failo formatas",
".jar plėtinys"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "JAR – Java archyvo failo formatas",
  "description": "Sužinokite apie JAR failo formatą ir API, kurios gali sukurti ir atidaryti JAR failą.",
  "linktitle": "JAR",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-ja-ltr"
}
},
  "lastmod": "2020-09-10"
}

## Kas yra JAR failas?

Failas su plėtiniu .jar yra Java archyvo failas, kuriame yra daug skirtingų su programa susijusių failų kaip vienas failas. Šis failo formatas buvo sukurtas siekiant sumažinti atsisiųstos Java programėlės įkėlimo į naršyklę greitį per HTTP operaciją, išvengiant kelių HTTP jungčių kūrimo. Viename JAR faile gali būti Java klasės failų ([.class](/programming/class/)), [images](/image/) ir [sounds](/audio/). Atskirus elementus JAR faile programos kūrėjas gali pasirašyti skaitmeniniu būdu, kad patvirtintų jų kilmę. JAR failai reguliariai naudojami kuriant funkcines API, kuriose yra specifinių funkcijų, susijusių su ta API.

## JAR failo formatas

JAR files are based on the popular [ZIP file format](/compression/zip/) that archives its individual content files in a single file. JAR file format supports compressions, resulting in a smaller file size for downloading and hence further improves the download time. The [JAR file specifications](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) artilce by Oracle gives complete details about the internal specifications of JAR files.

### Manifesto failas

Kai sukuriamas JAR failas, jame automatiškai sukuriamas manifesto failas, kuriame yra metaduomenų informacija apie JAR failo turinį. Šiame faile rodomas JAR failo viduje supakuotas turinys. Įprastas manifesto failas atrodo taip, o tai rodo aplankus ir klases, įtrauktus į JAR failą.

```
META-INF/
META-INF/MANIFEST.MF
pack/
pack/class1.class
pack/class2.class
..
..
```

#### Manifesto specifikacijos

Oracle apibrėžia manifesto specifikacijas taip.

Manifest-file: pagrindinės sekcijos nauja eilutė \*individual-section

`pagrindinis skyrius`: versija-info nauja eilutė \*pagrindinis atributas

`version-info`: Manifest-Version : version-number

`versijos numeris` : skaitmuo+{.skaitmuo+}*

main-attribute: (bet koks teisėtas pagrindinis atributas) nauja eilutė

individual-section: pavadinimas: reikšmė nauja eilutė \*perentry-atribute

`perentry-attribute`: (bet koks teisėtas nuolatinis atributas) nauja eilutė

nauja eilutė : CR LF | LF | CR (ne po LF)

skaitmuo: {0–9}

### Vykdomasis JAR

JAR failus taip pat gali sudaryti programa, kurią gali vykdyti Java virtualioji mašina (JVM), panašiai kaip ir bet kuri kita Microsoft Windows operacinės sistemos programa. Tokiu atveju JVM turi žinoti apie programos įėjimo tašką, kuris yra bet kuri klasė su viešuoju statiniu tuščiu pagrindiniu metodu. Aprašo failas identifikuoja tokią klasę su antrašte Main-Class tokiu formatu:

```
Main-Class: com.example.MyClassName
```



## Nuorodos

 * [JAR File Overview](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jarGuide.html)
 * [JAR failo formatas](https://en.wikipedia.org/wiki/JAR_(file_format))

