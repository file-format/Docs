{
  "date" : "2022-06-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "NPK filformat",
  "description":"Lær om NPK-filformat og API'er, der kan oprette og åbne NPK-filer.",
  "linktitle" : "NPK",
  "menu" : {
    "docs" : {
      "identifier":"compression-npk-da",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-21"
}

## Hvad er en NPK fil?

En NPK-fil er en softwareopgraderingspakkefil, der bruges af **MikroTik**-routere til opgradering af routerens operativsystem. Det kommer som et komprimeret binært arkiv, der indlæses i routeren til installation af softwareopdateringer. Oplysninger indeholdt i en NPK-filer omfatter netværksoplysninger såsom IP-adresse og IP-tjeneste, forbindelsesoplysninger (ethernet-grænseflader og seriel port), e-mail-opsætning, brokonfiguration og lokal brugeradministration.

## NPK filformat

NPK-filer gemmes som komprimeret binært arkiv. Det er et lukket filformat, der kun bruges af MikroTik selv. Det er ikke beregnet til at oprette RouterOS-tilføjelser via tredjeparter. NPK-filer vedligeholdes af MikroTik selv, og opgraderede versioner af samme kan downloades fra downloadsektionerne på [MikroTik](https://mikrotik.com/download)-webstedet.

Når en NPK-fil uploades til en router, træder routerens OS ikke i kraft, medmindre det genstartes. Derfor kræves en genstart, for at routerens OS kan opgraderes.

## Referencer

* [MikroTik - Opgradering af router OS](https://mikrotik.com/download)

* [Sådan opretter du NPK-filer](https://forum.mikrotik.com/viewtopic.php?t=87126)


