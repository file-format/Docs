{
  "date" : "2023-01-11",
  "keywords" : ["ac file", "what is an aci file", "file", "how to open ac file", "ac file extension","extension"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Foghlaim faoi fhormáid comhaid AC agus APIanna ar féidir leo comhaid ACCDB a chruthú agus a oscailt.",
  "title" : "Formáid Comhad AC - Comhad Script Autoconf",
  "linktitle" : "AC",
  "menu" : {
    "docs" : {
      "identifier":"executable-ac-ga",
      "parent" : "executable"
}
},
  "lastmod" : "2020-01-11"
}

## Cad is comhad AC ann?

Is é comhad AC an comhad script Autoconf. Is pacáiste sínte macraí M4 é **Autoconf** a tháirgeann scripteanna sliogán chun pacáistí cód foinse bogearraí a chumrú go huathoibríoch. Is féidir leis na scripteanna seo na pacáistí a oiriúnú do go leor cineálacha córais atá cosúil le UNIX gan idirghabháil láimhe úsáideora. Cruthaíonn Autoconf script cumraíochta do phacáiste ó chomhad teimpléad a liostaíonn na gnéithe córas oibriúcháin is féidir leis an bpacáiste a úsáid, i bhfoirm glaonna macra M4.

Producing configuration scripts using Autoconf requires GNU M4. Ba cheart duit GNU M4 a shuiteáil (leagan 1.4.6 ar a laghad, cé go moltar 1.4.13 nó níos déanaí) sula ndéantar Autoconf a chumrú, ionas gur féidir le script cumraíochta Autoconf é a aimsiú. Tá na scripteanna cumraíochta a tháirgtear ag Autoconf féin-chuimsitheach, mar sin ní gá go mbeadh Autoconf (nó GNU M4) ag a n-úsáideoirí.

## Conas comhad AC a oscailt?

Seasann AC do Chumraíocht Uathoibríoch. Is script é a ghineann GNU Autoconf a chuireann ar chumas cód foinse bogearraí a oiriúnú do chórais éagsúla cosúil le Posix trí thástáil le haghaidh gnéithe riachtanacha sa phacáiste. Tugtar comhad AC ar an script.

## Comhpháirteanna móra Autotools

An understanding of GNU autotools (`automake`, `autoconf` etc.) can be useful when working with ebuilds:

Is bailiúchán de phacáistí gaolmhara é Autotools a bhaineann, nuair a úsáidtear iad le chéile, go leor den deacracht a bhaineann le bogearraí iniompartha a chruthú. Úsáidtear na huirlisí seo, mar aon le cúpla comhad ionchuir sách simplí a chuirtear ar fáil in aghaidh an tsrutha, chun an córas tógála do phacáiste a chruthú.

**Forbhreathnú bunúsach ar an gcaoi a n-oireann príomhchodanna na n-uathuirlisí le chéile.**

![A basic overview of how the main autotools components fit together](https://devmanual.gentoo.org/general-concepts/autotools/diagram.png "A basic overview of how the main autotools components fit together")

I socrú simplí:

- Táirgeann an clár `autoconf` script cumraíochta ó `configure.in` nó `configure.ac`.
- Táirgeann an clár `automake` Makefile.in ó Makefile.am.
- Reáchtáiltear an script `chumrú` chun comhad Makefile amháin nó níos mó a tháirgeadh ó chomhaid Makefile.in.
- Úsáideann an clár `make` an Makefile chun an clár a chur le chéile.

## Tagairtí
* [Autoconf Software](https://www.gnu.org/software/autoconf/)
* [Bunús an Autotools]( https://devmanual.gentoo.org/general-concepts/autotools/index.html)



