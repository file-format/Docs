{
  "date" : "2022-06-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru NPK",
  "description":"Další informace o formátu souborů NPK a rozhraních API, která mohou vytvářet a otevírat soubory NPK.",
  "linktitle" : "NPK",
  "menu" : {
    "docs" : {
      "identifier":"compression-npk",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-21"
}

## Co je soubor NPK?

Soubor NPK je soubor balíčku pro aktualizaci softwaru používaný routery **MikroTik** pro upgrade operačního systému routeru. Dodává se jako komprimovaný binární archiv, který se načte do routeru pro instalaci aktualizací softwaru. Informace obsažené v souborech NPK zahrnují síťové informace, jako je IP adresa a služba IP, informace o konektorech (ethernetová rozhraní a sériový port), nastavení e-mailu, konfigurace mostu a správa místních uživatelů.

## Formát souboru NPK

Soubory NPK jsou uloženy jako komprimovaný binární archiv. Jedná se o uzavřený formát souboru, který používá pouze samotný MikroTik. Není určeno k vytváření doplňků RouterOS prostřednictvím třetích stran. Soubory NPK jsou spravovány samotným MikroTikem a jeho upgradované verze si můžete stáhnout ze sekce stahování na webu [MikroTik](https://mikrotik.com/download).

Když je soubor NPK nahrán do routeru, operační systém routeru se neprojeví, dokud nebude restartován. Proto je pro upgrade OS routeru vyžadován restart.

## Reference

* [MikroTik – Upgrading OS Router OS](https://mikrotik.com/download)
* [Jak vytvořit soubory NPK](https://forum.mikrotik.com/viewtopic.php?t=87126)

