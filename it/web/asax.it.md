{
  "date" : "2019-10-11",
  "keywords" :[ "asax","file asax", "formato file asax", "tipo di file asax", "file", "tipo", "cos'è un file asax" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASAX - File dell'applicazione server ASP.NET",
  "description" :"Impara a sapere cos'è un file ASAX e le API che possono creare e aprire file ASAX.",
  "linktitle" : "ASAX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-07"
}

## Che cos'è un file ASAX?

Un file con estensione .asax è un file utilizzato dalle applicazioni ASP.NET che risiede sul lato server. Contiene codice per rispondere agli eventi a livello di applicazione e di sessione generati da ASP.NET o dai moduli HTTP. Ciò include anche la gestione di determinati eventi all'avvio o alla chiusura dell'applicazione. I file ASAX sono facoltativi e un solo file ASAX viene aggiunto alle applicazioni Web per gestire gli eventi e gli errori a livello di applicazione a livello globale. A differenza delle pagine ASPX, i file ASAX non contengono codice per implementare la funzionalità dell'applicazione.

## Formato file ASAX

I file ASAX sono scritti in formato di file di testo normale e sono leggibili dall'uomo. Il file ASAX più comunemente utilizzato è Global.asax che risiede nella directory principale di un'applicazione ASP.NET. I server Web sono configurati per rifiutare qualsiasi chiamata in arrivo a questo file per impedire agli utenti di scaricare o visualizzare il codice di questo file.

### Global.ASAX - Un esempio di formato di file ASAX

Un singolo file ASAX è costituito da più sezioni scritte per gestire gli eventi a livello di applicazione. Questi sono i seguenti.

* **Direttive dell'applicazione**: le direttive dell'applicazione sono tag utilizzati per definire le impostazioni specifiche dell'applicazione facoltative che devono essere utilizzate dal parser ASP.NET durante l'elaborazione del file Global.asax. Queste direttive si trovano all'inizio del file Global.asax e sono definite come segue.

```
<%@ direttiva attributo=valore [attributo=valore … ]%>
```
* **Blocchi di dichiarazione di codice**: i blocchi di dichiarazione di codice vengono utilizzati per definire sezioni di codice del server incorporate nei file dell'applicazione ASP.NET all'interno di \<script> blocks marked with a runat="server" attribute. The following example shows how you can define event-handling logic for the EnterBtn_Click event.

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
* **Blocchi di rendering del codice**: definiscono il codice inline o le espressioni che vengono eseguite quando viene eseguito il rendering della pagina. I due stili dei blocchi di rendering del codice includono il codice inline e le espressioni inline. Il primo è usato per definire linee autonome o blocchi di codice, mentre il laterale è usato come scorciatoia per chiamare il metodo Write.

## Riferimenti

* [Panoramica dei gestori HTTP e dei moduli HTTP](https://msdn.microsoft.com/en-us/library/bb398986(v=vs.100))
* [Sintassi Global.asax](https://learn.microsoft.com/en-us/previous-versions/dotnet/netframework-4.0/2027ewzw(v=vs.100))

