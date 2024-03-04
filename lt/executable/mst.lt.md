{
  "date": "2021-06-30",
  "keywords": [
"mst failą",
"mst failo formatas",
"kas yra mst failas",
"failą",
"mst pavyzdys",
"mst failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie MST failo formatą ir API, kurios gali kurti ir atidaryti MST failus.",
  "title": "MST – „Windows Installer“ paketo failas",
  "linktitle": "MST",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ms-ltt"
}
},
  "lastmod": "2021-06-30"
}

## Kas yra MST failas?
Failai su plėtiniu .mst naudojami MSI paketo turiniui transformuoti. Paprastai juos naudoja sistemos administratoriai, norėdami pritaikyti pasirinktinius parametrus esamam MSI failui. MST failai naudojami kartu su originaliu MSI paketu jų programinės įrangos platinimo sistemose, pvz., grupės strategijose. MST failai paprastai naudojami kuriant programinę įrangą ir testuojant jų kuriamas programinės įrangos versijas.

## MST failo formatas
MST arba Transform failas naudojamas programų, kurios faile naudoja Microsoft Windows Installer, diegimo parinktis rinkti. Šie failai dažniausiai naudojami diegimo programos (MSIEXEC.EXE) komandų eilutėje arba programinės įrangos diegimo grupės politikoje; Microsoft Active Directory domene. MST failus taip pat galima naudoti su įvyniotomis vykdomosiomis diegimo programomis. Bendras atvejis yra tai, kad kažkas nori perduoti komandinės eilutės parametrus įpakuotai diegimo programai. Kad tai padarytumėte, jums reikia MST failo, kuris prideda ypatybę WRAPPED_ARGUMENTS į ypatybių lentelę. Šių failų negalima kurti ar redaguoti naudojant bendruosius redaktorius. Tam yra specialių įrankių.

### Kaip naudoti MST failus?
MST failus galima generuoti naudojant įvairius įrankius, o Ocra paprastai naudojama MST failams generuoti. Tada nustatymus galima pritaikyti pagal poreikį ir išsaugoti konkrečioje vietoje. Po to MST failus galima naudoti kartu su MSI failais. Jei norite išbandyti šiuos failus; komandinėje eilutėje naudokite šią sintaksę

```
msiexec /i setup_1.0.msi TRANSFORMS=mylog.mst
```
### TRANSFORMUOJA nuosavybę

Taip pat galite naudoti Windows diegimo programos ypatybę **TRANSFORMS**, kuri iš tikrųjų yra transformacijų, kurias diegimo programa taiko diegdama paketą, sąrašas. Diegimo programa vykdo transformacijas ta pačia tvarka, kokia jos nurodytos ypatybėje TRANSFORM. Transformacijas galima nurodyti pagal failo pavadinimą su .mst plėtiniu arba visu keliu. Norėdami nurodyti daugiau nei vieną transformaciją, atskirkite kiekvieną failo pavadinimą arba kabliataškį, kaip nurodyta toliau pateiktame pavyzdyje.

```
TRANSFORMS=transform1.mst;transform2.mst;transform3.mst
```

## Nuorodos 

* [MST transformacijos failai](https://www.exemsi.com/documentation/mst-transformation-files/)

* [TRANSFORMS nuosavybė](https://learn.microsoft.com/en-us/windows/win32/msi/transforms)



