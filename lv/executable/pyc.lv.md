{
  "date": "2022-05-09",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par PYC faila formātu un API, kas var izveidot un atvērt PYC failus.",
  "title": "PYC faila formāts - Python kompilētais fails",
  "linktitle": "PYC",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-py-lvc"
}
},
  "lastmod": "2022-05-09"
}

## Kas ir PYC fails?

PYC fails ir kompilēts izvades fails, kas ģenerēts no avota koda, kas rakstīts Python programmēšanas valodā. Kad PY fails tiek palaists, izmantojot Python tulku, izpildei tas tiek pārveidots par baitkodu. Tajā pašā laikā apkopotais baitkods tiek saglabāts arī kā .pyc fails, lai vēlāk, ja nepieciešams, to atkārtoti izmantotu no kešatmiņas.

## PYC faila formāta struktūra

PYC faili ir baitkodā, un to failu formātu specifikācijas nav pieejamas publiski. Tomēr dažu avotu veiktā izmeklēšana liecina, ka [structure of a PYC file](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html) sastāv no:

 * Četru baitu maģiskais skaitlis — vienkārši divi baiti, kas mainās ar katru šķirošanas koda maiņu, un pēc tam divi baiti 0d0a.
 * Četru baitu modifikācijas laikspiedols — Unix modifikācijas laikspiedols avota failam, kas ģenerēja .pyc, lai to varētu pārkompilēt, ja mainās avots.
 * Marshalled code object — koda objekta marshal.dump izvade, kas ir avota faila kompilēšanas rezultāts.

## FAQ

1. **Kā tiek ģenerēts PYC fails?** PYC fails tiek izveidots, kad Python avota kods tiek kompilēts, izmantojot Python tulku. Pēc tam apkopotais kods tiek saglabāts PYC failā.

1. **Vai PYC ir ātrāks par py?** PYC faili tiek saglabāti pēc Python pirmkoda kompilēšanas. Tā kā tie jau ir interpretēti, šie faili ir ātrāki nekā .py faili.

1. **Kāda ir atšķirība starp py un pyc failu?** PY failos ir programmas Python pirmkoda fails, savukārt .pyc failos ir interpretēts lietojumprogrammas baitkods.

1. **Vai PYC ir binārs fails?** Jā, PYC fails ir binārs fails, kas satur 4 baitu maģisko numuru, 4 baitu modifikācijas laikspiedolu un sakārtota koda objektu.

1. **Vai mēs varam pārvērst .pyc par .py?** Jā, ir iespējams konvertēt pyc failus uz py. Dekompilatorus, piemēram, Decompyle++, var izmantot, lai kompilēto Python baitu kodu pārvērstu atpakaļ derīgā un cilvēkam lasāmā Python avota kodā.

## Atsauces

* [.pyc failu struktūra](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html)


