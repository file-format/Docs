{
  "date" : "2021-05-24",
  "keywords" :["pac", "Plik", "Rozszerzenie", "Format pliku", "Rozszerzenie pliku", "Automatyczna konfiguracja serwera proxy"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAC - plik automatycznej konfiguracji serwera proxy (PAC)",
  "description":"Dowiedz się, czym jest format pliku PAC i interfejsy API, które mogą tworzyć i otwierać pliki PAC.",
  "linktitle" : "PAC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-17"
}

## Czym jest plik PAC?

Plik z rozszerzeniem .pac (Proxy Auto-Configuration) to plik konfiguracyjny zawierający reguły wysyłania żądań internetowych bezpośrednio do Internetu lub kierowania ich przez serwer proxy. Zawiera funkcję [JavaScript](/pl/web/js/), która kieruje żądania sieciowe przez jakiś internetowy serwer proxy zamiast wysyłać je bezpośrednio do miejsca docelowego. Serwer proxy jest jak man-in-the-middle, który przyjmuje żądania od wielu klientów i obsługuje je, przekazując dalej do miejsc docelowych. Służą one do kontrolowania obciążenia ruchu internetowego. Pliki PAC można otwierać za pomocą dowolnego edytora tekstu, takiego jak Notatnik firmy Microsoft.

## Więcej informacji o formacie pliku PAC

Pliki PAC zostały po raz pierwszy wprowadzone do przeglądarki Netscape Navigator w 1990 roku. Pliki PAC są zapisywane w zwykłym formacie tekstowym JavaScript i są czytelne dla człowieka. Przeglądarki internetowe mają możliwość określenia adresu URL serwera proxy, z którego pobierana jest lista adresów URL serwera proxy.

Funkcja zdefiniowana w PAC za pomocą JavaScript jest następująca:

```JavaScript
function FindProxyForURL(url, host) {
  // ...
}
```

### Przykładowy plik PAC

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
## Bibliografia

* [Co to jest plik PAC?](https://findproxyforurl.com/)

