{
  "date" : "2021-05-24",
  "keywords" :["pac", "파일", "확장자", "파일 형식", "파일 확장자", "프록시 자동 구성"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAC - 프록시 자동 구성(PAC) 파일",
  "description":"PAC 파일 형식과 PAC 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "PAC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-17"
}

## .PAC 파일이란?

확장자가 .pac(프록시 자동 구성)인 파일은 웹 요청을 인터넷으로 직접 전송하거나 프록시 서버를 통해 라우팅하는 규칙이 포함된 구성 파일입니다. 여기에는 웹 요청을 대상으로 직접 보내는 대신 일부 웹 프록시 서버를 통해 라우팅하는 [JavaScript](/ko/web/js/) 기능이 포함되어 있습니다. 프록시 서버는 여러 클라이언트의 요청을 수락하고 대상으로 전달하여 서비스를 제공하는 중간자(man-in-the-middle)와 같습니다. 이들은 인터넷 트래픽의 부하를 제어하는 데 사용됩니다. PAC 파일은 Microsoft 메모장과 같은 텍스트 편집기로 열 수 있습니다.

## PAC 파일 형식에 대한 추가 정보

PAC 파일은 1990년 Netscape Navigator에 처음 도입되었습니다. PAC 파일은 일반 JavaScript 텍스트 형식으로 작성되었으며 사람이 읽을 수 있습니다. 웹 브라우저에는 프록시 URL 목록을 가져오는 프록시 서버 URL 정보를 지정하는 옵션이 있습니다.

JavaScript를 사용하여 PAC 내부에 정의된 기능은 다음과 같습니다.

```JavaScript
function FindProxyForURL(url, host) {
  // ...
}
```

### 예제 PAC 파일

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
## 참고문헌

* [PAC 파일이란?](http://findproxyforurl.com/pac-file-introduction/)

