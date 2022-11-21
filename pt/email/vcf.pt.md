{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCF - Arquivo de contato virtual",
  "description":"Saiba mais sobre o formato de arquivo VCF e APIs que podem criar e abrir arquivos VCF.",
  "linktitle" : "VCF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo VCF?

VCF (Virtual Card Format) ou vCard é um formato de arquivo digital para armazenar informações de contato. O formato é amplamente usado para troca de dados entre aplicativos populares de troca de informações. A maioria dos sistemas operacionais, como Windows e MacOS, vem com aplicativos padrão para criar e abrir esses arquivos. Um único arquivo VCF pode conter informações de contato para um ou vários contatos. Um arquivo VCF geralmente contém informações como nome do contato, endereço, número de telefone, e-mail, aniversário, fotografias e áudio, além de vários outros campos. Sendo suportado por clientes e serviços de e-mail, não há perda de dados durante a transferência de contatos usando o formato vCard. O tipo de mídia para o formato de arquivo VCF é text/vcard.

## Formato de arquivo VCF

Os arquivos VCF são textuais por natureza e são legíveis por humanos. Eles podem ser abertos em editores de texto como o Bloco de Notas no Microsoft Windows e o TextEdit no MacOS. Se houver uma imagem no arquivo, no entanto, ela não será exibida no editor de texto.

[Microsoft Outlook](https://support.office.com/en-us/article/send-and-save-contacts-as-vcards-vcf-files-94a17a6f-105f-46c7-9308-33658c1c2690) fornece suporte para abrir arquivos VCF, bem como converter para vários outros formatos, como o popular formato [MSG](/pt/email/msg/). Formato de arquivo VCF aprimorado com o tempo da versão 2.1 para 4.0, adicionando informações detalhadas ao formato do arquivo. O formato também é usado para exportar contatos telefônicos e depois importar em outro dispositivo.

{{< figure src="../VCF.png" alt="Formato de arquivo VCF" >}}

### Exemplo de VCF 2.1

Segue um exemplo da versão 2.1.

```
BEGIN:VCARD
VERSION:2.1
N:Gump;Forrest;;Mr.
FN:Forrest Gump
ORG:Bubba Gump Shrimp Co.
TITLE:Shrimp Man
PHOTO;GIF:http://www.example.com/dir_photos/my_photo.gif
TEL;WORK;VOICE:(111) 555-1212
TEL;HOME;VOICE:(404) 555-1212
ADR;WORK;PREF:;;100 Waters Edge;Baytown;LA;30314;United States of America
LABEL;WORK;PREF;ENCODING#QUOTED-PRINTABLE;CHARSET#UTF-8:100 Waters Edge#0D#
 #0ABaytown\, LA 30314#0D#0AUnited States of America
ADR;HOME:;;42 Plantation St.;Baytown;LA;30314;United States of America
LABEL;HOME;ENCODING#QUOTED-PRINTABLE;CHARSET#UTF-8:42 Plantation St.#0D#0A#
 Baytown, LA 30314#0D#0AUnited States of America
EMAIL:forrestgump@example.com
REV:20080424T195243Z
END:VCARD
```

### Exemplo de VCF 3.0

Segue um exemplo da versão 3.0.

```
BEGIN:VCARD
VERSION:3.0
N:Gump;Forrest;;Mr.;
FN:Forrest Gump
ORG:Bubba Gump Shrimp Co.
TITLE:Shrimp Man
PHOTO;VALUE#URI;TYPE#GIF:http://www.example.com/dir_photos/my_photo.gif
TEL;TYPE#WORK,VOICE:(111) 555-1212
TEL;TYPE#HOME,VOICE:(404) 555-1212
ADR;TYPE#WORK,PREF:;;100 Waters Edge;Baytown;LA;30314;United States of America
LABEL;TYPE#WORK,PREF:100 Waters Edge\nBaytown\, LA 30314\nUnited States of America
ADR;TYPE#HOME:;;42 Plantation St.;Baytown;LA;30314;United States of America
LABEL;TYPE#HOME:42 Plantation St.\nBaytown\, LA 30314\nUnited States of America
EMAIL:forrestgump@example.com
REV:2008-04-24T19:52:43Z
END:VCARD
```

### Exemplo de VCF 4.0

Segue um exemplo da versão 4.0.

```
BEGIN:VCARD
VERSION:4.0
N:Gump;Forrest;;Mr.;
FN:Sheri Nom
ORG:Sheri Nom Co.
TITLE:Ultimate Warrior
PHOTO;MEDIATYPE#image/gif:http://www.sherinnom.com/dir_photos/my_photo.gif
TEL;TYPE#work,voice;VALUE#uri:tel:+1-111-555-1212
TEL;TYPE#home,voice;VALUE#uri:tel:+1-404-555-1212
ADR;TYPE#WORK;PREF#1;LABEL#"Normality\nBaytown\, LA 50514\nUnited States of America":;;100 Waters Edge;Baytown;LA;50514;United States of America
ADR;TYPE#HOME;LABEL#"42 Plantation St.\nBaytown\, LA 30314\nUnited States of America":;;42 Plantation St.;Baytown;LA;30314;United States of America
EMAIL:sherinnom@example.com
REV:20080424T195243Z
x-qq:21588891
END:VCARD
```

## Referências

* [VCF - Por Wikipedia](https://en.wikipedia.org/wiki/VCard)

