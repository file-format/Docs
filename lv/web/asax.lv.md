{
  "date": "2019-10-11",
  "keywords": [
"asax",
"asax fails",
"asax faila formāts",
"asax faila tips",
"failu",
"veids",
"kas ir asax fails"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASAX — ASP.NET servera lietojumprogrammas fails",
  "description": "Uzziniet, kas ir ASAX fails un API, kas var izveidot un atvērt ASAX failus.",
  "linktitle": "ASAX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-asa-lvx"
}
},
  "lastmod": "2021-06-07"
}

## Kas ir ASAX fails?

Fails ar paplašinājumu .asax ir fails, ko izmanto ASP.NET lietojumprogrammas, kas atrodas servera pusē. Tajā ir kods reaģēšanai uz lietojumprogrammas līmeņa un sesijas līmeņa notikumiem, ko rada ASP.NET vai HTTP moduļi. Tas ietver arī noteiktu notikumu apstrādi, kad lietojumprogramma tiek palaista vai izslēgta. ASAX faili nav obligāti, un tīmekļa lietojumprogrammām tiek pievienots tikai viens ASAX fails, lai globālā līmenī apstrādātu lietojumprogrammas līmeņa notikumus un kļūdas. Atšķirībā no ASPX lapām, ASAX faili nesatur kodu, lai ieviestu lietojumprogrammas funkcionalitāti.

## ASAX faila formāts

ASAX faili ir rakstīti vienkārša teksta faila formātā un ir lasāmi cilvēkiem. Visbiežāk izmantotais ASAX fails ir Global.asax, kas atrodas ASP.NET lietojumprogrammas saknes direktorijā. Tīmekļa serveri ir konfigurēti, lai noraidītu visus ienākošos zvanus uz šo failu, lai liegtu lietotājiem lejupielādēt vai skatīt šī faila kodu.

### Global.ASAX — ASAX faila formāta piemērs

Viens ASAX fails sastāv no vairākām sadaļām, kas ir rakstītas, lai apstrādātu lietojumprogrammas līmeņa notikumus. Tie ir šādi.

 * **Lietojumprogrammu direktīvas** — lietojumprogrammu direktīvas ir atzīmes, kas tiek izmantotas, lai definētu izvēles lietojumprogrammas iestatījumus, kas jāizmanto ASP.NET parsētājam, apstrādājot failu Global.asax. Šīs direktīvas atrodas Global.asax faila sākumā un ir definētas šādi.

```
<%@ direktīva atribūts=vērtība [atribūts=vērtība … ]%>
```
 * **Koda deklarācijas bloki** — koda deklarācijas bloki tiek izmantoti, lai definētu servera koda sadaļas, kas ir iegultas ASP.NET lietojumprogrammu failos \<script> blocks marked with a runat=server attribute. The following example shows how you can define event-handling logic for the EnterBtn_Click event.

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
 * **Koda renderēšanas bloki** — tie nosaka iekļauto kodu vai izteiksmes, kas tiek izpildītas, kad lapa tiek renderēta. Divi koda renderēšanas bloku stili ietver iekļauto kodu un iekļautās izteiksmes. Pirmo izmanto, lai definētu autonomas koda rindas vai blokus, savukārt sānu izmanto kā saīsni rakstīšanas metodes izsaukšanai.

## Atsauces

 * [HTTP apdarinātāju un HTTP moduļu pārskats](https://msdn.microsoft.com/en-us/library/bb398986(v=vs.100))
 * [Global.asax sintakse](https://learn.microsoft.com/en-us/previous-versions/dotnet/netframework-4.0/2027ewzw(v=vs.100))

