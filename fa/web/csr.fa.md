{
  "date" : "2022-09-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "فایل CSR - فرمت فایل درخواست امضای گواهی",
  "description" : "درباره فایل CSR و API هایی که می توانند فایل های CSR را ایجاد و باز کنند آشنا شوید.",
  "linktitle" : "CSR",
  "menu" : {
    "docs" : {
      "identifier":"web-csr-fa",
      "parent" : "web"
}
},
  "lastmod" : "2022-09-04"
}

## فایل CSR چیست؟

فایل CSR یک فایل **درخواست امضای گواهی** است که برای درخواست گواهی SSL/TLS استفاده می شود. زمانی که نیاز دارید گواهی SSL/TLS خود را داشته باشید، CSR را در همان سروری که در نهایت نصب خواهد شد ایجاد می کنید. این فایل CSR برای ایجاد گواهی با مرجع صدور گواهی (CA) به اشتراک گذاشته شده است. این شامل اطلاعاتی مانند نام مشترک، سازمان، کشور، و مهمتر از همه، **کلید عمومی** است که در فایل گواهی شما یکپارچه شده و با کلید خصوصی مربوطه امضا شده است.

برنامه هایی که می توانند **فایل های CSR** را باز کنند عبارتند از OpenSSL و Microsoft IIS.

## فرمت فایل درخواست امضای گواهی

یک فایل CSR با فرمت Base-64 PEM ایجاد می شود که می تواند در یک ویرایشگر متن ساده مانند Microsoft Notepad باز و مشاهده شود. این شامل یک سرصفحه **-----شروع درخواست گواهی جدید-----** در ابتدای فایل و یک پاورقی **-----پایان درخواست گواهی جدید-----** در انتهای فایل

### یک فایل CSR چگونه به نظر می رسد؟

یک مثال ساده از یک فایل CSR به شرح زیر است.

```
-----BEGIN NEW CERTIFICATE REQUEST-----
MIIuasd098f9567a0sd657f80a9sd8f09asdf80asd8f0asdDVDCCAr0CAQAweTEeMBwGA1UEAxMVd3d3L
mpvc2VwaGNoYXBtYW4uY29tMQ8wDQYDVQQLEwZEZXNpZ24xFjAUBgNVBAoTDUpvc2VwaENoYXBt567W4xE
jAQ657BgNVBAcTCU1haWRzdG9uZTENMAsGA1UECBMES2VudDELMAkGA1UEBhMCR0IwgZ8wDQYJKoZIhvcN
AQEBBQADgY0AMIGJAoGBAOEFDpnOKRabQhDa5asDxYPnG0cneW18e8apjOk1yuGRk+3GD7YQvuhBVS1x6w
kw1D267RnmnZgN1nNUK0cRK7sIvOyCh1+jgD7asdfasdfdsu46mLk81j+b4YSEmYZGPLIuclyocPDm0hXa
yjCUqWt7z6LMIKpLym8gayEZzz679Gn97PsbafasdfPkVFBAgMBAAGgggGZMBoGCisGAQQBgjcNAgMxDBY
KNS4xLjI2MDAuMjB7Bgo45457567658rBgEEAYI3AgEOMW0wazAOBgNVHQ452358BAf8EBAMsdfCBPAwRA
YJKoZIhvcNAQkPBDcwNTAOBggqhkiG9w234320DAgICAIAwDgYIKoZIhvcNAwQCAgCAMAcGBSsOAwIHMAo
GCCqGSIb3DQMHMBMGA1UdJQQMMAoGCCsGAQUsdfsdfFBwMB657M567IH9BgorBgEEAYI3DQICMYHu567MI
HrAgEBH567l567oAsdfsdTQBpAGMAcgBvAadsfadsHMAbwBmAHQAIABSAFMAQQAgAFMAQwBoAGEAbgBuAG
UAbAAgAEMAcgB5AHAAdABvAGcAcgBhAHAAaABpAGMAIABQAHIAb567wB2AGkAZABlAHIDg56YkAk0kfHSk
r48685jsEVya3mgfUoyaYMO456ECNZr4Cb+WhPgexfjOO5qwOG1oDOTa567rkc5pG+IPBQnq+4cotT8hWJ
Qwpc+qGb578xUETpxCok756768567567hrhN5079vFXq5dsHkmtOTwkSqSnz9yruVoxYeDQ8jI3KG3HTgx
wFto8oZnm+E+Y4oshUAAAAAAAAAADANB56756gkqhkiG9w0BAQUFAAOBgQAuAxetLz75667gfjBdWpjpix
e657VYZXuPZ+6jvZNL9hOw7Fk5pVVXWdr8csJ6JUW8QdH9KB6ZlM4yg8Df+vat1G6GuD2hiIR7fQ0NtP==
-----END NEW CERTIFICATE REQUEST-----
```

## چه اطلاعاتی در CSR گنجانده شده است؟

یک فایل CSR حاوی اطلاعات زیر است.

1. اطلاعات در مورد تجارت و وب سایت - شامل اطلاعاتی مانند نام مشترک، سازمان، واحد سازمانی، شهر/محل، ایالت/منطقه/منطقه (S)، کشور و آدرس ایمیل
1. کلید عمومی - در گواهی گنجانده شده است و برای رمزگذاری داده های ارسالی استفاده می شود که با استفاده از کلید خصوصی مربوطه رمزگشایی می شوند.
1. اطلاعات در مورد نوع و طول کلید - این معمولا RSA 2048 است اما ممکن است در اندازه های بزرگتر مانند RSA 4096+ نیز باشد.

## منابع

* [Concept Application Server] (https://github.com/Devronium/ConceptApplicationServer)


