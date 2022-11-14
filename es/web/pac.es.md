{
  "date" : "2021-05-24",
  "keywords" :["pac", "Archivo", "Extensión", "Formato de archivo", "Extensión de archivo", "Configuración automática de proxy"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAC: archivo de configuración automática de proxy (PAC)",
  "description":"Obtenga información sobre el formato de archivo PAC y las API que pueden crear y abrir archivos PAC",
  "linktitle" : "PAC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-17"
}

## ¿Qué es un archivo PAC?

Un archivo con extensión .pac (Proxy Auto-Configuration) es un archivo de configuración que contiene reglas que envían solicitudes web directamente a Internet o las enrutan a través de un servidor proxy. Contiene una función [JavaScript](/es/web/js/) que enruta las solicitudes web a través de algún servidor proxy web en lugar de enviarlas directamente al destino. Un servidor proxy es como un hombre en el medio que acepta solicitudes de múltiples clientes y las atiende reenviándolas a destinos. Estos se utilizan para controlar la carga en el tráfico de Internet. Los archivos PAC se pueden abrir con cualquier editor de texto como Microsoft Notepad.

## Más información sobre el formato de archivo PAC

Los archivos PAC se introdujeron por primera vez en Netscape Navigator en 1990. Los archivos PAC están escritos en formato de texto JavaScript sin formato y son legibles por humanos. Los navegadores web tienen la opción de especificar la información de URL del servidor proxy desde donde se obtiene la lista de URL de proxy.

La función definida dentro del PAC usando JavaScript es la siguiente:

```JavaScript
function FindProxyForURL(url, host) {
  // ...
}
```

### Ejemplo de archivo PAC

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
## Referencias

* [¿Qué es un archivo PAC?](http://findproxyforurl.com/pac-file-introduction/)

