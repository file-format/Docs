{
  "date" : "2022-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Soubor HDMP - formát souboru Windows Heap Dump",
  "description":"Další informace o formátu souborů HDMP a rozhraních API, která mohou vytvářet a otevírat soubory HDMP.",
  "linktitle" : "HDMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-08-19"
}

## Co je soubor HDMP?

Soubor HDMP je nekomprimovaný výpis paměti, když se aplikace nebo program zhroutí kvůli chybě. Je vytvořen pouze ve Windows XP/Vista a obsahuje výpis stavu aplikace, když došlo k jejímu zhroucení. Nekomprimované soubory HDMP zabírají na disku více místa ve srovnání se soubory Minidump [MDMP](/cs/system/mdmp/), které jsou komprimovány pro účely vytváření zpráv.

Aplikace, které lze použít k **otevření** nebo analýze souborů HDMP, zahrnují Microsoft Visual Studio s nástroji pro ladění pro Windows.

## Formát souboru HDMP

Soubory HDMP se ukládají na disk jako binární soubory a neposkytují žádnou výhodu, pokud jsou otevřeny bez příslušných aplikací. Ty obsahují relevantní systémová data zaznamenaná, když došlo k chybě.

### Rozdíl mezi formáty souborů HDMP a MDMP

HDMP jsou nekomprimované soubory výpisu paměti. Naproti tomu MDMP jsou soubory mini výpisu, které jsou komprimovány pro zmenšení velikosti souboru a odeslány společnosti Microsoft k nahlášení problému.

## reference ##

* [DMP – Microsoft](https://docs.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

