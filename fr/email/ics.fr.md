{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICS - Format de fichier iCalendar",
  "description":"En savoir plus sur le format de fichier ICS et les API qui peuvent créer et ouvrir des fichiers ICS.",
  "linktitle" : "ICS",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier ICS ?

L'Internet Calendaring and Scheduling Core Object Specification (iCalendar) est une norme Internet (RFC 2445) pour l'échange et le déploiement des événements de calendrier et de planification. Le format iCalendar est interopérable, assurant ainsi l'échange d'informations de calendrier entre les utilisateurs ayant différentes applications de messagerie. iCalendar formate les données d'entrée en tant qu'extensions de messagerie Internet polyvalentes (MIME) et facilite l'échange d'objets via différents protocoles de transport. Ces protocoles de transport peuvent être SMTP, HTTP, une communication asynchrone point à point et un transport réseau basé sur un support physique.

iCalendar permet aux utilisateurs de partager des événements, des tâches dépendant de la date/heure et des informations de disponibilité par e-mail avec d'autres utilisateurs qui peuvent répondre. Les fichiers iCalendar sont stockés en utilisant les suffixes ".ics" ".iCalendar" ou ".ifb" avec un type MIME de "text/calendar". iCalendar est maintenu pour être autonome sans aucune dépendance au protocole de transport. Les serveurs Web (avec protocole HTTP) peuvent transporter des informations iCalendar et les pages Web peuvent contenir des données iCalendar sous forme intégrée à l'aide d'iCalendar.

## Bref historique du format de fichier ICS

En 1998, l'Internet Engineering Task Force (IETF) a défini iCalendar comme une norme (RFC 2445). La norme a été documentée par Frank Dawson (Lotus Notes Corporation) et Derik Stenerson ( Microsoft). En 2009, la norme a de nouveau été affinée par Bernard Desruisseaux (Oracle) en tant que RFC 5545. Cette fois, de nouvelles fonctionnalités ont été ajoutées et certaines fonctionnalités obsolètes ont été obsolètes. En 2016, la RFC 7986 a été publiée et complétée par la RFC iCalendar originale. La RFC 7986 a ajouté de nouvelles caractéristiques à l'objet principal VCALENDAR et de nouvelles fonctionnalités de support ont également été introduites pour les systèmes de conférence.

## Format de fichier ICS ##

Le type MIME utilisé par les données d'iCalendar est « text/calendar ». Le jeu de caractères par défaut pour iCalendar est UTF-8, mais en fournissant des paramètres dans MIME, un jeu de caractères différent peut être utilisé. Un fichier iCalendar contient des sections, parmi ces sections "VCALENDAR", est la section globale qui encapsule toutes les autres sections. La section VEVENT définit les événements, VTODO répertorie tous les éléments à faire, VJOURNAL contient les entrées de journal et VTIMEZONE spécifie les informations de fuseau horaire. plusieurs sections de catégorie similaire sont autorisées. Pour de nombreux événements, plusieurs sections VEVENT peuvent être présentes dans un fichier iCalendar.

### Lignes de contenu ###

Les objets iCalendar sont organisés en lignes de texte distinctes "lignes de contenu". Dans ce format de fichier, la séquence CRLF termine une ligne alors que la longueur de la ligne est limitée à 75 octets hors saut de ligne. Un élément de données long peut s'étendre sur plusieurs lignes.

### Séparateurs de listes et de champs ###

Les propriétés et les paramètres spécifient une liste de valeurs séparées par une virgule. Les chaînes entre guillemets sont utilisées pour les valeurs de paramètre basées sur l'URI. La liste des paramètres peut être construite par la valeur de la propriété. Chaque paramètre de propriété de cette liste doit être séparé par un SEMICOLON.

Dans une liste de valeurs, un SEMICOLON isole les paramètres de propriété et une virgule sépare les valeurs de propriété. Un exemple est donné ci-dessous :

```
ATTENDEE;RSVP#TRUE;ROLE#REQ- contestant:mailto:
name@example.com
DATE;VALUE#DATE:20170304,20180504,2015704,201270904
```

### Valeurs multiples

Certaines propriétés peuvent avoir plusieurs valeurs. Générer simplement une nouvelle ligne de contenu avec le nom de la propriété est la règle de base pour les propriétés à valeurs multiples. Cependant, pour une valeur unique avec plusieurs variantes de langue, il ne faut pas utiliser de propriétés à valeurs multiples.

### Contenu binaire

Dans un objet iCalendar, la valeur de la propriété peut faire référence à des données de contenu binaire placées dans une entité MIME externe à l'aide d'un URI. Le contenu binaire en ligne peut être utilisé dans des situations particulières avec le paramètre "ENCODING", où l'application doit exprimer un objet iCalendar en tant qu'entité unique. L'exemple suivant explique une propriété "ATTACH" avec une référence URI :

ATTACHEZ : https://products.conholdate.app/viewer/view/KDDURXKkLk/fileformat.doc

### Jeu de caractères

Bien que le schéma de jeu de caractères par défaut pour un iCalendar soit UTF-8, aucun paramètre de propriété n'est spécifié pour définir le jeu de caractères d'une valeur de propriété. dans les transferts MIME, le paramètre "charset" DOIT être utilisé pour le jeu de caractères existant.

## Références

* [Spécification de l'objet de base de l'agenda et de la planification Internet](https://www.ietf.org/rfc/rfc5545.txt)
* [iCalendar (RFC 5545)](https://icalendar.org/RFC-Specifications/iCalendar-RFC-5545/)
* [iCalendar](https://en.wikipedia.org/wiki/ICalendar#History_and_design)

