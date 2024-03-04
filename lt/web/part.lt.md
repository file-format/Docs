{
  "date": "2021-06-24",
  "keywords": [
"DALIS",
"dalinis",
"pratęsimas",
"failą",
"formatu",
"žiniatinklio",
"atsisiųstas"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "DALIS – iš dalies atsisiųstas failas",
  "description": "Sužinokite apie PART failo formatą ir API, kurios gali kurti ir atidaryti PART failus.",
  "linktitle": "PART",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-par-ltt"
}
},
  "lastmod": "2021-06-24"
}

## Kas yra PART failas? ##

Dalies failas arba .part plėtinys yra iš dalies atsisiųstas failas. Jis naudojamas, kai atsisiuntimai vyksta arba buvo nutraukti dėl bet kokios problemos, todėl atsisiuntimų tvarkyklei suteikiama galimybė atnaujinti atsisiuntimą, kai tik įmanoma.
Tai reiškia, kad naršyklė, pvz., Firefox, arba failų persiuntimo programos, pvz., eMule, eMule plus, FlashGet ir kt., išsaugo failo dalį, vadinamą Dalies failu, kol atsisiunčiama jūsų įrenginyje. Šis dalies failas parodys, ar atsisiuntimas vyksta, ar buvo nutrauktas nepasibaigus. Ne tik šis, bet ir PART failas saugo visus duomenis, kol atsisiuntimas bus baigtas, todėl kai kuriuos iš jų vėliau galima atnaujinti, jei norite vėl pradėti atsisiuntimą.

## DALIS failo formatas ##

There are few browsers that break large download files into smaller downloads and assign each portion a .part extension. These files can be seen in the “Download” folder. Once the download is finished, the browser will combine all the PART files to give a final downloaded file. For example, while downloading a file from Firefox, the download manager will store the data being downloaded in a PART file and replaces the name with certain characters, and add a .part extension at the end, such as **doodle.or** becomes **JKzMn.or.part**. After completion, Firefox will remove the .part extension and the file will be ready to launch.
