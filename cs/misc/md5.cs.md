{
  "date" : "2021-07-29",
  "keywords" :[ "soubor md5", "formát souboru md5", "co je soubor md5", "soubor", "příklad md5", "přípona souboru md5", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MD5 - MD5 soubor kontrolního součtu",
  "description":"Další informace o souboru MD5 a rozhraních API, která mohou vytvářet a otevírat soubory MD5.",
  "linktitle" : "MD5",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2021-07-29"
}

## Co je soubor MD5?

Soubor MD5 je soubor kontrolního součtu používaný k ověření integrity souboru. Je podobný otisku prstu pro přidružený soubor a je jednoznačně generován pomocí algoritmu, který používá počet bitů v souboru. Používá se k ověření souboru pomocí softwaru, jako je [md5sum](http://www.gnu.org/software/coreutils/manual/html_node/md5sum-invocation.html). Jednou z výhod používání souborů MD5 je ověření, že stažené soubory nejsou poškozeny.

## Formát souboru MD5 – Další informace

Obvykle je soubor MD5 uložen se stejným názvem jako původní název souboru, ale s příponou .md5. Pokud je například přidružený název souboru `abc_987_123456.grb`, odpovídající název souboru MD5 bude `abc_987_123456.grb.md5`. Soubory MD5 pomáhají identifikovat, že přijatý nebo stažený soubor není poškozen nebo ovlivněn škodlivým obsahem. Stručně řečeno, soubory MD5 zaručují úplnost souboru.


## Jak zkontrolovat kontrolní součet MD5?

Jeden soubor lze zkontrolovat/ověřit na MD5 pomocí nástroje [md5sum](https://en.wikipedia.org/wiki/Md5sum) následovně.

```
md5sum -c abc_987_123456.grb.md5
```

## Reference

* [md5sum - Wikipedia](https://en.wikipedia.org/wiki/Md5sum)

