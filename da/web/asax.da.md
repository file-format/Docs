{
  "date": "2019-10-11",
  "keywords": [
"asax",
"asax fil",
"asax filformat",
"asax filtype",
"fil",
"type",
"hvad er en asax fil"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASAX - ASP.NET Server Application File",
  "description": "Lær at vide, hvad der er en ASAX-fil og API'er, der kan oprette og åbne ASAX-filer.",
  "linktitle": "ASAX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-asa-dax"
}
},
  "lastmod": "2021-06-07"
}

## Hvad er en ASAX fil?

En fil med filtypenavnet .asax er en fil, der bruges af ASP.NET-applikationer, som ligger på serversiden. Den indeholder kode til at reagere på hændelser på applikationsniveau og sessionsniveau rejst af ASP.NET eller HTTP-moduler. Dette inkluderer også håndtering af visse hændelser, når applikationen starter eller lukker ned. ASAX-filer er valgfrie, og kun en enkelt ASAX-fil føjes til webapplikationer for at håndtere hændelser og fejl på applikationsniveau på globalt niveau. I modsætning til ASPX-sider indeholder ASAX-filer ingen kode til at implementere applikationens funktionalitet.

## ASAX filformat

ASAX-filer er skrevet i almindeligt tekstfilformat og kan læses af mennesker. Den mest almindeligt anvendte ASAX-fil er Global.asax, der ligger i rodmappen til en ASP.NET-applikation. Webservere er konfigureret til at afvise alle indgående opkald til denne fil for at forhindre brugere i at downloade eller se koden for denne fil.

### Global.ASAX - Et eksempel på ASAX-filformat

En enkelt ASAX-fil består af flere sektioner, der er skrevet til at håndtere hændelser på programniveau. Disse er som følger.

 * **Applikationsdirektiver** - Applikationsdirektiver er tags, der bruges til at definere valgfri applikationsspecifikke indstillinger, der skal bruges af ASP.NET-parseren, når Global.asax-filen behandles. Disse direktiver er placeret i starten af Global.asax-filen og er defineret som følger.

```
<%@ direktiv attribut=værdi [attribut=værdi … ]%>
```
 * **Kodeerklæringsblokke** - Kodeerklæringsblokke bruges til at definere sektioner af serverkode, der er indlejret i ASP.NET-applikationsfiler i \<script> blocks marked with a runat=server attribute. The following example shows how you can define event-handling logic for the EnterBtn_Click event.

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
 * **Kodegengivelsesblokke** - Disse definerer den eller de indlejrede udtryk, der udføres, når siden gengives. De to stilarter af kodegengivelsesblokke inkluderer inline-kode og inline-udtryk. Førstnævnte bruges til at definere selvstændige linjer eller kodeblokke, mens lateralen bruges som en genvej til at kalde Write-metoden.

## Referencer

 * [Oversigt over HTTP-handlere og HTTP-moduler](https://msdn.microsoft.com/en-us/library/bb398986(v=vs.100))
 * [Global.asax Syntax](https://learn.microsoft.com/en-us/previous-versions/dotnet/netframework-4.0/2027ewzw(v=vs.100))

