{
  "date" : "2019-12-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier ZIM - fișier arhivă OpenZIM",
  "description":"Aflați despre formatul de fișier ZIM și despre API-urile care pot crea și deschide fișiere ZIM.",
  "linktitle" : "ZIM",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-12-09"
}

## Ce este un fișier ZIM? ##

Fișierele cu extensia .zim sunt arhive create pentru a stoca offline conținutul Wiki. Este considerat cel mai potrivit format de fișier deschis pentru stocarea Wikipedia pe un USB. Stochează conținutul site-ului într-un format compact. Numele său provine de la „Zeno IMproved”, care a fost formatul de fișier anterior Zeno. ZIM este întreținut de proiectul [openZIM ](https://openzim.org/), care este sponsorizat de Wikimedia CH și susținut de Fundația Wikimedia. Fișierele ZIM pot fi deschise de aplicații precum Kiwix și ZIMReader. Proiectul OpenZIM a găzduit implementarea formatului de fișier ZIM pe [Github](https://github.com/openzim) pentru contribuția comunității OpenSource.

## Specificații pentru formatul fișierului ZIM

Formatul de fișier ZIM a fost dezvoltat pe lângă [formatul de fișier Zeno](https://openzim.org/wiki/Zeno_file_format) și nu este compatibil cu versiunea inversă. Specificațiile de format ale formatului de fișier ZIM sunt [disponibile online](https://openzim.org/wiki/ZIM_file_format) de openZIM pentru referință de către dezvoltatori. OpenZIM a furnizat implementare C++ open source, [LibZim](https://openzim.org/wiki/Zimlib), pentru citirea și scrierea fișierelor ZIM.

Formatul de fișier ZIM utilizează compresia LZMA2 pentru a face conținutul compact.

{{< figure src="../ZIM_File_Format.jpeg" alt="Format de fișier ZIM" >}}


### Antet ZIM

Un fișier ZIM începe cu un antet care este la offset 0. Toți constituenții se bazează pe little-endian și toate numerele întregi sunt întregi fără semn, adică uint_16, uint_32, uint_64.

|Nume câmp |Tip| Offset| Lungime| Descriere|
---|---|---|---|---|
|magicNumber| întreg| 0| 4| Numărul magic pentru a recunoaște formatul fișierului, trebuie să fie 72173914 (0x44D495A)|
|majorVersion| întreg| 4| 2| Versiunea majoră a formatului de fișier ZIM (5 sau 6)|
|minorVersion| întreg| 6| 2| Versiune minoră a formatului de fișier ZIM|
|uuid| întreg| 8| 16| ID unic al acestui fișier zim|
|număr de articole| întreg| 24| 4| numărul total de articole|
|clusterCount| întreg| 28| 4| numărul total de clustere|
|urlPtrPos| întreg| 32| 8| poziţia listei de indicatori a directorului ordonată după URL|
|titlePtrPos| întreg| 40| 8| poziţia listei de indicatori a directorului ordonată după Titlu|
|clusterPtrPos| întreg| 48| 8| poziţia listei de pointeri cluster|
|mimeListPos| întreg| 56| 8| poziţia listei de tipuri MIME (de asemenea, dimensiunea antetului)|
|mainPage| întreg| 64| 4| pagina principală sau 0xffffffff dacă nu există o pagină principală|
|layoutPage| întreg| 68| 4| pagina de aspect sau 0xffffffffff dacă nu există o pagină de aspect|
|checksumPos| întreg| 72| 8| pointer către md5checksum a acestui fișier fără suma de control în sine. Aceasta indică întotdeauna cu 16 octeți înainte de sfârșitul fișierului.|

## Referințe ##

* [OpenZIM](https://openzim.org/)
* [C++ LibZim](https://openzim.org/wiki/Zimlib)

