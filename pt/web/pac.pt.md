{
  "date" : "2021-05-24",
  "keywords" :["pac", "Arquivo", "Extensão", "Formato de arquivo", "Extensão de arquivo", "Configuração automática de proxy"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAC - arquivo de configuração automática de proxy (PAC)",
  "description":"Saiba mais sobre o que é o formato de arquivo PAC e APIs que podem criar e abrir arquivos PAC.",
  "linktitle" : "PAC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-17"
}

## O que é um arquivo PAC?

Um arquivo com extensão .pac (Proxy Auto-Configuration) é um arquivo de configuração que contém regras que enviam solicitações da Web diretamente para a Internet ou as roteiam por meio de um servidor proxy. Ele contém uma função [JavaScript](/pt/web/js/) que roteia as solicitações da web por meio de algum servidor proxy da web em vez de enviá-las diretamente ao destino. Um servidor proxy é como um man-in-the-middle que aceita solicitações de vários clientes e as atende encaminhando para destinos. Estes são usados para controlar a carga no tráfego da Internet. Os arquivos PAC podem ser abertos com qualquer editor de texto, como o Microsoft Notepad.

## Mais informações sobre o formato de arquivo PAC

Os arquivos PAC foram introduzidos pela primeira vez no Netscape Navigator em 1990. Os arquivos PAC são escritos em formato de texto JavaScript simples e podem ser lidos por humanos. Os navegadores da Web têm a opção de especificar as informações de URL do servidor proxy de onde a lista de URLs de proxy é buscada.

A função definida dentro do PAC usando JavaScript é a seguinte:

```JavaScript
function FindProxyForURL(url, host) {
  // ...
}
```

### Exemplo de arquivo PAC

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
## Referências

* [O que é arquivo PAC?](http://findproxyforurl.com/pac-file-introduction/)

