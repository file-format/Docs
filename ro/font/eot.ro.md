{
  "date" : "2020-08-20",
  "keywords" :[ "fișier eot", "format fișier eot", "ce este un fișier eot", "fișier", "exemplu eot", "extensie fișier eot", "extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EOT - Format de fișier cu font TrueType",
  "description":"Aflați despre formatul fișierului EOT și despre API-uri pentru a crea și deschide fișiere EOT.",
  "linktitle" : "EOT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## Ce este un fișier EOT?

Un fișier cu extensia .eot este un font OpenType care este încorporat într-un document. Acestea sunt utilizate mai ales în fișiere web, cum ar fi o pagină Web. A fost creat de Microsoft și este acceptat de produsele Microsoft, inclusiv fișierul de prezentare PowerPoint [.pps](/ro/presentation/pps). Fișierul nu este de uz principal și este un fel de document care însoțește documentul principal sau pagina web. Similar cu fonturile OTF, EOT acceptă atât contururile Postscript, cât și TrueType pentru glife. Fișierele EOT sunt mai mici ca dimensiune, deoarece sunt comprimate folosind compresia LZ. EOT folosește un instrument Microsoft pentru a crea un font din fonturile TTF/OTF existente.

## Scurt istoric

Fontul EOT a fost trimis la W3C în 2007 ca parte a CSS3, dar din cauza cerințelor sale de a fi instalat permanent pe sistemul de la distanță a devenit motivul respingerii acestuia. A fost retrimis în martie 2008, dar W3C a ales în cele din urmă [Web Font Format](/ro/font/woff/) (WOFF), care a fost standardizat atunci.

## Format de fișier EOT

Detaliile formatului fișierului EOT pot fi găsite pe [pagina de trimitere W3](https://www.w3.org/Submission/EOT/#FileFormat) și elaborează structura utilizată de acest format de font. EOT constă dintr-o singură structură EMBEDDEDFONT care oferă suficiente informații de bază despre numele fontului și caracterele acceptate. Împachetarea acestor informații permite agenților de utilizator să evite despachetarea, decomprimarea sau instalarea fontului dacă acesta este deja prezent pe mașină.

### EMBEDDEDFONT Structura
Structura EMBEDDEDFONT a suferit trei revizuiri, cu adăugarea de date suplimentare la sfârșitul structurii cu fiecare revizuire. Ultima revizuire a structurii EMBEDDEDFONT este prezentată mai jos.

|Tip de date|Nume intrare|Descriere|
---|---|---|
|unsigned long|EOTSize|Lungimea totală a structurii în octeți (inclusiv datele șirurilor și fonturilor)|
|unsigned long|FontDataSize|Lungimea fontului OpenType (FontData) în octeți|
|unsigned long|Versiune|Numărul versiunii acestui format - 0x00020002|
|nesemnat lung|Steaguri|Steagme de procesare|
|byte[10]|FontPANOSE|Valoarea PANOSE pentru acest font - Consultați https://learn.microsoft.com/en-us/typography/opentype/spec/os2#pan|
|byte|Charset|În Windows, acesta este derivat din TEXTMETRIC.tmCharSet. Această valoare specifică setul de caractere al fontului. DEFAULT_CHARSET (0x01) indică nicio preferință. - Consultați https://learn.microsoft.com/en-us/windows/win32/api/wingdi/ns-wingdi-textmetrica|
|byte|Italic|Dacă bitul pentru ITALIC este setat în OS/2.fsSelection, valoarea va fi 0x01 - Vezi https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fss|
|unsigned long|Greutate|Valoarea greutății pentru acest font - Consultați https://learn.microsoft.com/en-us/typography/opentype/spec/os2#wtc|
|unsigned short|fsType|Type flags care oferă informații despre permisiunile de încorporare - Consultați https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fst|
|scurt nesemnat|MagicNumber|Număr magic pentru fișierul EOT - 0x504C. Folosit pentru a verifica dacă datele sunt deteriorate.|
|unsigned long|UnicodeRange1|os/2.UnicodeRange1 (biți 0-31) - Vezi https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange2|os/2.UnicodeRange2 (biții 32-63) - A se vedea https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange3|os/2.UnicodeRange3 (biți 64-95) - A se vedea https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange4|os/2.UnicodeRange4 (biții 96-127) - A se vedea https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|CodePageRange1|CodePageRange1 (biți 0-31) - Consultați https://learn.microsoft.com/en-us/typography/opentype/spec/os2#cpr|
|unsigned long|CodePageRange2|CodePageRange2 (biții 32-63) - Consultați https://learn.microsoft.com/en-us/typography/opentype/spec/os2#cpr|
|unsigned long|CheckSumAdjustment|head.CheckSumAdjustment - Consultați https://learn.microsoft.com/en-us/typography/opentype/spec/head|
|unsigned long|Reserved1|Rezervat - trebuie să fie 0|
|unsigned long|Reserved2|Rezervat - trebuie să fie 0|
|unsigned long|Reserved3|Rezervat - trebuie să fie 0|
|unsigned long|Reserved4|Rezervat - trebuie să fie 0|
|unsigned short|Padding1|Padding pentru a menține alinierea lungă. Valoarea de completare trebuie să fie întotdeauna setată la 0x0000.|
|unsigned short|FamilyNameSize|Numărul de octeți utilizați de matricea FamilyName|
|byte|FamilyName[FamilyNameSize]|Matrice de caractere UTF-16 cu lungimea de octeți FamilyNameSize. Acesta este șirul familiei de fonturi în limba engleză găsit în tabelul de nume al fontului (ID nume = 1) - Consultați https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding2|Valoarea padding trebuie să fie întotdeauna setată la 0x0000.|
|unsigned short|StyleNameSize|Numărul de octeți utilizați de StyleName|
|byte|StyleName[StyleNameSize]|Matrice de caractere UTF-16 cu lungimea de octeți StyleNameSize. Acesta este șirul subfamiliei de fonturi în limba engleză găsit în tabelul de nume al fontului (ID nume = 2) - Consultați https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding3|Valoarea padding trebuie să fie întotdeauna setată la 0x0000.|
|unsigned short|VersionNameSize|Numărul de octeți utilizați de VersionName|
|bytes|VersionName[VersionNameSize]|Matrice de caractere UTF-16 cu lungimea octeților VersionNameSize. Acesta este șirul versiunii în limba engleză găsit în tabelul de nume al fontului (nume ID = 5) - Consultați https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding4|Valoarea padding trebuie să fie întotdeauna setată la 0x0000.|
|unsigned short|FullNameSize|Numărul de octeți utilizați de FullName|
|byte|FullName[FullNameSize]|Matrice de caractere UTF-16 cu lungimea octeților FullNameSize. Acesta este șirul de nume complet în limba engleză găsit în tabelul de nume al fontului (ID nume = 4) - Consultați https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding5|Valoarea padding trebuie să fie întotdeauna setată la 0x0000.|
|unsigned short|RootStringSize|Numărul de octeți utilizați de matricea RootString|
|byte|RootString[RootStringSize]|Matrice de caractere UTF-16 cu lungimea de octeți RootStringSize.|
|unsigned long|RootStringCheckSum|Valoare RootString CheckSum. Vezi mai jos algoritmul pentru procesarea RootStringChecksum.|
|unsigned long|EUDCCodePage|Valoarea paginii de cod este necesară pentru suportul fonturilor EUDC.|
|unsigned short|Padding6|Valoarea padding trebuie să fie întotdeauna setată la 0x0000.|
|unsigned short|SignatureSize|Numărul de octeți utilizați de matricea Signature. Rezervat în prezent și ar trebui să fie setat la 0x0000.|
|byte|Semnătură[SignatureSize]|Rezervat în prezent. Dacă SignatureSize este 0x0000, nu există lungime pentru această matrice.|
|unsigned long|EUDCFlags|Semnale de procesare pentru fontul EUDC. Valorile tipice pot fi TTEMBED_XORENCRYPTDATA și TTEMBED_TTCOMPRESSED.|
|unsigned long|EUDCFontSize|Numărul de octeți utilizați de matricea Signature.|
|byte|EUDCFontData[EUDCFontSize]|Numărul de octeți utilizați pentru datele fontului EUDC. Dacă EUDCFontSize este 0x00000000, nu există lungime pentru această matrice.|
|byte|FontData[FontDataSize]|Datele fontului pentru acest fișier EOT. Datele pot fi comprimate sau criptate XOR, după cum este indicat de steagurile de procesare.|

## Referințe

* [Format fișier EOT](https://www.w3.org/Submission/EOT/)
* [Embedded OpenType](https://en.wikipedia.org/wiki/Embedded_OpenType)
* [Încorporarea fontului](https://en.wikipedia.org/wiki/Font_embedding)

