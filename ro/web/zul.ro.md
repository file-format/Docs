{
  "date" : "2021-05-24",
  "keywords" :["zul", "Fișier", "Extensie", "Format fișier", "Extensie fișier", "deschidere"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZUL - fișierul interfeței utilizator ZK",
  "description":"Aflați despre formatul de fișier ZUL și despre API-urile care pot crea și deschide fișiere ZUL.",
  "linktitle" : "ZUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Ce este un fișier ZUL?

Un fișier cu extensia .zul este un fișier web creat cu User Interface Markup Language (ZUML) și conține definiții pentru elementele interfeței cu utilizatorul. Clasele Ajax și Java acceptă utilizarea ZUML bazată pe [XML](/ro/web/xml/) pentru dezvoltarea fișierelor pe server. Formatul de fișier ZUL a fost dezvoltat de ZK, un cadru UI care vă permite să construiți aplicații web și mobile fără cunoștințele de JavaScript sau AJAX.

## Format de fișier ZUL

Fișierele ZUL sunt bazate pe XML, constând din diferite elemente pentru a construi interfața utilizator. Încărcătorul ZK utilizează fiecare element XML pentru a crea o componentă. Procesarea generală a elementelor paginii, cum ar fi titlul paginii, descrierea etc. sunt descrise de fiecare instrucțiune de procesare XML a ZUML.

### ZUL Exemplu

În următorul exemplu de cod ZUML, prima linie specifică titlul paginii, a doua linie creează o componentă rădăcină cu titlu și chenar, iar a treia linie creează un buton cu etichetă și un ascultător de evenimente.

```
<?page title="Super Application"?>
<window title="Super Hello" border="normal">
    <button label="hi" onClick='alert("hi")'/>
```
Schema ZUL poate fi descărcată de la https://www.zkoss.org/2005/zul/zul.xsd.
## Referințe

* [ZUL - De ZK](https://www.zkoss.org/wiki/ZK_Getting_Started/Tutorial)
* [Schema ZUL](https://www.zkoss.org/2005/zul/zul.xsd)

