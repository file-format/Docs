{
"datum": "22. 3. 2023",
  "keywords": [
"soubor cnf",
"co je soubor cnf",
"jak otevřít soubor cnf",
"soubor",
"přípona souboru cnf",
"rozšíření"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formát souboru CNF - konfigurační soubor MySQL",
  "description":"Další informace o formátu CNF a rozhraních API, která mohou vytvářet a otevírat soubory CNF.",
  "linktitle": "CNF",
  "menu": {
    "docs": {
      "identifier": "settings-cnf",
      "parent": "settings"
}
},
"lastmod": "2023-03-22"
}

## Co je soubor CNF?

Soubor CNF (také známý jako konfigurační soubor) v MySQL se používá k uložení konfiguračních nastavení serveru MySQL. Umístění souboru CNF se může lišit v závislosti na operačním systému a použité metodě instalace. Konfigurace obvykle zahrnuje různá nastavení, jako je výchozí kódování znaků, časové limity, konfigurace mezipaměti a vyrovnávací paměti, která lze upravit tak, aby optimalizovala výkon databáze na základě využití.

## Formát souboru CNF – Další informace

CNF můžete vytvořit pomocí následujících kroků v MySQL:

1. Otevřete textový editor např. Poznámkový blok a vytvořte nový soubor.
2. Přidejte do souboru požadované možnosti konfigurace, jednu na řádek. Zde je příklad:

```
[mysqld]
datadir=/var/lib/mysql
socket=/var/lib/mysql/mysql.sock
user=mysql
symbolic-links=0

[client]
user=root
password=password123
```

3. Uložte soubor s příponou .cnf, například „mysql.cnf“.
4. Přesuňte soubor do příslušného adresáře. Například v systémech Linux může být adresář /etc/mysql/conf.d/ nebo /etc/mysql/.
5. Restartujte server MySQL, aby se nové nastavení konfigurace projevilo.

Ujistěte se, že jste otestovali všechny změny provedené v souboru CNF v neprodukčním prostředí, než je implementujete do produkčního prostředí.

## Jak otevřít soubor CNF?

Soubor CNF je textový soubor a lze jej snadno otevřít pomocí libovolného textového editoru, jako je Poznámkový blok. Můžete jej také otevřít kliknutím pravým tlačítkem myši a výběrem možnosti „Otevřít pomocí“ z nabídky. Jakmile je soubor otevřen, můžete upravit nastavení konfigurace podle potřeby. CNF obsahuje různá nastavení související s MySQL serverem, např. číslo portu, možnosti protokolování a velikosti vyrovnávací paměti. Po úpravě nastavení uložte změny a zavřete textový editor. Nakonec restartujte server MySQL, aby se změny projevily.

Pamatujte, že je důležité být při úpravách konfiguračního souboru MySQL opatrní, protože nesprávné nastavení může způsobit, že se server bude chovat nepředvídatelně nebo se nespustí vůbec. Před provedením jakýchkoli změn se doporučuje vytvořit zálohu původního souboru, abyste jej mohli v případě potřeby obnovit.

## Reference
* [MySQL](https://en.wikipedia.org/wiki/MySQL)

