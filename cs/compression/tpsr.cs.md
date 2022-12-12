{
  "date" : "2022-06-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru TPSR - soubor zprávy TeamViewer Pilot Session",
  "description":"Další informace o formátu souboru TPSR a rozhraních API, která mohou vytvářet a otevírat soubory TPSR.",
  "linktitle" : "TPSR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-06"
}

## Co je soubor TPSR?

TPSR je soubor protokolu připojení používaný aplikací TeamViewer Assist AR (dříve známý jako TeamViewer Pilot). Informace uložené v souboru TPSR jsou uloženy v komprimovaném formátu souboru [ZIP](/cs/compression/zip/). TPSR obsahuje podrobnou historii spojení TeamViewer mezi odborníkem a technikem pro vyřešení problému a účely revize. Informace obsažené v souboru TPSR zahrnují typ zařízení, název, Assist AR ID, Expert ID, datum a čas a trvání připojení. Tato data jsou uložena v souboru [JSON](/cs/web/json/) uvnitř komprimovaného archivu TPSR.

## Formát souboru TPSR

Soubor TPSR je uložen na disk ve formátu archivu ZIP, kde je obsah uložen v souboru JSON. Generuje se automaticky po dokončení připojení Assist AR za předpokladu, že je v TeamViewer povolena možnost hlášení připojení.

TeamViewer Assist AR umožňuje odborníkům připojit se k technikům a získat LIVE přenos vzdáleného konce prostřednictvím mobilní kamery. Mohou pomoci technikům vyřešit problém po telefonu.

## Otevřete soubory TPSR

Soubory TPSR můžete otevřít pomocí desktopové verze softwaru TeamViewer. Pokud je na vašem počítači nainstalován, dvojitým kliknutím na soubor TPSR jej otevřete v softwaru TeamViewer. Soubory TPSR lze také exportovat do souborů [PDF](/cs/pdf/) nebo je lze vytisknout a získat tak vytištěnou kopii souboru protokolu.

## Reference ##

* [TPSR](https://community.teamviewer.com/English/kb/articles/46456-using-teamviewer-assist-ar)

