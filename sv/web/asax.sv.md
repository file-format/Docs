{
  "date" : "2019-10-11",
  "keywords" :[ "asax","asax fil", "asax filformat", "asax filtyp", "fil", "typ", "vad är en asax fil" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASAX - ASP.NET Server Application File",
  "description" :"Lär dig veta vad en ASAX-fil och API:er är som kan skapa och öppna ASAX-filer.",
  "linktitle" : "ASAX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-07"
}

## Vad är en ASAX fil?

En fil med tillägget .asax är en fil som används av ASP.NET-applikationer som finns på serversidan. Den innehåller kod för att svara på händelser på applikationsnivå och sessionsnivå som tas upp av ASP.NET eller av HTTP-moduler. Detta inkluderar även hantering av vissa händelser när applikationen startar eller stängs av. ASAX-filer är valfria och endast en enda ASAX-fil läggs till i webbapplikationer för att hantera händelser och fel på applikationsnivå på global nivå. Till skillnad från ASPX-sidor innehåller ASAX-filer ingen kod för att implementera applikationens funktionalitet.

## ASAX filformat

ASAX-filer är skrivna i vanlig textfilformat och är läsbara för människor. Den vanligaste ASAX-filen är Global.asax som finns i rotkatalogen för en ASP.NET-applikation. Webbservrar är konfigurerade att avvisa alla inkommande samtal till den här filen för att förbjuda användare från att ladda ner eller visa koden för denna fil.

### Global.ASAX - Ett exempel på ASAX-filformat

En enda ASAX-fil består av flera sektioner som är skrivna för att hantera händelser på programnivå. Dessa är följande.

* **Applikationsdirektiv** - Applikationsdirektiv är taggar som används för att definiera valfria applikationsspecifika inställningar som ska användas av ASP.NET-parsern vid bearbetning av Global.asax-filen. Dessa direktiv finns i början av Global.asax-filen och definieras enligt följande.

```
<%@ direktiv attribut=värde [attribut=värde … ]%>
```
* **Koddeklarationsblock** - Koddeklarationsblock används för att definiera delar av serverkod som är inbäddade i ASP.NET-programfiler i \<script> blocks marked with a runat="server" attribute. The following example shows how you can define event-handling logic for the EnterBtn_Click event.

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
* **Code Render Blocks** - Dessa definierar inline-koden eller uttrycken som körs när sidan renderas. De två stilarna av kodrenderingsblock inkluderar inline-kod och inline-uttryck. Den förra används för att definiera fristående rader eller kodblock, medan den laterala används som en genväg för att anropa Write-metoden.

## Referenser

* [Översikt över HTTP-hanterare och HTTP-moduler](https://msdn.microsoft.com/en-us/library/bb398986(v=vs.100))
* [Global.asax Syntax](https://learn.microsoft.com/en-us/previous-versions/dotnet/netframework-4.0/2027ewzw(v=vs.100))

