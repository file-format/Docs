{
  "date": "2021-08-02",
  "keywords": [
"comhad reg",
"formáid comhaid reg",
"cad is comhad reg",
"comhad",
"sampla reg",
"síneadh comhad reg",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid REG agus APIs ar féidir leo comhaid REG a chruthú agus a oscailt.",
  "title": "REG - Comhad Chlárlann Windows",
  "linktitle": "REG",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-re-gag"
}
},
  "lastmod": "2021-08-02"
}

## Cad is comhad REG ann?

Níl i gcomhad REG ach comhad téacs leis an síneadh .reg. De ghnáth cruthaítear na comhaid seo trí eochracha tipiciúla a onnmhairiú ón gClárlann. Is féidir na comhaid seo a úsáid freisin mar chúltaca den chlár (Go háirithe tá an chéim seo tábhachtach sula ndéantar athruithe!). Is féidir leat a fheiceáil gur chuir roinnt daoine ar fáil iad mar chomhaid in-íoslódáilte ar na suíomhanna céanna a thaispeánann duit conas hack Chlárlann a dhéanamh. Tá comhad REG úsáideach chun athruithe láimhe a dhéanamh ar an gClárlann agus na hathruithe sin a easpórtáil. Just a ghlanadh suas an comhad beagán agus ansin é a roinnt le daoine eile.

## Formáid comhaid REG

Dearadh an fhormáid comhaid REG chun codanna de chlár Windows a onnmhairiú agus a allmhairiú ag baint úsáide as comhréir bunaithe ar INI. Is bunachar sonraí coibhneasta nó ordlathach é Clárlann Windows a choinníonn na socruithe ísealleibhéil do chóras oibriúcháin Microsoft Windows agus feidhmchláir eile a úsáideann clárlann Windows. Mar mhalairt air sin, is féidir linn a rá, is éard atá sa chlár nó sa Chlárlann Windows ná faisnéis, roghanna, socruithe agus luachanna eile do chláir agus do chrua-earraí atá suiteáilte ar gach leagan de chórais oibriúcháin Microsoft Windows.

### Comhréir an chomhaid REG
Seo roinnt príomhghnéithe mar chuid de chomhréir comhaid REG:
- **RegistryEditorVersion**: M.sh. Leagan 5.00 Eagarthóir Clárlainne Windows do Windows 2000, Windows XP, agus Windows Server 2003.
- **Líne bhán**: Aithnítear tús conair nua clárlainne.
- **RegistryPathx**: Conair an fho-eochair a bhfuil an chéad luach á iompórtáil agat.
- **DataItemNamex**: Ainm na míre sonraí is mian leat a iompórtáil.
- **DataTypex**: An cineál sonraí don luach clárlainne.

Stóráiltear eochracha i gcomhaid .reg ag baint úsáide as an chomhréir seo a leanas:
```
[<Hive name>\<Key name>\<Subkey name>]
"Value name"=<Value type>:<Value data>
```
Is féidir leat Luach Réamhshocraithe eochair a chur in eagar trí @ a úsáid in ionad Ainm Luach:
```
[<Hive name>\<Key name>\<Subkey name>]
@=<Value type>:<Value data>
```
### Sampla

Seo sampla de chomhad REG
```
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SOFTWARE\Foobar]
"Value A"="<String value data with escape characters>"
"Value B"=hex:<Binary data (as comma-delimited list of hexadecimal values)>
"Value C"=dword:<DWORD value integer>
"Value D"=hex(0):<REG_NONE (as comma-delimited list of hexadecimal values)>
"Value E"=hex(1):<REG_SZ (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value F"=hex(2):<Expandable string value data (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value G"=hex(3):<Binary data (as comma-delimited list of hexadecimal values)> ; equal to "Value B"
"Value H"=hex(4):<DWORD value (as comma-delimited list of 4 hexadecimal values, in little endian byte order)>
"Value I"=hex(5):<DWORD value (as comma-delimited list of 4 hexadecimal values, in big endian byte order)>
"Value J"=hex(7):<Multi-string value data (as comma-delimited list of hexadecimal values representing UTF-16LE NUL-terminated strings)>
"Value K"=hex(8):<REG_RESOURCE_LIST (as comma-delimited list of hexadecimal values)>
"Value L"=hex(a):<REG_RESOURCE_REQUIREMENTS_LIST (as comma-delimited list of hexadecimal values)>
"Value M"=hex(b):<QWORD value (as comma-delimited list of 8 hexadecimal values, in little endian byte order)>
```

## Tagairtí

* [Clárlann Windows- le Vicipéid]( https://ga.wikipedia.org/wiki/Windows_Registry)

* [Conas subkeys agus luachanna clárlainne a chur leis, a mhodhnú nó a scriosadh trí chomhad .reg a úsáid]( https://support.microsoft.com/en-us/topic/how-to-add-modify-or-delete- clárlann-fo-eochracha-agus-luachanna-trí-úsáid-a-reg-comhad-9c7f37cf-a5e9-e1cd-c4fa-2a26218a1a23)


