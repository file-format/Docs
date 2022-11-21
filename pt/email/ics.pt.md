{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICS - formato de arquivo iCalendar",
  "description":"Saiba mais sobre o formato de arquivo ICS e APIs que podem criar e abrir arquivos ICS.",
  "linktitle" : "ICS",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo ICS?

O Internet Calendaring and Scheduling Core Object Specification (iCalendar) é um padrão da Internet (RFC 2445) para troca e implantação de eventos de calendário e agendamento. O formato iCalendar é interoperável, garantindo assim a troca de informações de calendário entre os usuários que possuem diferentes aplicativos de e-mail. O iCalendar formata os dados de entrada como MIME (Multipurpose Internet Mail Extensions) e facilita a troca de objetos por meio de diferentes protocolos de transporte. Esses protocolos de transporte podem ser SMTP, HTTP, comunicação assíncrona ponto a ponto e transporte de rede baseado em mídia física.

O iCalendar permite que os usuários compartilhem eventos, tarefas dependentes de data/hora e informações de disponibilidade por meio de e-mails para outros usuários que podem responder. Os arquivos iCalendar são armazenados usando sufixos ".ics" ".iCalendar" ou ".ifb" com um tipo MIME de "texto/calendário". O iCalendar é mantido para ser autossuficiente sem qualquer dependência de protocolo de transporte. Os servidores da Web (com protocolo HTTP) podem transportar informações do iCalendar e as páginas da Web podem conter dados do iCalendar em formato incorporado usando o iCalendar.

## Breve História do Formato de Arquivo ICS

Em 1998, a Internet Engineering Task Force (IETF) definiu o iCalendar como padrão (RFC 2445). O padrão foi documentado por Frank Dawson (Lotus Notes Corporation) e Derik Stenerson (Microsoft). Em 2009, o padrão foi novamente refinado por Bernard Desruisseaux (Oracle) como RFC 5545. Desta vez, alguns novos recursos foram adicionados e alguns recursos desatualizados foram preteridos. Em 2016, o RFC 7986 foi lançado e aumentado para o RFC original do iCalendar. A RFC 7986 adicionou novas características ao objeto principal VCALENDAR e novos recursos de suporte também foram introduzidos para sistemas de conferência.

## Formato de arquivo ICS ##

O tipo MIME usado pelos dados do iCalendar é “texto/calendário”. O conjunto de caracteres padrão para iCalendar é UTF-8, no entanto, ao fornecer parâmetros em MIME, um conjunto de caracteres diferente pode ser usado. Um arquivo iCalendar contém seções, entre essas seções "VCALENDAR", é a seção global que encapsula todas as outras seções. A seção VEVENT define eventos, VTODO lista todos os itens pendentes, VJOURNAL contém entradas de diário e VTIMEZONE especifica informações de fuso horário. várias seções de categoria semelhante são permitidas. Para vários eventos, várias seções VEVENT podem estar presentes em um arquivo iCalendar.

### Linhas de conteúdo ###

Os objetos iCalendar são organizados em linhas distintas de texto “linhas de conteúdo”. Neste formato de arquivo, a sequência CRLF termina uma linha, enquanto o comprimento da linha é limitado a 75 octetos, excluindo a quebra de linha. Um item de dados longo pode ser estendido para muitas linhas.

### Separadores de Listas e Campos ###

Propriedades e parâmetros especificam uma lista de valores separados por um caractere VÍRGULA. As strings entre aspas são usadas para valores de parâmetros baseados em URI. A lista de parâmetros pode ser construída pelo valor da propriedade. Cada parâmetro de propriedade nesta lista deve ser separado por um SEMICOLON.

Em uma lista de valores, um SEMICOLON isola os parâmetros de propriedade e uma vírgula separa os valores de propriedade. Exemplo é dado abaixo:

```
ATTENDEE;RSVP#TRUE;ROLE#REQ- contestant:mailto:
name@example.com
DATE;VALUE#DATE:20170304,20180504,2015704,201270904
```

### Vários valores

Algumas propriedades podem ter vários valores. Simplesmente gerar uma nova linha de conteúdo com o nome da propriedade é a regra básica para propriedades de vários valores. No entanto, para um único valor com várias variações de idioma, não se deve usar propriedades com vários valores.

### Conteúdo binário

Dentro de um objeto iCalendar, o valor da propriedade pode fazer referência a dados de conteúdo binário colocados em uma entidade MIME externa usando um URI. O conteúdo binário embutido pode ser usado em situações especiais com o parâmetro "ENCODING", onde o aplicativo precisa expressar um objeto iCalendar como uma entidade única. O exemplo a seguir explica uma propriedade "ATTACH" com uma referência de URI:

ANEXAR: https://products.conholdate.app/viewer/view/KDDURXKkLk/fileformat.doc

### Conjunto de caracteres

Embora o esquema de conjunto de caracteres padrão para um iCalendar seja UTF-8, nenhum parâmetro de propriedade é especificado para definir o conjunto de caracteres de um valor de propriedade. em transferências MIME o parâmetro "charset" DEVE ser usado para o charset existente.

## Referências

* [Especificação do objeto principal de calendário e agendamento da Internet](https://www.ietf.org/rfc/rfc5545.txt)
* [iCalendar (RFC 5545)](https://icalendar.org/RFC-Specifications/iCalendar-RFC-5545/)
* [iCalendar](https://en.wikipedia.org/wiki/ICalendar#History_and_design)

