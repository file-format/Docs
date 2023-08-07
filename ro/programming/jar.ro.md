{
  "date" : "2019-10-11",
  "keywords" :[ "JAR", ".jar", "ce este un fișier jar", "cum se deschide un fișier jar", "extensie", "fișier", "fișier jar", "format de fișier jar", "extensie .jar"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JAR – Format de fișier arhivă Java",
  "description":"Aflați despre formatul de fișier JAR și despre API-urile care pot crea și deschide fișierul JAR.",
  "linktitle" : "JAR",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Ce este un fișier JAR?

Un fișier cu extensia .jar este un fișier Java Archive care conține multe fișiere diferite legate de aplicații ca un singur fișier. Acest format de fișier a fost creat pentru a reduce viteza de încărcare a unui Applet Java descărcat în browser prin tranzacție HTTP, evitând crearea de conexiuni HTTP multiple. Un singur fișier JAR poate conține fișiere de clasă Java ([.class](/ro/programming/class/)), [imagini](/ro/image/) și [sunete](/ro/audio/). Elementele individuale dintr-un fișier JAR pot fi semnate digital de către dezvoltatorul aplicației pentru a le autentifica originea. Fișierele JAR sunt utilizate în mod regulat pentru a crea API funcționale care conțin funcționalități specifice legate de acel API.

## Format de fișier JAR

Fișierele JAR se bazează pe popularul [format de fișier ZIP](/ro/compression/zip/) care arhivează fișierele individuale de conținut într-un singur fișier. Formatul de fișier JAR acceptă compresii, ceea ce duce la o dimensiune mai mică a fișierului pentru descărcare și, prin urmare, îmbunătățește și mai mult timpul de descărcare. [Specificațiile fișierului JAR](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) articol de Oracle oferă detalii complete despre specificațiile interne ale fișierelor JAR.

### Fișierul manifest

Când este creat un fișier JAR, în interiorul acestuia este creat automat un fișier manifest care conține informații despre metadate despre conținutul fișierului JAR. Acest fișier arată conținutul care este împachetat în fișierul JAR. Un fișier Manifest tipic arată după cum urmează, care arată folderele și clasele incluse în fișierul JAR.

```
META-INF/
META-INF/MANIFEST.MF
pack/
pack/class1.class
pack/class2.class
..
..
```

#### Specificații Manifest

Specificațiile manifestului sunt definite de Oracle după cum urmează.

`fișier-manifest`: secțiunea principală newline \*secțiune-individuală

`main-section`: info-versiune newline \*principal-atribut

`version-info`: Manifest-Version: versiune-număr

`version-number`: cifră+{.cifră+}*

`principal-atribut`: (orice atribut principal legitim) linie nouă

`secțiune-individuală`: Nume: valoare newline \*perentry-attribute

`perentry-attribute`: (orice atribut perentry legitim) linie nouă

`newline`: CR LF | LF | CR (nu urmat de LF)

`digit`: {0-9}

### JAR executabil

Fișierele JAR pot cuprinde, de asemenea, o aplicație care poate fi executată de Java Virtual Machine (JVM) similar cu orice altă aplicație de pe sistemul de operare Microsoft Windows. În acest caz, JVM-ul trebuie să știe despre punctul de intrare al aplicației care este orice clasă cu o metodă publică static void main. Fișierul manifest identifică o astfel de clasă cu antetul „Main-Class” în următorul format:

```
Main-Class: com.example.MyClassName
```



## Referințe

* [Prezentare generală a fișierului JAR](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jarGuide.html)
* [Format fișier JAR](https://en.wikipedia.org/wiki/JAR_(file_format))

