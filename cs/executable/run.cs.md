{
  "date" : "2023-01-31",
  "keywords" :["spustit soubor", "co je soubor běhu", "soubor", "jak otevřít soubor běhu", "spustit příponu souboru","přípona"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souboru RUN a rozhraních API, která mohou vytvářet a otevírat soubory RUN.",
  "title" :"RUN File Format - Linux Executable File",
  "linktitle" : "RUN",
  "menu" : {
    "docs" : {
      "identifier":"executable-run",
      "parent" : "executable"
}
},
  "lastmod" : "2023-01-31"
}

## Co je soubor RUN?

Formát souboru .run se běžně používá pro distribuci instalačních programů softwaru nebo aplikací v prostředí Linuxu. Chcete-li nainstalovat software, budete muset soubor vytvořit spustitelným, což lze provést pomocí následujícího příkazu:

```bash
chmod +x file_name.run 
```

Poté můžete soubor spustit pomocí následujícího příkazu:

```bash
./file_name.run 
```

Proces instalace se může lišit v závislosti na konkrétním souboru a programu, který se pokoušíte nainstalovat.

Formát souboru .run je typ skriptu shellu používaného k distribuci instalačních programů softwaru nebo aplikací v prostředí Linuxu. Jedná se o samostatný balíček, který obsahuje vše potřebné k instalaci softwaru, včetně binárních souborů, knihoven a konfiguračních souborů.

Je důležité si uvědomit, že soubory .run mohou obsahovat i škodlivý kód, proto je vždy dobré před spuštěním souboru ověřit jeho zdroj a prohledat jej na přítomnost virů.

Některé soubory .run mohou navíc ke spuštění a instalaci vyžadovat oprávnění uživatele root, takže ke spuštění souboru se zvýšenými oprávněními možná budete muset použít příkaz „sudo“:

```bash
sudo ./filename.run
```

## Jak otevřít soubor RUN?

Chcete-li otevřít soubor .run, musíte jej nastavit jako spustitelný, což lze provést příkazem "chmod":

```bash
chmod +x filename.run 
```

Jakmile se soubor stane spustitelným, můžete jej spustit zadáním:

```bash
./filename.run
```

Spuštění souboru .run není totéž jako jeho otevření v textovém editoru. Spuštěním souboru .run se provede jeho instrukce, což může být cokoliv od instalace programu po spuštění skriptu. Chcete-li zobrazit obsah souboru .run, musíte jej otevřít v textovém editoru, jako je nano nebo vim:

```
nano filename.run
```
nebo
```
vim filename.run
```

## Reference
* [Jak spustit soubory .bin a .run v Ubuntu](https://vitux.com/how-to-execute-bin-and-run-files-in-ubuntu/)


