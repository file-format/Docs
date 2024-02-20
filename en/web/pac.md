{
  "date": "2021-05-24",
  "keywords": [
    "pac",
    "File",
    "Extension",
    "File Format",
    "File Extension",
    "Proxy Auto-Configuration"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "PAC - Proxy Auto-Configuration (PAC) file",
  "description": "Learn about what is PAC file format and APIs that can create and open PAC files.",
  "linktitle": "PAC",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-pac"
    }
  },
  "lastmod": "2021-06-17"
}

## What is a PAC file?

A file with .pac (Proxy Auto-Configuration) extension is a configuration file that contains rules sending web requests directly to internet or route these via a proxy server. It contains a [JavaScript](/web/js/) function that routes the web requests via some web proxy server instead of sending these directly to the destination. A proxy server is like a man-in-the-middle that accepts requests from multiple clients and serves these by forwarding to destinations. These are used to control the load on internet traffic. PAC files can be opened with any text editor such as Microsoft Notepad.

## More Information about PAC File Format

PAC files were first introduced into Netscape Navigator in 1990. PAC files are written in plain JavaScript text format and are human readable. Web browsers have the option to specify the proxy server URL information from where the proxy URLs list is fetched.

The function defined inside the PAC using JavaScript is as follow:

```JavaScript
function FindProxyForURL(url, host) {
  // ...
}
```

### Example PAC File

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
## References

* [What is PAC file?](https://findproxyforurl.com/)
