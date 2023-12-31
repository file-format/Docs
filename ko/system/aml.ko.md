{
  "date" : "2022-04-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AML 파일 - ACPI 기계어 파일",
  "description":"ACPI AML 파일 형식과 AML 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
      "identifier" : "system-aml",
      "parent" : "system"
}
},
  "lastmod" : "2022-04-12"
}

## .AML 파일이란?

AML 파일은 하드웨어 속성을 구성하는 데 사용되는 ACPI(고급 구성 및 전원 인터페이스) 언어로 만든 시스템 파일입니다. 여기에는 컴퓨터 종료와 같은 간단한 작업에도 하드웨어를 구성하는 데 사용되는 기계 독립적 바이트 코드가 포함되어 있습니다. AML 파일에는 시스템에 설치되는 목적에 따라 지침이 포함될 수 있습니다. ACPI 표준을 구현하면 P55 마더보드와 같은 마더보드 장치를 구성하기 위한 강력한 인터페이스와 전원 관리 기능을 향상시킬 수 있습니다.

## ACPI AML 파일 형식

AML 파일은 바이트 코드로 작성된 내용과 함께 디스크에 바이너리 파일로 저장됩니다. ACPI 표준의 파일 형식 사양은 [uefi](https://uefi.org/)에서 확인할 수 있습니다. 이 언어는 안정성과 이전 버전과의 호환성을 제공하도록 설계되어 애플리케이션 스택을 다시 작성하거나 다시 빌드할 필요가 없습니다.

## AML 파일 형식 사양

AML 파일은 DSDT 및 SSDT 테이블로 구성됩니다. AML 바이트 코드는 이러한 각 테이블의 시작 부분에서 읽고 구문 분석됩니다. 이것은 ACPI 네임스페이스에 있는 장치 및 개체의 정의에 대한 정보를 제공합니다. 이 정보를 사용하여 AML 인터프리터는 시스템에서 사용 가능한 모든 장치의 목록과 지원되는 속성 및 기능을 생성할 수 있습니다.

### DSDT용 ASL 코드 예

DSDT에 대한 ASL 코드의 예는 다음과 같습니다.

```
DefinitionBlock ("test.aml", "DSDT", 1, "OEMID ", "TABLEID  ", 0x00000000)
{
    Scope (_SB)
    {
        Device (PCI0)
        {
            Name (_HID, EisaId ("PNP0A03"))
    }
}
}
```

## 참고문헌

* [ACPI AML](https://wiki.osdev.org/AML)
* [DSDT](https://wiki.osdev.org/DSDT)
* [SSDT](https://wiki.osdev.org/SSDT)

