{
  "date" : "2019-10-11",
  "keywords" :[ "fișier rtf", "format fișier rtf", "ce este un fișier rtf", "fișier", "exemplu rtf", "extensie fișier rtf", "extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RTF – Format text îmbogățit",
  "description":"Aflați despre formatul de fișier RTF și despre API-urile care pot crea și deschide fișiere RTF.",
  "linktitle" : "RTF",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier RTF?

Introdus și documentat de Microsoft, formatul de text îmbogățit (**RTF**) reprezintă o metodă de codificare a textului formatat și a graficelor pentru utilizare în cadrul aplicațiilor. Formatul facilitează schimbul de documente pe mai multe platforme cu alte produse Microsoft, servind astfel scopului interoperabilității. Această capacitate îl face un standard de transfer de date între software-ul de procesare a textului și, prin urmare, conținutul poate fi transferat de la un sistem de operare la altul fără a pierde formatarea documentului. Specificațiile de format de fișier sunt disponibile de Microsoft pentru [descărcare] public (https://interoperability.blob.core.windows.net/files/Archive_References/%5bMSFT-RTF%5d.pdf) și pot fi consultate din perspectiva dezvoltatorului.

## Scurt istoric al formatului de fișier RTF ##

Formatul de fișier RTF a suferit mai multe revizuiri de la publicarea sa. Versiunea sa oficială pentru citire/scriere a fost publicată ca parte a Microsoft Word 3.0 pentru Macintosh cu specificațiile versiunii 1.0. Versiunea finală a specificațiilor, 1.9.1, a fost publicată de Microsoft în martie 2008. După aceasta, nu se mai fac îmbunătățiri ale specificațiilor. În prezent, aproape toate sistemele de operare au mai multe aplicații bogate în caracteristici care au minimizat/eradicat utilizarea formatului de fișier RTF.

## Specificații pentru formatul fișierului RTF ##

RTF servește ca standard de transfer de date între software-ul de procesare a textului și de transfer de conținut de la un sistem de operare la altul. Acest lucru se realizează folosind cuvinte de control care au fost introduse de Microsoft Office Word până în 2007. Un fișier RTF standard este format din ASCII pentru a reprezenta text îmbogățit și cu caractere non-ASCII care sunt convertite în valori de cod adecvate. Versiunile mai noi de Word pot citi fișiere RTF generate cu versiunile anterioare, în timp ce versiunile mai vechi ignoră cuvintele de control și grupurile pe care nu le înțeleg.

### Înțelegerea bazelor RTF ###

Fișierele RTF folosesc text simplu ASCII pe 7 biți, constând din:

* cuvinte de control
* simboluri de control, și
* grupuri.

Acestea acționează ca elemente de bază pentru reprezentarea datelor RTF ca text ușor de înțeles și codificare de caractere.

#### Cuvânt de control ####

Acestea reprezintă comenzi formatate special folosite pentru a marca caractere pentru afișare și nu pot fi mai lungi de 32 de litere. Un cuvânt de control este definit prin:

\<ASCII Letter Sequence> //<//Delimiter//> //

Fiecare cuvânt de control este sensibil la majuscule și începe cu o bară oblică inversă. Secvența de litere ASCII poate conține alfabete ASCII (de la a la z și de la A la Z). The<Delimite> marchează sfârșitul numelui cuvântului de control și poate fi unul dintre următoarele:

* Un spațiu. Acesta servește doar la delimitarea unui cuvânt de control și este ignorat în procesarea ulterioară.
* O cifră numerică sau un semn ASCII minus, care indică faptul că un parametru numeric este asociat cu cuvântul de control. Secvența digitală ulterioară este apoi delimitată de orice caracter, altul decât o cifră ASCII (de obicei, un alt cuvânt de control care începe cu o bară oblică inversă). Parametrul poate fi un număr zecimal pozitiv sau negativ. Intervalul valorilor pentru număr este nominal de la –32768 la 32767, adică un număr întreg cu semn de 16 biți. Un număr mic de cuvinte de control iau valori în intervalul‌ −2.147.483.648 până la 2.147.483.647 (întreg cu semn pe 32 de biți). Aceste cuvinte de control includ **\binN**, **\revdttmN//**, **\rsidN** cuvinte de control asociate și unele proprietăți ale imaginii, cum ar fi **\bliptagN**. Aici **N** reprezintă parametrul numeric. Un parser RTF trebuie să permită până la 10 cifre precedate opțional de un semn minus. Dacă delimitatorul este un spațiu, acesta este aruncat, adică nu este inclus în procesarea ulterioară.
* Orice caracter, altul decât o literă sau o cifră. În acest caz, caracterul de delimitare termină cuvântul de control și nu face parte din cuvântul de control. Cum ar fi o bară oblică inversă „\”, care înseamnă că urmează un nou cuvânt de control sau un simbol de control.

#### Simbol de control ####

Un simbol de control reprezintă o apariție specială care are o semnificație specifică în funcție de conținutul său. Constă dintr-o bară oblică inversă urmată de un caracter special (caracter nealfabetic) și nu are delimitatori.

#### Grup ####

Un grup poate consta din text, cuvinte de control sau simboluri de control cuprinse între acolade (**{ }**). Acolada de deschidere (**{** ) indică începutul grupului, iar acolada de închidere ( **}**) indică sfârșitul grupului. Fiecare grup specifică textul afectat de grup și diferitele atribute ale textului respectiv.

### Structura fișierului RTF ###

Un fișier RTF are următoarea sintaxă standard:

Introdus și documentat de Microsoft, formatul de text îmbogățit (**RTF**) reprezintă o metodă de codificare a textului formatat și a graficelor pentru utilizare în cadrul aplicațiilor. Formatul facilitează schimbul de documente pe mai multe platforme cu alte produse Microsoft, servind astfel scopului interoperabilității. Această capacitate îl face un standard de transfer de date între software-ul de procesare a textului și, prin urmare, conținutul poate fi transferat de la un sistem de operare la altul fără a pierde formatarea documentului. Specificațiile de format de fișier sunt disponibile de Microsoft pentru [descărcare] public (https://interoperability.blob.core.windows.net/files/Archive_References/%5bMSFT-RTF%5d.pdf) și pot fi consultate din perspectiva dezvoltatorului.

#### Antet RTF ####

Un antet RTF are următoarea reprezentare.

|Câmp|Descriere
---|---|
|\<header> |**\rtf1\fbidis**? \<character set> \<from> ? \<deffont> \<deflang> \<fonttbl> ? \<filetbl> ? \<colortbl> ? \<stylesheet> ? \<stylerestrictions> ? \<listtables> ? \<revtbl> ? \<rsidtable> ? \<mathprops> ? \<generator> ?

Tabelele de antet trebuie să apară în această ordine dacă există. Fișierul RTF poate include grupuri pentru fonturi, stiluri, culoarea ecranului, imagini, note de subsol, comentarii (adnotări), anteturi și subsoluri, informații rezumate, câmpuri, marcaje, proprietăți de formatare a documentelor, secțiunilor, paragrafelor și caracterelor, matematică, imagini și obiecte. Dacă fontul, fișierul, stilul, culoarea, marca de revizuire și grupurile de informații rezumate și proprietățile de formatare a documentului sunt incluse în fișier, acestea trebuie să apară în antetul RTF, care precede corpul RTF. Dacă nu este utilizat conținutul niciunui grup, grupul poate fi omis. Orice grup care utilizează proprietățile definite într-un alt grup trebuie să apară după grupul care definește acele proprietăți. De exemplu, proprietățile de culoare și font trebuie să precedă grupul de stil.

#### Versiune RTF ####

Un document RTF trebuie să înceapă cu aceste șase caractere:

```
{\rtf1
```
unde 1 arată numărul versiunii RTF.

#### Set de caractere ####

După {\rtf1, documentul ar trebui să declare ce set de caractere folosește. Modul de declarare a unui set de caractere este cu una dintre aceste comenzi:

`\ansi` - Documentul se află în setul de caractere ANSI, cunoscut și sub numele de Pagina de cod 1252, setul obișnuit de caractere MSWindows.

`\mac` - Documentul se află în setul de caractere MacAscii, setul de caractere obișnuit din versiunile vechi (înainte de 10) de Mac OS.

`\pc` - Documentul se află în pagina de cod DOS 437, setul de caractere implicit pentru MS-DOS. Dactilografele cu memorie musculară bună vor observa că acesta este setul de caractere care este încă folosit pentru interpretarea codurilor „Alt numerice” – adică, când țineți apăsat Alt și tastați „130” pe tastatura numerică, se produce un é, deoarece caracterul 130 în CP437 este un é. Aceasta este singura utilizare pe care o vede CP437 în aceste zile.

`\pca` - Documentul se află în pagina de coduri DOS 850, cunoscută și sub numele de pagina de coduri multilingve MS-DOS.

#### Comandă font ####

Definiția setului de caractere este urmată de comanda `\deffN`. Aceasta definește faptul că numărul de font N este fontul implicit pentru acest document. Numărul fontului N este referit din tabelul de fonturi. Comanda `\deffN` este opțională din punct de vedere tehnic, dar ar trebui să fie acolo pentru a fi în siguranță ca un prolog comun, cum ar fi următoarele alegeți fontul 0 ca font implicit.

`{\rtf1\ansi\deff0`

#### Tabel cu fonturi ####

Toate fonturile care pot fi utilizate într-un document sunt listate într-un tabel de fonturi în care fiecare font este reprezentat de un număr de font. Documentul trebuie să aibă un tabel cu fonturi, deși unele programe vor funcționa și fără asta.

Sintaxa pentru un tabel de fonturi este {\fonttbl //...declarations//...}, în care fiecare declarație are această sintaxă de bază:

`{\fnumber\familycommand Fontname;}`

Un tabel de fonturi cu patru declarații este următorul:

```
{\fonttbl
{\f0\froman Times;}
{\f1\fswiss Arial;}
{\f2\fmodern Courier New;}
}
```

Într-un document cu acel tabel de fonturi, `{\f2 stuff}` ar tipări „lucruri” în Courier New. Un font nu poate fi folosit într-un document până când nu este listat în tabelul cu fonturi.

### Sfârșitul documentului ###

Fiecare document RTF trebuie să se încheie cu un }, pentru a închide grupul deschis de { care este primul caracter din document. Nimic nu poate urma finalul }, cu excepția posibilului o nouă linie.

## Referințe ##

* [Specificații RTF 1.9.1](https://interoperability.blob.core.windows.net/files/Archive_References/%5bMSFT-RTF%5d.pdf)
* [Rich Text Format](https://en.wikipedia.org/wiki/Rich_Text_Format)

