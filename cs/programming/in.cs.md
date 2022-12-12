{
  "date" : "2022-04-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Ve formátu souboru - Autoconf Input File",
  "description":"Další informace o formátu souboru IN a rozhraních API, která mohou vytvářet a otevírat soubory IN.",
  "linktitle" : "IN",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-26"
}

## Co je soubor IN?

Soubor IN je vstupní soubor, který GNU Autoconf používá při sestavování aplikace. Při spuštění procesu konfigurace může skript Autoconf (soubor .AC) odkazovat na jeden nebo více souborů ".in" nebo ".h.in". Soubory IN definují proměnné, na které se odkazuje během instalace programu, jako je číslo verze aplikace a datum vydání. Soubory IN lze také použít k určení přítomnosti nebo nepřítomnosti funkcí v konkrétní instalaci. K otevírání a úpravě souborů IN lze použít aplikace jako Notepad a Notepad++.

## Formát souboru IN – Další informace

Autoconf je součást sestavení GNU systému, která generuje vlastní sestavení aplikací pro různé platformy. Je to jeden z několika nástrojů pro sestavení GNU. Mezi další nástroje patří Automake, Gnulib a Libtool. Bez nutnosti ručního zásahu uživatele mohou tyto skripty přizpůsobit balíčky široké škále systémů podobných UNIXu. Autoconf generuje konfigurační skript balíčku ze souboru šablony, který uvádí funkce operačního systému, které může balíček používat ve formě volání maker M4.

## Reference

* [Autoconf](https://www.gnu.org/software/autoconf/)

