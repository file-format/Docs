{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTACCESS File - Apache HTACCESS File Format",
  "description" :"Váš průvodce formátem souboru, abyste zjistili, co je soubor HTACCESS",
  "linktitle" : "HTACCESS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor HTACCESS?

Soubor HTACCESS je konfigurační soubor Apache, který poskytuje mechanismus umožňující změny konfigurace pro různé složky/adresáře webu. Zahrnuje konfigurační direktivy, které jsou použitelné pro adresář a podadresáře.

Soubor HTACCESS provádí řadu kontrol, jako je definování indexové stránky webu, výpis chybové stránky 404 (Stránka nenalezena), přesměrování stránky 301 nebo 302, blokování přístupu z konkrétní IP adresy nebo jiných webů. Použití souborů .htaccess tak zpomaluje celkový výkon vašeho Apache HTTP serveru.

## Formát souboru HTACCESS

Soubory HTACCESS se ukládají na disk ve formátu prostého textu. To znamená, že tyto soubory můžete otevřít a upravit v libovolném textovém editoru. Před "." není žádné jméno. v souboru .htaccess, což ukazuje, že se jedná o skrytý soubor ve složce.

## Běžná použití souboru HTACCESS

Následuje pět běžných použití souboru HTACCESS.

### Mod_Rewrite

Soubor HTACCESS lze použít k určení a změně způsobu, jakým se uživatelům zobrazují adresy URL a webové stránky na webu.

### Autentizace

Ověření lze dosáhnout pomocí .htaccess vytvořením souboru passowrd s názvem .htpasswd. To umožňuje návštěvníkům webu zadat heslo, pokud chtějí navštívit určitou část webové stránky.

### Vlastní chybové stránky

Můžete vytvořit vlastní chybové stránky, jako je 400 Chybný požadavek, 401 Vyžaduje autorizaci, 403 Zakázaná stránka, 404 Soubor nenalezen a 500 Vnitřní chyba se souborem .htaccess. Ty však zpomalí výkon serveru, protože všechny tyto kontroly budou prováděny při přístupu na stránky.

### Typy MIME

Soubory Apache HTACCESS lze upravit tak, aby zahrnovaly typy MIME (Multipurpose Internet Mail Extensions). To vašemu serveru umožní podporovat doručování aplikačních souborů, které nebyly podporovány webem.

### SSI

Zahrny na straně serveru (SSI) fungují na webu jako skvělá úspora času. SSI lze povolit vložením následujícího kódu hte do vašeho souboru .htaccess.

```
AddType text/html .shtml
AddHandler server-parsed .shtml</pre>
```

## Příklad souboru Apache HTACCESS

```
AuthType Basic
AuthName "Restricted Content"
AuthUserFile /etc/apache2/.htpasswd
Require valid-user
```

## Reference

* [Výukový program Apache HTTP Server: soubory .htaccess](https://httpd.apache.org/docs/current/howto/htaccess.html)

