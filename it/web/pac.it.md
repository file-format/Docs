{
  "date" : "2021-05-24",
  "keywords" :["pac", "File", "Estensione", "Formato file", "Estensione file", "Configurazione automatica proxy"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAC - File di configurazione automatica proxy (PAC)",
  "description":"Scopri cos'è il formato di file PAC e le API che possono creare e aprire file PAC.",
  "linktitle" : "PAC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-17"
}

## Che cos'è un file PAC?

Un file con estensione .pac (Proxy Auto-Configuration) è un file di configurazione che contiene regole che inviano richieste Web direttamente a Internet o le instradano tramite un server proxy. Contiene una funzione [JavaScript](/it/web/js/) che instrada le richieste Web tramite un server proxy Web invece di inviarle direttamente alla destinazione. Un server proxy è come un man-in-the-middle che accetta richieste da più client e le serve inoltrandole alle destinazioni. Questi vengono utilizzati per controllare il carico sul traffico Internet. I file PAC possono essere aperti con qualsiasi editor di testo come Microsoft Notepad.

## Ulteriori informazioni sul formato file PAC

I file PAC sono stati introdotti per la prima volta in Netscape Navigator nel 1990. I file PAC sono scritti in un semplice formato di testo JavaScript e sono leggibili dall'uomo. I browser Web hanno la possibilità di specificare le informazioni sull'URL del server proxy da cui viene recuperato l'elenco degli URL proxy.

La funzione definita all'interno del PAC utilizzando JavaScript è la seguente:

```JavaScript
function FindProxyForURL(url, host) {
  // ...
}
```

### Esempio di file PAC

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
## Riferimenti

* [Cos'è il file PAC?](https://findproxyforurl.com/)

