{
  "date" : "2021-06-21",
  "keywords" :[ "UDL", "přípona", "soubor udl", "formát souboru udl", "Typ souboru databáze", "Formát souboru databáze", "co je soubor udl" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souboru UDL a rozhraních API, která mohou vytvářet a otevírat soubory UDL.",
  "title" :"UDL - Microsoft Universal Data Link File",
  "linktitle" : "UDL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-21"
}

## Co je soubor UDL?
Soubor s příponou .udl se nazývá soubor Microsoft Universal Data Link; určení atributů připojení; používané aplikacemi Windows k navázání spojení s databází. Soubor UDL obsahuje připojovací řetězec pro zdroj dat OLE DB; s uživatelským jménem a heslem a základními vlastnostmi připojovacího řetězce. Chcete-li se vyhnout přímému zadání vlastností ručně v připojovacím řetězci, lze jako alternativu použít dialogové okno Vlastnosti Data Link k uložení informací o připojení do souboru .udl.

## Formát souboru UDL
Soubor UDL (Universal Data Link) je v zásadě jednoduchý textový soubor, který se skládá z připojovacího řetězce databáze s konkrétními atributy nebo vlastnostmi. Jakmile je soubor UDL vytvořen, lze jej otestovat pomocí SQL Server Management Studio k ověření připojení.

### Vlastnosti připojovacího řetězce
Pro zajištění správné konektivity lze v UDL nastavit následující vlastnosti:

- **Název serveru**: umístění serveru, kde se nachází databáze, ke které chcete přistupovat.
- **Možnosti ověření**
- **Ověření systému Windows**: Ověření pro SQL Server pomocí přihlašovacích údajů k účtu Windows aktuálně přihlášeného uživatele.
- ** SQL Server Authentication**: Autentizace pomocí přihlašovacího ID a hesla.
- **Active Directory - Integrované**: Integrované ověřování s identitou Azure Active Directory; lze také použít pro ověřování Windows na SQL Server.
- **Active Directory - Password**: Ověření ID uživatele a hesla pomocí identity Azure Active Directory.
- **Active Directory - Univerzální s podporou MFA**: Interaktivní ověřování pomocí identity Azure Active Directory.
- **Active Directory - Principal služby**: Ověřování pomocí objektu služby Azure Active Directory.
- **Server SPN**: Pokud používáte důvěryhodné připojení, můžete zadat hlavní název služby (SPN) pro server.
- **Uživatelské jméno**: Zadejte ID uživatele, které se má použít pro ověření, když se přihlašujete ke zdroji dat.
- **Heslo**: Zadejte heslo, které se použije pro ověření, když se přihlašujete ke zdroji dat.
- **Prázdné heslo**: Pokud je zaškrtnuto, povolí zadanému poskytovateli použít prázdné heslo v připojovacím řetězci.
- **Povolit uložení hesla**: Umožňuje uložit heslo s připojovacím řetězcem.
- **Použít silné šifrování dat**: data, která procházejí připojením, budou šifrována.
- **Certifikát důvěryhodného serveru**: Certifikát serveru bude ověřen.
- **Databáze**: Název databáze, ke které chcete získat přístup.
- **Připojit databázový soubor jako název databáze**: Určuje název primárního souboru pro připojitelnou databázi.

## Reference ##

* [Microsoft Data Access Components](https://en.wikipedia.org/wiki/Microsoft_Data_Access_Components#Universal_data_link)
* [Konfigurace Universal Data Link (UDL)](https://learn.microsoft.com/en-us/sql/connect/oledb/help-topics/data-link-pages?view=sql-server-ver15)

