{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru CMS - soubor profilu služby Správce připojení",
  "description":"Další informace o souboru CMS a rozhraních API, která mohou vytvářet a otevírat soubory CMS.",
  "linktitle" : "CMS",
  "menu" : {
    "docs" : {
      "identifier": "misc-cms",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Co je soubor CMS?

Soubor CMS je datový soubor, který obsahuje informace o profilu používané Správcem připojení systému Microsoft Windows. Umožňuje vzdáleným uživatelům připojit se k síti pomocí těchto informací o profilu. Informace uložené v souboru CMS zahrnují data o operačním systému uživatele a oprávněních, která se používají k navázání spojení mezi vzdáleným uživatelem a sítí. Správci CMS používají ke generování souborů CMS sadu Connection Manager Administrator Kit (CMAK).

## Formát souboru CMS – Další informace

Soubory CMS se na uživatelských počítačích běžně nenacházejí. Vzhledem k tomu, že se používají speciálně k tomu, aby umožnili vzdáleným uživatelům přístup k síti, najdete je na počítačích, které se používají k připojení k firemní síti nebo nějaké specifické kanceláři. Ve většině případů se používá k připojení k organizační síti, jako je virtuální privátní síť (VPN), která je vyhrazena pouze pro společnost. Jako správce sítě nastavíte přístup k takové síti pomocí Správce připojení, abyste mu umožnili přistupovat k firemní síti ze vzdáleného místa.

### Co je insdie CMS?

Soubor profilu CMS je vytvořen pomocí Connection Manager a je zabalen s dalšími konfiguračními soubory, než je poskytnut vzdálenému uživateli. Tyto další soubory mohou zahrnovat CMP a soubor INF, které jsou zabaleny společně do souboru [EXE](/cs/executable/exe/). Tento kompletní balíček je poskytován vzdálenému uživateli pro připojení k síti.

## Reference

* [Pochopení a konfigurace Správce připojení systému Windows](https://learn.microsoft.com/en-us/windows-hardware/drivers/mobilebroadband/understanding-and-configuring-windows-connection-manager)

