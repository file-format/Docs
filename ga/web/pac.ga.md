{
  "date": "2021-05-24",
  "keywords": [
"pac",
"Comhad",
"Síneadh",
"Formáid Chomhaid",
"Síneadh Comhad",
"Proxy Auto-Cumraíocht"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PAC - Comhad um Uathchumraíocht Seachfhreastalaí (PAC).",
  "description": "Foghlaim faoi cad is formáid comhaid PAC ann agus APIanna ar féidir comhaid PAC a chruthú agus a oscailt.",
  "linktitle": "PAC",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-pa-gac"
}
},
  "lastmod": "2021-06-17"
}

## Cad is comhad PAC ann?

Is comhad cumraíochta é comhad a bhfuil síneadh .pac (Seachfhreastalaí Uathchumraíocht air) ann ina bhfuil rialacha chun iarratais ghréasáin a sheoladh go díreach chuig an idirlíon nó iad seo a sheoladh trí sheachfhreastalaí. Tá feidhm [JavaScript](/web/js/) ann a stiúrann iarratais ghréasáin trí sheachfhreastalaí gréasáin éigin in ionad iad a sheoladh go díreach chuig an gceann scríbe. Tá seachfhreastalaí cosúil le fear sa lár a ghlacann le hiarratais ó chliaint iolracha agus a fhreastalaíonn orthu trí chur ar aghaidh chuig cinn scríbe. Úsáidtear iad seo chun an t-ualach ar thrácht idirlín a rialú. Is féidir comhaid PAC a oscailt le haon eagarthóir téacs ar nós Microsoft Notepad.

## Tuilleadh Eolais maidir le Formáid Chomhaid PAC

PAC files were first introduced into Netscape Navigator in 1990. Scríobhtar comhaid PAC i bhformáid téacs simplí JavaScript agus tá siad inléite ag daoine. Tá an rogha ag brabhsálaithe Gréasáin faisnéis URL an tseachfhreastalaí a shonrú ón áit a bhfaightear an liosta URLanna seachfhreastalaí.

Seo a leanas an fheidhm a shainmhínítear taobh istigh den PAC ag baint úsáide as JavaScript:

```JavaScript
function FindProxyForURL(url, host) {
  // ...
}
```

### Sampla de Chomhad PAC

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
## Tagairtí

* [Cad é comhad PAC?](https://findproxyforurl.com/)


