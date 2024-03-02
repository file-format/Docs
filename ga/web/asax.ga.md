{
  "date": "2019-10-11",
  "keywords": [
"asax",
"comhad asax",
"formáid comhaid asax",
"cineál comhaid asax",
"comhad",
"cineál",
"cad is comhad asax ann"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASAX - Comhad Feidhmchláir Freastalaí ASP.NET",
  "description": "Faigh amach cad is comhad ASAX agus APIs ann ar féidir comhaid ASAX a chruthú agus a oscailt.",
  "linktitle": "ASAX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-asa-gax"
}
},
  "lastmod": "2021-06-07"
}

## Cad is comhad ASAX ann?

Comhad le síneadh .asax is ea comhad a úsáideann feidhmchláir ASP.NET a chónaíonn ar thaobh an fhreastalaí. Tá cód ann chun freagra a thabhairt ar imeachtaí ar leibhéal an fheidhmchláir agus ar leibhéal an tseisiúin arna dtarraingt anuas ag ASP.NET nó ag modúil HTTP. Áiríonn sé seo freisin déileáil le himeachtaí áirithe nuair a sheoltar nó nuair a stoptar an feidhmchlár. Tá comhaid ASAX roghnach agus ní chuirtear ach comhad ASAX amháin le feidhmchláir ghréasáin chun imeachtaí agus earráidí ar leibhéal an fheidhmchláir a láimhseáil ar an leibhéal domhanda. Murab ionann agus leathanaigh ASPX, níl aon chód i gcomhaid ASAX chun feidhmiúlacht an fheidhmchláir a chur i bhfeidhm.

## Formáid Chomhaid ASAX

Scríobhtar comhaid ASAX i bhformáid gnáth-théacs agus tá siad inléite ag daoine. Is é an comhad ASAX is coitianta a úsáidtear ná Global.asax a chónaíonn i bhfréamheolaire feidhmchlár ASP.NET. Tá Freastalaithe Gréasáin cumraithe chun diúltú d'aon ghlaonna isteach chuig an gcomhad seo chun cosc a chur ar úsáideoirí cód an chomhaid seo a íoslódáil nó féachaint air.

### Global.ASAX - Sampla de Formáid Chomhaid ASAX

Is éard atá i gcomhad ASAX amháin ná go leor ranna a scríobhtar chun imeachtaí ar leibhéal an fheidhmchláir a láimhseáil. Seo a leanas iad.

 * **Treoracha Feidhmchláir** - Is clibeanna iad na treoracha feidhmchláir a úsáidtear chun socruithe roghnacha a bhaineann go sonrach le feidhmchlár a shainiú a bheidh le húsáid ag parsálaí ASP.NET agus an comhad Global.asax á phróiseáil. Tá na treoracha seo suite i dtús an chomhaid Global.asax agus sainmhínítear iad mar seo a leanas.

```
<%@ directive attribute=value [attribute=value… ]%>
```
 * **Bloic Dearbhaithe Cóid** - Úsáidtear bloic dearbhaithe cóid chun codanna de chód an fhreastalaí atá leabaithe i gcomhaid feidhmchláir ASP.NET laistigh den \ \ a shainiú.<script> blocks marked with a runat=server attribute. The following example shows how you can define event-handling logic for the EnterBtn_Click event.

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
 * **Bloic Rindreála Cóid** - Sainmhíníonn siad seo an cód inlíne nó na habairtí a fheidhmíonn nuair a dhéantar an leathanach a rindreáil. Áirítear leis an dá stíl de bhloic rindreála cód cód inlíne agus nathanna inlíne. Úsáidtear an chéad cheann chun línte féinchuimsitheacha nó bloic cód a shainiú, agus úsáidtear an cliathánach mar aicearra chun an modh Scríobh a ghlaoch.

## Tagairtí

 * [Láimhseálaithe HTTP agus Forbhreathnú ar Mhodúil HTTP](https://msdn.microsoft.com/en-us/library/bb398986(v=vs.100))
 * [Global.asax Comhréir](https://learn.microsoft.com/en-us/previous-versions/dotnet/netframework-4.0/2027ewzw(v=vs.100))

