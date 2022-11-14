{
  "date" : "2021-05-24",
  "keywords" :["pac", "Fichier", "Extension", "Format de fichier", "Extension de fichier", "Configuration automatique du proxy"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAC - Fichier de configuration automatique du proxy (PAC)",
  "description":"En savoir plus sur le format de fichier PAC et les API qui peuvent créer et ouvrir des fichiers PAC.",
  "linktitle" : "PAC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-17"
}

## Qu'est-ce qu'un fichier PAC ?

Un fichier avec l'extension .pac (Proxy Auto-Configuration) est un fichier de configuration qui contient des règles envoyant des requêtes Web directement à Internet ou les acheminant via un serveur proxy. Il contient une fonction [JavaScript](/fr/web/js/) qui achemine les requêtes Web via un serveur proxy Web au lieu de les envoyer directement à la destination. Un serveur proxy est comme un homme du milieu qui accepte les demandes de plusieurs clients et les sert en les transmettant aux destinations. Ceux-ci sont utilisés pour contrôler la charge du trafic Internet. Les fichiers PAC peuvent être ouverts avec n'importe quel éditeur de texte tel que Microsoft Notepad.

## Plus d'informations sur le format de fichier PAC

Les fichiers PAC ont été introduits pour la première fois dans Netscape Navigator en 1990. Les fichiers PAC sont écrits au format texte JavaScript brut et sont lisibles par l'homme. Les navigateurs Web ont la possibilité de spécifier les informations d'URL du serveur proxy à partir desquelles la liste des URL proxy est extraite.

La fonction définie à l'intérieur du PAC à l'aide de JavaScript est la suivante :

```JavaScript
function FindProxyForURL(url, host) {
  // ...
}
```

### Exemple de fichier PAC

```JavaScript
function FindProxyForURL(url, host) {

// If the hostname matches, send direct.
	if (dnsDomainIs(host, "intranet.domain.com") ||
		shExpMatch(host, "(*.abcdomain.com|abcdomain.com)"))
		return "DIRECT";

// If the protocol or URL matches, send direct.
	if (url.substring(0, 4)=="ftp:" ||
		shExpMatch(url, "http://abcdomain.com/folder/*"))
		return "DIRECT";

// If the requested website is hosted within the internal network, send direct.
	if (isPlainHostName(host) ||
		shExpMatch(host, "*.local") ||
		isInNet(dnsResolve(host), "10.0.0.0", "255.0.0.0") ||
		isInNet(dnsResolve(host), "172.16.0.0",  "255.240.0.0") ||
		isInNet(dnsResolve(host), "192.168.0.0",  "255.255.0.0") ||
		isInNet(dnsResolve(host), "127.0.0.0", "255.255.255.0"))
		return "DIRECT";

// If the IP address of the local machine is within a defined
// subnet, send to a specific proxy.
	if (isInNet(myIpAddress(), "10.10.5.0", "255.255.255.0"))
		return "PROXY 1.2.3.4:8080";

// DEFAULT RULE: All other traffic, use below proxies, in fail-over order.
	return "PROXY 4.5.6.7:8080; PROXY 7.8.9.10:8080";

}
```
## Références

* [Qu'est-ce qu'un fichier PAC ?] (http://findproxyforurl.com/pac-file-introduction/)

