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
  "title": "PAC - প্রক্সি অটো-কনফিগারেশন (PAC) ফাইল",
  "description": "PAC ফাইল ফরম্যাট এবং APIগুলি কী যেগুলি PAC ফাইলগুলি তৈরি এবং খুলতে পারে সে সম্পর্কে জানুন৷",
  "linktitle": "PAC",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-pac-bn"
    }
  },
  "lastmod": "2021-06-17"
}

## একটি PAC ফাইল কি?

.pac (প্রক্সি অটো-কনফিগারেশন) এক্সটেনশন সহ একটি ফাইল হল একটি কনফিগারেশন ফাইল যাতে সরাসরি ইন্টারনেটে ওয়েব অনুরোধ পাঠানোর নিয়ম রয়েছে বা প্রক্সি সার্ভারের মাধ্যমে রুট করা হয়। এটিতে একটি [JavaScript](/web/js/) ফাংশন রয়েছে যা সরাসরি গন্তব্যে পাঠানোর পরিবর্তে কিছু ওয়েব প্রক্সি সার্ভারের মাধ্যমে ওয়েব অনুরোধগুলিকে রুট করে৷ একটি প্রক্সি সার্ভার হল একটি ম্যান-ইন-দ্য-মিডল যেটি একাধিক ক্লায়েন্টের কাছ থেকে অনুরোধ গ্রহণ করে এবং গন্তব্যে ফরোয়ার্ড করে সেগুলি পরিবেশন করে। এগুলি ইন্টারনেট ট্র্যাফিকের লোড নিয়ন্ত্রণ করতে ব্যবহৃত হয়। PAC ফাইলগুলি মাইক্রোসফ্ট নোটপ্যাডের মতো যে কোনও পাঠ্য সম্পাদক দিয়ে খোলা যেতে পারে।

## PAC ফাইল ফরম্যাট সম্পর্কে আরও তথ্য

PAC files were first introduced into Netscape Navigator in 1990. PAC ফাইলগুলি সাধারণ জাভাস্ক্রিপ্ট টেক্সট বিন্যাসে লেখা হয় এবং মানুষের পাঠযোগ্য। ওয়েব ব্রাউজারগুলির কাছে প্রক্সি সার্ভারের ইউআরএল তথ্য নির্দিষ্ট করার বিকল্প রয়েছে যেখান থেকে প্রক্সি ইউআরএল তালিকা আনা হয়।

জাভাস্ক্রিপ্ট ব্যবহার করে PAC এর ভিতরে সংজ্ঞায়িত ফাংশনটি নিম্নরূপ:

```JavaScript
function FindProxyForURL(url, host) {
  // ...
}
```

### উদাহরণ PAC ফাইল

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
## তথ্যসূত্র

* [পিএসি ফাইল কী?](https://findproxyforurl.com/)


