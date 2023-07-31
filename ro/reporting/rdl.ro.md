{
  "date" : "2021-03-01",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RDL - Fișierul limbajului de definire a raportului",
  "keywords" :[ "rdl", "limbaj de definire a raportului", "XmlTextWriter", "XSD", "element RDL"],
  "description":"Aflați despre formatul de fișier RDL, care este o reprezentare XML a unei definiții de raport SQL Server Reporting Services.",
  "linktitle" : "RDL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-01"
}

## Ce este un fișier RDL? ##

RDL (Report Definition Language) este un etalon stabilit de Microsoft pentru definirea rapoartelor. Un fișier RDL constă dintr-unul sau mai multe elemente RDL. În timp ce un element RDL constă în tipul de date și cardinalitatea acestuia. Un element poate fi simplu sau complex. Elementul simplu nu are niciun element sau atribute copil, în timp ce un element complex are copii și atribute opționale.

## Definiția schemei XML RDL
Un fișier XML Schema Definition (XSD) validează fișierul RDL. Schema definește regulile unde pot apărea elementele RDL într-un fișier .rdl. Un element RDL poate fi simplu sau complex. Un element simplu nu are elemente sau atribute copil, iar un element complex are copii și, opțional, atribute.

## Se creează RDL
Deoarece RDL este de natură deschisă și extensibilă, multe dintre aplicații și instrumente pot fi construite care generează fișiere RDL pe baza schemei sale XML. Una dintre cele mai simple moduri de a crea RDL dintr-o aplicație este să utilizați clasele Microsoft .NET Framework ale spațiului de nume **System.Xml** și spațiului de nume System.Linq. În special, clasa **XmlTextWriter** poate fi folosită pentru a scrie RDL. Puteți genera o definiție completă a raportului de la început până la sfârșit în orice aplicație .NET Framework folosind **XmlTextWriter**. Dezvoltatorii pot adăuga, de asemenea, elemente de raport personalizate cu proprietăți personalizate pentru a extinde RDL.

## Tipuri RDL
Următorul tabel listează tipurile și atributele utilizate în elementele RDL.

|Tip|Descriere|
---|---|
|Binar |O proprietate cu o valoare binară codificată în bază 64.|
|Boolean| O proprietate cu adevărat sau fals ca valoare a obiectului. Dacă nu se specifică altfel, valoarea unui obiect boolean opțional omis este False.|
|Dată |O proprietate cu o dată complet specificată sau o valoare datetime specificată în formatul de dată ISO8601: AAAA-LL-ZZ[THH:LL[:SS[.S]]].|
|Enum |O proprietate cu o valoare text șir care trebuie să fie una dintr-o listă de valori desemnate.|
|Float |O proprietate cu o valoare flotant. Un punct (.) este folosit ca separator zecimal opțional.|
|Întreg |O proprietate cu o valoare întreagă (int32).|
|Limba |O proprietate cu o valoare text care conține un cod de limbă și cultură, cum ar fi „en-us” pentru engleza SUA. Valoarea trebuie să fie fie o limbă specifică, fie o limbă neutră pentru care este definită o limbă implicită în Microsoft .NET Framework.|
|Nume |O proprietate cu o valoare text șir. Numele trebuie să fie unice în spațiul de nume al articolului. Dacă nu este specificat, spațiul de nume pentru un articol este cel mai interior obiect care conține un nume.|
|NormalizedString |O proprietate cu o valoare text șir care a fost normalizată.|
|Dimensiune |Un element de dimensiune trebuie să conţină un număr (cu un caracter punct folosit ca separator zecimal opţional). Numărul trebuie să fie urmat de un indicator pentru o unitate de lungime CSS, cum ar fi cm, mm, in, pt sau pc. Un spațiu între număr și indicator este opțional. Pentru mai multe informații despre indicatorii de dimensiune, consultați Referința pentru valori și unități CSS. În RDL, valoarea maximă pentru Dimensiune este de 160 inchi. Dimensiunea minimă este de 0 inchi.|
|Șir |O proprietate cu o valoare text șir.|
|UnsignedInt |O proprietate cu o valoare întreagă fără semn (uint32).|
|Varianta |O proprietate cu orice tip XML simplu.|

## Tipuri de date RDL
În RDL, DataType Enumeration definește tipul de date al unui atribut, expresie sau parametru. Următorul tabel arată cum tipurile de date CLR corespund tipurilor de date RDL.

|Tipul(e) CLR |Tipul de date corespunzător|
---|---|
|Boolean| Boolean|
|DateTime, DateTimeOffset |DateTime|
|Int16, Int32, UInt16, Byte, SByte |Integer|
|Single, dublu |Plutitor|
|Șir, Char, GUID, Timespan |Șir|


## Referințe ##

- [Limba definiției raportului (Wikipedia)](https://en.wikipedia.org/wiki/Limba_definiției_raportului)
- [Limbajul de definire a rapoartelor (SSRS)](https://learn.microsoft.com/en-us/sql/reporting-services/reports/report-definition-language-ssrs)

