{
  "date": "2021-04-22",
  "keywords": [
"msix failą",
"pratęsimas",
"formatu",
"Kaip atidaryti msix failą",
"msix failo formatas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MSIX – kas yra MSIX failas?",
  "description": "Sužinokite apie MSIX failą ir API, kurios gali kurti ir atidaryti MSIX failus.",
  "linktitle": "MSIX",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-msi-ltx"
}
},
  "lastmod": "2021-12-16"
}

## Kas yra MSIX failas?

An MSIX file is a Windows app packaging format that is used to create and distribute applications in Windows 10. Tai yra modernus paketo failo formatas, palyginti su [APPX](/programming/appx/) ir MSI, kuris pagaliau bus palaipsniui pašalintas į šį naują failo formatą. Jis gali būti naudojamas Win32, WPF ir Windows Forms programoms diegti. MSIX failai yra patikimi ir skirti tinklo ir vietos diske optimizavimui. Kūrėjai juos naudoja platindami programas galutiniams vartotojams per Microsoft Store (anksčiau vadintą Windows Store).

## MSIX failo formatas – daugiau informacijos

MSIX failai yra [ZIP](/compression/zip/) suglaudinti, o visi failai įtraukti į supakuotą failą. Be su programa susijusių failų, MSIX faile yra [.xml](/web/xml/) konfigūracijos failų, kuriuose yra informacijos, susijusios su programos diegimu.

## Kas yra MSIX paketo viduje?

MSIX paketą sudaro šie failai.

 * AppxBlockMap.xml – žinomas kaip paketo bloko žemėlapio failas, tai XML dokumentas, kuriame yra programos failų sąrašas su indeksais ir kriptografinėmis maišomis kiekvienam pakete saugomam duomenų blokui.
 * AppxManifest.xml – XML dokumentas, kuriame yra informacija, reikalinga MSIX programai diegti, rodyti ir atnaujinti. Ši informacija apima paketo tapatybę, paketo priklausomybes, reikalingas galimybes, vaizdinius elementus ir išplėtimo taškus.
 * AppxSignature.p7x – failas, sugeneruojamas pasirašius paketą. Visi MSIX paketai turi būti pasirašyti prieš įdiegiant. Su AppxBlockmap.xml platforma gali įdiegti paketą ir būti patvirtinta.

## Nuorodos

 * [MSIX apžvalga](https://learn.microsoft.com/en-us/windows/msix/overview)
 * [Sukurkite APPX failus naudodami Microsoft Visual Studio](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

