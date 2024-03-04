{
  "date" : "2023-01-11",
  "keywords" : ["ac file", "what is an aci file", "file", "how to open ac file", "ac file extension","extension"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Sužinokite apie AC failo formatą ir API, kurios gali kurti ir atidaryti ACCDB failus.",
  "title" : "AC failo formatas – Autoconf scenarijaus failas",
  "linktitle" : "AC",
  "menu" : {
    "docs" : {
      "identifier":"executable-ac-lt",
      "parent" : "executable"
}
},
  "lastmod" : "2020-01-11"
}

## Kas yra AC failas?

AC failas yra Autoconf scenarijaus failas. **Autoconf** yra išplečiamas M4 makrokomandų paketas, sukuriantis apvalkalo scenarijus, skirtas automatiškai konfigūruoti programinės įrangos šaltinio kodo paketus. Šie scenarijai gali pritaikyti paketus daugeliui UNIX tipo sistemų be rankinio vartotojo įsikišimo. Autoconf sukuria paketo konfigūracijos scenarijų iš šablono failo, kuriame pateikiamos operacinės sistemos funkcijos, kurias paketas gali naudoti M4 makrokomandų iškvietimų forma.

Producing configuration scripts using Autoconf requires GNU M4. Prieš konfigūruodami Autoconf, turėtumėte įdiegti GNU M4 (bent jau 1.4.6 versiją, nors rekomenduojama 1.4.13 ar naujesnė versija), kad Autoconf konfigūravimo scenarijus galėtų jį rasti. Autoconf sukurti konfigūracijos scenarijai yra savarankiški, todėl jų vartotojams nereikia turėti Autoconf (arba GNU M4).

## Kaip atidaryti AC failą?

AC reiškia automatinę konfigūraciją. Tai GNU Autoconf sugeneruotas scenarijus, leidžiantis programinės įrangos šaltinio kodą pritaikyti įvairioms Posix tipo sistemoms, išbandant reikiamas paketo funkcijas. Scenarijus vadinamas AC failu.

## Pagrindiniai automatinių įrankių komponentai

An understanding of GNU autotools (`automake`, `autoconf` etc.) can be useful when working with ebuilds:

Autotools yra susijusių paketų rinkinys, kurį naudojant kartu pašalinama daug sunkumų, susijusių su nešiojamos programinės įrangos kūrimu. Šie įrankiai kartu su keliais gana paprastais įvesties failais, naudojami paketo kūrimo sistemai sukurti.

**Pagrindinė apžvalga, kaip pagrindiniai automatinių įrankių komponentai dera tarpusavyje.**

![A basic overview of how the main autotools components fit together](https://devmanual.gentoo.org/general-concepts/autotools/diagram.png "A basic overview of how the main autotools components fit together")

Paprasta sąranka:

- Programa autoconf sukuria konfigūravimo scenarijų iš configure.in arba configure.ac.
- Programa automake sukuria Makefile.in iš Makefile.am.
– Paleidžiamas scenarijus configure, kad iš Makefile.in failų būtų sukurtas vienas ar daugiau Makefile failų.
- Programa make programai kompiliuoti naudoja Makefile.

## Nuorodos
* [Autoconf Software](https://www.gnu.org/software/autoconf/)
* [Autotools pagrindai](https://devmanual.gentoo.org/general-concepts/autotools/index.html)



