{
  "date" : "2021-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFML - Fișier limbaj de marcare ColdFusion",
  "description" :"Aflați despre ce este un fișier CFML și API-urile care pot crea și deschide fișiere CFML.",
  "linktitle" : "CFML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-19"
}

## Ce este un fișier CFML?

Un fișier cu extensia .cfml este un fișier ColdFusion Markup Language care este utilizat pentru a crea o pagină web. Se referă la un set de reguli folosite pentru a defini modul în care va fi dezvoltată aplicația ColdFusion de către programator. ColdFusion este un limbaj de programare care este folosit pentru a crea aplicații web pe server rapid și cu mai puțin decât alte tehnologii, cum ar fi [ASP](/ro/web/asp/), [PHP](/ro/web/php/), etc. Unele dintre aplicațiile care pot deschide fișiere CML includ Adobe ColdFusion 2018, Adobe ColdFusion Builder și Adobe Dreamweaver.

## Format de fișier CFML - Mai multe informații

Fișierele CFML sunt fișiere de marcare și conțin elemente web sub formă de etichete. Acestea sunt fișiere text care pot fi deschise și editate în orice editor de text. Fișierele CFML constau din mai multe etichete care sunt similare cu [HTML](/ro/web/html/) și de obicei cuprind o etichetă de deschidere și o etichetă de închidere. Aceste etichete pot conține, de asemenea, unul sau mai multe atribute.

### Sintaxa etichetelor

Mai jos este sintaxa generalizată a etichetelor CFML.

```
<tagname>
  Code/text that is affected by the surrounding tags.
</tagname>
```

Majoritatea etichetelor acceptă atribute și sunt definite după cum urmează.

```
<tagname attribute="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

Unele dintre aceste etichete acceptă, de asemenea, mai multe atribute cu următoarea sintaxă.

```
<tagname attribute1="value" attribute2="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

## Exemplu de cod CFML

Iată un exemplu care utilizează o etichetă CFML reală - eticheta `cfoutput`:

```
<cfoutput>
  #firstname#
</cfoutput>
```

## Referințe

* [ColdFusion](https://www.quackit.com/coldfusion/tutorial/)

