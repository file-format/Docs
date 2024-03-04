{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "TVS failo formatas – „Connection Manager“ paslaugos profilio failas",
  "description":"Sužinokite apie TVS failą ir API, kurios gali kurti ir atidaryti TVS failus.",
  "linktitle" : "CMS",
  "menu" : {
    "docs" : {
      "identifier": "misc-cms-lt",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Kas yra TVS failas?

TVS failas yra duomenų failas, kuriame yra Microsoft Windows Connection Manager naudojama profilio informacija. Tai leidžia nuotoliniams vartotojams prisijungti prie tinklo naudojant šią profilio informaciją. CMS faile saugoma informacija apima duomenis apie vartotojo operacinę sistemą ir leidimus, kurie naudojami ryšiui tarp nuotolinio vartotojo ir tinklo užmegzti. TVS administratoriai TVS failams generuoti naudoja Connection Manager Administrator Kit (CMAK).

## TVS failo formatas – daugiau informacijos

CMS failai vartotojų įrenginiuose paprastai nerandami. Kadangi jie naudojami specialiai leisti nuotoliniams vartotojams prisijungti prie tinklo, juos rasite kompiuteriuose, kurie naudojami prisijungti prie įmonės tinklo arba tam tikros paskirties biuro. Daugeliu atvejų jis naudojamas prisijungti prie organizacijos tinklo, pavyzdžiui, virtualaus privataus tinklo (VPN), kuris skirtas tik įmonei. Būdami tinklo administratoriumi, nustatysite prieigą prie tokio tinklo naudodami Ryšių tvarkyklę, kad jis galėtų pasiekti įmonės tinklą iš nuotolinės vietos.

### Kas yra vidinė TVS?

TVS profilio failas sukuriamas naudojant Connection Manager ir yra supakuotas su kitais konfigūracijos failais prieš pateikiant jį nuotoliniam vartotojui. Į šiuos papildomus failus gali būti įtrauktas CMP ir INF failas, kuris yra supakuotas kartu į [EXE](/executable/exe/) failą. Šis visas paketas pateikiamas nuotoliniam vartotojui prisijungti prie tinklo.

## Nuorodos

* [„Windows Connection Manager“ supratimas ir konfigūravimas](https://learn.microsoft.com/en-us/windows-hardware/drivers/mobilebroadband/understanding-and-configuring-windows-connection-manager)


