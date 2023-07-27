{
  "date" : "2021-05-24",
  "keywords" :["zul", "File", "Estensione", "Formato file", "Estensione file", "open"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZUL - File interfaccia utente ZK",
  "description":"Scopri il formato di file ZUL e le API che possono creare e aprire file ZUL.",
  "linktitle" : "ZUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Che cos'è un file ZUL?

Un file con estensione .zul è un file Web creato con lo User Interface Markup Language (ZUML) e contiene le definizioni per gli elementi dell'interfaccia utente. Le classi Ajax e Java supportano l'utilizzo di ZUML basato su [XML](/it/web/xml/) per lo sviluppo di file lato server. Il formato di file ZUL è stato sviluppato da ZK, un framework dell'interfaccia utente che consente di creare applicazioni Web e mobili senza la conoscenza di JavaScript o AJAX.

## Formato file ZUL

I file ZUL sono basati su XML, costituiti da diversi elementi per costruire l'interfaccia utente. Il caricatore ZK utilizza ogni elemento XML per creare un componente. L'elaborazione complessiva degli elementi della pagina come il titolo della pagina, la descrizione, ecc. sono descritti da ciascuna istruzione di elaborazione XML di ZUML.

### Esempio ZUL

Nell'esempio seguente di codice ZUML, la prima riga specifica il titolo della pagina, la seconda riga crea un componente radice con titolo e bordo e la terza riga crea un pulsante con etichetta e un listener di eventi.

```
<?page title="Super Application"?>
<window title="Super Hello" border="normal">
    <button label="hi" onClick='alert("hi")'/>
```
Lo schema ZUL può essere scaricato da https://www.zkoss.org/2005/zul/zul.xsd.
## Riferimenti

* [ZUL - Di ZK](https://www.zkoss.org/wiki/ZK_Getting_Started/Tutorial)
* [Schema ZUL](https://www.zkoss.org/2005/zul/zul.xsd)

