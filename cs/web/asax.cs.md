{
  "date" : "2019-10-11",
  "keywords" :[ "asax", "soubor asax", "formát souboru asax", "typ souboru asax", "soubor", "typ", "co je soubor asax" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASAX - ASP.NET Server Application File",
  "description" :"Naučte se vědět, co je soubor ASAX a rozhraní API, která mohou vytvářet a otevírat soubory ASAX.",
  "linktitle" : "ASAX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-07"
}

## Co je soubor ASAX?

Soubor s příponou .asax je soubor používaný aplikacemi ASP.NET, který je umístěn na straně serveru. Obsahuje kód pro reakci na události na úrovni aplikace a relace vyvolané ASP.NET nebo moduly HTTP. To také zahrnuje zpracování určitých událostí při spuštění nebo vypnutí aplikace. Soubory ASAX jsou volitelné a do webových aplikací se přidává pouze jeden soubor ASAX, aby se zpracovávaly události a chyby na úrovni aplikace na globální úrovni. Na rozdíl od stránek ASPX neobsahují soubory ASAX žádný kód pro implementaci funkčnosti aplikace.

## Formát souboru ASAX

Soubory ASAX jsou psány ve formátu prostého textu a jsou čitelné pro člověka. Nejčastěji používaným souborem ASAX je Global.asax, který se nachází v kořenovém adresáři aplikace ASP.NET. Webové servery jsou nakonfigurovány tak, aby odmítaly všechna příchozí volání tohoto souboru a zakazovaly uživatelům stahování nebo prohlížení kódu tohoto souboru.

### Global.ASAX - Příklad formátu souboru ASAX

Jeden soubor ASAX se skládá z několika sekcí, které jsou napsány pro zpracování událostí na úrovni aplikace. Tyto jsou následující.

* **Aplikační direktivy** – Aplikační direktivy jsou značky, které se používají k definování volitelných nastavení specifických pro aplikaci, která má použít analyzátor ASP.NET při zpracování souboru Global.asax. Tyto direktivy jsou umístěny na začátku souboru Global.asax a jsou definovány následovně.

```
<%@ direktiva atribut=hodnota [atribut=hodnota … ]%>
```
* **Bloky deklarace kódu** – Bloky deklarace kódu se používají k definování částí kódu serveru, které jsou vloženy do aplikačních souborů ASP.NET v \<script> blocks marked with a runat="server" attribute. The following example shows how you can define event-handling logic for the EnterBtn_Click event.

```
<html>
  <script language="C#" runat="server">
      void EnterBtn_Click(Object Src, EventArgs E) {
          Message.Text = "Hi " + Name.Text + ", welcome to ASP.NET!";
  }
  </script>

  <body>
   <form runat="server">
    Enter your name: <asp:textbox id="Name" runat=server/>
                     <asp:button text="Enter" Onclick="EnterBtn_Click" runat="server"/>
        <p>
        <asp:label id="Message" runat=server/>
    </form>
  </body>
</html>
```
* **Bloky vykreslování kódu** – definují vložený kód nebo výrazy, které se spouštějí při vykreslování stránky. Dva styly bloků vykreslení kódu zahrnují vložený kód a vložené výrazy. První se používá k definování samostatných řádků nebo bloků kódu, zatímco postranní se používá jako zkratka pro volání metody Write.

## Reference

* [Přehled obslužných rutin HTTP a modulů HTTP](https://msdn.microsoft.com/en-us/library/bb398986(v=vs.100))
* [Global.asax syntaxe](https://docs.microsoft.com/en-us/previous-versions/dotnet/netframework-4.0/2027ewzw(v=vs.100))

