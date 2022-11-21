{
  "date" : "2022-09-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ไฟล์ CSR - รูปแบบไฟล์คำขอลงนามใบรับรอง",
  "description" :"เรียนรู้เกี่ยวกับไฟล์ CSR และ API ที่สามารถสร้างและเปิดไฟล์ CSR ได้",
  "linktitle" : "CSR",
  "menu" : {
    "docs" : {
      "identifier":"web-csr",
      "parent" : "web"
}
},
  "lastmod" : "2022-09-04"
}

## ไฟล์ CSR คืออะไร??

ไฟล์ CSR คือไฟล์ **คำขอลงนามใบรับรอง** ที่ใช้เพื่อขอใบรับรอง SSL/TLS เมื่อคุณจำเป็นต้องมีใบรับรอง SSL/TLS คุณจะต้องสร้าง CSR บนเซิร์ฟเวอร์เดียวกันกับที่จะติดตั้งใบรับรองนั้นในที่สุด ไฟล์ CSR นี้แชร์กับ Certificate Authority (CA) เพื่อสร้างใบรับรอง ประกอบด้วยข้อมูล เช่น ชื่อสามัญ องค์กร ประเทศ และที่สำคัญกว่านั้นคือ **พับลิกคีย์** ที่รวมอยู่ในไฟล์ใบรับรองของคุณและลงนามด้วยคีย์ส่วนตัวที่เกี่ยวข้อง

แอปพลิเคชันที่สามารถ **เปิดไฟล์ CSR** ได้แก่ OpenSSL และ Microsoft IIS

## รูปแบบไฟล์คำขอลงนามใบรับรอง

ไฟล์ CSR ถูกสร้างขึ้นในรูปแบบ Base-64 PEM ที่สามารถเปิดและดูได้ในโปรแกรมแก้ไขข้อความอย่างง่าย เช่น Microsoft Notepad โดยมีส่วนหัว **-----BEGIN NEW CERTIFICATE REQUEST-----** ที่จุดเริ่มต้นของไฟล์และส่วนท้าย **-----END NEW CERTIFICATE REQUEST-----** ที่ ท้ายไฟล์.

### ไฟล์ CSR มีลักษณะอย่างไร

ตัวอย่างไฟล์ CSR อย่างง่ายมีดังนี้

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

## ข้อมูลใดบ้างที่รวมอยู่ใน CSR

ไฟล์ CSR มีข้อมูลต่อไปนี้

1. `ข้อมูลเกี่ยวกับธุรกิจและเว็บไซต์` - รวมข้อมูลต่างๆ เช่น ชื่อสามัญ องค์กร หน่วยองค์กร เมือง/ท้องที่ รัฐ/เขต/ภูมิภาค (S) ประเทศ และที่อยู่อีเมล
1. `รหัสสาธารณะ' - รวมอยู่ในใบรับรองและใช้เพื่อเข้ารหัสข้อมูลที่ส่งซึ่งถอดรหัสโดยใช้รหัสส่วนตัวที่เกี่ยวข้อง
1. `ข้อมูลเกี่ยวกับประเภทคีย์และความยาว' - โดยปกติจะเป็น RSA 2048 แต่อาจมีขนาดใหญ่กว่าเช่น RSA 4096+

## อ้างอิง

* [เซิร์ฟเวอร์แอปพลิเคชันแนวคิด](https://github.com/Devronium/ConceptApplicationServer)

