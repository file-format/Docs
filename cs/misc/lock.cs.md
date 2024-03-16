{
  "date" : "2022-01-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru LOCK - Co je soubor zámku?",
  "description":"Další informace o formátu souboru LOCK a jeho .",
  "linktitle" : "LOCK",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-26"
}

## Co je soubor LOCK?

Soubor **LOCK** je přejmenovaný soubor, který používají aplikace a operační systémy k označení souboru nebo některého zařízení jako uzamčeného. Tím sdělíte ostatním aplikacím, aby soubor nepoužívaly, pokud není volný od aplikace, která jej používá. Ve většině případů jsou tyto soubory zámku prázdné, ale v jiných případech mohou obsahovat informace související se zámkem, jako jsou vlastnosti a nastavení.

Někdy je soubor .lock používán rozhraním .NET Framework společnosti Microsoft k vytváření **uzamčených** kopií databázového souboru. V takovém případě se otevře kopie databázového souboru s příponou .lock. To uživateli neumožňuje provádět změny v souboru, když jej používá jiný uživatel.

## Formát souboru LOCK – Další informace

Soubor LOCK je vytvořen každou aplikací a jeho formát souboru je specifický pro danou aplikaci. Tyto soubory zámku lze uložit v textovém i binárním formátu.

Přítomnost souborů zámku zabraňuje současnému přístupu zdroje k více souborům, které se pokoušejí o přístup k tomuto prostředku. Vytvoří se kopie původního souboru s příponou .lock s příponou k jeho názvu. Tím sdělíte ostatním aplikacím, aby měly k souboru přístup pouze pro čtení. Například resource.dat se změní na resource.data.lock.

U programovacího jazyka Ruby se můžete setkat se souborem **gemfile.lock**. Zde Bundler uchovává záznamy o přesných verzích, které byly nainstalovány. Když je tedy projekt/knihovna přesunuta na jiný počítač, běžící balíček vyhledá přesnou relevantní verzi v Gemfile.

## Zamknout soubor v Linuxu

Linux podporuje dva typy zámků souborů: poradní zámky a povinné zámky.

* **Advisory Locks**: Typ uzamčení, které není vynuceno. V tomto případě zúčastněné procesy vzájemně spolupracují a explicitně získávají zámky. Pokud to není možné, jsou poradní zámky ignorovány.

* **Povinné uzamčení**: V případě povinného zamykání vynucuje operační systém uzamčení souboru tím, že zabrání jiným procesům ve čtení nebo zápisu souboru. To nevyžaduje žádnou spolupráci mezi procesy.

povinné zamykání nevyžaduje žádnou spolupráci mezi zúčastněnými procesy. Jakmile je u souboru aktivován povinný zámek, operační systém zabrání dalším procesům ve čtení nebo zápisu souboru.

## Reference

* [GemFile a Gemfile.lock v Ruby](https://medium.com/never-hop-on-the-bandwagon/gemfile-and-gemfile-lock-in-ruby-65adc918b856)
* [Uzamykání v Linuxu](https://www.baeldung.com/linux/file-locking)
