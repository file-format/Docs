{
  "date" : "2019-10-11",
  "keywords" :[ "fișier dng", "format fișier dng", "ce este un fișier dng", "fișier", "exemplu dng", "extensie fișier dng", "extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DNG – Format de fișier imagine al camerei digitale",
  "description":"Aflați despre formatul de fișier DNG și despre API-urile care pot crea și deschide fișiere DNG.",
  "linktitle" : "DNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier DNG?

DNG este un format de imagine pentru camera digitală utilizat pentru stocarea fișierelor brute. A fost dezvoltat de Adobe în septembrie 2004. A fost dezvoltat practic pentru fotografia digitală. DNG este o extensie a formatului standard [TIFF](/ro/image/tiff/)/EP și utilizează metadatele în mod semnificativ. Pentru a manipula datele brute de la camerele digitale cu ușurința de flexibilitate și control artistic, fotografi optează pentru fișierele brute ale camerei. Formatele JPEG și TIFF stochează imagini care sunt procesate de cameră, prin urmare, nu este disponibil prea mult spațiu pentru modificare în astfel de formate.

## Istoricul și versiunile formatului de fișier DNG

Până acum au existat 5 versiuni ale specificațiilor DNG până acum. Versiunea 1.0.0.0 a fost lansată în septembrie 2004 împreună cu lansarea „2.3” (ACR și DNG Converter). În februarie 2005 a fost publicată versiunea 1.1.0.0. În mai 2008 a fost lansată versiunea 1.2.0.0 și a fost folosită în „4.4”. Versiunea 1.3.0.0 a fost publicată în iunie 2009. Versiunea 1.4.0.0 a apărut în 2012.

## Format de fișier DNG

În timp ce fișierele raw ale camerei captează date neprocesate sau procesate slab direct de la senzor. Deoarece sunt similare cu negativele de film, formatele brute ale camerei sunt cunoscute și sub denumirea de „negative digitale”. Beneficiul formatelor brute este controlul artistic sporit pentru utilizatorul final. Utilizatorul poate ajusta diverse intervale de parametri în funcție de cerințe, cum ar fi balansul de alb, maparea tonurilor, reducerea zgomotului, clarificarea și așa mai departe. Pe de altă parte, fișierul raw al camerei trebuie procesat pentru orice utilizare prin orice software sau printr-un convertor.

Deoarece nu exista un format standard disponibil pentru fișierele raw ale camerei, a creat mai multe probleme pentru utilizatorul final. Aceste probleme au fost abordate de Adobe și au definit un format neproprietar pentru fișierele raw ale camerei. Formatul este cunoscut sub numele de Digital Negative sau DNG. DNG poate fi utilizat de o gamă largă de hardware și software pentru procesarea fișierelor brute. În plus, DNG poate fi folosit și ca format intermediar pentru stocarea imaginilor care au fost capturate inițial de camerele cu propriile lor formate brute.

### Specificații pentru formatul fișierului DNG

În această secțiune vom descrie formatul DNG ca o extensie a TIFF 6.0.

* **Extensii de fișiere**: DNG utilizează extensii „.DNG” sau „.TIF”.
* **Arborii SubIFD**: DNG nu acceptă lanțurile SubIFD, în schimb DNG recomandă utilizarea arborilor SubIFD așa cum este menționat în specificațiile TIFF-EP. Cea mai înaltă calitate și rezoluție pot folosi NewSubFileType de 0, în timp ce miniaturile de calitate redusă ar trebui să utilizeze NewSubFileType egal cu 1. De asemenea, este recomandat, dar nu este necesar, ca primul IFD să aibă o calitate scăzută sau o miniatură cu rezoluție scăzută.
* **Ordinea octetilor**: Ordinea octetilor trebuie să fie acceptată de cititoarele DNG, de asemenea, pentru fișierele de la un anumit model de cameră.
* **Pixeli mascați**: Majoritatea senzorilor camerei calculează pixeli complet mascați la marginea senzorului prin codificare neagră. Acești pixeli pot fi fie incluși, fie tăiați înainte ca imaginea să fie stocată în format DNG. Dacă pixelii mascați nu sunt tăiați, atunci aria acestor pixeli trebuie menționată în eticheta ActiveArea. Informațiile adunate de la acești pixeli despre nivelul de codare de negru ar trebui utilizate fie înainte ca datele brute să fie stocate, fie pot fi incluse în fișierul DNG care specifică nivelul de negru.
* **Pixeli defecte**: înainte de stocarea datelor brute ca DNG, pixelii defecte ar trebui excluși.
* **Metadate**: metadatele pot fi incluse în DNG în oricare dintre următoarele moduri:
** Prin utilizarea etichetelor de metadate TIFF-EP sau EXIF
** Prin eticheta de metadate IPTC (33723)
** Folosind eticheta de metadate XMP (700)
* **Date de proprietate**: în mod normal, vânzătorii includ date de proprietate în fișiere brute pentru a fi utilizate de propriile convertoare. DNG își stochează datele proprietare în etichete private, IFD-uri private și într-un MakerNote privat. Furnizorii trebuie să folosească etichetele DNGPrivateData și MakerNoteSafety pentru a se asigura că aplicațiile care editează fișiere DNG păstrează aceste date proprietare.

Următoarele sunt câteva restricții importante și extensii etichete TIFF.

**BitsPerSample**

Sunt acceptați 8 până la 32 de biți/eșantion. Trebuie să existe aceeași adâncime pentru fiecare probă atunci când SamplesPerPixel nu este egal cu 1. Dar dacă BitsPerSample nu este egal cu 8 sau 16 sau 32, atunci biții trebuie împachetați în octeți folosind TIFF implicit FillOrder de 1 (big-endian).

**Comprimare**

Sunt acceptate două valori de etichetă de compresie:

* Valoarea # 1: date necomprimate.
* Valoarea # 7: date comprimate JPEG, fie JPEG DCT de bază, fie compresie JPEG fără pierderi.

**Interpretare fotometrică**

Următoarele valori sunt acceptate numai pentru IFD-uri în miniatură și previzualizare:

* 1 = BlackIsZero. Se presupune că se află într-un spațiu de culoare gamma 2.2.
* 2 = RGB. Se presupune că se află în spațiul de culoare sRGB.
* 6 = YCbCr. Folosit pentru imaginile de previzualizare codificate JPEG.

Următoarele valori sunt acceptate pentru IFD brut și se presupune că sunt spațiul de culoare nativ al camerei:

* 32803 # CFA (Color Filter Array).
* 34892 # LinearRaw.

**Orientare**

Eticheta de orientare este utilizată pentru browserele de fișiere, astfel încât acestea să poată efectua rotația fără pierderi a fișierelor DNG. Cititoarele DNG trebuie să accepte toate orientările posibile, inclusiv orientările în oglindă.

## Caracteristici în cea mai recentă versiune a DNG

Versiunea DNG 1.4 octombrie 2012 are următoarele caracteristici avansate.

* Decupare implicită de utilizator
* Transparență
* virgulă flotantă (HDR)
* Compresie cu pierderi
* Proxy

## Referințe ##

* [Specificații DNG - de Adobe](https://web.archive.org/web/20170829200857/http://wwwimages.adobe.com/content/dam/Adobe/en/products/photoshop/pdfs/dng_spec_1.4.0.0.pdf)
* [Digital Negative - Wikipedia](https://en.wikipedia.org/wiki/Digital_Negative)
* [DNG - Formatul public de arhivă pentru datele brute ale camerei digitale](https://helpx.adobe.com/photoshop/digital-negative.html)

