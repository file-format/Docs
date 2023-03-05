{
  "date" : "2022-03-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSO - Microsoft Office Macro Reference File",
  "description":"Další informace o souboru MSO a rozhraních API, která mohou vytvářet a otevírat soubory MSO.",
  "linktitle" : "MSO",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-03-12"
}

## Co je soubor MSO?

Soubor MSO je formát souboru datového kontejneru, který se vytvoří při odeslání zprávy HTML pomocí aplikace Microsoft Outlook. K tomu dochází většinou u aplikací Microsoft Office 2000. Ve většině případů je e-mailová zpráva připojena s názvem souboru **Oledata.mso**. Příjemce e-mailu, když takový e-mail otevře, může soubor správně zobrazit, i když nemá nainstalovaný stejný software. Soubory MSO odkazují na [Microsoft Compound Document File Format (MCDF)](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b).

## Formát souborů Microsoft MSO

Soubory MSO se ukládají ve formátu Microsoft Compound Document File Format (MCDF), který je také známý jako binární formát pro implementaci složených souborů pro strukturované úložiště a vkládání objektů (OLE) nebo Component Object Model (COM).

### Struktura formátu souborů MSO

Vnitřní struktura formátu souboru formátu MSO je dobře definována v [Strukturách](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/28488197-8193-49d7-84d8-dfd692418ccd ) sekce dokumentace MCDF. File Allocation Table (FAT) spravuje alokaci sektorů a sektorové řetězce. Obsahuje pole 32bitových čísel sektorů. Každý index v poli představuje číslo sektoru, zatímco jeho hodnota představuje další sektor v řetězci nebo speciální hodnotu.

## Reference

* [COM Structured Storage](https://en.wikipedia.org/wiki/COM_Structured_Storage)
* [Microsoft Compound Document File Format (MCDF)](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b)

