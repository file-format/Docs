{
  "date" : "2021-08-02",
  "keywords" :[ "reg 파일", "reg 파일 형식", "reg 파일이란", "파일", "reg 예제", "reg 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"REG 파일을 만들고 열 수 있는 API 및 REG 파일 형식에 대해 알아보세요.",
  "title" :"REG - Windows 레지스트리 파일",
  "linktitle" : "REG",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-02"
}

## .REG 파일이란?
REG 파일은 단순히 .reg 확장자를 가진 텍스트 파일입니다. 이러한 파일은 일반적으로 레지스트리에서 일반적인 키를 내보내 생성됩니다. 이 파일은 레지스트리 백업으로도 사용할 수 있습니다(특히 이 단계는 변경하기 전에 중요합니다!). 레지스트리 해킹을 수행하는 방법을 보여주는 동일한 사이트에서 일부 파일을 다운로드 가능한 파일로 제공한 것을 볼 수 있습니다. REG 파일은 레지스트리를 수동으로 변경하고 해당 변경 사항을 내보내는 데 유용합니다. 파일을 약간 정리한 다음 다른 사람들과 공유하십시오.

## REG 파일 형식
REG 파일 형식은 INI 기반 구문을 사용하여 Windows 레지스트리의 일부를 내보내고 가져오기 위해 설계되었습니다. Windows 레지스트리는 Microsoft Windows 운영 체제 및 Windows 레지스트리를 사용하는 기타 응용 프로그램에 대한 하위 수준 설정을 유지하는 관계형 또는 계층적 데이터베이스입니다. 대안으로 레지스트리 또는 Windows 레지스트리는 모든 버전의 Microsoft Windows 운영 체제에 설치된 프로그램 및 하드웨어에 대한 정보, 옵션, 설정 및 기타 값으로 구성되어 있다고 말할 수 있습니다.
### REG 파일의 구문
다음은 REG 파일 구문의 일부인 몇 가지 핵심 요소입니다.
- **RegistryEditorVersion**: 예: Windows 2000, Windows XP 및 Windows Server 2003용 "Windows 레지스트리 편집기 버전 5.00".
- **빈 줄**: 새 레지스트리 경로의 시작을 식별합니다.
- **RegistryPathx**: 가져오는 첫 번째 값을 보유하는 하위 키의 경로입니다.
- **DataItemNamex**: 가져올 데이터 항목의 이름입니다.
- **DataTypex**: 레지스트리 값의 데이터 유형입니다.

키는 다음 구문을 사용하여 .reg 파일에 저장됩니다.
```
[<Hive name>\<Key name>\<Subkey name>]
"Value name"=<Value type>:<Value data>
```
"값 이름" 대신 "@"를 사용하여 키의 기본값을 편집할 수 있습니다.
```
[<Hive name>\<Key name>\<Subkey name>]
@=<Value type>:<Value data>
```
### 예시
다음은 REG 파일의 예입니다.
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

## 참고문헌

* [Windows 레지스트리 - Wikipedia 제공](https://en.wikipedia.org/wiki/Windows_Registry)
* [.reg 파일을 사용하여 레지스트리 하위 키 및 값을 추가, 수정 또는 삭제하는 방법](https://support.microsoft.com/en-us/topic/how-to-add-modify-or-delete- 레지스트리 하위 키 및 값 사용-a-reg-file-9c7f37cf-a5e9-e1cd-c4fa-2a26218a1a23)


