{
  "date": "2019-10-11",
  "keywords": [
"asax",
"asax failą",
"asax failo formatas",
"asax failo tipas",
"failą",
"tipo",
"kas yra asax failas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASAX – ASP.NET serverio programos failas",
  "description": "Sužinokite, kas yra ASAX failas ir API, kurios gali kurti ir atidaryti ASAX failus.",
  "linktitle": "ASAX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-asa-ltx"
}
},
  "lastmod": "2021-06-07"
}

## Kas yra ASAX failas?

Failas su plėtiniu .asax yra ASP.NET programų naudojamas failas, esantis serverio pusėje. Jame yra kodas, skirtas reaguoti į programos lygio ir seanso lygio įvykius, kuriuos sukelia ASP.NET arba HTTP moduliai. Tai taip pat apima tam tikrų įvykių tvarkymą, kai programa paleidžiama arba išsijungia. ASAX failai yra neprivalomi ir tik vienas ASAX failas pridedamas prie žiniatinklio programų, kad būtų galima tvarkyti programos lygio įvykius ir klaidas pasauliniu lygiu. Skirtingai nuo ASPX puslapių, ASAX failuose nėra kodo, skirto programos funkcijoms įgyvendinti.

## ASAX failo formatas

ASAX failai yra parašyti paprasto teksto failo formatu ir yra skaitomi žmonėms. Dažniausiai naudojamas ASAX failas yra Global.asax, kuris yra ASP.NET programos šakniniame kataloge. Žiniatinklio serveriai sukonfigūruoti atmesti bet kokius įeinančius skambučius į šį failą, kad vartotojai negalėtų atsisiųsti ar peržiūrėti šio failo kodo.

### Global.ASAX – ASAX failo formato pavyzdys

Vieną ASAX failą sudaro keli skyriai, parašyti programos lygio įvykiams tvarkyti. Tai yra taip.

 * **Programų direktyvos** – taikomųjų programų direktyvos yra žymos, kurios naudojamos pasirenkamiems konkrečios programos parametrams, kuriuos ASP.NET analizatorius naudos apdorodamas Global.asax failą, apibrėžti. Šios direktyvos yra Global.asax failo pradžioje ir apibrėžiamos taip.

```
<%@ direktyva atributas=vertė [atributas=vertė … ]%>
```
 * **Kodo deklaravimo blokai** – kodo deklaravimo blokai naudojami apibrėžti serverio kodo dalis, kurios yra įterptos į ASP.NET taikomųjų programų failus \<script> blocks marked with a runat=server attribute. The following example shows how you can define event-handling logic for the EnterBtn_Click event.

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
 * **Kodo pateikimo blokai** – jie apibrėžia eilutinį kodą arba išraiškas, kurios vykdomos pateikiant puslapį. Du kodo atvaizdavimo blokų stiliai apima eilutinį kodą ir įterptąsias išraiškas. Pirmoji naudojama savarankiškoms kodo eilutėms ar blokams apibrėžti, o šoninė naudojama kaip rašymo metodo iškvietimo nuoroda.

## Nuorodos

 * [HTTP tvarkyklių ir HTTP modulių apžvalga](https://msdn.microsoft.com/en-us/library/bb398986(v=vs.100))
 * [Global.asax sintaksė](https://learn.microsoft.com/en-us/previous-versions/dotnet/netframework-4.0/2027ewzw(v=vs.100))

