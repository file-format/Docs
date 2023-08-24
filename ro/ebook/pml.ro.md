{
  "date" : "2021-03-08",
  "keywords" :[ "PML", "eReader", "extensie", "format", "eBook", "Palm Markup Language"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul fișierului PML, limbajul Palm Markup și API-urile care pot crea și deschide fișiere PML.",
  "title" :"PML - Fișier limbajul de marcare Palm",
  "linktitle" : "PML",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-08"
}

## Ce este un fișier PML?

Palm Inc a introdus formatul de fișier PML, care înseamnă Palm Markup Language File. Scopul său este de a crea documente pentru eReader, care este un dispozitiv de citire a cărților electronice similar cu tableta. Fișierul PML oferă aspectul unui fișier [PDB](/ro/programming/pdb/) (conținând diferite fișiere de date) pentru a fi afișat pe un dispozitiv Palm.

## Detalii tehnice ale fișierelor PML

Structura fișierelor PML constă din etichete pentru crearea unei configurații de carte electronică, inclusiv paragrafe, titluri, indentări și referințe. De asemenea, permite formatarea etichetelor precum Bold, Small Caps și Superscript. Dezvoltatorii pot adăuga, de asemenea, imagini la cărți electronice.

### Palm Markup Language
Următorul tabel specifică comenzile PML:

|Comandă|Descriere|
---|---|
| \p | Pagina nouă |
| \x | Capitol nou; provoacă, de asemenea, o nouă întrerupere de pagină. Anexați titlul capitolului (și orice coduri de stil) cu \x și \x |
| \Xn | Capitol nou, n niveluri indentate (n între 0 și 4 inclusiv) în dialogul Capitol; nu provoacă o întrerupere de pagină. Anexați titlul capitolului (și orice coduri de stil) cu \Xn și \Xn |
| \Cn="Titlul capitolului" | Inserați „Titlul capitolului” în lista de capitole, cu nivelul n (cum ar fi \Xn). Textul nu este afișat pe pagină și nu forțează o întrerupere de pagină. Acest lucru poate fi uneori util pentru a introduce un semn de capitol la începutul unei introduceri la capitol, de exemplu. |
| \c | Centrați acest bloc de text; închideți cu \c la începutul liniei |
| \r | Bloc de text justificare dreapta; închideți cu \r la începutul liniei |
| \i | Blocare cu caractere italice; inchide cu \i |
| \u | Bloc de subliniere; aproape cu \u |
| \o | Bloc de depășire; închide cu \o |
| \v | Text invizibil; închideți cu \v (poate fi folosit pentru comentarii) |
| \t | Bloc de indentare. Începeți la începutul unei linii, închideți cu \t la sfârșitul unei linii |
| \T="50%" | Indentează procentul specificat din lățimea ecranului, 50% în acest caz. Dacă poziția curentă a desenului depășește deja locația specificată a ecranului, această etichetă este ignorată. |
| \w="50%" | Încorporați o regulă orizontală a unui procent dat de lățime a ecranului, în acest caz 50%. Această etichetă provoacă o întrerupere de linie înainte și după ea. Regula este centrată. Semnul procentual este obligatoriu. |
| \n | Comutați la fontul „normal”, care este specificat de utilizator |
| \s | Comutați la stdFont; închideți cu \s pentru a reveni la fontul normal |
| \b | Comutați la boldFont; închideți cu \b pentru a reveni la fontul normal (învechit; folosiți \B în schimb) |
| \l | Comutați la largeFont; închideți cu \l pentru a reveni la fontul normal |
| \B | Marcați textul ca aldine. Spre deosebire de eticheta \b, \B nu schimbă fontul, așa că puteți avea un text aldine mare. Nu puteți amesteca \b și \B în același fișier PML. |
| \Sp | Marcați textul ca superscript. Nu ar trebui să fie amestecat cu alte stiluri, cum ar fi aldine, cursive etc. Închideți textul suprascript cu \Sp. |
| \Sb | Marcați textul ca indice. Nu ar trebui să fie amestecat cu alte stiluri, cum ar fi aldine, cursive etc. Închideți textul în indice cu \Sb. |
| \k | Faceți textul inclus în majuscule mici; închide cu \k. Orice caractere incluse în etichetele \k (inclusiv cele cu accente) sunt făcute cu majuscule și sunt redate la o dimensiune mai mică decât un caracter majuscule obișnuit. |
| \\ | Reprezintă o singură bară oblică inversă |
| \aXXX | Introduceți un caracter non-ASCII al cărui cod Windows-1252 este zecimal XXX. Consultați tabelul de caractere PML pentru detalii. |
| \UXXXX | Introduceți un caracter non-ASCII al cărui cod Unicode este XXXX hexazecimal. Consultați tabelul de caractere PML extins pentru detalii. |
| \m="nume imagine.png" | Introduceți imaginea numită. Consultați secțiunea Imagini de mai jos. |
| \q="#linkanchor"Un text\q | Faceți referire la o ancoră de link care se află într-un alt punct din document. Șirul de după specificația ancorei și înainte de următorul \q este subliniat sau altfel arătat a fi un link atunci când vizualizați documentul. |
| \Q="linkanchor" | Specificați o ancoră de legătură în document. |
| \- | Introduceți o cratimă moale. O cratima moale apare numai dacă este necesar să despărțiți un cuvânt peste o linie. |
| \Fn="footnote1"1\Fn | Conectați „1” la o notă de subsol al cărei nume este nota de subsol1, etichetată la sfârșitul documentului PML. Consultați secțiunea despre Note de subsol și bare laterale de mai jos. |
| \Sd="sidebar1"Sidebar\Sd | Conectați textul „Bară laterală” la o bară laterală al cărei nume este bara laterală1, etichetată la sfârșitul documentului PML. Consultați secțiunea despre Note de subsol și bare laterale de mai jos. |
| \I | Marcați ca element de index de referință. Închideți elementul index (și orice coduri de stil) cu \I și \I.|
 


## Referințe

* [Palm Markup Language - Prin MobileRead](https://wiki.mobileread.com/wiki/EReader)
* [E-Reader - de MobileRead](https://en.wikipedia.org/wiki/E-reader)

