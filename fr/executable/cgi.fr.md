{
  "date" : "2021-06-28",
  "keywords" :[ "fichier cgi", "qu'est-ce qu'un fichier cgi", "fichier", "exemple cgi", "extension de fichier cgi","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier CGI et les API qui peuvent créer et ouvrir des fichiers CGI.",
  "title" :"CGI - Fichier de script d'interface de passerelle commune",
  "linktitle" : "CGI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-28"
}

## Qu'est-ce qu'un fichier CGI ?
Un fichier CGI est connu sous le nom de script Common Gateway Interface utilisé par un serveur Web pour exécuter un programme externe afin de traiter les demandes des utilisateurs. Le script enregistré dans un fichier avec l'extension .cgi est généralement écrit en langages de programmation C ou Perl. Le avait été introduit depuis les débuts du Web, lorsque les développeurs Web voulaient connecter des bases de données à leurs serveurs Web. Un serveur prenant en charge une passerelle commune entre le serveur Web et les bases de données était bien adapté pour exécuter le code CGI.

## Format de fichier CGI
Les scripts CGI sont utilisés par le serveur Web pour aider le propriétaire à configurer la manière dont une URL sera gérée. La procédure est généralement effectuée en marquant un nouveau répertoire (où se trouvent principalement les documents) comme contenant des scripts CGI ; son nom communément connu est cgi-bin. Par exemple, /usr/local/apache/htdocs/cgi-bin peut être choisi comme répertoire CGI sur le serveur Web. Lorsqu'un navigateur Web demande une URL qui pointe vers un fichier dans le répertoire CGI, alors, au lieu de simplement envoyer ce fichier (/fr/usr/local/apache/htdocs/cgi-bin/printenv.pl) au navigateur Web, le protocole HTTP serveur exécute le script spécifié et renvoie la sortie du script au navigateur Web. En bref, tout ce que le script CGI est envoyé à la sortie standard est transféré au client Web au lieu d'être affiché dans un terminal de fenêtre.

### Exemple CGI

Voici le script CGI écrit en Perl qui affiche toutes les variables d'environnement passées par le serveur Web :
```
#!/usr/bin/env perl

=head1 DESCRIPTION

printenv — a CGI program that just prints its environment

=cut
print "Content-Type: text/plain\n\n";

for my $var ( sort keys %ENV ) {
    printf "%s=\"%s\"\n", $var, $ENV{$var};
}
```

La sortie sera comme suit :
```
COMSPEC="C:\Windows\system32\cmd.exe"
DOCUMENT_ROOT="C:/Program Files (x86)/Apache Software Foundation/Apache2.4/htdocs"
GATEWAY_INTERFACE="CGI/1.1"
HOME="/home/SYSTEM"
HTTP_ACCEPT="text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8"
HTTP_ACCEPT_CHARSET="ISO-8859-1,utf-8;q=0.7,*;q=0.7"
HTTP_ACCEPT_ENCODING="gzip, deflate, br"
HTTP_ACCEPT_LANGUAGE="en-us,en;q=0.5"
HTTP_CONNECTION="keep-alive"
HTTP_HOST="example.com"
HTTP_USER_AGENT="Mozilla/5.0 (Windows NT 6.1; WOW64; rv:67.0) Gecko/20100101 Firefox/67.0"
PATH="/home/SYSTEM/bin:/bin:/cygdrive/c/progra~2/php:/cygdrive/c/windows/system32:..."
PATHEXT=".COM;.EXE;.BAT;.CMD;.VBS;.VBE;.JS;.JSE;.WSF;.WSH;.MSC"
PATH_INFO="/foo/bar"
PATH_TRANSLATED="C:\Program Files (x86)\Apache Software Foundation\Apache2.4\htdocs\foo\bar"
QUERY_STRING="var1=value1&var2=with%20percent%20encoding"
REMOTE_ADDR="127.0.0.1"
REMOTE_PORT="63555"
REQUEST_METHOD="GET"
REQUEST_URI="/cgi-bin/printenv.pl/foo/bar?var1=value1&var2=with%20percent%20encoding"
SCRIPT_FILENAME="C:/Program Files (x86)/Apache Software Foundation/Apache2.4/cgi-bin/printenv.pl"
SCRIPT_NAME="/cgi-bin/printenv.pl"
SERVER_ADDR="127.0.0.1"
SERVER_ADMIN="(server admin's email address)"
SERVER_NAME="127.0.0.1"
SERVER_PORT="80"
SERVER_PROTOCOL="HTTP/1.1"
SERVER_SIGNATURE=""
SERVER_SOFTWARE="Apache/2.4.39 (Win32) PHP/7.3.7"
SYSTEMROOT="C:\Windows"
TERM="cygwin"
WINDIR="C:\Windows"
```
## Utilisations des scripts CGI
Les fichiers CGI contenant les scripts CGI sont généralement utilisés pour traiter les données d'entrée de l'utilisateur et produire les données de sortie pertinentes. L'implémentation d'un wiki est l'un des exemples de programme CGI. Si l'agent utilisateur envoie une requête pour le nom d'une entrée, le serveur Web exécute le programme CGI. Le programme CGI obtient la source de la page de cette entrée, la convertit en HTML et imprime le résultat. Le serveur Web reçoit la sortie du programme CGI et la renvoie à l'agent utilisateur. Ensuite, si l'agent utilisateur appelle la fonction d'édition en cliquant sur le bouton "Modifier la page", le programme CGI affiche une zone de texte HTML ou un autre contrôle d'édition avec le contenu de la page. Enfin, si l'agent utilisateur clique sur le bouton "Publier la page", le programme CGI convertit le HTML mis à jour dans la source de la page de cette entrée et l'enregistre.



## Références

* [Interface de passerelle commune - par Wikipewdia] (https://en.wikipedia.org/wiki/Common_Gateway_Interface)

