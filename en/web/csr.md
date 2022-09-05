{
  "date" : "2022-09-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "CSR File - Certificate Signing Request File Format",
  "description" : "Learn about what is an CSR file and APIs that can create and open CSR files.",
  "linktitle" : "CSR",
  "menu" : {
    "docs" : {
      "identifier":"web-csr",
      "parent" : "web"
    }
  },
  "lastmod" : "2022-09-04"
}

## What is a CSR file?

A CSR file is a **Certificate Signing Request** file that is used to request for SSL/TLS certificate. When you need to have your SSL/TLS certificate, you generate the CSR on the same server where it will finally be installed. This CSR file is shared with the Certificate Authority (CA) for creation of the certificate. It contains information such as common name, organization, country, and, more importantly, the **public key** that is integrated within your certificate file and is signed with the corresponding private key.

Applications that can **open CSR files** include OpenSSL and Microsoft IIS.

## Certificate Signing Request File Format

A CSR file is created in a Base-64 PEM format that can be opened and viewed in a simple text editor such as Microsoft Notepad. It includes a header **-----BEGIN NEW CERTIFICATE REQUEST-----** at the start of the file and a footer **-----END NEW CERTIFICATE REQUEST-----** at the end of the file.

### How does a CSR file look like?

A simple example of a CSR file is as follow.

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

## What information is included in a CSR?

A CSR file contains the following information.

1. `Information about Business and Website` - Includes information such as Common Name, Organization, Organizational Unit, City/Locality, State/County/Region (S), Country and Email Address
1. `Public Key` - It is included in the certificate and is used to encrypt transmitted data which is decrypted using the corresponding private key
1. `Information about Key Type and Length` - This is usually RSA 2048 but may also come in larger sizes such as RSA 4096+

## References

* [Concept Application Server](https://github.com/Devronium/ConceptApplicationServer)
